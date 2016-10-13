---
layout: page
title: "508 Support within the Kaltura Player Toolkit"
date: 2013-09-09 16:57:48
---

  
All Kaltura players that use the <a href="{{site.url}}/documentation/Knowledge/kaltura-player-toolkit.html" target="_blank">Kaltura Player Toolkit</a> are now 508 compliant by default and are based on on <a href="http://www.w3.org/TR/wai-aria/" target="_blank">W3C Accessible Rich Internet Applications (WAI-ARIA)</a>. The screen reader includes friendly markup and testing controls. The player uses HTML controls even when using Flash for video on older browsers. 

<span>Kaltura Player v2 </span> delivers a great keyboard input experience for users unable to use a mouse and a seamless browser-managed experience for better integration with web accessibility tools. The player also includes [keyboard shortcuts][1] for all main player functions and player plug-ins**<span>.</span>**  

 [1]: #shortcuts

<img src="../../assets/1209">

  
<span class="mce-sub-heading">Features</span>

The Kaltura Player v2 features include: 

*   Screen reader support ( fully tested against JAWS limited testing with others )
*   HTML5 first, Flash is chromeless and not responsible for any UI components, all UI components are in accessible HTML. 
*   Audio description tracks
*   Captions 
*   Tab index for all user interactive components
*   Tab into and tab out of player HTML role markups and area-labels for all controls, including sliders used for playhead scrubber and volume control
*   Keyboard short cut controls matching internet video player pseudo standard ( youtube ), with enhancements around rate control and support for custom mapping arbitrary notifications ( easily making plugins accessible )

<p class="mce-sub-heading">
  Default Keyboard Mappings
</p>

The following table lists the default keyboard mappings:

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <strong><a name="shortcuts"></a>Keyboard Shortcut</strong>
      </td>
      
      <td valign="top" width="435">
        <p>
          <strong>Action (the seekbar should be selected)</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          Left / Right arrow 
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          Jump back / ahead 5 seconds in the current video
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          Home / End
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          Seek to the beginning / last seconds of the video
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          Spacebar
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          Play / Pause
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          Numbers 1 to 9
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="Copyright">
          Seek to the 10% to 90% of the video
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          Number 0 [] +-     
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="Copyright">
          <span>Seek to the beginning of the video    </span><br /><span>Rate control (plugin) + faster - slower</span>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-sub-heading">
  Code Sample
</p>

A sample of the code used for the player is:

<img src="../../assets/1182">

<p class="mce-heading-2 mce-heading-3">
   
</p>