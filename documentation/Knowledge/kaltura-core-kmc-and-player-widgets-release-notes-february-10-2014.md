---
layout: page
title: "Kaltura Core, KMC, and Player Widgets - Release Notes - February 10, 2014"
date: 2014-02-11 16:08:34
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Feb.10, 2014</span>

These release notes pertain to the Hercules SaaS update released Feb 10, 2014. 

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
          IX-9.10.0
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
          IX-9.10.0
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
          5.37.9
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.7" target="_blank">v3.9.7</a>
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
          <a href="https://github.com/kaltura/mwEmbed/releases">2.2.1 </a><a href="https://github.com/kaltura/mwEmbed/releases" target="_blank">(v2)<br /></a>
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
          Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="286">
        <p>
          Plays from feeds (Kaltura playback on non-Kaltura players) are counted in the data-base.
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
          SUP-1335
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          Email notifications are no longer automatically sent to the account owner as CC.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          SUP-1384
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          Resolved an issue of an occasional internal server error that occurred when trying to replace an entry.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          SUP-1416
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          The CC from the Email notifications templates was removed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          SUP-1355
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          The player now can load any entry and there is no black screen displayed while loading.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" width="126">
        <p class="TableBodyText">
          SUP-1303
        </p>
      </td>
      
      <td style="text-align: left;" width="668">
        <p class="TableBodyText">
          The player can now show the hovering control bar on mobile devices as on the iPad.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><br />KMC Tested Browsers</span>

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
          <a href="https://github.com/kaltura/mwEmbed/releases">2.2.1 </a><a href="https://github.com/kaltura/mwEmbed/releases" target="_blank">(v2)</a><a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank"><br /></a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="128">
        <span>iPad2 iOS 6.0.1 & 7.0.2, Galaxy S3 & Galaxy Tab 4.0.4</span> 
      </td>
    </tr>
  </tbody>
</table>