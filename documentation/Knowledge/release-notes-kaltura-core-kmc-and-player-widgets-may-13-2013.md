---
layout: page
title: "Release Notes -  Kaltura Core, KMC, and Player Widgets May 13, 2013"
date: 2013-05-12 12:59:28
---

<span style="color: #ff0000;"></span><span class="mce-heading-3">May 13, 2013</span>

These release notes pertain to the Gemini SaaS update released May 13, 2013. 

These release notes are intended for Kaltura SaaS customers.

<table style="width: 633px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p>
          <strong>Product/Component</strong>
        </p>
      </td>
      
      <td valign="top" width="435">
        <p>
          <strong>Version Number / Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          Release Tag
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          2013_04_15
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          Server Version
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          7.1.4
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          KMC Version
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          5.35.2
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          KDP Version
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="Copyright">
          <a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank">3.8.4</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          HTML5 Version
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="Copyright">
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes#1.8.4" target="_blank">1.8.4</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

### <span style="font-size: 1.5em;">Resolved Issues</span>

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="65">
        <p class="TableHeading">
          <strong>QC #</strong>
        </p>
      </td>
      
      <td valign="bottom" width="275">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          7275
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="275">
        <p>
          The issue with “Search in Captions” option on MediaSpace’s not applying on default content was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          7832
        </p>
      </td>
      
      <td style="text-align: left;" width="275">
        <p>
          The issue with  a thumbnail that is included in entries bulk upload CSV not being set as the entry’s default thumbnail in some cases was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          8094
        </p>
      </td>
      
      <td style="text-align: left;" width="275">
        <p>
          A fix was made to enable proper filtering when using the Media list API with duration filter for listing media under a specific duration.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          8179
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="275">
        <p>
          The issue with  Kaltura.com domain added to the access control blocked domains list when using access control domain blocking was fixed. As a result it is now possible to view the video in the Kaltura generated tiny URL also when domain blocking (blocking other domains) is included in the access control profile. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          8198
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="275">
        <p>
          Thee KDP VAST Mute Event is no longer sent twice
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          8255
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="275">
        <p>
          The KDP now allows “play” of image entry when access control includes a KS restriction.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          8136
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="275">
        <p>
          Mouse focus issues in the KDP annotations box (annotation plugin) has been resolved
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          7526
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="275">
        <p>
          The KDP now properly sets the playback initial bitrate when playing with Akamai HD delivery method - according to preferedFlavorBR var settings.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          <a href="https://kaltura.atlassian.net/browse/FEC-153">FEC-153</a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="275">
        <p>
          The HTML5 player now sets pre-roll ads in a playlist according to KMC’s studio pre-roll display rule (display 1 pre-roll ad every 3rd video, starting with the 1st video )
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="65">
        <p>
          FEC-156
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="275">
        <p>
          The KDP now sends the VAST 3.0 Skip beacon properly.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><br />Known Issues</span>

<span class="mce-note-graphic">Some of the known bugs below will be fixed in upcoming days/weeks according to their severity.</span>

<table style="width: 595px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="84">
        <p>
          <strong>QC #</strong>
        </p>
      </td>
      
      <td width="86">
        <p>
          <strong>Component</strong>
        </p>
      </td>
      
      <td width="426">
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="84">
        <p>
          N/A
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="86">
        <p>
          KMC – Live Streaming
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="426">
        <p>
          The current IP Address populated as default value in the Add Live Stream window is sometimes not “pingable”. In such cases the live stream provisioning process will fail.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="84">
        <p>
          N/A
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="86">
        <p>
          KMC – Live Streaming
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="426">
        <p>
          The KMC notification on live stream activation with the CDN expected time is not aligned with actual provisioning time on Akamai which is sometimes higher than 20 min.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="84">
        <p>
          8064
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="86">
        <p>
          KDP
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="426">
        <p>
          KDP playback of DRM content fails in some cases when using Mac. A temporary fix can be provided per account.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #666560; font-size: 12pt; font-weight: bold;">KMC Tested Browsers</span>

The following browsers were tested for this release (recommended resolution 1024x768):

*   Firefox (latest)
*   Chrome (latest)
*   IE 9 on Windows 7

<p class="mce-heading-4">
  Player Tested Devices
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="98">
        <p align="center">
          <strong>Platform</strong>
        </p>
      </td>
      
      <td width="111">
        <p align="center">
          <strong>Version</strong>
        </p>
      </td>
      
      <td width="128">
        <p align="center">
          <strong>Reference Device</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="98">
        <p>
          KDP
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="111">
        <p>
          v3.8.4
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="128">
        <p>
          Chrome (latest) FF(latest) IE9, IE8
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="98">
        <p>
          HTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="111">
        <p>
          1.8.4
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="128">
        <p>
          iPad2 iOS 5.1.1 and 6.0.1
        </p>
      </td>
    </tr>
  </tbody>
</table>

 