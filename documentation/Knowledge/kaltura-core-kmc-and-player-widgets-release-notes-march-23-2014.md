---
layout: page
title: "Kaltura Core, KMC, and Player Widgets - Release Notes - March 23, 2014"
date: 2014-03-24 11:39:06
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">March 3, 2014</span>

These release notes pertain to the Hercules SaaS update released March 23, 2014. 

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
          IX-9.13.0
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
          IX-9.13.0
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
          5.37.14
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
          v<a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank">3.9.8</a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.6</a> (default)
        </p>
        
        <p>
          <a href="https://github.com/kaltura/mwEmbed/releases/tag/v2.5">2.5</a> v2
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><span style="font-size: 14pt;"><span style="font-size: 14pt;">Resolved Issues</span></span></span>

 

<table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="126">
        <p class="TableHeading">
          <strong>Issue ID</strong>
        </p>
      </td>
      
      <td valign="bottom" width="668">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          SUP-1625
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          Notification jobs are no longer created when notification email is not configured.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          SUP-1581
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          Remix feature is no longer exposed in previously existing KDP templates.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          SUP-1426
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          When you play a video using the HTML5 lib (v2.0.2) then leave the page, the error message is no longer displayed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          SUP-1580
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          The custom loading icon has been fixed and displayes correctly in IE 8, 9 and 10.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          FEC-1105
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          Opening then closing the "Support" modal page, no longer causes an error in the KMC.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          PLAT-1038
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          The problem with the column width configuration in the KMC that was caused by closing the the  "Preview & Embed" has been fixed in IE11 and Chrome.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">KMC Tested Browsers</span>

<p class="mce-heading-3">
   
</p>

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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.7" target="_blank">v</a><a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank">3.9.8</a><a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.7" target="_blank"></a><a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank"><br /></a>
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
          <a href="https://github.com/kaltura/mwEmbed/releases/tag/v2.5">2.5</a><a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank"> v2<br /></a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="128">
        <span>iPad2 iOS 6.0.1 & 7.0.2, Galaxy S3 & Galaxy Tab 4.0.4</span> 
      </td>
    </tr>
  </tbody>
</table>