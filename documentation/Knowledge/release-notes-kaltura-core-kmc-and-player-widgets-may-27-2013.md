---
layout: page
title: "Release Notes -  Kaltura Core, KMC, and Player Widgets May 27, 2013"
date: 2013-05-26 11:23:37
---

<span style="color: #ff0000;"></span><span class="mce-heading-3">May 27, 2013</span>

These release notes pertain to the Hercules SaaS update released May 27, 2013. 

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
          5.35.6
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank">3.8.5</a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes#1.8.5" target="_blank">1.8.5</a>
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
          Ingestion flow for Webex recording files
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="300">
        <p class="TableBodyText" style="text-align: left;">
          Ingestion of Webex’s proprietary ARF files and converting them to customer’s flavor set, with the ability for multi-platform playback.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          The workflow supports:
        </p>
        
        <ul>
          <li style="text-align: left;">
            Import directly from Webex server
          </li>
          <li style="text-align: left;">
            Upload from desktop  
          </li>
          <li style="text-align: left;">
            Bulk upload (CSV, XML)<span style="font-size: 10px; text-align: center;"> </span>
          </li>
        </ul>
      </td>
      
      <td valign="top" width="210">
        <p class="TableBodyText" style="text-align: left;">
          <span style="color: #ff0000;">Limited Availability</span>.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          <span>Please contact your Account Manager for more information.</span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          Live Stream
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="300">
        <p>
          IP checks for live streaming provisioning were added to verify that the provided IP address is ‘pingable’ prior to a provisioning attempt.
        </p>
      </td>
      
      <td valign="top" width="210">
        <p style="text-align: left;">
          Available in all KMC accounts where the Live Stream option is enabled.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          Widevine DRM
        </p>
      </td>
      
      <td valign="top" width="300">
        <ul>
          <li style="text-align: left;">
            Support for multi-bitrate DRM packaging and adaptive bitrate playback has been added.
          </li>
          <li style="text-align: left;">
            Simplified the end-user experience for the initial download of the Widevine browser plugin. The existing redirect to the Widevine download page was removed and the download is now triggerred directly from Kaltura.
          </li>
          <li style="text-align: left;">
            Added appropriate messages to end-users when DRM content is loaded through a browser on devices that do not support Flash. (e.g. iOS)
          </li>
          <li style="text-align: left;">
            Automated update of Widevine assets distribution window according to entry scheduling.
          </li>
          <li style="text-align: left;">
            Support for DRM Packaging when transcoding with a local transcoders (flavors are uploaded to Kaltura)
          </li>
        </ul>
      </td>
      
      <td valign="top" width="210">
        <p style="text-align: left;">
          Available in all KMC accounts where the Widevine DRM- option is enabled. Widevine Distribution Window update requires separate activation 
        </p>
        
        <p style="text-align: left;">
          Please contact your Account Manager for more information.
        </p>
        
        <p style="text-align: left;">
          <strong> </strong>
        </p>
        
        <p style="text-align: left;">
          <strong>Note</strong>: Adaptive bitrate requires updates to existing transcoding profiles and DRM enabled players per information available in <a href="http://knowledge.kaltura.com/kaltura%E2%80%99s-digital-rights-management-drm-service-widevine-setup-and-workflow-guide" target="_blank">this article.</a>
        </p>
        
        <p>
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  Players
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
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          Akamai Media Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="300">
        <p>
          Supports overrides for custom Akamai media analytics properties.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          Widevine – DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="300">
        <p>
          Support for new DRM options.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <span style="font-size: 1.5em;">Resolved Issues</span>
</p>

 

<table style="width: 632px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="66">
        <p class="TableHeading">
          <strong>#</strong>
        </p>
      </td>
      
      <td valign="bottom" width="566">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          8071
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="566">
        <p class="TableBodyText">
          The issue with player from the preview and embed window staying on the KMC page after closing the window on IE browser, was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          8062
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="566">
        <p class="TableBodyText">
          The issue with KMC preview and embed window displaying poorly on Windows XP/IE8 was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          SUP-46
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="566">
        <p class="TableBodyText">
          A specific issue with subtitles not working in on iPad was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          8172
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="566">
        <p class="TableBodyText">
          A specific issue with a thumbnail not being distributed to YouTube together with the entry was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          7947
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="566">
        <p class="TableBodyText">
          The issue with KMC prompting an error message after unchecking flavors which were already removed from the account,  was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          7936
        </p>
      </td>
      
      <td style="text-align: left;" width="566">
        <p class="TableBodyText">
          The issue with playlist feed sent via URL not working on HTML5 player was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          SUP-90
        </p>
      </td>
      
      <td style="text-align: left;" width="566">
        <p class="TableBodyText">
          The issue with annotation tool (VAT) not encoding some special characters in user input ("<" and ">") was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          SUP-71
        </p>
      </td>
      
      <td style="text-align: left;" width="566">
        <p>
          The issues with playing an entry on an Android device (OS 4.1.2) when pre-roll ads were set was fixed by ignoring pre-roll ads in case the device does not support them. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="66">
        <p class="TableBodyText">
          8212
        </p>
      </td>
      
      <td style="text-align: left;" width="566">
        <p class="TableBodyText">
          The issue with a pre-roll ad using a DFP Small Business Tag not playing on KDP was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="66">
        <p class="TableBodyText">
          8039
        </p>
      </td>
      
      <td style="text-align: left;" width="566">
        <p class="TableBodyText">
          An issue with updating metadata objects, that causeddeletion of metadata schemas in some cases was fixed.
        </p>
      </td>
    </tr>
  </tbody>
</table>

 

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Known Issues</span>

<span class="mce-note-graphic">Some of the known bugs below will be fixed in upcoming days/weeks according to their severity.</span>

<table style="width: 595px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="83">
        <p class="TableHeading">
           #
        </p>
      </td>
      
      <td width="91">
        <p class="TableHeading">
          Component
        </p>
      </td>
      
      <td width="421">
        <p class="TableHeading">
          Summary
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          8384
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          When the intermediate H264 flavor is not transcoded due to a lower quality of the source flavor,  the Widevine single-bit-rate flavor expecting the transcoded flavor is stuck in a ‘waiting for conversion’ state. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          8383
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          When using a local transcoder and adding one of the intermediate H264 flavors by importing it manually from the Entry’s Flavors tab, the ingestion process may not complete properly.  
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          8382
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          Widevine flavor names do not appear in full within the playlist filter area in the KMC.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          8360
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          When an account is set to update the Widevine distribution window from entry scheduling, the Widevine distribution window info is deleted upon media replacement of the entry.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          8353
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          Repackaging of multi-bitrate flavor after one of the H264 flavors was re-transcoded does not finish properly.  (This issue is assumed to be Widevine related and is being investigated by Widevine)
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-185
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          After the DRM feature is disabled on a partner account,the  existing encrypted content will not play, however a relevant message is not displayed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          8250
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          HTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          If an entry has two pre-roll ads, the skip option is shown only at first preroll. Thesecond preroll skip option is unavailable.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Known Limitations</span>

<table style="width: 594px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="91">
        <p class="TableHeading">
          <strong>Component</strong>
        </p>
      </td>
      
      <td width="503">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="503">
        <p class="TableBodyText">
          DRM packaging requires that the source or the H264 flavors that should be encrypted be uploaded to Kaltura. DRM packaging is not supported when H264 flavors are only linked by Kaltura from a Remote storage location.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="503">
        <p class="TableBodyText">
          After manual processing of an H264 flavor that is part of a DRM package, manual DRM packaging should be initiated from the Flavor tab to update the existing DRM package.
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
          v3.8.5
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
          1.8.5
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

<h2 class="mce-heading-3 mce-heading-4">
  OS/Browsers Verified for Widevine DRM
</h2>

The following OS/Browsers were verified to support Widevine DRM including verification of Widevines’ browser plugin download and install.

√ - tested and OK

X – Was not tested

N/A – OS/browser combination is not applicable.  

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="126">
        <p>
          <strong> </strong>
        </p>
      </td>
      
      <td valign="top" width="93">
        <p>
          <strong>MAC 10.7.5</strong>
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          <strong>Windows 8</strong>
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          <strong>Windows 7</strong>
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          <strong>Windows Vista</strong>
        </p>
      </td>
      
      <td valign="top" width="95">
        <p>
          <strong>Windows XP</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p>
          <strong>Safari 5.1.7</strong>
        </p>
      </td>
      
      <td valign="top" width="93">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="95">
        <p>
          X
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p>
          <strong>Firefox (latest)</strong>
        </p>
      </td>
      
      <td valign="top" width="93">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="95">
        <p>
          √
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p>
          <strong>Chrome (latest)</strong>
        </p>
      </td>
      
      <td valign="top" width="93">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="95">
        <p>
          √
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p>
          <strong>IE 10</strong>
        </p>
      </td>
      
      <td valign="top" width="93">
        <p>
          NA
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="95">
        <p>
          NA
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p>
          <strong>IE 9</strong>
        </p>
      </td>
      
      <td valign="top" width="93">
        <p>
          NA
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="95">
        <p>
          NA
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p>
          <strong>IE 8</strong>
        </p>
      </td>
      
      <td valign="top" width="93">
        <p>
          NA
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="95">
        <p>
          √
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p>
          <strong>IE 7</strong>
        </p>
      </td>
      
      <td valign="top" width="93">
        <p>
          NA
        </p>
      </td>
      
      <td valign="top" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="top" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="top" width="95">
        <p>
          √
        </p>
      </td>
    </tr>
  </tbody>
</table>

 