---
layout: page
title: "Kaltura Core, KMC, and Player Widgets - Dec 16, 2013"
date: 2013-12-16 14:21:40
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Dec 16, 2013</span>

These release notes pertain to the Hercules SaaS update released Dec. 16, 2013. 

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
          IX-9.6.0
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
          IX-9.6.0
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
          5.37
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.6.</a>
        </p>
        
        <p>
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.0.3</a> 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"><span> </span></span></span>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"><span>Resolved Issues</span></span></span>

 

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="98">
        <p>
          <strong>JIRA #</strong>
        </p>
      </td>
      
      <td valign="bottom" width="421">
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1080
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The issue that caused files uploaded via an FTP drop folder to hang in “uploading” status was resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1142
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The issue with entries being marked as Ready even when the source files were invalid was resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1131
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The issue source files hanging in the “exporting” status (while files were actually exported to a remote storage) was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1102
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          Multi request API calls now work properly from the API test console.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1166
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The problem when the Kaltura Java client library was being used by an application running on IE8 was resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1210
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          An issue with Comcast MRSS connector configuration was resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          SUP-1087
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The Play analytics on the iPad are now sent properly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          PLAT-463
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The metadata value of type Date is now presented with the correct format within email notification.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          PLAT-135
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          A specific issue with deleted entries still showing up in the KMC was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          PLAT-571
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          The link to the drop folders guide in the KMC help page was fixed.
        </p>
        
        <div>
           
        </div>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"><span> </span></span></span>

 

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;">Known Issues</span></span>

 

<table style="width: 761px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="98">
        <p class="TableHeading">
          <strong>JIRA #</strong>
        </p>
      </td>
      
      <td valign="top" width="243">
        <p class="TableHeading">
          <strong>Module</strong>
        </p>
      </td>
      
      <td valign="top" width="421">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p class="TableBodyText">
          PLAT-434
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="243">
        <p class="TableBodyText">
          WebEx
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p class="TableBodyText">
          When 2 WebEx conversions are processed in parallel, a video may be produced without sound.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          PLAT-614
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="243">
        <p>
          DRM
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          When an ingestion of pre-encrypted assets is done directly to remote storage, playback does not work properly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          PLAT-602
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="243">
        <p>
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          After deleting a KMC user role, it’s not possible to create a role with the same name.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="98">
        <p>
          PLAT-590
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="243">
        <p>
          Thumbnails
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          The filename extension of downloaded thumbnails is always .jpg, even when the actual file is not a jpg.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="98">
        <p>
          PLAT-618
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="243">
        <p>
          KDP
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          The free preview option defined in an access control profile is not available in some cases when using RTMP delivery and KDP.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="98">
        <p>
          PLAT-567
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="243">
        <p>
          API
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          Animated GIF cropping may not working properly.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"> </span></span>

 

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">KMC Tested Browsers</span>

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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.0.3</a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="128">
        <span>iPad2 iOS 6.0.1 & 7.0.2, Galaxy S3 & Galaxy Tab 4.0.4</span> 
      </td>
    </tr>
  </tbody>
</table>