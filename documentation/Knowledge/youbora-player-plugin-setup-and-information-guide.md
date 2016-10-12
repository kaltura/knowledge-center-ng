---
layout: page
title: "Youbora Player Plugin Setup and Information Guide  "
date: 2016-03-09 13:04:56
---

<p class="mce-heading-1">
    <span>Youbora Overview</span>
  </p>
  
  <p>
    <span>Youbora provides a business intelligence solution for broadcasters, OTTs, telcos and media to support your business decisions and drive performance. The ability to harness data across various integrated capabilities and services has become increasingly important to support multiple organizations across a video business, including marketing, and to drive consumer engagement and loyalty.</span>
  </p>
  
  <p>
    <span>The Youbora player plugin is integrated with the Kaltura player. The plugin listens and reports all the different player states in the current video session to Youbora Analytics. By taking all the data from inside the player, Youbora Analytics is capable of measuring the quality of the video experience from its source, the end user, and in turn analyzing the delivery process end to end. </span>
  </p>
  
  <p>
    <span class="mce-heading-3">Youbora Account Setup</span>
  </p>
  
  <ul>
    <li>
      Contact your Youbora represntative to receive account configuration details.
    </li>
  </ul>
  
  <p>
    <span class="mce-heading-3">Kaltura KMC Setup </span>
  </p>
  
  <p class="mce-procedure">
    To configure the Youbora plugin in the KMC Studio
  </p>
  
  <ol>
    <li>
      Log into the  Kaltura Management Console and click on the "Studio" tab and select the "Universal Studio" tab.
    </li>
    <li>
      Select the player you want to add the plug-in to.
    </li>
    <li>
      Select  the "Analytics" icon from the left pane.
    </li>
    <li>
      Check the "Youbora" plugin checkbox and open it to fill its parameters:
    </li>
  </ol>
  
  <table border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="148">
          Field
        </td>
        
        <td valign="top" width="135">
          Attribute
        </td>
        
        <td valign="top" width="210">
          Value
        </td>
        
        <td valign="top" width="293">
          Description
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="148">
          <p class="p1">
            <span class="s1">userId</span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="135">
          string
        </td>
        
        <td style="text-align: left;" valign="top" width="210">
           
        </td>
        
        <td style="text-align: left;" valign="top" width="293">
          Your Youbora user ID. 
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="148">
          bufferUnderrunThreshold
        </td>
        
        <td style="text-align: left;" valign="top" width="135">
          number
        </td>
        
        <td style="text-align: left;" valign="top" width="210">
          The default is 1000.
        </td>
        
        <td style="text-align: left;" valign="top" width="293">
          The minimum buffering time (in milliseconds) required to trigger the buffer under-run beacon.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="148">
          Track Event Monitor
        </td>
        
        <td style="text-align: left;" valign="top" width="135">
          trackEventMonitor
        </td>
        
        <td style="text-align: left;" valign="top" width="210">
          kalturaSendAnalyticEvent
        </td>
        
        <td style="text-align: left;" valign="top" width="293">
          Enables you to send the same events that you are sending to Youbora to other functions. For example addtional 3rd party systems. <br /><br />
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    <span class="mce-heading-4">Additonal Properties </span>
  </p>
  
  <p>
    In addition to the three properties available in the Kaltura <a href="http://knowledge.kaltura.com/node/1148#youbora" target="_blank">Universal Studio</a> for Youbora Analytics: user id, buffer underrun threshold, and trackEventMonitor, the following Youbora plugin properties may be configured through Flashvars.
  </p>
  
  <ul>
    <li>
      <a href="#contentMetadata">contentMetadata</a>
    </li>
    <li>
      <a href="#Param">Param[n]</a>
    </li>
  </ul>
  
  <h3>
    <a name="contentMetadata"></a>contentMetadata
  </h3>
  
  <p>
    The following example displays a JSON object holding metadata fields that you may send to Youbora with for each reported event.
  </p>
  
  <p>
                                                 "contentMetadata": {
  </p>
  
  <p>
                                                                "title": "{mediaProxy.entry.name}",
  </p>
  
  <p>
                                                                "genre": "", 
  </p>
  
  <p>
                                                                "language": "", 
  </p>
  
  <p>
                                                                "year": "",
  </p>
  
  <p>
                                                                "cast": "", 
  </p>
  
  <p>
                                                                "director": "", 
  </p>
  
  <p>
                                                                "owner": "", 
  </p>
  
  <p>
                                                                "duration": "{mediaProxy.entry.duration}", 
  </p>
  
  <p>
                                                                "parental": "", 
  </p>
  
  <p>
                                                                "price": "", 
  </p>
  
  <p>
                                                                "rating": "", 
  </p>
  
  <p>
                                                                "audioType": "", 
  </p>
  
  <p>
                                                                "audioChannels": ""
  </p>
  
  <p>
                                                 }
  </p>
  
  <p>
     
  </p>
  
  <p>
    The evaluated expressions are used to get media info. Only properties that contain values are sent to Youbora. In this example, only the title and duration are sent.
  </p>
  
  <p>
    Additional information on available properties that are stored in the Kaltura platform, that can be evaluated can be found <a href="http://player.kaltura.com/docs/api#evaluate-desc" target="_blank">here</a>.
  </p>
  
  <h3>
    <a name="Param"></a>Param[n]
  </h3>
  
  <p>
    You can define additional parameters to be sent to Youbora with each event. The params are defined as param1, param2, param3 etc.
  </p>
  
  <p>
    For example:
  </p>
  
  <p>
    “section”: “sport”,
  </p>
  
  <p>
    “demographic”: “male 24-35"
  </p>
  
  <p>
     
  </p>