---
layout: page
title: "Release Notes -  Kaltura Core, KMC, and Player Widgets - September 15, 2013"
date: 2013-09-09 17:10:21
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Sept 15, 2013</span>

These release notes pertain to the Hercules SaaS update released Sept. 15, 2013. 

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
          IX-9.2.0
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
          IX-9.2.0
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
          5.36.8
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.2" target="_blank">v3.9.2</a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.2</a>
        </p>
        
        <p>
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.0.0</a> 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 1.17em;"><span style="font-size: 14pt;">What's New this Release</span></span> 
</p>

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="94">
        <p class="TableBodyText">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="357">
        <p>
          <strong>Description</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="158">
        <p class="TableBodyText">
          <strong>Feature Availability</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="94">
        <p>
          <a href="http://player.kaltura.com/docs/" target="_blank">508 compliant Player</a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="357">
        <p>
          All Kaltura players that use the HTML5 <a href="{{site.url}}/documentation/Knowledge/kaltura-player-toolkit.html" target="_blank">Kaltura Player Toolkit</a> are now 508 compliant by default and are based on <a href="http://www.w3.org/TR/wai-aria/" target="_blank">W3C Accessible Rich Internet Applications (WAI-ARIA)</a>. Specifications of the accessibility features are described in the article: <a href="{{site.url}}/documentation/Knowledge/508-support-within-kaltura-player-toolkit.html" target="_blank">508 Support within the Kaltura Player Toolkit</a>
        </p>
        
        <p>
           <a href="{{site.url}}/documentation/Knowledge/508-support-within-kaltura-player-toolkit.html" target="_blank"><br /></a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="158">
        <p>
          Limited avialability.
        </p>
        
        <p>
          Integration testing should be done prior to upgrading production players.
        </p>
        
        <p>
          For more information,  please contact your Kaltura account manager
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="94">
        <p>
          <a href="{{site.url}}/documentation/Knowledge/kaltura-player-toolkit.html" target="_blank">W</a>ebEx
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="357">
        <ul>
          <li>
            Added support for including user defined WebEx Panels.
          </li>
          <li>
            Automated import to Kaltura – Ability to automatically import videos from a WebEx account to a Kaltura account via a WebEx drop folder configuration.<ul>
              <li>
                Keeping end-user ownership
              </li>
              <li>
                Option to auto-assign imported WebEx recoding  to user defined category
              </li>
            </ul>
          </li>
        </ul>
      </td>
      
      <td style="text-align: left;" valign="top" width="158">
        <p>
          General  Availability.
        </p>
        
        <p>
          Paid feature.
        </p>For more information,  please contact your Kaltura account manager.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="94">
        <p>
          Transcoding Usage Reports
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="357">
        <p>
          The Transcoding Usage report was added to “Bandwidth & Storage Reports” in th KMC, and Multi-Account Management Console.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="158">
        <p>
          General  Availability.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="94">
        <p>
          Custom Metadata
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="357">
        <p>
          You can  now enable more than 4 searchable custom data fields of type integer (created via API) or date.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="158">
        <p>
          General  Availability.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 1.17em;"><span style="font-size: 14pt;"><span>Resolved Issues</span></span></span>
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
        <p>
          SUP-632
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          A specific issue with distributing content to YouTube via the YouTube SFTP connector was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-623
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          The issue with a KMS channel member not being deleted from the channel, after the user account was deleted directly via Kaltura API was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-681
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          A specific issue with poor video quality for an HD clip was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-302
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          An issue with captions not playing in the HTML5 player, when the caption file is DFXP,  was fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          SUP-673
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="337">
        <p>
          A specific issue with uploading images to the KMC that was not working properly was fixed.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<table style="width: 415px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" width="78">
        <p>
          KMS-255 
        </p>
      </td>
      
      <td style="text-align: left;" width="337">
        <p>
          Entries are now properly ordered by the number of comments in MediaSpace.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          PLAT-237
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="337">
        <p>
          The issue with 30 categories only displayed in entry edit window (when the actual system maximum is 32) is now fixed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          PLAT-203
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="337">
        <p>
          The issue with navigation between Analytics reports being blocked in the KMC after 2-3 user clicks was resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="78">
        <p>
          PLAT-178
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="337">
        <p>
          The issue with KMC display adding 30 minutes to video durations when KMC is viewed by users in half-hour time zones was fixed.  
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="78">
        <p>
          FEC-421
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="337">
        <p>
          The issue with HTML5 player not loading a proper message when attempting to play DRM encrypted entry and when non-encrypted flavors are blocked by access control was fixed.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 14pt;">Known Limitations</span>
</p>

<table style="width: 595px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="83">
        <p class="TableHeading">
          <strong>JIRA #</strong>
        </p>
      </td>
      
      <td width="93">
        <p class="TableHeading">
          <strong>Component</strong>
        </p>
      </td>
      
      <td width="420">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" width="83">
        <p>
          PLAT-263
        </p>
      </td>
      
      <td style="text-align: left;" width="93">
        <p>
          KMC Transcoding Usage Reports
        </p>
      </td>
      
      <td style="text-align: left;" width="420">
        <p>
          The Transcoding Usage does not display as a KMC analytics graph option, and is included only within the KMC Bandwidth and Storage report table.
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
        <p>
          PLAT-272
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p>
          KCW
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          KCW flashvars defined within the “Additional Flashvars” are not  transferred to the KCW.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          PLAT-289
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="91">
        <p>
          KMC System Reports
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="421">
        <p>
          An internal server error is prompted within the KMC  when attempting to use the Application filters in the Browsers report.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p>
          PLAT-291
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p>
          KMC Help
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          The “Learn more about drop folders” link in the KMC is not working properly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="83">
        <p>
          PLAT-296
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="91">
        <p>
          WebEx Automated import
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="421">
        <p>
          A WebEx recording file is imported twice after its name was changed in the Webex account, and when it is the last file currently in the list of files within the WebEx account.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 14pt;">KMC Tested Browsers</span>
</p>

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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.9.2" target="_blank">3.9.2</a><a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank"><br /></a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.9.2</a>
        </p>
        
        <p>
           
        </p>
        
        <p class="Copyright">
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">2.0.0</a> 
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