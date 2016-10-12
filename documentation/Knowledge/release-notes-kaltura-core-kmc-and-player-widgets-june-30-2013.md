---
layout: page
title: "Release Notes -  Kaltura Core, KMC, and Player Widgets - June 30, 2013"
date: 2013-06-30 01:08:31
---

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">June 30, 2013</span>

These release notes pertain to the Hercules SaaS update released June 30, 2013. 

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
          2013_06_04
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
          7.2.0
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
          5.36.3
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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.8.7:" target="_blank">v3.8.7</a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes" target="_blank">1.8.7</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  <span style="font-size: 1.17em;">What's New in this Release</span>
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="150">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="bottom" width="281">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Feature Availability</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p>
          Support for Webex Recording Files
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p class="TableBodyText">
          End-2-End workflow for ingestion, management and playback of of Webex’s proprietary ARF files while converting them to customer’s flavor set, and enabling multi-platform playback are now available.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          General Availability in all KMC accounts.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          Widevine DRM Enhancements
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <ul>
          <li>
            Support for multi-bitrate DRM packaging and adaptive bitrate playback has been added.
          </li>
          <li>
            The end-user experience for the initial download of the Widevine browser plugin has been simplified. The existing redirect to the Widevine download page was removed and the download is now triggered directly from Kaltura. Please refer to <a href="#os_browsers">OS/Browser Support Matrix</a>.
          </li>
          <li>
            Appropriate messages to end-users have been added when DRM content is loaded through a browser on devices that do not support Flash. (for example,. iOS)
          </li>
          <li>
            The Widevine assets distribution window is automatically updated according to entry scheduling. This feature requires account activation.
          </li>
          <li>
            Support for DRM Packaging when transcoding with a local transcoders (flavors are uploaded to Kaltura) is now available.
          </li>
        </ul>
        
        <p>
          For additional information please refer to <a href="http://knowledge.kaltura.com/node/838" target="_blank">Kaltura’s Digital Rights Management (DRM) Service with Widevine Setup and Workflow Guide</a>.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Available with account enablement for Widevine DRM.
        </p>
        
        <p class="TableBodyText">
          Paid Feature
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          DRM in Mobile Reference Applications
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p class="TableBodyText">
          Widevine DRM has been added to Kaltura iOS/Android reference applications and SDKs.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Access to iOS/Android SDKs and Reference applications is available from the <a href="http://www.kaltura.com/api_v3/testme/client-libs.php" target="_blank">Kaltura API Client libraries download page</a>.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          Monetization
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p>
          Ad server plugins for <a href="http://player.kaltura.com/docs/DoubleClick" target="_blank">DFP-Doubleclick</a>, <a href="http://player.kaltura.com/docs/FreeWheel" target="_blank">Freewheel</a> and <a href="http://player.kaltura.com/docs/Tremor" target="_blank">Tremor</a> may now be defined in KMC Studio.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          General Availability in all KMC accounts.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          Transcoding
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p class="TableBodyText">
          Dedicated transcoding resources for handling time-sensitive  content are now offered as a service.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Available with account enablement.
        </p>
        
        <p class="TableBodyText">
          Paid Feature
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          Internationalization  support (i18n)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p>
          Kaltura core infra was added to facilitate account localization options in applications (for example,  MediaSpace) Email notifications and default content.
        </p>
        
        <p>
          Out-of-the-box German and Spanish MediaSpace is available including, metadata input, search capabilities and default content.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p>
          General Availability
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          KMC - Upload file type filter
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p>
          The KMC Upload from Desktop option now allows a selection of files from the admin’s desktop without limiting to specific file type extensions. Default detection of entry type (video/audio/image) is kept as is.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          General Availability in all KMC accounts
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          KMC - Entries/Categories Search
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p class="TableBodyText">
          Search with special characters on <a href="http://knowledge.kaltura.com/node/247" target="_blank">entries</a> and <a href="http://knowledge.kaltura.com/node/881" target="_blank">categories</a> are now supported.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          General Availability in all KMC accounts
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          KMC - Entries/Categories Search
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p class="TableBodyText">
          When ordering Entries and categories by name in the Entries and Categories tables, the order is no longer limited to the first 4 characters.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          General Availability in all KMC accounts
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          KMC - Rule-Based Playlist Settings
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p class="TableBodyText">
          A new ordering method was added to the <a href="http://knowledge.kaltura.com/faq/how-create-add-single-rule-playlist">rule based playlist settings</a> enabling ordering by Entry Name without limiting the number of characters taken into account for ordering.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          General Availability in all KMC accounts
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          KMC  - Thumbnail Crop Utility Enhancements
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p class="TableBodyText">
          The Distribution connector name was added to thumbnail dimension menu (for distribution connectors that require thumbnails).
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Available in KMC accounts that are enabled with Kaltura Distribution Module
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          Chunked Upload
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p class="TableBodyText">
          An HTML5 based stand-alone File Upload widget with multiple file selection, drag&drop support, progress bars, validation and preview images, audio and video for jQuery.<br />Supports cross-domain, chunked and resumable file uploads and client-side image resizing. For more information please visit the <a href="http://kaltura.github.io/jQuery-File-Upload/" target="_blank">File Upload Demo page</a>.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Limited Availability
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="150">
        <p class="TableBodyText">
          Transcoding
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="281">
        <p>
          Support for ffmpeg version 1.1.1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          General Availability
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Known Limitations</span>

<div>
  <table border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td width="91">
          <p class="TableHeading">
            <strong>Component</strong>
          </p>
        </td>
        
        <td width="533">
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
        
        <td style="text-align: left;" valign="bottom" width="533">
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
        
        <td style="text-align: left;" valign="bottom" width="533">
          <p class="TableBodyText">
            If your content is encrypted, you must have at least one non-encrypted source/flavor for the following features to work.
          </p>
          
          <ul>
            <li>
              <span>KMC thumbnail creation options (grab from video, crop)</span>
            </li>
            <li>
              <span>KMC clipping/Trimming/Advertising cue point editor</span>
            </li>
            <li>
              <span>Thumbnail APIs</span>
            </li>
          </ul>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="bottom" width="91">
          <p class="TableBodyText">
            DRM
          </p>
        </td>
        
        <td style="text-align: left;" valign="bottom" width="533">
          <p class="TableBodyText">
            DRM is supported only for Video Entries.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="bottom" width="91">
          <p class="TableBodyText">
            DRM
          </p>
        </td>
        
        <td style="text-align: left;" valign="bottom" width="533">
          <p class="TableBodyText">
            After manual processing of an H264 flavor that is part of a DRM package, manual DRM packaging should be initiated from the Flavor tab to update the existing DRM package.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="bottom" width="91">
          <p class="TableBodyText">
            Chunk Upload
          </p>
        </td>
        
        <td style="text-align: left;" valign="bottom" width="533">
          <p class="TableBodyText">
            Please refer to <a href="#chunck"><span>H</span><span>TML5 Chunk Upload Supported Devices/OS/Browsers</span></a>.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="bottom" width="91">
          <p class="TableBodyText">
            Mobile Reference Applications
          </p>
        </td>
        
        <td style="text-align: left;" valign="bottom" width="533">
          <p class="TableBodyText">
            Access control rules are ignored when logging into the application with KMC user credentials.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p class="mce-heading-3">
    <span style="font-size: 14pt;">Known Issues</span>
  </p>
</div>

<p class="mce-heading-4">
  <span class="mce-note-graphic"></span><span style="color: #666560; font-size: 12pt; font-weight: bold;">KDP</span>
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <strong>ID</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p class="TableBodyText">
          FEC-169
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p class="TableBodyText">
          The media ready event is not always triggered on Safari & Chrome
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p class="TableBodyText">
          FEC-195
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p class="TableBodyText">
          The Error Message is not displaying correctly when Progressive Download option is Disabled for the account.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p class="TableBodyText">
          FEC-168
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p class="TableBodyText">
          When content is encrypted for DRM, the video frame may get stuck (in rare cases) when manually changing the bitrate from high to low.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p class="TableBodyText">
          FEC-171
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p class="TableBodyText">
          Entry duration counters on the player control area are sometimes trimmed when the entry duration is longer  than an hour.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p class="TableBodyText">
          FEC-176
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p class="TableBodyText">
          Scrollbars are displayed in some screen resolutions when captions are enabled.
        </p>
      </td>
    </tr>
  </tbody>
</table>

 <span style="color: #666560; font-size: 12pt; font-weight: bold;">HTML5 Player</span>

<table style="width: 600px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-294
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          The player size does not change after resizing the window in IE.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-289
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          When switching captions from the captions menu on Android, the player may get stuck in a paused state.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-288
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          The Captions menu does not work properly in some cases on desktop browsers.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-194
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          In a rule based playlist the total number of entries in HTML5 is displayed incorrectly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-255
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          It is  sometimes not possible to switch the player in iPad devices to a full screen mode after the player was minimized.  
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-232
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          Toggling a player to minimized state may cause the player to stretch in native browser on Android s2 and s3.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-257
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          An error message may be displayed in a wrong position in an HTML5 player on IE10.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-188
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          Scrolling between entries in a playlist player on Android 4.1.2 does not work properly in some cases.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-187
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          VAST 2.0 - If an entry has two pre-roll ads, the skip option is shown only at first preroll. The second preroll skip option is unavailable.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          <a href="https://kaltura.atlassian.net/browse/FEC-186">FEC-186</a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          VAST 2.0 – When a playlist is set to have two pre-roll ads, the second preroll may not play properly on some devices.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          FEC-158
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          In some cases, the player scrubber does not show properly on iPad, when using an iFrame embed code.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="83">
        <p>
          8131
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="517">
        <p>
          The DVR option for live streaming is not shown in the iFrame embed code before pressing Play.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  KMC/Core
</p>

<table style="width: 612px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" width="114">
        <p>
          <strong>QC/JIRA #</strong>
        </p>
      </td>
      
      <td style="text-align: left;" width="498">
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="114">
        <p class="TableBodyText">
          8069
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="498">
        <p class="TableBodyText">
          Large files (6GB) cannot be uploaded to KMC from a Drop folder.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="114">
        <p class="TableBodyText">
          8161
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="498">
        <p class="TableBodyText">
          When using the KMC bulk download action and selecting entries where the flavor required for the download is not available, the conversion of the requested flavor impedes the bulk download process. An email specifying the URLs for downloads is not sent to the user.<a href="file:///C:/Users/Debbie/Documents/Gemini/Release_Notes/Gemini_04-28-2013_production_update_internal_release_notesdz4kcedited4cf.docx#_msocom_1"><br /> </a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="114">
        <p class="TableBodyText">
          8383
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="498">
        <p class="TableBodyText">
          When using a local transcoder and adding one of the intermediate H264 flavors by importing it manually from the Entry’s Flavors tab, the ingestion process may not complete properly.  
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="114">
        <p class="TableBodyText">
          8291
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="498">
        <p class="TableBodyText">
          Intermediate flavors are not deleted as they should be after DRM packaging, when flavors are added manually from the entry flavors tab
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="114">
        <p class="TableBodyText">
          8567
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="498">
        <p class="TableBodyText">
          When converting a rotated entry using the Letterbox flavor parameter, the video’s dimensions are scaled down.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="114">
        <p class="TableBodyText">
          FEC-222
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="498">
        <p class="TableBodyText">
          A technical message is prompted when trying to upload a non-media file from the KMC <em>upload from desktop</em> option.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="114">
        <p class="TableBodyText">
          FEC-219
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="498">
        <p class="TableBodyText">
          A timer animation stays on the KMC screen after uploading a non-media file from the KMC’s upload from desktop option.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<div>
  <p class="mce-heading-4">
     Mobile Reference Applications
  </p>
  
  <table style="width: 606px;" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td width="83">
          <p>
            <strong>JIRA  #</strong>
          </p>
        </td>
        
        <td width="523">
          <p>
            <strong>Summary</strong>
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-226
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            IOS- iPad2 – The Application crashes in some cases when upload is suspended and resumed.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-244
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS-iPad - The playhead does not reach till the end of the scrubber.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-241
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS iPad- The player's progress time line disappears during playback in some cases.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-287
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS iPad- Category entries are not listed properly.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-286
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android- Occasional app crashing.  
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-273
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android- Audio entries are not supported.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-278
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android - Media is played only in 'Landscape' mode.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-293
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android Tablet- Occasionally the player becomes non-responsive after playing.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-283
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android- A self-recorded video may be twisted.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-284
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android- The Entry’s duration does not show correctly in some cases.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-261
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS iPad- There is a redundant categories side menu in the 'Most Popular' page.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-258
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- Long category names may display poorly or be cut off.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-271
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android- The Settings page does not switch to horizontal mode.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-282
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android Tablet- The Category list remains on the screen after selecting a category.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-266
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- Android- Categories are sorted by creation time instead of alphabetically.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-218
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS - Android- The player's volume control is horizontal.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-248
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS iPhone- Filtering by category is not working properly.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-292
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            Android - Share with Facebook is not working properly.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-252
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- Share media with Twitter / Facebook / Gmail is not working properly.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-243
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- Android- Image entries are not displayed.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-246
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- Android- The Entry name is not displayed in the player page.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-216
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- There is an incorrect notification message in case there is no internet access.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-253
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- A 'No Results' indication in an empty search is missing.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-247
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- Android- There is no indication for the number of entries.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-209
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- When an invalid user name/password has been entered, the home page button is disabled.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="83">
          <p class="TableBodyText">
            FEC-214
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="523">
          <p class="TableBodyText">
            iOS- Android- An indication is missing when attempting to log in with empty username/ password fields.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
</div>

<p class="mce-heading-3">
  <span><a name="chunck"></a>H</span><span>TML5 Chunk Upload Supported Devices/OS/Browsers</span>
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="117">
        <p class="TableHeading">
          <strong>Device\Browser</strong>
        </p>
      </td>
      
      <td width="63">
        <p class="TableHeading">
          <strong>Native</strong>
        </p>
      </td>
      
      <td width="68">
        <p class="TableHeading">
          <strong>Chrome (latest)</strong>
        </p>
      </td>
      
      <td width="65">
        <p class="TableHeading">
          <strong>FireFox (latest)</strong>
        </p>
      </td>
      
      <td width="63">
        <p class="TableHeading">
          <strong>IE 10</strong>
        </p>
      </td>
      
      <td width="62">
        <p class="TableHeading">
          <strong>IE 9</strong>
        </p>
      </td>
      
      <td width="62">
        <p class="TableHeading">
          <strong>IE 8</strong>
        </p>
      </td>
      
      <td width="147">
        <p class="TableHeading">
          <strong>Comments</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td width="117">
        <p class="TableBodyText">
          <strong>Android-S3</strong>
        </p>
      </td>
      
      <td valign="top" width="63">
        <p class="TableBodyText">
          <span>Not available</span>
        </p>
      </td>
      
      <td valign="top" width="68">
        <p class="TableBodyText">
          <span>Not available</span>
        </p>
      </td>
      
      <td width="65">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="147">
        <ol>
          <li>
            Native: Media is not uploaded with  the chunk.
          </li>
          <li>
            Native: Image entry is not presented with the chunk.
          </li>
          <li>
            Native and Chrome: Resume is not performed with the chunk.
          </li>
          <li>
            Native and Chrome: Voice recorder is not created with the chunk.
          </li>
          <li>
            Native and Chrome: Cannot upload media from Dropbox.
          </li>
        </ol>
      </td>
    </tr>
    
    <tr>
      <td width="117">
        <p class="TableBodyText">
          <strong>Android-S2</strong>
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          Not tested
        </p>
      </td>
      
      <td width="68">
        <p class="TableBodyText">
          Not tested
        </p>
      </td>
      
      <td width="65">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="147">
        <p class="TableBodyText">
          Not tested
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="117">
        <p class="TableBodyText">
          <strong>Android-S1</strong>
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          Not tested
        </p>
      </td>
      
      <td width="68">
        <p class="TableBodyText">
          Not tested
        </p>
      </td>
      
      <td width="65">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="147">
        <p class="TableBodyText">
          Not tested
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="117">
        <p class="TableBodyText">
          <strong>iphone4 version 6</strong>
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          <span>Works OK</span>
        </p>
      </td>
      
      <td valign="top" width="68">
        <p class="TableBodyText">
          <span>Not available</span>
        </p>
      </td>
      
      <td width="65">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="147">
        <ol>
          <li>
            Chrome v23.0.1271.100 and 27.0.1453.10: Cannot upload a media-Entry. An error status is returned.
          </li>
          <li>
            Chrome v23.0.1271.100 and 27.0.1453.10: Resume is not performed.
          </li>
        </ol>
      </td>
    </tr>
    
    <tr>
      <td width="117">
        <p class="TableBodyText">
          <strong>ipad version 6</strong>
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          <span>Works OK</span>
        </p>
      </td>
      
      <td valign="top" width="68">
        <p class="TableBodyText">
          <span>Not available</span>
        </p>
      </td>
      
      <td width="65">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="147">
        <ol>
          <li>
            Chrome: Cannot upload a media-Entry. An error status is returned.
          </li>
          <li>
            Chrome: Chunk and Resume are not performed.
          </li>
        </ol>
      </td>
    </tr>
    
    <tr>
      <td width="117">
        <p class="TableBodyText">
          <strong>Mac</strong>
        </p>
      </td>
      
      <td width="63">
        <p>
          <span>Partially working</span>
        </p>
      </td>
      
      <td width="68">
        <p>
          <span>Works OK</span>
        </p>
      </td>
      
      <td width="65">
        <p class="TableBodyText">
          Not tested
        </p>
      </td>
      
      <td width="63">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          NA
        </p>
      </td>
      
      <td width="147">
        <ol>
          <li>
            Safari version 5: Chunk and Resume are not performed.
          </li>
          <li>
            Safari version 5 and 6: The player preview does not present the video (mp4) . The video gets stuck while loading.
          </li>
        </ol>
      </td>
    </tr>
    
    <tr>
      <td width="117">
        <p class="TableBodyText">
          <strong>Windows 7</strong>
        </p>
      </td>
      
      <td width="63">
        <p>
          NA
        </p>
      </td>
      
      <td width="68">
        <p>
          <span>Works OK</span>
        </p>
      </td>
      
      <td width="65">
        <p>
          <span>Works OK</span>
        </p>
      </td>
      
      <td width="63">
        <p>
          <span>Partially working</span>
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          <span>Not available</span>
        </p>
      </td>
      
      <td width="62">
        <p class="TableBodyText">
          <span>Not available</span>
        </p>
      </td>
      
      <td width="147">
        <p class="TableBodyText">
          Cannot upload the file on IE below  IE version 10.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><a name="os_browsers"></a>OS/Browsers Verified for Widevine DRM</span>

 The following OS/Browsers were verified to support Widevine DRM including verification of Widevine’s browser plugin download and install.

√ - tested and OK

X – Was not tested

N/A – OS/browser combination is not applicable.  

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="bottom" width="126">
        <p>
          <strong> </strong>
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          <strong>MAC 10.7.5</strong>
        </p>
      </td>
      
      <td valign="bottom" width="89">
        <p>
          <strong>Windows 8</strong>
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          <strong>Windows 7</strong>
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          <strong>Windows Vista</strong>
        </p>
      </td>
      
      <td valign="bottom" width="95">
        <p>
          <strong>Windows XP</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="126">
        <p>
          <strong>Safari 5.1.7</strong>
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="89">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="95">
        <p>
          X
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="126">
        <p>
          <strong>Firefox (latest)</strong>
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="95">
        <p>
          √
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="126">
        <p>
          <strong>Chrome (latest)</strong>
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="95">
        <p>
          √
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="126">
        <p>
          <strong>IE 10</strong>
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          NA
        </p>
      </td>
      
      <td valign="bottom" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="95">
        <p>
          NA
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="126">
        <p>
          <strong>IE 9</strong>
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          NA
        </p>
      </td>
      
      <td valign="bottom" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="95">
        <p>
          NA
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="126">
        <p>
          <strong>IE 8</strong>
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          NA
        </p>
      </td>
      
      <td valign="bottom" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="95">
        <p>
          √
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="126">
        <p>
          <strong>IE 7</strong>
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          NA
        </p>
      </td>
      
      <td valign="bottom" width="89">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          √
        </p>
      </td>
      
      <td valign="bottom" width="107">
        <p>
          X
        </p>
      </td>
      
      <td valign="bottom" width="95">
        <p>
          √
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">KMC Tested Browsers</span>

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
          <a href="http://knowledge.kaltura.com/kdp-release-notes#Version3.8.7:" target="_blank">3.8.7</a><a href="http://knowledge.kaltura.com/kdp-release-notes" target="_blank"><br /></a>
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
          <a href="http://html5video.org/wiki/Kaltura_HTML5_Release_Notes">1.8.7</a>
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