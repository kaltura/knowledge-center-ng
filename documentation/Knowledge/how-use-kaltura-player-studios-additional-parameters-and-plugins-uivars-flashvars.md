---
layout: page
title: "How to use the Kaltura Player Studio's Additional Parameters and Plugins (UIVars, flashvars)"
date: 2012-01-06 03:41:02
---

<p class="mce-note-graphic">
  Kaltura UIVars are an incredibly powerful feature of the Kaltura Players which allow publishers to pre-set or override the value of any FlashVar (object level parameters), show, hide and disable existing UI element, add new plugins and UI elements to an existing player, and modify attributes of all the player's elements.
</p>

<p class="mce-note-graphic">
  <span style="font-size: 10px;">Plugin configuration values can be overwritten at runtime by flashvar configuration. See the <a href="http://knowledge.kaltura.com/node/1148#uivars">Universal Studio Information Guide</a> for information about using UI Variables.</span>
</p>

<p class="mce-heading-2">
  <a name="set_UIVARS"></a>Setting UIVars - For versions previous to Iris 
</p>

To simplify the management of many of the player features, Kaltura has implemented the “UIVars” to override and configure player features.

UIVars are set using the Studio view in the <a href="http://www.kaltura.com/index.php/kmc/kmc4#studio|playersList" target="_blank" title="Kaltura Management Console - The Player Studio Tab">Kaltura Management Console</a> (KMC).  When editing a player instance in the <a href="http://www.kaltura.com/index.php/kmc/kmc4#studio|playersList" target="_blank" title="Kaltura Management Console - The Player Studio Tab">Player Studio</a>, select the Features tab on the left and expand the “Additional parameters and plugins” panel in the features list accordion:

<div id="attachment_3006" class="wp-caption aligncenter">
  <img src="../../assets/237.img">
</div>

In the ***“Additional parameters and plugins”*** panel, there are two options to add parameters:

*   Click Add and add the parameter name and it’s value to the list of the variables.
*   Paste a URL encoded list of parameters (name1=value1&name2=value2…) into the “Paste your plug-in line here” box and click "go”. The parameters will be broken down to variables in the list.

<p class="mce-procedure">
  To use the “Additional parameters and plug-ins” interface, you should be aware of the following:
</p>

*   The “Paste your plug-in line here” box is used in one direction only, to add a given UIVars string to the variables list. After a UIVars string is parsed (by clicking “go”), if you edit the fields in the list directly, the changes will not be reflected back to the UIVars string.
*   Every time you click “go”, a new set of variables will be added to the list. Existing variables will not be overridden by new ones.
*   When variables are added to the list, they are added to the end of the list. When many variables are added, to access the variables, scroll the list using the scrollbars.

<p class="mce-note-graphic">
  <strong>NOTE: </strong>uiVars/flashvars configurations apply to both the HTML5 and Flash (KDP) players alike. For a full list of cross-platform compatibility (which configurations available for each platform), please see: <a href="http://html5video.org/wiki/Kaltura_KDP_API_Compatibility" target="_blank">Kaltura KDP API Compatibility</a>.
</p>

<p class="mce-heading-2">
  The uiConf XML and the UIVars Representation
</p>

The UIVars created through the Players Studio are added as ***<var>*** nodes under the ***<uiVars>*** node (the very last node) in the UIConf XML file.

Developers can also manually add UIVars to the UIConf XML using the uiConf API. 

<p class="mce-note-graphic">
  If you manually edit a player’s UIConf XML and afterwards edit that player in the Studio tab, your manually added changes will be overridden by the Player's Studio settings.
</p>

<p class="mce-heading-2">
  <a name="CommonKalturaPlayerCustomization"></a>Common Kaltura Player Customization (Media Player UI Modifications Using UIVars)
</p>

The following list shares common player modifications required by Kaltura publishers. Follow the steps to [set UIVars][1] to your Kaltura Players to achieve the desired modifications.

 [1]: #set_UIVARS

This section provides procedures for selected common use cases. For the full list of common use cases, see [Common Kaltura Media Player UIVars Use Cases][2].

 [2]: #KalturaCommonMediaPlayerUIVarsUseCases

<p class="mce-heading-3">
  Customizing The Player Logo
</p>

<p class="mce-procedure">
  To change the small Kaltura Sun Icon to a custom icon
</p>

1.  Copy the following UIVars string to the ”Paste your plug-in line here” box and then click  “go”.
    
    <pre><span style="font-family: 'courier new', courier;">kalturaLogo.visible=false&kalturaLogo.includeInLayout=false&mylogo.plugin=true&mylogo.className=Watermark&mylogo.width=30&mylogo.height=30&mylogo.watermarkPath=YOURLOGO&mylogo.watermarkClickPath=YOURURL&mylogo.position=after&mylogo.relativeTo=kalturaLogo</span>&nbsp;</pre>

2.  Scroll the variables list and find the ***mylogo.watermarkPath*** variable. Change the value of this variable (*YOURLOGO*) to the URL of your desired icon (swf, png or jpg file).
3.  Scroll down and find the ***mylogo.watermarkClickPath*** variable. Change the value of this variable (*YOURURL*) to the URL to which the user will be taken, when clicking on the icon.
4.  Save and preview your player.

<p class="mce-heading-3">
  Append a Bumper Video After The Media Playback
</p>

It’s a common practice to play a short message video after every media playback. For example, for all the videos on your site, play a 2 second video of your company logo rotating and shining.

<p class="mce-procedure">
  To append a bumper video, using UIVars
</p>

1.  Go to the Studio tab and then select the Advertising tab.
2.  In the Ad Timeline *se*ction, click on Bumper Video.
3.  Toggle on Bumper Video Enabled.
4.  Paste the Kaltura Entry ID that will be used as the bumper.
5.  Enter the URL in the Click URL field.
6.  In the Features tab on the left, select the Additional Parameters and Plugins section.
7.  Enter the following and click Go:

<pre><span style="font-family: 'courier new', courier;">bumper.preSequence=0&bumper.postSequence=1</span></pre>

<p class="mce-heading-3">
  Modify The Playback Behavior
</p>

Using UIVars, it is also possible to manipulate internal player parameter.  For example, indicate different start and stop times for the playback.

<p class="mce-procedure">
  To begin playback at a specific time (jump ahead of the beginning of the video), use the following UIVars
</p>

<div>
  <pre><span style="font-family: 'courier new', courier;">mediaProxy.mediaPlayFrom=25</span></pre>
</div>

<p class="mce-heading-4 mce-procedure">
  To stop the playback at a specific time, use the following UIVars
</p>

<pre><span style="font-family: 'courier new', courier;">mediaProxy.mediaPlayTo=74</span></pre>

<p class="mce-heading-3">
  Creating a Chromeless Player
</p>

Another common requirement is to make a player UI-less. While it is easy to remove the marks from all the features in the Player Studio, the control bar will still remain. You can set the UIVars to remove the control bar UI disappear from the player.

<p class="mce-procedure">
  To create a UI-less player, <span>use the following UIVars</span>
</p>

<pre><span style="font-family: 'courier new', courier;">ControllerScreenHolder.visible=false&ControllerScreenHolder.includeInLayout=false</span></pre>

<p class="mce-procedure">
  To create a UI-less player, that loops playback and begins playback when loaded
</p>

<pre><span style="font-family: 'courier new', courier;">controlsHolder.includeInLayout=false&controlsHolder.visible=false&externalInterfaceDisabled=false&loop=true&autoPlay=true<br /></span></pre>

For advertising purposes it is also common to start playback in mute (without volume). To achieve that either visit the Basics tab when editing the player in KMC, and check the "Start player muted" option or add the following uiVar:

<pre><span style="font-family: 'courier new', courier;">autoMute=true</span></pre>

<p class="mce-heading-3">
  How to Stretch a Thumbnail?
</p>

When the player size is set to a 4:3 aspect ratio, with a content that is 16:9, it is common requirement to have the thumbnail stretch to the size of the player while keeping the video at it's original 16:9 aspect ratio. 

<p class="mce-procedure">
  To set the thumbnail to stretch to the size of the player regardless of its aspect ratio, <span>use the following UIVars</span>
</p>

<pre><span style="font-family: 'courier new', courier;">video.stretchThumbnail=true</span></pre>

Another option is to create a custom thumbnail and set it as the default thumbnail of the video entry.

<span><span class="mce-heading-3">How to make the Flash player download button download a different specific flavor?</span> <br /> <!--[if !supportLineBreakNewLine]-->

<br /><span class="mce-procedure"> <!--[endif]--></span></span>

<span class="mce-procedure">To change the Flash player download button to download a different specific flavor</span>

Add the following additionalParam to the player:

<pre>key=download.flavorId<br />value=FlavorID taken from KMC-&gt;Settings-&gt;Transcoding Settings-&gt;ID (from ID column).<br />*If the flavor does not exist, it will fall back to the default flv.</pre>

<span class="mce-heading-3">How to make the Flash player start playback using a specific bitrate flavor? (when adaptive bitrate enabled)</span>

Using the following two parameters will force the player to begin playback from a specific bitrate flavor ignoring the default or previously chosen bitrate.

<pre class="brush: plain;fontsize: 100; first-line: 1; ">mediaProxy.preferedFlavorBR=4000&disableBitrateCookie=true</pre>

*   mediaProxy.preferedFlavorBR=4000 – will choose the flavor with the bitrate closer to 4000k (or any value you choose).
*   disableBitrateCookie=true – optional, if set to true, the player will ignore the choice previously saved in the flash cookie.

<p class="mce-heading-3">
  How to change the Flash player’s control bar color?
</p>

<p class="mce-procedure">
  To change the Flash player's control bar color
</p>

1.  Go to the Studio tab and then select the player you want to modify.
2.  In the Features tab on the left, select the Additional Parameters and Plugins section.
3.  Enter the following and click Go:

<pre style="padding-left: 60px;">key: ControllerScreenHolder.bgColor<br />value: [YOUR_COLOR for example 0x00338d]</pre>

<pre style="padding-left: 60px;">key: ControllerScreen.bgColor<br />value: [YOUR_COLOR for example 0x00338d]</pre>

<p class="mce-heading-2">
  <a name="KalturaCommonMediaPlayerUIVarsUseCases"></a>Common <span>Kaltura </span>Media Player UIVars Use Cases
</p>

This table provides the full list of common use cases of player modifications required by Kaltura publishers. For procedures of selected common use cases, see [Common Kaltura Player Customization (Media Player UI Modifications Using UIVars)][3].  

 [3]: #CommonKalturaPlayerCustomization

<table border="1" cellspacing="0" cellpadding="0" align="left">
  <thead>
    <tr align="left">
      <td style="text-align: center;" width="115">
        <strong>Main Use</strong>
      </td>
      
      <td style="text-align: center;" width="149">
        <strong>Use case</strong>
      </td>
      
      <td style="text-align: center;" width="392">
        <strong>flashvars</strong>
      </td>
      
      <td style="text-align: center;" width="184">
        <strong>Notes</strong>
      </td>
      
      <td style="text-align: center;" width="129">
        <strong>Common use cases</strong>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" rowspan="3" width="115">
        <strong>Player Logo</strong>  
      </td>
      
      <td style="text-align: left;" width="149">
        Remove logo
      </td>
      
      <td style="text-align: left;" width="392">
        kalturaLogo.visible=false&kalturaLogo.includeInLayout=false
      </td>
      
      <td style="text-align: left;" width="184">
        Remove the Kaltura logo from the player
      </td>
      
      <td style="text-align: left;" width="129">
        White label the Kaltura player
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Redirect click on logo to a different URL
      </td>
      
      <td style="text-align: left;" width="392">
        kalturaLogo.kClick=navigate('required URL')
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Add Custom logo
      </td>
      
      <td style="text-align: left;" width="392">
        kalturaLogo.visible=false&kalturaLogo.includeInLayout=false&mylogo.<br />plugin=true&mylogo.className=Watermark&mylogo.width=30&mylogo.<br />height=30&mylogo.watermarkPath=YOURLOGO&mylogo.watermarkClickPath=<br />YOURURL&mylogo.position=after&mylogo.relativeTo=kalturaLogo
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong>Bumper Ads</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Add post bumper ad
      </td>
      
      <td style="text-align: left;" width="392">
        bumper.preSequence=0&bumper.postSequence=1
      </td>
      
      <td style="text-align: left;" width="184">
        Add a bumper ad to play after the selected video
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong>Auto-Replay</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Automatically replay when the video has reached end of playback ("loop playback")
      </td>
      
      <td style="text-align: left;" width="392">
        loop=true
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="2" width="115">
        <strong>Google Analytics</strong> 
      </td>
      
      <td style="text-align: left;" width="149">
        Enable Google Analytics
      </td>
      
      <td style="text-align: left;" width="392">
        googleAnalytics.plugin=true&googleAnalytics.debugMode=<br />false&googleAnalytics.path=http://cdnexchange.kaltura.com/sites/<br />exchange.kaltura.com/files/applications/releases/Kalturian/16/<br />googleAnalytics.swf&googleAnalytics.relativeTo=<br />PlayerHolder&googleAnalytics.position=lastChild 
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Customize events going out from the GA plugin
      </td>
      
      <td style="text-align: left;" width="392">
        googleAnalytics.plugin=true&googleAnalytics.path=/content/uiconf/ps/<br />kaltura/kdp/v3.5.21/plugins/googleAnalyticsPlugin.swf&googleAnalytics.<br />relativeTo=video&googleAnalytics.position=before&googleAnalytics.<br />width=0&googleAnalytics.height=0&googleAnalytics.customEvents=<br />mute,unmute,doGigya&googleAnalytics.visualDebug=false<br /><strong>(customEvents="mute,unmute,doGigya" - <br />a comma separated events names to filter.)</strong> 
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong>VAST</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Disable VAST pre-rolls for specific entry
      </td>
      
      <td style="text-align: left;" width="392">
        vast.preSequence=0
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="7" width="115">
        <strong>Playlist Player</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Change thumbnails dimensions
      </td>
      
      <td style="text-align: left;" width="392">
        irImageIrScreen.width=0&
      </td>
      
      <td style="text-align: left;" width="184">
        Enter width in PX
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Set width and height
      </td>
      
      <td style="text-align: left;" width="392">
        playlist.width=[WidthInPx]&playlist.height=[HeightInPx]&playlist.visible=true&playlist.includeInLayout=true
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Hidden playlist
      </td>
      
      <td style="text-align: left;" width="392">
        playlist.visible=false&playlist.includeInLayout=false
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Change the color of the text of the tabs in a multitab playlist
      </td>
      
      <td style="text-align: left;" width="392">
        tabBar.color1=hexcolor&tabBar.color2Selected=true&tabBar.<br />color2=hexcolo
      </td>
      
      <td style="text-align: left;" width="184">
        Change the hexcolor into 0xFFFFFF of your choice
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Audio playlist
      </td>
      
      <td style="text-align: left;" width="392">
        PlayerHolder.visible=false&PlayerHolder.includeInLayout=false&player.height=80
      </td>
      
      <td style="text-align: left;" width="184">
        The value of player.height needs to be changed as well to match the size of the audio playlist
      </td>
      
      <td style="text-align: left;" width="129">
        For audio files
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Playlist Loop
      </td>
      
      <td style="text-align: left;" width="392">
        <p class="p1">
          playlistAPI.loop=true
        </p>
      </td>
      
      <td style="text-align: left;" width="184">
        Auto replay at the end of the playlist (loop through the playlist items)
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        C<span style="text-align: center;">hange the playlist items text color in a playlist player</span>
      </td>
      
      <td style="text-align: left;" width="392">
        <span style="text-align: center;">[labelId].dynamicColor=true</span><br /><span style="text-align: center;">[labelId].color1=[your color]</span>
      </td>
      
      <td style="text-align: left;" width="184">
        See<a href="{{site.url}}/documentation/Knowledge/what-flashvars-can-you-use-change-playlist-items-text-color-playlist-player.html" target="_blank"> </a><span style="text-align: center;"><a href="{{site.url}}/documentation/Knowledge/what-flashvars-can-you-use-change-playlist-items-text-color-playlist-player.html" target="_blank">What flashvars can you use to change the playlist items text color in a playlist player</a>.<a href="{{site.url}}/documentation/Knowledge/what-flashvars-can-you-use-change-playlist-items-text-color-playlist-player.html" target="_blank"></a></span>
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong>Chromeless player</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Hidden controls
      </td>
      
      <td style="text-align: left;" width="392">
        ControllerScreenHolder.visible=false&ControllerScreenHolder.<br />includeInLayout=false
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
        Player for images only
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="2" width="115">
         <strong>Full screen</strong> 
      </td>
      
      <td style="text-align: left;" width="149">
        Hiding the scrubber in full screen mode
      </td>
      
      <td style="text-align: left;" width="392">
        scrubber.hideInFullScreen=true&
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Hiding the controller in full screen mode
      </td>
      
      <td style="text-align: left;" width="392">
        controlsHolder.hideInFullScreen=true&
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="2" width="115">
        <strong>Screen overlay</strong> 
      </td>
      
      <td style="text-align: left;" width="149">
        Text changes for the message
      </td>
      
      <td style="text-align: left;" width="392">
        strings.FREE_PREVIEW_END=text&
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Text changes for top line
      </td>
      
      <td style="text-align: left;" width="392">
        strings.ENTRY_PENDING=text&
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="2" width="115">
        <strong>Promotion text</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Remove the data in the right click 
      </td>
      
      <td style="text-align: left;" width="392">
        aboutPlayer=text&
      </td>
      
      <td style="text-align: left;" rowspan="2" width="184">
        Changes the right click information on the player.
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Add a URL
      </td>
      
      <td style="text-align: left;" width="392">
        aboutPlayerLink=text
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="2" width="115">
        <strong>Advertising Countdown</strong> 
      </td>
      
      <td style="text-align: left;" rowspan="2" width="149">
        Change color 
      </td>
      
      <td style="text-align: left;" width="392">
        noticeMessage.dynamicColor=true
      </td>
      
      <td style="text-align: left;" rowspan="2" width="184">
        Change the hexcolor into 0xFFFFFF of your choice 
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="392">
        noticeMessage.color1=hexcolor 
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="2" width="115">
        <strong>Controllers buttons customization</strong> 
      </td>
      
      <td style="text-align: left;" width="149">
        Play tooltip 
      </td>
      
      <td style="text-align: left;" width="392">
        playBtnControllerScreen.upTooltip=text 
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Pause tooltip
      </td>
      
      <td style="text-align: left;" width="392">
        playBtnControllerScreen.selectedTooltip=text 
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="2" width="115">
        <strong><span><a name="start-play-from"></a>Stop/start playing at a certain point in time</span></strong>
      </td>
      
      <td style="text-align: left;" width="149">
        <span>Start video later</span> 
      </td>
      
      <td style="text-align: left;" width="392">
        <span>mediaProxy.mediaPlayFrom=25</span> 
      </td>
      
      <td style="text-align: left;" width="184">
        <span>Start video later than 0s</span> 
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        <span>Stop at certain time</span>
      </td>
      
      <td style="text-align: left;" width="392">
        <span>mediaProxy.mediaPlayTo=74</span>
      </td>
      
      <td style="text-align: left;" width="184">
        <span>Stop video at 74s</span>
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong><span>Change KDP version</span></strong>
      </td>
      
      <td style="text-align: left;" width="149">
        <span>FlashVar KDP version change</span>
      </td>
      
      <td style="text-align: left;" width="392">
        <span>kdpUrl=http://www.kaltura.com/flash/kdp3/v3.3.9/kdp3.swf</span>
      </td>
      
      <td style="text-align: left;" width="184">
        <span>Can be done in the FlashVars</span>
      </td>
      
      <td style="text-align: left;" width="129">
        <span>Testing different types of version</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong><span>Stretch thumbnail to player's size</span></strong>
      </td>
      
      <td style="text-align: left;" width="149">
         
      </td>
      
      <td style="text-align: left;" width="392">
        <span>video.stretchThumbnail=true</span>
      </td>
      
      <td style="text-align: left;" width="184">
         
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong>Message strings</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        List of message strings that can be overridden via the configuration xml or FlashVars
      </td>
      
      <td style="text-align: left;" width="392">
        The full list is in <a href="http://www.kaltura.org/demos/kdp3/docs.html#designlocale" target="_blank">Kaltura Dynamic Player version 3 -> Flashvars-> Player Design and Locale -> strings.ALERT_ID -> Available messages</a>.
      </td>
      
      <td style="text-align: left;" width="184">
        <p>
          Example (1):
        </p>
        
        <p>
          CLIP_NOT_FOUND -> Media not found
        </p>
        
        <p>
          Example (2):
        </p>
        
        <p>
          CLIP_NOT_FOUND_TITLE-> Sorry, clip not found
        </p>
      </td>
      
      <td style="text-align: left;" width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong><a name="defcaptions"></a>Captions</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Set the default selected captions language 
      </td>
      
      <td style="text-align: left;" width="392">
        <ul>
          <li>
            <span style="text-align: center;">When using the “captions on video” feature, use</span><strong style="text-align: center;">: closedCaptionsOverPlayer.defaultLanguageKey</strong>
          </li>
          <li>
            <span style="text-align: center;">When using the "Captions for accessibility" feature use: </span><strong style="text-align: center;">ccUnderComboBox.defaultLanguageKey</strong>
          </li>
        </ul>
      </td>
      
      <td style="text-align: left;" width="184">
        <p>
          <a href="{{site.url}}/documentation/Knowledge/how-set-captions-display.html">Read more about the captions features</a>. This flashvar is used to set the default language to be used when the player begins to play.
        </p>
      </td>
      
      <td style="text-align: left;" width="129">
        Identify the page language and set the default captions on the player.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong>Player Progress Bar</strong> 
      </td>
      
      <td style="text-align: left;" width="149">
        Set the colors of the buffering and progress lines in the playback progress bar 
      </td>
      
      <td style="text-align: left;" width="392">
        <p class="p1">
          <span style="text-align: center;">This will set the buffering color to white:</span>
        </p>
        
        <p class="p1">
          <span style="text-align: center;">scrubber.color1=</span><span style="text-align: center;">0xffffff</span>
        </p>
        
        <span style="text-align: center;"><span></span></span><p class="p1">
          This will set the buffering color to red:
        </p>
        
        <span style="text-align: center;"><span></span></span><p class="p1">
          scrubber.color1=0xFF0000
        </p>
      </td>
      
      <td width="184">
        <span>Note that the transparency of the buffering is not dynamic and is set from the skin asset</span><span></span><br /><p>
           
        </p>
      </td>
      
      <td width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="115">
        <strong>Display flavors by video dimensions instead of bitrate</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Will set the flavor selector to show the available flavors pixel dimensions instead of bitrates
      </td>
      
      <td style="text-align: left;" width="392">
        <p class="p1">
           
        </p>
        
        <p class="p1">
          mediaProxy.displayFlavorPixels=true
        </p>
        
        <p class="p1">
          flavorComboControllerScreen.usePixels={mediaProxy.displayFlavorPixels}
        </p>
        
        <p class="p1">
           
        </p>
      </td>
      
      <td width="184">
        Supported only in KDP version 3.6.5 and above<br /> 
      </td>
      
      <td width="129">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" rowspan="2" width="115">
        <strong>KCW metadata screen</strong>
      </td>
      
      <td style="text-align: left;" width="149">
        Predefining a <strong>category</strong>
      </td>
      
      <td style="text-align: left;" width="392">
        <p>
          Additional 2 flashvars to the embed code:
        </p>
        
        <p>
          enforceCategory=video      // to enforce a specific category
        </p>
        
        <p>
          disableCategories=true      // disable the category UI
        </p>
      </td>
      
      <td style="text-align: left;" width="184">
        <span>The entry will automatically be under the category “video”</span>
      </td>
      
      <td style="text-align: left;" width="129">
        <span>Add the ability to set categories and block user from changing them.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="149">
        Predefining a <strong>tag</strong>
      </td>
      
      <td style="text-align: left;" width="392">
        <p>
          Additional 2 flashvars to the embed code:
        </p>
        
        <p>
          enforceTags=UGC        // to enforce a specific tag
        </p>
        
        <p>
          disableTags = true       //disable the tags UI
        </p>
      </td>
      
      <td style="text-align: left;" width="184">
        <span>The entry will automatically be tagged, with the tag “UGC”</span>
      </td>
      
      <td style="text-align: left;" width="129">
        <span>Allow a client to define default tags  for  the uploaded entry and  to define whether the Tag section on the upload form will be disabled.</span>
      </td>
    </tr>
  </tbody>
</table>

 

<span style="font-size: medium;"> </span>