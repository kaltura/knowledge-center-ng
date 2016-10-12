---
layout: page
title: "Release Notes -  Kaltura Core, KMC, and Player Widgets March 3, 2013"
date: 2013-02-28 15:25:29
---

<span style="color: #ff0000;"></span><span class="mce-heading-3">March 3, 2013</span>

These release notes pertain to the Kaltura Core, KMC, and Player Widgets, released March 3rd, 2013. 

These release notes are intended for Kaltura SaaS customers.

<p class="mce-heading-4">
  <span>Release Components Details</span>
</p>

<table style="width: 633px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p>
          Product/Component
        </p>
      </td>
      
      <td valign="top" width="435">
        <p>
          Version Number / Description
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="198">
        <p style="text-align: left;">
          Release Tag
        </p>
      </td>
      
      <td valign="top" width="435">
        <p style="text-align: left;">
          gemini_2013_02_18
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p style="text-align: left;">
          Server Version
        </p>
      </td>
      
      <td valign="top" width="435">
        <p style="text-align: left;">
          Gemini 7.1.0
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p style="text-align: left;">
          KMC Version
        </p>
      </td>
      
      <td valign="top" width="435">
        <p style="text-align: left;">
          5.32.1 (Note that by default, KMC points to KDP 3.6.17 and not KDP 3.7.2)
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p style="text-align: left;">
          KDP Version
        </p>
      </td>
      
      <td valign="top" width="435">
        <p style="text-align: left;">
          <a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank">3.7.2</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p style="text-align: left;">
          HTML5 Version
        </p>
      </td>
      
      <td valign="top" width="435">
        <p style="text-align: left;">
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes#1.7.2" target="_blank">1.7.2</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  What's New in this Release?
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableHeading">
          <strong>Feature Availability</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText" style="text-align: left;">
          Live Delivery of video to Flash and HTML5
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText" style="text-align: left;">
          You can  provision live streams for both Flash HTTP Dynamic Streaming (HDS) and iOS HTTP Live Streaming. You can also associate entries with custom live URLs, for cases where 3<sup>rd </sup>party live streamers are used. For more information see <a href="http://knowledge.kaltura.com/node/816">What are the live streaming types available in the KMC</a>.
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText" style="text-align: left;">
          Requires account activation. Please contact your Account Manager for more information.
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText" style="text-align: left;">
          Preview and Embed feature enhancements
        </p>
      </td>
      
      <td valign="top" width="435">
        <ul>
          <li style="text-align: left;">
            Ability to preview all types of players such as: single entry, playlist, multiple playlists, live stream and on-page plugins.
          </li>
          <li style="text-align: left;">
            User settings are saved to the browser.
          </li>
          <li style="text-align: left;">
            Ability to copy the actual embed code in one click (no more Ctrl + C!)
          </li>
          <li style="text-align: left;">
            iFrame embed code added to preview and embed options. Good for pages that do not allow 3rd party JavaScript or have stringent page security requirements
          </li>
        </ul>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText" style="text-align: left;">
          Requires account activation. Please contact your Account Manager for more information.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  <span style="font-size: 12pt;">Known Issues</span>
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="81">
        <p class="TableHeading">
          <strong>ID</strong>
        </p>
      </td>
      
      <td valign="top" width="183">
        <p class="TableHeading">
          <strong>Module</strong>
        </p>
      </td>
      
      <td width="372">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="81">
        <p class="TableBodyText">
           7262/6935
        </p>
      </td>
      
      <td valign="top" width="183">
        <p class="TableBodyText" style="text-align: left;">
          HTML5
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          If you are using access control to restrict playback for a live stream entry, the player may get stuck while loading if the access control check was applied and not met. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="81">
        <p class="TableBodyText">
           7228
        </p>
      </td>
      
      <td valign="top" width="183">
        <p class="TableBodyText" style="text-align: left;">
          KDP
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          The "waiting for broadcasting" text is missing in live stream entry. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="81">
        <p class="TableBodyText">
          7159
        </p>
      </td>
      
      <td valign="top" width="183">
        <p class="TableBodyText" style="text-align: left;">
          KMC
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          Analytics: Only 10 rows are exported for the following reports: (User Engagement Report drilldown, End User Storage Report, End User Storage Report drilldown).
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="81">
        <p class="TableBodyText">
          7132
        </p>
      </td>
      
      <td valign="top" width="183">
        <p class="TableBodyText" style="text-align: left;">
          HTML5
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          The playback may get stuck loading if the entry has a bumper video ad.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="81">
        <p class="TableBodyText">
          7130
        </p>
      </td>
      
      <td valign="top" width="183">
        <p class="TableBodyText" style="text-align: left;">
          HTML5
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          A Flash error is returned (in the debug Flash player) each time a player is loaded when working with the new HTML5 library.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  Limitations
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="81">
        <p class="TableHeading">
          ID
        </p>
      </td>
      
      <td valign="top" width="183">
        <p class="TableHeading">
          Module
        </p>
      </td>
      
      <td width="372">
        <p class="TableHeading">
          Description
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="81">
        <p class="TableBodyText">
           N/A
        </p>
      </td>
      
      <td valign="top" width="183">
        <p class="TableBodyText">
           KMC 
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          The new preview and embed window is <strong>not</strong> operable in IE broswers.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span class="mce-heading-4">Resolved Issues</span>

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="198">
        <p class="TableHeading">
          <strong>ID</strong>
        </p>
      </td>
      
      <td width="372">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          6983
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          The FreeWheel Distribution error for reported cases has been resolved. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          6939
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          The control bar is now available with the flashvar autoplay (Live stream content).
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          7135
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          XML Bulk upload - The default thumbnail from a URL is now updating correctly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          6183
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableBodyText" style="text-align: left;">
          KMC: The 'Export to CSV' in the KMC limitation has been changed from the KMC pager size to all lines in the report. 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span class="mce-heading-4"><span style="font-size: 12pt;">Tested Browsers</span></span>

The following browsers were tested for this release (recommended resolution 1024x768):

*   Firefox (latest)
*   Chrome (latest)
*   IE 9 on Windows 7

<p class="mce-heading-4">
  Player Tested Devices
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="367">
        <p style="text-align: left;">
          KDP
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="367">
        Chrome (latest) FF(latest) IE9, IE8 
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="367">
        HTML5  
      </td>
      
      <td style="text-align: left;" valign="top" width="367">
        iPad2 iOS 5.1.1 and 6.0.1 
      </td>
    </tr>
  </tbody>
</table>