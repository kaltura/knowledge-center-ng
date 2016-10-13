---
layout: page
title: "CVAA Support within the Kaltura Player Toolkit"
date: 2016-08-31 13:21:39
---

<p>
    <br />The <a href="https://www.fcc.gov/consumers/guides/21st-century-communications-and-video-accessibility-act-cvaa">Twenty-First Century Communications and Video Accessibility Act of 2010 (CVAA)</a> focuses on ensuring that communications and media services, content, equipment, emerging technologies, and new modes of transmission are accessible to users with disabilities.  All Kaltura players that use the <a href="{{site.url}}/documentation/Knowledge/kaltura-player-toolkit.html" target="_blank">Kaltura Player Toolkit</a> are now CVAA compliant by default and are based on on <a href="http://www.fcc.gov/guides/21st-century-communications-and-video-accessibility-act-2010" target="_blank" title="Twenty-First Century Communications Accessibility Act 2010">Twenty-First Century Communications and Video Accessibility Act of 2010 (CVAA)</a>.  The player includes capabilties for editing the style and display of captions and can be modified by the end user. The closed captions styling editor includes easy to use markup and testing controls.  The Kaltura Player v2 delivers a great keyboard input experience for users and a seamless browser-managed experience for better integration with web accessibility tools. This is in addition to including the capability of turning closed captions on or off. 
  </p>
  
  <p>
    <img src="../../assets/3400">
  </p>
  
  <p>
    <span class="mce-sub-heading">Features</span>
  </p>
  
  <p>
    The Kaltura Player v2 CVAA features include: 
  </p>
  
  <ul>
    <li>
      Studio support - Enable options menu
    </li>
    <li>
      Captions types: XML, SRT/DFXP, VTT(outband)
    </li>
    <li>
      Displaying and changing fonts in 64 color combinations using eight standard caption colors currently required for television sets.
    </li>
    <li>
      Adjusting character opacity
    </li>
    <li>
      Ability to adjust caption background in eight specified colors.
    </li>
    <li>
      Ability to adjust character edge (i.e., non, raised, depressed, uniform or drop shadow).
    </li>
    <li>
      Ability to adjust caption window color and opacity.
    </li>
    <li>
      Support for displaying multiple language tracks and simplified or reduced captions.
    </li>
    <li>
      Ability to preview setting changes, have display setting remembered between viewings and turn captions on or off as easily as muting or adjusting the volume.
    </li>
    <li>
      Capability of displaying various caption formats (i.e., pop-on, roll-up and paint-on)
    </li>
  </ul>
  
  <p>
    For more information on how to configure and use the captions styling editor see the <a href="https://knowledge.kaltura.com/node/1148#cvaa">Universal Studio Information Guide</a>.
  </p>
  
  <h1>
    Caption Styles API
  </h1>
  
  <p>
    You can update caption styles via API call, using the following object format:
  </p>
  
  <pre class="brush: xml;fontsize: 100; first-line: 1; "> kWidget.addReadyCallback( function( playerId ){
    var kdp = document.getElementById( playerId );
     kaltura_player.sendNotification("newCaptionsStyles",
       {
           "fontFamily": "Courier New, Courier, Nimbus Mono L, Cutive Mono, monospace",
           "fontColor": "rgb(123, 33, 111, 0.8)",
           "fontSize": "3em",
           "backgroundColor": "rgba(1, 1, 1, 0.5)",
           "windowColor": "rgba(255, 255, 0, 0.8)",
           "charEdgeStyle": "rgb(34, 34, 34) 2px 2px 3px, rgb(34, 34, 34) 2px 2px 4px, rgb(34, 34, 34) 2px 2px 5px"
       }
     );
 });</pre>
  
  <p>
     You can set up the default styles settings, using "cvaaDefaultSettings" flashvar:
  </p>
  
  <pre class="brush: xml;fontsize: 100; first-line: 1; ">  'flashvars': {
            'cvaa':{
                'cvaaDefaultSettings': {
                     'fontFamily': "Arial, Roboto, Arial Unicode Ms, Helvetica, Verdana, PT Sans Caption, sans-serif",
                     'fontColor': "#ffffff",
                     'fontOpacity': 100,
                     'fontSize': 12,
                     'backgroundColor': "#000000",
                     'backgroundOpacity': 75,
                     'windowColor': "#ffffff",
                     'windowOpacity': 0,
                     'edgeStyle': "none"
                 }
             }
         }

NOTE:The caption menu style settings are saved using cookies per page. You can disable cookies, however, when you refresh the settings will not be saved and the default will be used.
To disable cookie for the plugin set the following flashvar to false:

        'flashvars': {
            'cvaa':{
                'useCookie': false
             }
         }</pre>