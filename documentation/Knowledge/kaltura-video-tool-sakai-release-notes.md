---
layout: page
title: "Kaltura Video Tool for Sakai CLE Release Notes"
date: 2012-07-03 14:27:55
---

#### <a name="Version_3.0"></a>Version 3.0

These release notes pertain to the Kaltura Video Tool for Sakai CLE released March, 2013.

These release notes are intended for administrators of institutions installing the Kaltura Video Tool for Sakai CLE version 3.0 and for Kaltura internal use.

What's New in this Release?

<table style="width: 633px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="198">
        <p>
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="bottom" width="435">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Clipping
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="435">
        <p class="TableBodyText">
          Ability to create video clips to highlight relevant parts of a video, divide long videos to shorter ones for easy viewing, use in tests and more.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Improved Media Management
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="435">
        <p class="TableBodyText">
          An administrator can now view which entries belong to which courses and assign entries to specific courses using the Kaltura Management Console (KMC) or perform a bulk upload to specific courses.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          User Experience Enhancements 
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="435">
        <p class="TableBodyText">
          Additional enhancements requested by the Kaltura Sakai community:
        </p>
        
        <ul>
          <li>
            Unifying collection selection workflow – You can now select media from “My Media” as well as from the Site Library.
          </li>
          <li>
            Improved the  “My Media” workflow - Added media directly to “My Media”
          </li>
          <li>
            Increased default number of items shown in collections and site library.
          </li>
          <li>
            Permissions moved from a tab to a link
          </li>
          <li>
            Default item visibility is based on the user’s role.
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Limitations

<table style="width: 633px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="198">
        <p>
          <strong>Limitation</strong>
        </p>
      </td>
      
      <td valign="bottom" width="435">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Kaltura On-Prem compatibility
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          The minimum Kaltura On-Prem for this version is Gemini.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Webcam recording
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          <span>If you are using On-prem version Gemini and up, and want to use the webcam recording feature, you need to change the default KCW of SKE (or SKE My-media KCW) to point to version 2.2.1 to work correctly with the bundled webcam recording server in the Kaltura On-Prem package.</span>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### Kn.own Issues

<table style="width: 632px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="136">
        <p>
          <strong>ID</strong>
        </p>
      </td>
      
      <td valign="bottom" width="224">
        <p>
          <strong>Module</strong>
        </p>
      </td>
      
      <td valign="bottom" width="272">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="136">
        <p class="TableBodyText">
          7658
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="224">
        <p class="TableBodyText">
          Migration
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="272">
        <p class="TableBodyText">
          Users who browsed to the site before migrating might need to clear the cache on their browser for everything to be rendered correctly. (after migrating from version 2.0 to version 3.0)
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="136">
        <p class="TableBodyText">
          7659
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="224">
        <p class="TableBodyText">
          KDP-playback context
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="272">
        <p class="TableBodyText">
          Statics are not collected on the Site level for items that are in other Sakai tools (Playback context is  not being sent while playing an item created by html\text tool)
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### Resolved Issues

<table style="width: 633px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="198">
        <p>
          <strong>Issue</strong>
        </p>
      </td>
      
      <td valign="bottom" width="435">
        <p>
          <strong>Fix</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          All galleries: Site Library, Collection, My Media
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          It may take a few of seconds for the gallery to render when first loading it.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Image entry support on iPad
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          Image entries are not displayed in the HTML5 player in iPads.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          All galleries: Site Library, Collection, My Media
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          When loading an audio entry directly following an image, the audio entry cannot be played.
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### Tested Browsers

The following browsers were tested for this release (recommended resolution 1024x768):

*   Safari 5.1.3 on Mac
*   Chrome 19
*   FF 13
*   IE9 on Windows 7

#### Tested Devices

<table style="width: 616px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Platform</strong>
        </p>
      </td>
      
      <td valign="top" width="162">
        <p class="TableHeading">
          <strong>Version</strong>
        </p>
      </td>
      
      <td valign="top" width="256">
        <p class="TableHeading">
          <strong>Reference Device</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="bottom" width="198">
        <p>
          iOS
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="162">
        <p>
          <a href="http://en.wikipedia.org/wiki/IOS">v5.x</a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="256">
        <p>
          iPad2
        </p>
      </td>
    </tr>
  </tbody>
</table>

 

#### <a name="Version2.0"></a>Version 2.0 

These release notes pertain to the Kaltura Video Tool for Sakai CLE released July, 2012.

These release notes are intended for administrators of institutions installing the Kaltura Video Tool version 2.0 for Sakai CLE and for Kaltura internal use.

#### What's New in this Release?

<table style="width: 633px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Mobile and tablets
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          View videos on any device – support for video playback on mobile and tablets.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          My Media
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          A personal searchable repository for uploading, viewing, and managing media content has been added. Media items within My Media may be added to an unlimited number of collections, and reused <strong>across all Sakai sites</strong>, as well as across various Kaltura applications in the institution.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Additional admin controls
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          Granular control over permissions; you can determine whether the Site Library is invisible to students/non-administrators
        </p>
        
        <p class="TableBodyText">
          Support for easy course content duplication (semester-end scenario).
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Additional changes
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p class="TableBodyText">
          Localization/internationalization: Changing the texts of the tool to different languages.
        </p>
        
        <p class="TableBodyText">
          Removed the Remix Tool.
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### Known Issues

<table style="width: 636px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="81">
        <p>
          <strong>ID</strong>
        </p>
      </td>
      
      <td valign="top" width="183">
        <p>
          <strong>Module</strong>
        </p>
      </td>
      
      <td width="372">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="81">
        <p class="TableBodyText">
          2674
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="183">
        <p class="TableBodyText">
          All galleries: Site Library, Collection, My Media
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        <p class="TableBodyText">
          It may take a few of seconds for the gallery to render when first loading it.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="81">
        <p class="TableBodyText">
          3529
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="183">
        <p class="TableBodyText">
          Image entry support on iPad
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        <p>
          Image entries are not displayed in the HTML5 player in iPads.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="81">
        <p class="TableBodyText">
          3568
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="183">
        <p class="TableBodyText">
          All galleries: Site Library, Collection, My Media
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        <p>
          When loading an audio entry directly following an image, the audio entry cannot be played.
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### <span style="font-size: 1em;">Resolved Issues</span>

<table style="width: 570px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="198">
        <p>
          <strong>Issue</strong>
        </p>
      </td>
      
      <td width="372">
        <p>
          <strong>Fix</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          The embed code does not change\refresh when selecting a different media (regression).
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        <p class="TableBodyText">
          Changing the chosen entry now refreshes the player area, metadata and the embed code.
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### Tested Browsers

The following browsers were tested for this release (recommended resolution 1024x768):

*   Safari 5.1.3 on Mac
*   Chrome 19
*   FF 13
*   IE9 on Windows 7

#### Tested Devices

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="145">
        <p>
          <strong>Platform</strong>
        </p>
      </td>
      
      <td valign="top" width="220">
        <p>
          <strong>Version</strong>
        </p>
      </td>
      
      <td width="245">
        <p>
          <strong>Reference Device</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="145">
        <p class="TableBodyText">
          iOS
        </p>
      </td>
      
      <td style="text-align: left;" width="220">
        <p>
          <a href="http://en.wikipedia.org/wiki/IOS">v5.x</a>
        </p>
      </td>
      
      <td style="text-align: left;" width="245">
        <p>
          iPad2
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="145">
        <p class="TableBodyText">
          <a href="http://en.wikipedia.org/wiki/BlackBerry_OS">Android</a>
        </p>
      </td>
      
      <td style="text-align: left;" width="220">
        <p>
          <a href="http://en.wikipedia.org/wiki/Windows_Phone">v3.1</a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="245">
        <p>
          Xoom-Tablet
        </p>
      </td>
    </tr>
  </tbody>
</table>