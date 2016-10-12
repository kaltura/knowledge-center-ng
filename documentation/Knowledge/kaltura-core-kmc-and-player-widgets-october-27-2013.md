---
layout: page
title: "Kaltura Core, KMC, and Player Widgets - October 27, 2013"
date: 2013-10-28 13:48:30
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Oct. 27, 2013</span>

These release notes pertain to the Hercules SaaS update released Oct. 27, 2013. 

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
          IX-9.3.1
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
          IX-9.3.1
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.4</a>
        </p>
        
        <p>
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.0.0</a> 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 1.17em;"><span style="font-size: 14pt;"><span style="font-size: 14pt;">Resolved Issues</span></span></span>
</p>

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
        <p class="TableBodyText">
          SUP-49
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          The CC button in the HTML5 player can now be set through uiVars, to be displayed only when captions are actually available.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-801
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          An SRT caption file with invalid characters is now processed to strip invalid characters when the SRT file is uploaded to enable proper caption search results in KMS.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-886
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          WebM videos can now be processed while being uploaded via Aspera drop folder.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-965
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          An occasional issue with the VAST ad countdown message (“your video will start in..”) appearing on the KDP even when the ad is not being displayed was resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-610
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          It is now possible to clear tooltips from player buttons (except for full screen and play buttons).
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-877
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          The specific issue with the uiconf clone/update API not working as expected was fixed.
        </p>
      </td>
    </tr>
  </tbody>
</table>

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
          HTML5
        </p>
      </td>
      
      <td valign="bottom" width="98">
        <p>
           
        </p>
        
        <p class="Copyright">
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.4</a>
        </p>
        
        <p>
           
        </p>
        
        <p class="Copyright">
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.0.0</a> 
        </p>
      </td>
      
      <td valign="bottom" width="128">
        <p>
          iPad2 iOS 6.0.1 & 7.0.2, Galaxy S3 & Galaxy Tab 4.0.4
        </p>
        
        <div>
           
        </div>
      </td>
    </tr>
  </tbody>
</table>