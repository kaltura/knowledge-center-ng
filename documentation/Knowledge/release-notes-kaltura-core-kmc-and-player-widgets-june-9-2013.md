---
layout: page
title: "Release Notes -  Kaltura Core, KMC, and Player Widgets June 9, 2013"
date: 2013-06-10 13:37:10
---

<span style="color: #ff0000;"></span><span class="mce-heading-3">June 9, 2013</span>

These release notes pertain to the Hercules SaaS update released June 9, 2013. 

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
          2013_05_06
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
          7.1.5
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
          5.35.7
        </p>
        
        <p class="TableBodyText">
          KMC’s default player versions:
        </p>
        
        <p class="TableBodyText">
          KDP <a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank">3.8.5</a>
        </p>
        
        <p>
          HTML5 <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes#1.8.5" target="_blank">1.8.5</a>
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank">v3.8.6.rc1</a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes#1.8.6" target="_blank">1.8.6</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<h3 class="mce-heading-3">
  <span style="font-size: 1.5em;">What's New in this Release</span>
</h3>

<p class="mce-heading-4">
  Core/KMC
</p>

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="120">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="bottom" width="300">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="top" width="210">
        <p class="TableHeading">
          <strong>Feature Availability</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p>
          KMC Upload file type filter 
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="300">
        <p class="TableBodyText">
          The KMC Upload from Desktop option now allows a selection of files from the admin’s desktop without limiting to specific file type extensions. Default detection of entry type (video/audio/image) is kept as is.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <p class="TableBodyText">
          <span style="color: #000000;">General Avaiability in all KMC accounts</span>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  <span style="font-size: 1.5em; color: #828a8c;">Resolved Issues</span>
</p>

<table style="width: 393px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="102">
        <p class="TableHeading">
          <strong>QC #</strong>
        </p>
      </td>
      
      <td valign="bottom" width="291">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="102">
        <p class="TableBodyText">
          SUP-237
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="291">
        <p class="TableBodyText">
          The issue with DRM content not playing when the entry’s access control is set with domain restriction was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-204
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="291">
        <p class="TableBodyText">
          The issue with the “Media not Found” error message not showing properly in specific cases on Android devices with HTML5 player was fixed
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-201
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="291">
        <p class="TableBodyText">
          The specific issue with content stored on the wrong CDN was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-193
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="291">
        <p class="TableBodyText">
          The specific issue with thumbnails not transmitted to the YouTube-SFTP distribution target was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-144
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="291">
        <p class="TableBodyText">
          A KDP option was added to disable the player load spinner.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-116
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="291">
        <p class="TableBodyText">
          A type in KMC bulk upload error message (internal server error occurred) was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-115
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="291">
        <p class="TableBodyText">
          The issue with server errors prompted in specific cases when using bulk upload XML was fixed
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-87
        </p>
      </td>
      
      <td style="text-align: left;" width="291">
        <p class="TableBodyText">
          The issue with the KMC view being cut off in some cases when working with Windows XP-IE8 was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-85
        </p>
      </td>
      
      <td style="text-align: left;" width="291">
        <p class="TableBodyText">
          The issue with the HTML5 player not expanding to a full screen on some Android devices was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          SUP-63
        </p>
      </td>
      
      <td style="text-align: left;" width="291">
        <p class="TableBodyText">
          A specific issue with an entry stuck in “approved for distribution” status was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="102">
        <p class="TableBodyText">
          7804
        </p>
      </td>
      
      <td style="text-align: left;" width="291">
        <p class="TableBodyText">
          A warning message was added to indicate when a user selects unsupported entry types (e.g. live stream entries) for bulk download in the KMC.  
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="102">
        <p class="TableBodyText">
          8384
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="291">
        <p class="TableBodyText">
          When the intermediate H264 flavor is not transcoded due to a lower quality of the source flavor,  the Widevine single-bit-rate flavor expecting the transcoded flavor is stuck in a ‘waiting for conversion’ state. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="102">
        <p class="TableBodyText">
          8360
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="291">
        <p class="TableBodyText">
          When an account is set to update the Widevine distribution window from entry scheduling, the Widevine distribution window info is deleted upon media replacement of the entry.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"><br />Known Issues</span></span>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"></span></span>

<table style="width: 595px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          <strong>#</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          <strong>Component</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-194
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          HTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          The total number of entries in a rule based playlist is shown incorrectly in some cases with in HTML5 player on Android devices
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-222
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          Upload from Desktop
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          A non-user friendly message is prompted  when trying to upload a non-media file from the KMC <em>upload from desktop</em> option
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-219
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          Upload from Desktop
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          A timer animation stays on the KMC screen after uploading a non-media file from the KMC’s upload from desktop option
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #666560; font-size: 12pt; font-weight: bold;"><br />KMC Tested Browsers</span>

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
      
      <td style="text-align: left;" valign="bottom" width="128">
        <p>
          iPad2 iOS 5.1.1 and 6.0.1
        </p>
      </td>
    </tr>
  </tbody>
</table>