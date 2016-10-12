---
layout: page
title: "Kaltura Core, KMC, and Player Widgets - Nov. 18, 2013"
date: 2013-11-04 15:58:59
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Nov. 18, 2013</span>

These release notes pertain to the Hercules SaaS update released Nov. 18, 2013. 

These release notes are intended for Kaltura SaaS customers.

<table border="1" cellspacing="0" cellpadding="0">
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
          Release Branch 
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          IX-9.4.0
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
          IX-9.4.0
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
          5.36.10
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
        <p>
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.3" target="_blank">v3.9.3</a>
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
        <p>
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.5.</a>
        </p>
        
        <p>
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.0.0</a> 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">What's New in this Release</span>

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="92">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="top" width="228">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="bottom" width="288">
        <p class="TableHeading">
          <strong>Feature Availability</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="92">
        <p class="TableBodyText">
          Audio Codec
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="228">
        <p>
          Improved audio quality by utilizing FDK-AAC audio codec. Applicable to all H264/AAC flavors (default and custom)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="288">
        <p class="TableBodyText">
          General Availability
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="92">
        <p class="TableBodyText">
          HTML5 Player
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="228">
        <p>
          Initial release of the<a href="http://knowledge.kaltura.com/node/969" target="_blank"> HTML5 v2 player</a>. The new HTML5 version is the default for players created <span style="text-decoration: underline;">or updated </span>from the KMC.
        </p>
        
        <p>
          <strong>Note</strong>:  A few known issues related to Ads, sharing and IE compatibility are intended to be fixed in the next update.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="288">
        <p class="TableBodyText">
          General Availability
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Known Issues</span>

<table style="width: 415px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="78">
        <p class="TableHeading">
          <strong>JIRA #</strong>
        </p>
      </td>
      
      <td valign="top" width="337">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          PLAT-442
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          When categories are deleted while related batch processing is not active, the entries associated to the deleted categories are not assigend to the parent category.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          PLAT-434
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          When 2 WebEx conversions are processed in parallel, a video may be produced without sound.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          PLAT-429
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          is a specific case, when playing a Widevine flavor with access control restriction to allow playback from Canada only, the entry is played from all regions.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          FEC-543
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          The HTML5 player sends events at 25%, 50%, 75%, 100% of playback that should not be sent in live stream.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"></span><span style="font-size: 14pt; color: #828a8c; font-weight: bold;">Resolved Issues</span>

<table style="width: 415px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="78">
        <p class="TableHeading">
          <strong>JIRA #</strong>
        </p>
      </td>
      
      <td valign="bottom" width="337">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-1038
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          The issue with the HTML player not loading when VAST ad video of flv format, which is not playable on HTML5 was fixed. The player now continues loading ignoring the non-playable video.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-924
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          A specific KCW issue with categories selection not applying on uploaded videos was fixed (KCW v2.2.4)
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-806
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          A specific issue causing an uploaded video to hang in Pending Status in the KMC was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-728
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          A specific issue with videos uploaded via a drop folder indicating that the status was Ready, when actually the videos were not ingested properly, was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-1027
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          The problem with a playlist player triggering auto-play when clicking twice on playlist items was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-1046
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          An issue with delayed playback within a MediaSpace player due to a redundant character in the stream URL was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          PLAT-282
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          KMC’s Bandwidth and Storage Analytics table can now be ordered by the Transcoding Consumption column.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="78">
        <p class="TableBodyText">
          FEC-441
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          A specific issue with a clip not loading into the HTML5 player on IE 8 was fixed.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
   
</p>

<span style="font-size: 14pt; color: #828a8c; font-weight: bold;">KMC Tested Browsers</span>

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
      
      <td width="98">
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
      <td valign="bottom" width="98">
        <p>
          KDP
        </p>
      </td>
      
      <td valign="bottom" width="98">
        <p>
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.3" target="_blank">3.9.3</a><a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank"><br /></a>
        </p>
      </td>
      
      <td valign="bottom" width="128">
        <p>
          Chrome (latest) FF(latest) IE9, IE8
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="98">
        <p>
          <span>HTML5</span>
        </p>
      </td>
      
      <td valign="bottom" width="98">
        <p>
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.4</a><a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.3" target="_blank"></a>
        </p>
        
        <p>
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.0.0</a>
        </p>
      </td>
      
      <td valign="bottom" width="128">
        <span>iPad2 iOS 6.0.1 & 7.0.2, Galaxy S3 & Galaxy Tab 4.0.4</span> 
      </td>
    </tr>
  </tbody>
</table>