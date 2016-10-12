---
layout: page
title: "Omniture Plugin for the Kaltura Dynamic Player (KDP) Installation Guide"
date: 2014-09-21 13:25:41
---

<p class="mce-heading-2">
  Omniture Overview
</p>

Adobe Omniture SiteCatalyst (<http://www.omniture.com/en/products/analytics/sitecatalyst>) provides marketers with actionable, real-time web analytics intelligence about digital strategies and marketing initiatives. Adobe SiteCatalyst helps marketers quickly identify the most profitable paths through a website, segment traffic to spot high-value web visitors, determine where visitors are navigating away from the site, and identify critical success metrics for online marketing campaigns.

<p class="mce-heading-2">
  Omniture Kaltura Plugin Overview
</p>

The KDP plugin sends video-tracking events about the video played by the player. Events supported by the plugin are:

*   videoViewEvent
*   shareEvent
*   openFullscreenEvent
*   closefullscreenEvent
*   saveEvent
*   replayEvent
*   seekEvent
*   changeMediaEvent
*   gotoContributorWindowEvent
*   gotoEditorWindowEvent
*   playerPlayEndEvent
*   mediaReadyEvent

<p class="mce-procedure">
  To Install the Omniture Plugin for the Kaltura Dynmaic Player 
</p>

1.  Contact your Adobe Omniture representative and receive account information parameters.
2.  Log into the Kaltura Management Console.
3.  Click the Studio tab and select Flash Studio.
4.  Select the player you want to add the plug-in to and select “Edit” under actions.
5.  Select the Features tab.
6.  Add the Omniture plugin configuration parameters under the “Additional Parameters and Plugins”  (omniture.path, omniture.plugin, etc.)

<p style="padding-left: 30px;">
  <img src="{{site.url}}/assets/1629">
</p>

The following lists the parameters for the plugin:

<table style="width: 752px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          <strong>Parameter name</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          <strong>Parameter description </strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          <strong>Sample Value</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          <strong>Required</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          path
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          The path to the plugin
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          omniture.path=“omniturePlugin/v3.4.20/omniturePlugin.swf”
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          plugin
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          Defines the plugin
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          omniture.plugin=true
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          position
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          Determins the location of the plugin in the player UI config XML
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          omniture.position=lastChild
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          relativeTo
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          Determines location of the plugin line in the player UI Config XML
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          omniture.relativeTo=PlayerHolder
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          height
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          omniture.height=0
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          width
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          omniture.width=0
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          includeInLayout
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          Display the plugin in the KDP layout
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          omniture.includeInLayout=false
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          account
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          The customer’s Omniture account
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          trackingServer
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          Omniture tracking server URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          “w88.go.com”
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          Yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          trackMilestones
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          Percentiles of the video that should be tracked
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          25, 50, 75, 100
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          visitorNamespace
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          Omniture visitor namespace
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          customEvents
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
          Defines  custom events that are not part of the out of the box events.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          adStart, adClick, myCustomPluginNotification
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          channel
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="184">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <p>
          "{mediaProxy.entryMetadata.Omniturech}"
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <p>
          No
        </p>
      </td>
    </tr>
  </tbody>
</table>

Each of the plugin dynamic events can get custom *eVars* and custom *props*. The Omniture plugin has a mechanism that parses dynamic attributes that are configured in the uiConf and added to the relevant event. So for example, for the saveEvent the following uiConf parameters may be configured:

<pre class="brush: php;fontsize: 100; first-line: 1; ">//this part of omniture UiConf node will deal with the save event
saveEvent="event22"

saveEventEvar1="eVar18" saveEventEvar1Value="{mediaProxy.entry.name}"

saveEventEvar2="eVar19" saveEventEvar2Value="{configProxy.flashvars.referer}"

saveEventProp1="prop33" saveEventProp1Value="{mediaProxy.entry.id}"

saveEventProp2="prop32" saveEventProp2Value="{configProxy.flashvars.myFlashvar}"</pre>

<p class="mce-heading-3">
  Structure for Dynamic Events
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="217">
        <p style="text-align: left;">
          <strong>Parameter name</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Parameter description</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Sample Value</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Required</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="217">
        <p>
          [EVENT NAME]
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Map the event to a specific Omniture event number
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          videoViewEvent=”event1”
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="217">
        <p>
          [EVENT NAME]Evar[Number]
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Specify an individual eVar name for an specific event
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          saveEventEvar1=”eVar18”
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="217">
        <p>
          [EVENT NAME]Evar[Number]Value
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Specify an individual eVar value for an specific event
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          saveEventEvar1Value="{mediaProxy.entry.name}"
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="217">
        <p>
          [EVENT NAME]Prop[Number]
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Specify an individual prop name for an specific event
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          saveEventProp1=”prop33”
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="217">
        <p>
          [EVENT NAME]Prop[Number]Value
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Specify an individual prop value for an specific event
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          saveEventPropValue="{mediaProxy.entry.id}"
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p style="text-align: left;">
          No
        </p>
        
        <div>
           
        </div>
      </td>
    </tr>
  </tbody>
</table>

 