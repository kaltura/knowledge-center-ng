---
layout: page
title: "Release Notes -  Kaltura Core, KMC, and Player Widgets - July 22, 2013"
date: 2013-07-20 22:52:36
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">July 22, 2013</span>

These release notes pertain to the Hercules SaaS update released July 22, 2013. 

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
          Release Tag
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          <span>2013_07_16</span>
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
          <span>8.0.1</span>
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
          <span>5.36.3</span>
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.8.9" target="_blank">v3.8.9</a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.8.9</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 1.17em;">What's New in this Release</span>
</p>

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="180">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="top" width="270">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="bottom" width="159">
        <p class="TableHeading">
          <strong>Feature Availability</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" width="180">
        <p class="TableBodyText">
          KMC Preview and Embed
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="270">
        <ul>
          <li>
            <span style="text-align: center;">External stand-alone preview page is now clearly marked as not targeted for production usages.</span>
          </li>
          <li>
            <span style="text-align: center;">Embed codes now include Kaltura SEO links only in trial account.</span>
          </li>
          <li>
            <span style="text-align: center;">External stand-alone preview page  was moved from the <a href="http://corp.kaltura.com/" target="_blank">kmc.kaltura.com</a> domain to the </span><a href="http://corp.kaltura.com/" target="_blank" style="text-align: center;">www.kaltura.com</a><span style="text-align: center;"> domain for security reasons (preventing JS hacking).</span>
          </li>
          <li>
            <span style="text-align: center;">The embed code text area was set to view only mode, to prevent embed errors that resulted from user editing.</span>
          </li>
        </ul>
      </td>
      
      <td style="text-align: left;" valign="top" width="159">
        <p class="TableBodyText">
          General Availability in all KMC accounts
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Resolved Issues
</p>

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="bottom" width="78">
        <p class="TableHeading">
          <strong>JIRA #</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="337">
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
          SUP-307
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          An issue with the flavor’s setting having no impact on readiness behavior was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-428
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          A fix in the KDP Akamai HD Plugin was set to avoid unneeded calls to localhost/crossdomain.xml.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-423
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          A playback issue in HTC One Andorid phone (os version 4.1.2) was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-288
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          An issue causing duplication of the m3u8 flavor in the player flavor selector on iPad was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-360
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          An issue with non-accurate video duration presented in the KMC was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-450
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          An issue with having sporadic black screen in the KDP was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-125
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          An issue causing “categories are locked” API error when creating a channel in MediaSpace was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-412
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          The incorrect "Off Air"  indication during live streaming was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-438
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          The problem HTML5 pre-roll / mid-roll ads when using a LiveRail JavaScript tag implementation was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-305
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          A specific issue with live stream entry not playing in KDP while playing in HTML5, was fixed
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-395
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          A specific issue with access control geo-blocking when using mobile devices and legacy Flash embed code was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p class="TableBodyText">
          SUP-403
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p class="TableBodyText">
          A specific issue with Omniture analytics not being sent correctly from the KDP was fixed.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 14pt;">Known Issues</span>
</p>

<table style="width: 595px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="83">
        <p class="TableHeading">
          <strong>JIRA #</strong>
        </p>
      </td>
      
      <td width="91">
        <p class="TableHeading">
          <strong>Component</strong>
        </p>
      </td>
      
      <td width="421">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-336
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          KDP
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          eventType of 75% is not sent from KDP for pre/mid/post roll ads
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-335
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          KDP
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          eventType:16 (Replay) is not sent from KDP after a post roll ad.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 14pt;">KMC Tested Browsers</span>
</p>

The following browsers were tested for this release (recommended resolution 1024x768):

*   Firefox (latest0
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.8.9" target="_blank">3.8.9</a><a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank"><br /></a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.8.9</a><a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes"><br /></a>
        </p>
      </td>
      
      <td valign="bottom" width="128">
        <p>
          iPad2 iOS 5.1.1 and 6.0.1
        </p>
        
        <div>
           
        </div>
      </td>
    </tr>
  </tbody>
</table>