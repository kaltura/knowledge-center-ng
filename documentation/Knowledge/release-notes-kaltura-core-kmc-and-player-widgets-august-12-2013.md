---
layout: page
title: "Release Notes -  Kaltura Core, KMC, and Player Widgets - August 12, 2013"
date: 2013-08-08 16:55:55
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">August 12, 2013</span>

These release notes pertain to the Hercules SaaS update released August 12, 2013. 

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
          Server Version
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          <span>9.0.0</span>
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
          <span>5.36.5</span>
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.8.9" target="_blank">v3.9.0</a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.0</a>
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
      <td valign="bottom" width="167">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="top" width="302">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="bottom" width="140">
        <p class="TableHeading">
          <strong>Feature Availability</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="167">
        <p class="TableBodyText">
          Core improvements
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="302">
        <ul>
          <li>
            Batch job improvements as support in filtering jobs by urgency and support in multiple batch versions.
          </li>
          <li>
            Workers ‘keep alive’ – to support restarting the schedulers and keep the workers running.
          </li>
          <li>
            Extending automatic intermediate-source processing.
          </li>
        </ul>
      </td>
      
      <td style="text-align: left;" width="140">
        <p class="TableBodyText">
          GA
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="167">
        <p class="TableBodyText">
          Python client library change
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="302">
        <p>
          The library was refactored to make it installable as a PyPI package.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="140">
        <p class="TableBodyText">
          GA
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Resolved Issues
</p>

<table style="width: 600px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="85">
        <p class="TableHeading">
          JIRA #
        </p>
      </td>
      
      <td valign="bottom" width="515">
        <p class="TableHeading">
          Summary
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          Uploaded videos no longer remain in Converting status.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-307
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          In a remote storage that is configured with "ready behavior" the first flavor is no longer exported to the wrong XSL path. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-390
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          When removing entries from a category, the page has been fixed to auto-refresh.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-328
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          The error message "Entry already assigned to this category" but does not specify which entry or entrie<a href="https://kaltura.atlassian.net/browse/SUP-328">s</a>, has been fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-497
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          When distributing an entry using cross Kaltura distribution and getting “Error: couldn't connect to host” the log now states which host it was.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-523
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          The "Last Updated" field in the Admin Console for:
        </p>
        
        <p class="TableBodyText">
          Remote Storage Profiles and Distribution Connectors has been added.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-571
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          The Share plugin is now enabled in the HTML5 player.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-535
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          The Adap.tv plugin integration no longer causes analytics issues.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-433
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          The latest HTML5 library works in UIWebView.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="85">
        <p class="TableBodyText">
          SUP-553
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="515">
        <p class="TableBodyText">
          The issue that sent a notification from AVN, that some assets appear missing after distributing entries to "Active Video Networks", has been fixed.
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
          <strong>ID#</strong>
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
          PLAT-38
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          Drop Folders
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          The original bulk xml file (from a dropfolder) does not download correctly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-356
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          HTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          forceMobileHTML5 does not work in iFrame embed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-353
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          The player is loaded in HTTP instead of HTTPS in the Preview and Embed page.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-347
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          There is no notice displayed in the KMC when a custom distribution asset is missing.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-346
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          HTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          The player and timer may flicker  in the HTML5 player when viewing livestream entries.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-342
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          When using iFrame embed in IE10, the player stays on the screen after closing the Preview and Embed page          
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-340
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          Help links in Preview and Enbed do not work in IE.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-339
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          HTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          An erroneous message is displayed in the HTML5 player when the entry has past scheduling.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-351
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          HTML5 new skin buttons are not displayed correctly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-358
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          HTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          The audio is muted in the Galaxy tab after replay/seek in FF
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          FEC-360
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          HTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          The Video is not played when moving it to another playlist in a multiple playlist.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          PLAT-122
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          Email Notifications
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          The "Recipient Name" field that was set for email notifications is ignored.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          PLAT-135
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          Entries
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          Deleted entries are shown in the KMC.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          PLAT-141
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          Permissions
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          An entry is playable even though the category it is assigned to is set to Private.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p class="TableBodyText">
          PLAT-144
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p class="TableBodyText">
          Event Notifications
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p class="TableBodyText">
          All entries get an Event Notification Error: Sending HTTP request failed..
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="font-size: 14pt; color: #828a8c; font-weight: bold;">KMC Tested Browsers</span>

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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.8.9" target="_blank">3.9.0</a><a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank"><br /></a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.0</a><a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes"><br /></a>
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