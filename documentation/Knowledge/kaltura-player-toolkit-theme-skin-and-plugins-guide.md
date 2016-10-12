---
layout: page
title: "Kaltura Player Toolkit Theme, Skin and Plugins Guide"
date: 2013-10-17 20:46:49
---

<span style="color: #000000; font-size: small;">This document provides a detailed walkthrough on skinning the Kaltura Player v2, starting with architecture overview, why Kaltura leads with HTML5, and a detailed description of how to include and build custom skin resources. The contents of this document are targeted for designers with a technical understanding of web front-end (specifically HTML5, CSS and JavaScript). A complimentary document will detail skinning and configuration with the friendly HTML5  player studio user interface. </span>

<span style="color: #000000; font-size: small;">For a listing of all the relevent player APIs see <a href="http://player.kaltura.com/docs/api" title="player api">player.kaltura.com/docs/api</a><br /></span>

<p class="mce-heading-2">
  Architecture Overview 
</p>

The Kaltura Player v2 Toolkit, aka Player v2, greatly simplifies the configuration and skinning of Kaltura players vs. previous versions. Let's look at some differences between Player v2 and the older KDP + HTML5 player model:

<table style="border: 1px solid #cccccc; width: 100%;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td class="mce-sub-heading" valign="top" width="10%">
        <p>
           
        </p>
      </td>
      
      <td class="mce-sub-heading" valign="top" width="45%">
        <p>
          Player Toolkit v2
        </p>
      </td>
      
      <td class="mce-sub-heading" valign="top" width="45%">
        <p>
          KDP + HTML5 v1
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="10%">
        <p>
          Skinning
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          CSS for all players.
        </p>
      </td>
      
      <td valign="top" width="33%">
        <p>
          Swf files, uiConf xml updates and CSS + javascript to skin HTML5 player.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="10%">
        <p>
          Configuration
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          JSON
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          UiConf XML, and some inline settings calls for HTML5 settings
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="10%">
        <p>
          Iframe Plugins
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          Once in HTML5
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          You have to write iframe plugins twice once for HTML5 and once for Flash / KDP.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="10%">
        <p>
          On Page Plugins or page Scripting
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          Same On Page KDP API as v1
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          Robust on-page KDP player API.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="10%">
        <p>
          Native
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          Wraps native player components against the HTML5 library for full Kaltura player feature and skinning support in native iOS and Android environments.
        </p>
      </td>
      
      <td valign="top" width="45%">
        <p>
          Native players with different runtimes, Object C and Android Java needed to be skinned, customized and configured separately. 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <span style="color: #666560; font-size: 12pt; font-weight: bold;">Kaltura Player v2 Toolkit Architecture Diagram</span>
</p>

The following diagram visualizes the architecture of Kaltura Player v2 Toolkit, and highlights its flexibility and robustness across platforms and devices: 

<img src="{{site.url}}/assets/1642">

 

As the diagram outlines, we can leverage native components for <a href="https://github.com/kaltura/player-sdk-native-ios/" target="_blank">iOS</a> and <a href="https://github.com/kaltura/player-sdk-native-android" target="_blank" title="android native player component">Android</a> in conjunction with the HTML5 runtime and Adobe flash or Microsoft Silverlight plugins, to transcend platform limitations across devices and browsers, while delivering the full Player v2 Toolkit experience. 

## Unified Player Property Managment

Another important aspect of the player architecture is the unified handing of all player and plugin properties. These properties which can be configured in JSON, at runtime, or set dynamically. See API documentation on properties. These properties can also be combined via macros as a value for any property. For example your vast plugin property vast.adTagURL can include evaluations that reference any other plugin, player or context state. The follow diagram helps illustrate how context and content can be used in ad tag urls, the same macro mapping is used in player-serverices ( ad stitching ) product. Also see vast ad tags documentation. This can be used outside of ads and analytics, for example using content metadata to define watermark image url; accomplishing many business logic requirements as purely configuration. 

<img src="{{site.url}}/assets/2240">

<p class="mce-heading-2">
  Leading With HTML5
</p>

What about old versions of Internet Explorer, Android Fragmentation, and iOS limitations? As the architecture diagram highlights, we seamlessly switch to a Chromeless Flash player in a desktop where needed. For example, you are broadcasting a live stream to a target browser that does not support mpeg-dash delivery, the player will seamlessly switch to the HLS in Flash or HDS stream. Or if you must deliver content controls on content, an iOS native component can be used for video delivery in native environment while maintaining the same look and feel across platforms.

<p class="mce-heading-2">
  <a name="native"></a>Why Native?
</p>

What advantages are gained by going native? Here is a feature list that will help explain the advantages of Kaltura Player Toolkit in native environments:

<table style="width: 100%; border: 1px solid #cccccc;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="89">
        <p>
           
        </p>
      </td>
      
      <td class="mce-sub-heading" valign="top" width="89">
        <p>
          iOS WebView
        </p>
      </td>
      
      <td class="mce-sub-heading" valign="top" width="89">
        <p>
          iOS Native with Kaltura Player Toolkit
        </p>
      </td>
      
      <td class="mce-sub-heading" valign="top" width="89">
        <p>
          Android WebView
        </p>
      </td>
      
      <td class="mce-sub-heading" valign="top" width="89">
        <p>
          Android with Kaltura Player Toolkit
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          CSS Skin
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Not supported on iPhone
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          JS Plugins
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          Apple HLS Playback
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Broken support across fragmented platform
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported, with consistent experience across android versions.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          MPEG-Dash
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Unsupported, dependent on Apple.
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported via partners software players
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          No support in android < 4.1, Android Chrome supports in webview
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported via partners software players
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          ChromeCast
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          <span>Unsupported</span>
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          <span>Unsupported</span>
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          <span>Supported</span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          AirPlay
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          <span>Supported</span>
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          <span>Supported</span>
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          <span>Unsupported</span>
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          <span>Unsupported</span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          AutoPlay
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Unsupported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Unsupported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          HTML5 Overlays
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Not supported on iPhone
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported on iPhone and iPad
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Broken support across fragmented platform
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          Fullscreen
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Only native controls in true fullscreen
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supports custom HTML controls in fullscreen
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          No support in android < 4.1, Android Chrome supports fullscreen.
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supports custom HTML controls in fullscreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          Volume Control
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Only device level volume control
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supports in-player ui for volume control
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Only device level volume control
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supports in-player ui for volume control
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          Ads
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Native controls on iPhone, ads can be skipped ui does not reflect “ad state”
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Full Support via HTML controls that reflect ad playback
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          No support in android < 4.1, Android Chrome supports HTML controls
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Supported, with consistent experience across android versions.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          Offline Playback
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Unsupported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Coming soon
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Unsupported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Coming soon
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="89">
        <p>
          DRM and Content Controls
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Unsupported
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Via Partners and part of offering
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Unsupported, outside of latest version of Android Chrome with Encrypted Media Extension (EME) w/ Widevine & ClearText
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          Via partners and part of offering.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span class="mce-heading-2">Getting Started with Skinning a Kaltura Player </span>

<p class="mce-procedure">
  The following steps outline a basic "hello world" approach for CSS based player skin, and setup a player development environment:
</p>

1.  Login into your Kaltura Management Console (KMC) and open the <a href="http://kmc.kaltura.com/index.php/kmc/kmc4#studio|playersList" target="_blank" title="kmc player list">Studio's player list</a>. 
2.  Create a "new" player in the "[Universal Studio][1]" and give it a title such as "Player V2 Custom Skin".
3.  Select Content from the Actions dropdown menu for the v2 Player you created.
4.  Select "Preview and embed" from the Actions menu, for an arbitrary entry from the <a href="http://kmc.kaltura.com/index.php/kmc/kmc4#content|manage" target="_blank" title="kmc content listing">content list</a>,
5.  In the Preview and embed window, select Advanced Options and then select Dynamic Embed.
6.  Copy the respective code.
7.  Paste the code into a page hosted on a webserver ( locally or remote ). Note you should access the page via a web server with http:// not file://  
    You should now have a page that looks like this:  
    <img src="{{site.url}}/assets/1281">
8.  Create a new file called "customSkin.css" in the same folder. For starters this will just change the play button to a jack-o-lantern.
9.  <pre class="brush: jscript;gutter: false; light: true; fontsize: 100; first-line: 1; ">/* clear out the font based icon */
.largePlayBtn.icon-play:before {
    content: "";
}
/* replace play button with jack-o-lantern: */
.mwPlayerContainer .largePlayBtn, .mwPlayerContainer .largePlayBtn:hover{
    background-image: url('http://0.tqn.com/d/webclipart/1/0/o/s/4/Jack-O-Lantern2.png');
    background-size: 93px 100px;
    width:93px;
    height:100px;
    padding: 0px;
    margin:-50px;
}</pre>

10. Save the file.
11. Point the player to the css file with the "IframeCustomPluginCss1" configuration option bold in the sample code:   
    <pre class="brush: jscript;gutter: false; light: true; fontsize: 100; first-line: 1; ">&lt;script&gt;
kWidget.embed({
    "targetId": "kaltura_player_1382198751",
    "wid": "_243342",
    "uiconf_id": 20540612,
    "flashvars": {
        "streamerType": "auto",
        "IframeCustomPluginCss1" : 'customSkin.css'
    },
    "cache_st": 1382198751,
    "entry_id": "1_sf5ovm7u"
});
&lt;/script&gt;</pre>

12. Now load the page in your browser. You should get:  
      
     <img src="{{site.url}}/assets/1282">
      
    

 [1]: http://knowledge.kaltura.com/universal-studio-information-guide "universal player studio"

Because of the robust CSS based layout support, many skins can be built almost entirely using CSS. You can inspect the player to see the CSS target names of various player components.   
When moving to production you should host your CSS file in an absolute URL and reference it from the same config line. In the near future we plan to support hosting all player related assets within Kaltura. 

<p class="mce-heading-2 mce-heading-3">
  Edit UIVars, Adding CSS or JS to JSON config with the Universal Studio
</p>

After you are satisfied with your CSS adjustments and have pushed your CSS or JavaScript to a CDN location, you can use the <a href="http://knowledge.kaltura.com/universal-studio-information-guide" target="_blank" title="Universal studio">Universal Studio</a> to quickly insert your custom CSS & JS into the JSON config. Within the Universal Studio go to the "Plugins -> uiVars" section, and then use the same keys IframeCustomPluginCss1 & IframeCustomPluginJs1 to insert the values: 

<img src="{{site.url}}/assets/1576">

<p class="mce-heading-3">
  JSON Config vs uiConf Config
</p>

The Kaltura Player v2 principal configuration format is JSON. Older players used uiConf xml. The Kaltura Player v2 can convert uiConf xml on the fly to the JSON format that is uses, but you won't have as fine grain control over layout plugins configuration using the converter. Going forward, it is best to use the JSON format to configure your v2 player. A uiConf that broadly enables features with default configuration looks like this: 

<pre class="brush: jscript;gutter: false; light: true; fontsize: 100; first-line: 1; ">{
    "plugins":{
        "topBarContainer": {},
        "titleLabel": {},
        "controlBarContainer": {
            "hover": true
        },
        "largePlayBtn": {},
        "scrubber": {},
        "playPauseBtn": {},
        "volumeControl": {},
        "fullScreenBtn": {},
        "durationLabel": {},
        "currentTimeLabel": {},
        "sourceSelector": {},
        "closedCaptions": {},
        "watermark": {
            "cssClass": "topLeft",
            "img": "http://www.kaltura.com/content/uiconf/kaltura/kmc/appstudio/kdp3/exampleWatermark.png"
        },
        "logo": {},
        "infoScreen": {}
    },
    "uiVars":[{
        "key":"autoPlay",
        "value":false,
        "overrideFlashvar":false

    }],
    "layout":{
        "skin": "kdark",
        "cssFiles":[]
    }
}</pre>

Custom plugins can be written directly into the JSON with the same external resource attributes. These are:  
iframeHTML5Js1 = location of custom javascript resource  
iframeHTML5Css = location of custom css resource

 

<p class="mce-heading-3">
  Editing JSON locally
</p>

During development it can be beneficial to load and edit a local JSON file. To do this simply use the "jsonConfig" var and a local request. Assuming you saved the above json example as myplayer.json

<pre class="brush: as3;fontsize: 100; first-line: 1; ">&lt;script&gt;<br />$.ajax( "myplayer.json", function(jsonConfig){
   kWidget.featureConfig({
	'targetId' : 'kaltura_player',
	'wid' : '_243342',
	'uiconf_id' : '5994862',
	'entry_id' : '0_uka1msg4',
	jsonConfig: JSON.stringify(jsonConfig)
   })<br />});
&lt;/script&gt;</pre>

<p class="mce-heading-3">
  How Can I Update server side jsonConfig Today? 
</p>

Using the API, you can update the the JSON config with the <a href="http://player.kaltura.com/kWidget/tests/PlayerVersionUtility.html" target="_blank" title="player version utility">player version utility</a>. The Universal Player Studio also updates these JSON configuration files directly. 

<p class="mce-heading-3">
  Adding a New Component to Your Player
</p>

To add a JavaScript component to the player you can use the "iframeHTML5Js1" attribute to add a JS file to your player. For example:

<pre class="brush: as3;fontsize: 100; first-line: 1; ">&lt;script&gt;
kWidget.featureConfig({
	'targetId' : 'kaltura_player',
	'wid' : '_243342',
	'uiconf_id' : '5994862',
	'entry_id' : '0_uka1msg4',
	'flashvars': {
		"myComponent":{
			"plugin": true, // plugins should be enabled with plugin=true attribute 
		    	"iframeHTML5Js" : "myComponent.js" // your component javascript.
			"iframeHTML5Js1" : "moreStuff.js" // additional component javascript.
			"iframeHTML5Css": "myComponent.css" // you components css              
		}
	}
})
&lt;/script&gt;
</pre>

**NOTE: **Flashvar based resoruce includes will only work on relative paths. You should save absolute external resource URLs to your configuration file for them to work in your pdocution players. Absolute URLs are also important in production players, so that your component or plugin wil work wherever your player is embeded.    

This sample component file adds a logo to the control bar, Its configuration options are defined by the "defaultConfig" set.  

Please note the **mw.kalturaPluginWrapper(function(){ **wrapping. This is needed for any external plugin because of how external resources are opertunitily loaded.

<pre class="brush: as3;fontsize: 100; first-line: 1; ">mw.kalturaPluginWrapper(function(){

	mw.PluginManager.add( 'myComponent', mw.KBaseComponent.extend({
		defaultConfig: {
			parent: "controlsContainer",    // the container for the button 
			order: 41,                      // the display order ( based on layout )
			displayImportance: 'low',       // the display importance, determines when the item is removed from DOM
			align: "right",                 // the alignment of the button

			cssClass: "kaltura-logo",       // the css name of the logo
			href: 'http://www.kaltura.com', // the link for the logo
			title: 'Kaltura',               // title
			img: null                       // image
		},
		isSafeEnviornment:function(){
		        // any runtime checks to determine the plugin can be active 
		        // for example if you need to check if this partner has a key against your service: 
		        var deferred = $.Deferred();
		       $.ajax ( myAjaxRequst, function( data ){
		           deferred.resolve( !!data.isUserAllowed );
		        });
		        return deferred.promise();
		},
		setup: function(){
		       // The place to set any of your player bindings like:
		      this.bind( 'playerReady', function(){
		              // do something on player ready
		       });
		},
		getComponent: function() {
			if( !this.$el ) {
				var $img = [];
				if( this.getConfig('img') ){
					$img = $( '&lt;img /&gt;' )
								.attr({
									alt: this.getConfig('title'),
									src: this.getConfig('img')
								});
				}
				this.$el = $('&lt;div /&gt;')
								.addClass ( this.getCssClass() )
								.append(
								$( '&lt;a /&gt;' )
								.attr({
									'title': this.getConfig('title'),
									'target': '_blank',
									'href': this.getConfig('href')
								}).append( $img )
							);
			}
			return this.$el;
		}
	}));

});</pre>

You can see all sort of components in the [code repository][2]. Remember the entire Player v2 Toolkit is open source ;)

 [2]: http://github.com/kaltura/mwEmbed

<p class="mce-heading-2">
  Player States CSS
</p>

CSS states are CSS classes that are added to the outer most interface element at given player state. These are very useful for quickly building a given look and feel at a given player state, without involving a lot of complicated javascript bindings.  

*   **<span style="font-family: 'courier new', courier;">.fullscreen</span>** - The player in fullscreen
*   **<span style="font-family: 'courier new', courier;">.touch</span>** - Indicates that we're currently on touch device.
*   **<span style="font-family: 'courier new', courier;">.player-out</span>** - The player is focus out ( I use it to hide the control bar ).
*   **<span style="font-family: 'courier new', courier;">.start-state</span>** - The player is on start screen ( before user clicked play ).
*   **<span style="font-family: 'courier new', courier;">.load-state</span>** - The player is in loading state ( on startup, change media ).
*   **<span style="font-family: 'courier new', courier;">.play-state</span>** - The player is playing.
*   **<span style="font-family: 'courier new', courier;">.pause-state</span>** - The player was paused.
*   **<span style="font-family: 'courier new', courier;">.end-state</span>** - The player is on end screen ( video completed )
*   **<span style="font-family: 'courier new', courier;">.adplay-state</span>** - The player is currently playing an ad.
*   **<span style="font-family: 'courier new', courier;">.disabled</span>** - The current component is "disabled" i.e the click or touch binding for this button is not active. 
*   <span style="font-size: 10px;"><strong><span style="font-family: 'courier new', courier;">.size-tiny</span></strong> – less than 300px</span>
*   <span style="font-size: 10px;"></span><span style="font-size: 10px;"><strong><span style="font-family: 'courier new', courier;">.size-small</span></strong> – less than 450px</span>
*   <span style="font-size: 10px;"></span><span style="font-size: 10px;"><strong><span style="font-family: 'courier new', courier;">.size-medium</span></strong> – less than 700px</span>
*   <span style="font-size: 10px;"></span><span style="font-size: 10px;"><strong><span style="font-family: 'courier new', courier;">.size-large</span></strong> – more than 700px</span>

<p class="mce-heading-3">
  CSS States Usage Examples
</p>

<span class="mce-sub-heading">On screen redBox HTML</span>

<pre class="brush: xml;gutter: false; light: true; fontsize: 100; first-line: 1; ">&lt;div class="redBox"&gt;&lt;/div&gt;</pre>

<span class="mce-sub-heading">In the CSS files</span> 

<pre class="brush: css;gutter: false; light: true; fontsize: 100; first-line: 1; ">.redBox {
    width: 100px;
    height: 100px;
    background-color: red;
}</pre>

<p class="mce-sub-heading">
  To hide the box when the mouse cursor is over the player 
</p>

<pre class="brush: css;gutter: false; light: true; fontsize: 100; first-line: 1; ">.player-out .redBox { display: none; }</pre>

As default, have your UI visible, and when it should be hidden use the <span style="font-family: 'courier new', courier;"><strong>.player-out</strong></span> class.

<p class="mce-sub-heading">
  To increase the box size when player is in fullscreen state
</p>

<pre class="brush: css;gutter: false; light: true; fontsize: 100; first-line: 1; ">.fullscreen .redBox { width: 300px; height: 300px; }</pre>

<p class="mce-sub-heading">
  To change the color to of the box to green when the video is paused
</p>

<pre class="brush: css;gutter: false; light: true; fontsize: 100; first-line: 1; ">.pause-state .redBox { background-color: green; }</pre>

<p class="mce-heading-3">
  CSS Animations Between Player States
</p>

You can also make use of [CSS animations][3] to transition between player states.

 [3]: https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_CSS_animations

<p class="mce-sub-heading">
  To transition the <span style="font-family: 'courier new', courier;">redBox</span> box size transformation when entering fullscreen state
</p>

<pre class="brush: css;gutter: false; light: true; fontsize: 100; first-line: 1; ">.redBox { transition: width 0.3s ease-in-out, height 0.3s ease-in-out;}
.fullscreen .redBox { width: 300px; height: 300px; } </pre>

<p class="mce-heading-2">
  Template Magic
</p>

Almost all plugin configuration options that end up being displayed on the player support templetized values. You have very powerful mechanisms at your disposal to create highly custom experiences with minimal effort. Let's take a simple example of [displaying the view count][4].  Here we have simply updated the title button text for its default "{mediaProxy.entry.name}" to "{mediaProxy.entry.name} has {mediaProxy.entry.views} views"<span> Templates work by substituting data mappings against the current player / content instance.</span>

 [4]: http://kgit.html5video.org/pulls/437/modules/KalturaSupport/tests/TitleLabel.qunit.html#config%3D%7B%22flashvars%22%3A%7B%22titleLabel%22%3A%7B%22text%22%3A%22%7BmediaProxy.entry.name%7D%20has%20%7BmediaProxy.entry.views%7D%20views%22%2C%22includeInLayout%22%3Afalse%7D%7D%7D "sample template"

<p class="mce-heading-2">
  <span>Universal Studio</span>
</p>

<span>Read about the Player Universal Studio at length in the <a href="http://knowledge.kaltura.com/node/1148">Universal Studio Information Guide</a>.</span>

<span> </span>

###  