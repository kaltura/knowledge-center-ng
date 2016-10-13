---
layout: page
title: "Omniture Plugin Setup and Information Guide"
date: 2014-09-21 13:29:02
---

<div id="main-header" class="mce-heading-2">
  <div id="title-heading">
    Omniture Overview
  </div>
</div>

<p class="wiki-content">
  Adobe Omniture SiteCatalyst (<a href="http://www.omniture.com/en/products/analytics/sitecatalyst" rel="nofollow">http://www.omniture.com/en/products/analytics/sitecatalyst</a>) provides marketers with actionable, real-time web analytics intelligence about digital strategies and marketing initiatives. Adobe SiteCatalyst helps marketers quickly identify the most profitable paths through a website, segment traffic to spot high-value web visitors, determine when visitors are navigating away from the site, and identify critical success metrics for online marketing campaigns.Omniture Kaltura Plugin Overview and built-in eventsThe KDP plugin sends video-tracking events about the video played by the player. Events triggered by the plugin are:
</p>

*   Media.open
*   Media.play
*   Media.stop
*   Media.close
*   Media.openAd
*   Media.complete
*   Media.monitor

<p id="main-content" class="wiki-content">
  Milestone events (25%, 50%, 75%) A test page demonstrating these events can be found <a href="http://player.kaltura.com/docs/OmnitureOnPage" target="_blank" class="external-link" rel="nofollow">here</a>. A test page demonstrating ad events handling can be found <a href="http://kgit.html5video.org/tags/v2.27.1/kWidget/onPagePlugins/omnitureOnPage/OmnitureOnPageAds.qunit.html" target="_blank" class="external-link" rel="nofollow">here</a>. (Omniture sCode Config, SiteCatalyst 15 + VAST Ads)<br />In addition to the plugin built-in events, all of Kaltura player events can be registered by the plugin and reported to Omniture. See the <a href="#custom_setup">custom events setup</a> for more details.Plugin SetupYou will need to havd am Omniture and KMC account setup.
</p>

<p class="wiki-content">
  <span class="mce-heading-3">Omniture Account Setup</span>
</p>

*   Contact your Adobe Omniture representative and receive account information parameters.

<p class="wiki-content">
  <span class="mce-heading-3">Kaltura KMC Setup</span>
</p>

<div class="wiki-content">
  <ul>
    <li>
      Log into the  Kaltura Management Console and perform the following:
    </li>
  </ul>
</div>

**For Legacy Flash (V1) players:**

1.  Click on the "Studio" tab and select the "Flash Studio" tab.
2.  Select the player you want to add the plug-in to and select "Edit" under actions.
3.  Add the Omniture plugin configuration parameters under the "Additional Parameters and Plugins" (omniture.path, omniture.plugin, etc.).
4.  For full parameter specs, please see the <a href="{{site.url}}/documentation/Knowledge/omniture-plugin-kaltura-dynamic-player-kdp-installation-guide.html" target="_blank">Omniture Plugin for the Kaltura Dynamic Player (KDP) Installation Guide</a>.

**For HTML5 Universal (V2) players:**

1.  Click on the "Studio" tab and select the "Universal Studio" tab.
2.  Select the player you want to add the plug-in to
3.  Select  the "Analytics" icon from the left pane.
4.  Check the "Omniture on page" plugin checkbox and open it to fill its parameters:

**Plugin parameters setup:**

<div class="table-wrap">
  <table class="confluenceTable">
    <tbody>
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          <strong>FlashVar</strong>
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          <strong>Studio Parameter name</strong>
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          <strong>Parameter description</strong>
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          <strong>Sample Value</strong>
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          <strong>Required</strong>
        </td>
      </tr>
      
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          s_codeUrl
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Code url
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          The URL to the Ominture generated sCode file that must be set in the uiConf (not via flashvars). This parameter is required for the plugin to work.
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          adobe_sample_s_code.js
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Yes
        </td>
      </tr>
      
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          s_codeVarName
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Entry code name
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          The name of the s_code entry point in the global window scope. ("s" by default ).
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          s
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Yes
        </td>
      </tr>
      
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          monitorEventInterval
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Monitor event tracking interval
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Set to an interval (in seconds) for tracking the Omniture 'monitor' event.
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          10
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Yes
        </td>
      </tr>
      
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          trackEventMonitor
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Omniture events function name
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          A global callback function for logging Omniture events.
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          omnitureTrackingLog
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          no
        </td>
      </tr>
      
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          concatMediaName
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Media name concatenation rules
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          A per partner key for special media name concatenation rules. By default this parameter should be left null.
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
           
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          no
        </td>
      </tr>
      
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          customEvents
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Kaltura player events
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          A comma separated list of Kaltura player events you want to track.
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          "openFullScreen,closeFullScreen"
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          no
        </td>
      </tr>
      
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          additionalEvarsAndProps
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Omniture variables and properties
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          A comma separated list of Omniture evars and props, you wish to pass along with every media event.
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          "eVar51,prop44"
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          no
        </td>
      </tr>
      
      <tr>
        <td class="confluenceTd" style="text-align: left;" colspan="1">
          additionalEvarsAndPropsValues
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          Kaltura values
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          A comma separated list of Kaltura values, you want to pass along with every media event. <br class="atl-forced-newline" />Values will correspond to the evars and props comma separated map defined in the "Omniture variables and properties" field.
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          "{mediaProxy.entry.creatorId},{mediaProxy.entry.createdAt}"
        </td>
        
        <td class="confluenceTd" style="text-align: left;">
          no
        </td>
      </tr>
    </tbody>
  </table>
</div>

<p class="mce-heading-3">
  Registering Kaltura Player Events to Additional Player Events  
</p>

In addition to the plugin build-in events, all of Kaltura player events can be registered by the plugin and reported to Omniture. Additional properties can be sent with these events.

A test page demonstrating custom events can be found <a href="http://player.kaltura.com/docs/OmnitureOnPage" target="_blank" class="external-link" rel="nofollow">here</a>.

<a name="custom_setup"></a><span class="mce-procedure">To set up Omniture custom events</span>

1.  Define the player events you want to track by filling the "Kaltura player events" field in the Universal Studio ('customEvents' Flashvar). This should be a comma-delimited string holding the event strings.   
    For example:   
    <span><em>"openFullScreen,closeFullScreen,firstQuartile"</em></span>   
    **Note:** do not use spaces between the event strings.
2.  For each player event, define an Omniture event string.  
    For example:   
    <span><em>'openFullScreenEvent': 'event50'</em></span>
3.  Define one or more variables for each event. For each variable, you need to define a value, which can be fixed or evaluated using curly brackets syntax.   
    For example: <span><em>'openFullScreenEvar1': "eVar50"',<br />openFullScreenEvar1Value': "{mediaProxy.entry.id}"',<br />openFullScreenEvar2': "eVar51"',<br />openFullScreenEvar2Value': "{mediaProxy.entry.name}" </em></span>
4.  Define one or more properties for each event. For each property, you need to define a value, which can be fixed or evaluated using curly brackets syntax. For example:<span><em>'openFullScreenProp1': "prop50"</em></span> <span><em>'openFullScreenProp1Value': "{configProxy.flashvars.referer}"</em></span>
5.  You can also define generic variables and properties that will be sent with all custom events. These can be fixed or evaluated as well:<ol style="list-style-type: lower-alpha;">
      <li>
        Define the variables / properties names as a comma-delimited string in the "Omniture variables and properties" field in the Universal Studio ('additionalEvarsAndProps' Flashvar). <br />For example: <br /><span><em>'additionalEvarsAndProps': "eVar51,prop44"</em></span> <br /><strong>Note:</strong> do not use spaces between the strings.
      </li>
      <li>
        For each variable / property, define its value using a comma-delimited string in the "Kaltura values" field in the Universal Studio ('additionalEvarsAndPropsValues Flashvar). The order of the values corresponds to the order of the variables defined in the 'additionalEvarsAndProps' Flashvar. <br />For example: <br /><span><em>'additionalEvarsAndPropsValues': "{mediaProxy.entry.creatorId},{mediaProxy.entry.createdAt}"</em></span> <br /><strong>Note:</strong> do not use spaces between the strings.
      </li>
    </ol>

<p class="mce-heading-3">
  Example for Omniture setup using Flashvars with Custom Events
</p>

<pre class="brush: jscript;fontsize: 100; first-line: 1; ">'flashvars': {
 'omnitureOnPage' :{

 'plugin': true,
'includeInLayout':false,
'loadInIframe':true,
'onPageJs1': "{onPagePluginPath}/omnitureOnPage/resources/omnitureOnPage.js",
's_codeUrl': "resources/adobe_sample_s_code.js",
's_codeVarName': 's',
'trackEventMonitor': 'omnitureTrackingLog',
'monitorEventInterval': 10,
'customEvents': "openFullScreen,closeFullScreen,firstQuartile",
'firstQuartileEvent': "event45",
'firstQuartileEvar1': "eVar45",
'firstQuartileEvar1Value': "{mediaProxy.entry.name}",
'openFullScreenEvent': "event50",
'openFullScreenEvar1': "eVar50",
'openFullScreenEvar1Value': "{mediaProxy.entry.id}",
'openFullScreenEvar2': "eVar51",
'openFullScreenEvar2Value': "{mediaProxy.entry.name}",
'openFullScreenProp1': "prop50",
'openFullScreenProp1Value': "{configProxy.flashvars.referer}",
'closeFullScreenEvent': "event40",
'closeFullScreenEvar1': "eVar40",
'closeFullScreenEvar1Value': "{mediaProxy.entry.id}",
'closeFullScreenEvar2': "eVar41",
'closeFullScreenEvar2Value': "{mediaProxy.entry.name}",
'closeFullScreenProp1': "prop40",
'closeFullScreenProp1Value': "{configProxy.flashvars.referer}",
'additionalEvarsAndProps': "eVar51,prop44",
'additionalEvarsAndPropsValues': "{mediaProxy.entry.creatorId},{mediaProxy.entry.createdAt}"

 }

 }</pre>

 

<div id="likes-and-labels-container">
   
</div>