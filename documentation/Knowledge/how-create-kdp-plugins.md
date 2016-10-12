---
layout: page
title: "How to Create KDP Plugins"
date: 2012-03-27 00:00:06
---

This article describes how to create KDP 3.x plugins. To learn how to set up the Flash Builder with the KDP3 project, see <a href="http://www.kaltura.org/setting-kdp-flash-builder-4" target="_blank">Setting up the KDP in Flash Builder 4</a>. KDP version 3.0.0 and above is built in AS3 only, and is not based on the Flex framework, enabling easier and faster deployment and smaller file sizes. Flex modules are no longer supported and only AS3 based plugins may be used.

## KDP3 Plugin Definition on the Layout Document (uiConf)

KDP 3 plugins are defined by the <span><Plugin</span><span> </span><span>/> tag</span>. This tag indictates to load an external .swf file to the KDP3 at runtime. A plug-in can be visual or a unit of logic only, for example:

<pre class="brush: as3;fontsize: 100; first-line: 1; ">&lt;Plugin id="statistics" width="0%" height="0%" includeInLayout="false"/&gt;</pre>

The KDP 3 plugin is a logical plugin (no visual parts in the UI). Its attributes are width and height 0% and since the includeInLayout=false, it will be hidden. The Plugin id=statistics, indicates to relate to the plugin instance at runtime, and the plugin id. Refer to the [KDP 3 uiConf docs][1] to learn more.

 [1]: http://www.kaltura.org/demos/kdp3/docs.html#layout

## Link Your Plugin from the Application Studio

  
Since uiConf is overridable from flashvars, it is possible to define a plugin from flashvars as well. Use the Additional Parameters and Plugins section on the player creation window within [Application Studio][2] to link the plugin you created (and hosted on your server) to the player created using Application Studio.  
![Additional Parameters and Plugins][3] 

 [2]: http://www.kaltura.com/index.php/kmc/kmc2#appstudio|players_list
 [3]: http://www.kaltura.org/sites/default/files/imagepicker/k/Kalturian/aa_2.png

Decide on a name (machine readable - no spaces and starts with a character), and replace the following {Plugin name} token with the name of your plugin.

*   {Plugin name}.plugin = true - Triggers the loading of the plugin. This will be the id of the plugin if an id is not specified - MANDATORY
*   {Plugin name}.path = path - The path from where to load the plugin. If not specified the plugin will be loaded from Kaltura's plugin path.
*   {Plugin name}.relativeTo = id - Component id within the layoutas to the relative position of where to place the plugin - MANDATORY
*   {Plugin name}.position = [before,after,firstChild,lastChild] - The relative position next to the given component id specified in relativeTo - MANDATORY
*   {Plugin name}.pluginName = class name - Used in case the plugin swf contains multiple plugins
*   {Plugin name}.loadingPolicy = {[wait,ondemand]} - Instructs whether to wait for the plugin to load before enabling the KDP ui.
*   {Plugin name}.width = A number representing the width in pixels or a number between 0 to 100 followed by % representing the width as percentage of the parent's width.
*   {Plugin name}.height = A number representing the height in pixels or a number between 0 to 100 followed by % representing the height as percentage of the parent's height.
*   {Plugin name}.includeInLayout = [true, false] - Default: true. Specifies whether this component is included in the layout of the parent container. If true, the object is included in its parent container's layout. If false, the object is positioned by its parent container as per its layout rules, but it is ignored for the purpose of computing the position of the next child.
*   {Plugin name}.hideInFullscreen = [true, false] - Default: true. Specifies whether this component will be included in fullscreen state or not.
*   {Plugin name}.visible = [true, false] - Default: true. Specifies whether the plugin's visual parts are shown or not.
*   {Plugin name}.{any additional attribute} = {value} - Use to set any additional attribute specific to the plugin.

If you want your plugin to be included in the display list, and present visual elements over the player, be certain that the plugin has a defined width and height larger than 0, and that the position is defined relative to another visual component. For example, overlay ad plugins usually need to be loaded above the whole video screen. Be certain that the overlay ad plugin has a width and height of 100% and that it is positioned as the lastChild relative to the playerHolder (the id of the container component that holds the video). myplugin.relativeTo=PlayerHolder myplugin.position=lastChild

<p class="mce-procedure">
  To create the KDP plugin
</p>

These steps describe how to write the plugin code.

1.  Create a new project and provide a descriptive name for the plugin.
2.  Link the new project to the kdp3Lib project and set it's output bin-debug folder to the plugin's folder inside the KDP_3 project.
3.  Create YourClassPlugin.as and YourClassPluginCode.as files.   
    KDP is based on PureMVC as it's core framework, the fastest way to learn it works - refer to the <a href="http://puremvc.org/content/view/98/189/" target="_blank">PureMVC docs</a>. 
4.  (Optional) To get attributes from the uiConf, add them to the YourClassPluginCode.as as public properties. KDP 3 will automatically populate them.
5.  (Optional) To send notifications to the KDP 3, use the KDP façade to send it.
6.  (Optional) To listen on notifications from the KDP, create a mediator and register it to the various events.

## Breaking Down the Code

The most basic plugin must have the following two classes:

*   YourClassPlugin.as
*   YourClassPluginCode.as

### YourClassPlugin

YourClassPlugin is the document class that will be first to instantiate by the KDP3 application when you load the plugin. YourClassPlugin is used as a factory to create the plugin instances.

<pre class="brush: as3;fontsize: 100; first-line: 1; ">package com.kaltura.kdpfl.plugin
{
	public interface IPluginFactory
	{
		/**
		 * Creates a new IPlugin instance. And is implemented by the plugin application class 
		 * @param pluginName the plugin name to be created in case there are multiple plugins with
		 *     the same plugin swf file 
		 * @return An instance of the plugin 
		 */
		function create(pluginName : String = null) : IPlugin;	
	}
}</pre>

### YourClassPluginCode

YourClassPluginCode implements IPlugin and establishes the core plugin that will interact and listen to KDP notifications.

<pre class="brush: as3;fontsize: 100; first-line: 1; ">package com.kaltura.kdpfl.plugin
{
	import org.puremvc.as3.interfaces.IFacade;
	
	public interface IPlugin
	{
		/**
		 * This function is automatically called by the player after the plugin has loaded.
		 * the facade used to comunicate with the hosted player  
		 * @param 
		 * 
		 */		
		function initializePlugin( facade : IFacade ) : void
		
		/**
		 * 
		 * @param styleName
		 * @param setSkinSize
		 * 
		 */		
		function setSkin( styleName : String , setSkinSize : Boolean = false) : void;
	}
}</pre>

When plugins are created, the first method called is **setSkin.** This function defines the skin elements used by the plugin. The second method called is **initializePlugin** where the KDP façade is sent to the plugin for registration. The façade (<a href="http://puremvc.org/pages/docs/AS3/standard/framework_asdoc/org/puremvc/as3/patterns/facade/Facade.html" target="_blank">PureMVC façade</a>) allows us to register to and trigger notifications, retrieve <a href="http://puremvc.org/pages/docs/AS3/standard/framework_asdoc/org/puremvc/as3/patterns/proxy/Proxy.html" target="_blank">proxies</a> and <a href="http://puremvc.org/pages/docs/AS3/standard/framework_asdoc/org/puremvc/as3/patterns/mediator/Mediator.html" target="_blank">mediators</a> and relate to other KDP plugins. **Plugins with visual elements**- The YourClassPluginCode is also the visual component that is added to the KDP view. Be certain that you add all the plugin children to this class.

### <span class="mce-procedure">To Listen for a KDP Notification</span> 

1.  Create a Mediator class, a Mediator is a Class that wraps view components and can register to the façade notifications.
    
    Your Mediator class should extend the base Mediator class:
    
    <pre class="brush: as3;fontsize: 100; first-line: 1; ">org.puremvc.as3.patterns.mediator.Mediator</pre>

2.  In your mediator class, override **listNotificationInterests** and **handleNotification**. For example:

<pre style="padding-left: 60px;">override public function listNotificationInterests():Array
{
	return  [ "playerPlayed" ];
}

override public function handleNotification(note:INotification):void
{
	switch(note.getName())
	{
		// this means that the main container will be 100% X 100% always
		case "playerPlayed":
			trace("test plugin");
		break;
	}
}</pre>

You do not have to pass a reference to the façade from the YourClassPluginCode to YourMediator; Mediators reference to the façade when created.

If your plugin is short with lines of code, it is also ok to implement both interfaces (IPlugin and IPluginFactory) in the same class that will be both your plugin factory and instance (The factory will return "this").

<p class="mce-procedure">
  To call a KDP Notification
</p>

1.  Create a Mediator class. A Mediator class wraps view components and can register to the façade notifications.
    
    The Mediator class should extend the base Mediator class:
    
    <pre class="brush: as3;fontsize: 100; first-line: 1; ">org.puremvc.as3.patterns.mediator.Mediator&nbsp;</pre>
    
    Mediators can call KDP notifications to perform various actions like play and pause the playback, enable or disable the UI, go into FullScreen mode, etc.

2.  To call a notification in a Mediator call the inherited "sendNotification" command.

<pre class="brush: as3;fontsize: 100; first-line: 1; ">sendNotification(commandToCall:String, parametersOfTheCommand:Object)</pre>

*   The following sample function shows how to call the "doPlay" notification, making the playback sequence to start:<pre class="brush: as3;fontsize: 100; first-line: 1; ">public function playMedia () : void
{
        sendNotification("doPlay");
}</pre>

*   The following sample function shows how to call the "doPause" notification, making the playback sequence to pause:<pre class="brush: as3;fontsize: 100; first-line: 1; ">public function playPause () : void
{
        sendNotification("doPause");
}</pre>

<h2 class="mce-heading-2">
  Common Use-cases Implementations
</h2>

This section provides some of the more common functions used in plugins.

*   [Seek (jump) to Time in the Playing Video][4]
*   [Change the Playing Media Entry][5]
*   [Enable or Disable the Player Controls][6]
*   [Replace the Kaltura Session][7]

 [4]: #seek
 [5]: #change
 [6]: #enable
 [7]: #replace

### <a name="seek"></a>Seek (jump) to Time in the Playing Video

Often plugins need to jump to specific locations in the playing video. A common use-case is a chapters plugin that shows a list of sections within the playing video. The following function seeks the player to a given second (float). Call this function from within your Mediator class.

<pre class="brush: as3;fontsize: 100; first-line: 1; ">public function seekPlayerToTime (positionInSeconds : Number) : void
{
	sendNotification(NotificationType.DO_SEEK, positionInSeconds); 
}</pre>

### <a name="change"></a>Change the Playing Media Entry

This function is used to change the playing media entry. Following a call to this function, the player calls the Kaltura API requesting the new given media entry and replaces the media that is currently playing. Call this function from within your Mediator class.

<pre class="brush: as3;fontsize: 100; first-line: 1; ">private function changeMedia():void
{
	// Replace the playing media entry -
	var notificationDetails:Object = new Object();
	notificationDetails.entryId = 'the entry id of the video playing';
	sendNotification(NotificationType.CHANGE_MEDIA, notificationDetails);
}</pre>

### <a name="enable"></a>Enable or Disable the Player Controls

The following function shows how to enable or disable the player controls. This practice is a common requirement during ads playback. Call this function from within your Mediator class.

<pre class="brush: as3;fontsize: 100; first-line: 1; ">// Pass true to enable the controls and false to disable.
public function enableGUI (enabled : Boolean) : void
{
	sendNotification("enableGui", {guiEnabled : enabled, enableType : "full"});
}</pre>

### <a name="replace"></a>Replace the Kaltura Session

When implementing entitlement use cases, such as pay per view or single-sign-on authentication, that use the "Free Preview" option under Access Control, a player plugin will need to communicate with 3rd party server to retrieve a new Kaltura Session after a successful authentication occurred. Replacing the Kaltura Session used by the player is simply done by retrieving the ServicesProxy from the player facade, accessing the kalturaClient object (which is responsible for all Kaltura API communication) and changing the value of the "ks" variable. Call this function from within your Mediator class.

<pre class="brush: as3;fontsize: 100; first-line: 1; ">private function changeKalturaSession(kalturaSession:String):void
{
	// Replace the Kaltura Session (e.g. video Preview endded and the user purchased the rest) -
	(facade.retrieveProxy(ServicesProxy.NAME) as ServicesProxy).kalturaClient.ks = kalturaSession;
}</pre>

To learn more about the Kaltura ActionScript3 client library refer to [Utilizing the Kaltura ActionScript3 Client Library][8]. To learn more about data proxies, refer to [Playerdata Proxies and their Use][9].

 [8]: #utilizing
 [9]: #proxies

## <a name="utilizing"></a>Utilizing the Kaltura ActionScript3 Client Library

The KDP3 holds reference to the Kaltura client.

<p class="mce-procedure">
  To create and execute Kaltura API calls
</p>

1.  Get a reference to Kaltura Client. 
    
    <pre class="brush: as3;fontsize: 100; first-line: 1; ">var kalturaClient : Object = facade.retrieveProxy("servicesProxy")["kalturaClient"];</pre>

2.  Follow the [Kaltura Flex Client Library guidelines][10].

 [10]: http://www.kaltura.org/kaltura-client-library-adobe-flex

## Accessing the Video Player Object

Based on PureMVC, objects in the KDP are usually accessible via their Mediators.

<p class="mce-procedure">
  To access the main video player object use the following:
</p>

<pre class="brush: as3;fontsize: 100; first-line: 1; ">var playerMediator:KMediaPlayerMediator = façade.retrieveMediator(KMediaPlayerMediator.NAME) as KMediaPlayerMediator;
//To access the currently played media element:
trace(ObjectUtil.toString(playerMediator.player.media);
//To access the current time of the playing video:
trace(ObjectUtil.toString(playerMediator.player.currentTime);</pre>

## <a name="proxies"></a>Playerdata Proxies and their Use

KDP Proxies are essentially <a href="http://puremvc.org/pages/docs/AS3/standard/framework_asdoc/org/puremvc/as3/patterns/proxy/Proxy.html" target="_blank">PureMVC Proxy</a> classes used to retain application data. In PureMVC, Proxy classes are used to manage parts of the application's data model. A Proxy may be used to manage a reference to a local data object, in which case interacting with it might involve setting and getting its' data in a synchronous manner.

<p class="mce-note-graphic">
  KDP Flash Plugins and KDP Javascript API access proxies in a different manner: <br />Inside Flash, KDP access the proxy data (the VO, "Value Object") as ProxyName.vo.fieldName. <br />In Javascript, the KDP exposes the VO fields directly in the proxy object as: ProxyName.fieldName.
</p>

<p class="mce-note-graphic">
  Examples: In Flash Plugin: mediaProxy.vo.entry.name <br />In JS Code: mediaProxy.entry.name <br />In Flash Plugin: sequenceProxy.vo.isInSequence <br />In JS Code: sequenceProxy.isInSequence
</p>

### Known <a name="core"></a>Core KDP Proxies

*   The "mediaProxy" – Holds information related to the media and Kaltura entry loaded.  
    For example:  
    mediaProxy.entry – The entry object currently playing in the KDP.  
    mediaProxy.entryMetadata – The custom metadata related to the entry currently playing in the KDP (latest profile or the profile as defined in metadataProfileId flashvar).
*   The "sequenceProxy" – Holds information related to the pre/post roll sequences.   
    For example:  
    sequenceProxy.isInSequence – Indicates whether KDP is currently playing an ad.
*   The "configProxy" – Used to retrieve the flashvars.   
    For Example:  
    configProxy.flashvars – The flashvars used by the KDP
*   The "servicesProxy" – Used to retrieve the Kaltura Client object (accessible from v3.5.7.6 and onwards) and current API session details.  
    servicesProxy.kalturaClient - The KalturaClient object. For example: servicesProxy.kalturaClient.ks will retrieve the KS being used.

<p class="mce-procedure">
  To see how to access proxies in KDP Flash Plugins
</p>

Refer to the following example plugin: <a href="http://www.kaltura.org/kalorg/kdp/trunk/plugins/KDPProxyDump/" target="_blank">http://www.kaltura.org/kalorg/kdp/trunk/plugins/KDPProxyDump/</a>. The KDP Proxy Dump plugin below prints all the available fields in the [Core KDP proxies][11].  


 [11]: #core

## Explore KDP 3 plugins

### Google Analytics

Download the [KDP 3 Google Analytics Plugin][12]. The Google Analytics plugin utilizes the [gaforflash][13] tracking library to aggregate and send statistical data to a google analytics account passed on uiConf or via flashvars. Import the project to Flash Builder 4 and follow the inline documentation on the project two class.

 [12]: /sites/default/files/googleAnalytics%20-%20Code.zip
 [13]: http://code.google.com/p/gaforflash/

#### The classes in the project

*   googleAnalytics.as - The plugin main class, implementing IPlugin and IPluginFactory. Instantiating the mediator.
*   GAStatisticsMediator.as - The mediator class, responsible for registering to the various KDP notifications and sending the events through the GATracker instance.

<h4 class="mce-procedure">
  To Use the Google Analytics Plugin with your Player
</h4>

1.  Enter the KMC and select the Studio tab. 
2.  Edit the player of your choice. 
3.  Go to the Features tab. 
4.  Under Additional parameters and plugins, copy and paste the following variables:  
    <br class="Apple-interchange-newline" /><table>
      <tbody>
        <tr>
          <th>
            Parameter
          </th>
          
          <th style="text-align: left;">
            Value
          </th>
        </tr>
        
        <tr>
          <td style="text-align: left;">
            googleAnalytics.plugin
          </td>
          
          <td style="text-align: left;">
            true
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;">
            googleAnalytics.urchinCode
          </td>
          
          <td style="text-align: left;">
            UA-7714780-1
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;">
            googleAnalytics.debugMode
          </td>
          
          <td style="text-align: left;">
            false
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;">
            googleAnalytics.path
          </td>
          
          <td>
            http://exchange.kaltura.com/sites/exchange.kaltura.com/files/applications/releases/Kalturian/16/googleAnalytics.swf
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;">
            googleAnalytics.relativeTo
          </td>
          
          <td style="text-align: left;">
            PlayerHolder
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;">
            googleAnalytics.position
          </td>
          
          <td style="text-align: left;">
            lastChild
          </td>
        </tr>
      </tbody>
    </table> 

5.  Modify the googleAnalytics.urchinCode parameter to your Google Analytics tracking id (in the form of UA-#######-#). 
6.  Change the googleAnalytics.debugMode parameter to true to get visual debugging information window over the player.   
    For additional information see the <a href="http://exchange.kaltura.com/content/google-analytics" target="_blank">Kaltura Exchange Plugin page</a>.