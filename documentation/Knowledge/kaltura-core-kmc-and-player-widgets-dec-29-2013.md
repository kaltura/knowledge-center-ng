---
layout: page
title: "Kaltura Core, KMC, and Player Widgets - Dec 29, 2013"
date: 2014-01-05 20:22:34
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Dec 29, 2013</span>

These release notes pertain to the Hercules SaaS update released Dec. 29, 2013. 

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
          IX-9.7.0
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
          IX-9.7.0
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
          5.37.3
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.4" target="_blank">v3.9.4</a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.6</a>
        </p>
        
        <p>
          <a href="https://github.com/kaltura/mwEmbed/releases" target="_blank">2.1 </a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"><span>What's New in this Release</span></span></span>

<table style="width: 761px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="115">
        <p>
          API
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="286">
        <p>
          New API service: <em>fileAsset</em> – enabling API based file asset association with any object type.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="360">
        <p class="TableBodyText">
          General Availability
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="115">
        <p>
          API
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="286">
        <p>
          Relative time filter options for date fields were added for listing of objects, where the date field is within a specific timeframe from the API call time.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="360">
        <p class="TableBodyText">
          General Availability
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"><span>Resolved Issues</span></span></span>

 

<table style="width: 519px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          <strong>JIRA #</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1137
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The specific issue with analytics info dropping to 0 on specific dates was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1144
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The specific issue with Widevine packaging failure on screen recording captures without audio was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-959
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The issue with bulk upload log rows in the KMC not being deleted was fixed. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1263
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The issue with downloading flavors from the KMC not using the optimal API call was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1105
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The specific issue with changing the KMC account owner in the Account Settings that was not working properly in some cases, was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1192
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The specific issue with the HTML5 player on Android devices when loading a video did not complete, was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1114
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The specific issue with pre-roll ads not playing on Chrome Androids was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          PLAT-463
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          The Date custom data field value has been fixed and is presented properly in the email notifications.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          PLAT-462
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          The issue with adding categories from the API test console that failed when executed in multi-request was fixed.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">KMC Tested Browsers</span>

The following browsers were tested for this release (recommended resolution 1024x768):

*   Firefox (latest)
*   Chrome (Windows & Mac - latest)
*   IE 9 and IE10 on Windows 7

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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.4" target="_blank">3.9.4</a><a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank"><br /></a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="128">
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.6</a><a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.3" target="_blank"></a>
        </p>
        
        <p>
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.1</a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="128">
        <span>iPad2 iOS 6.0.1 & 7.0.2, Galaxy S3 & Galaxy Tab 4.0.4</span> 
      </td>
    </tr>
  </tbody>
</table>