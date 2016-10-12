---
layout: page
title: "Kaltura MediaSpace 4.5 Release Notes"
date: 2012-09-12 16:03:03
---

<span class="mce-heading-4">Version 4.5, Build 4.5.17</span>

These release notes pertain to MediaSpace version 4.5, released December 2012.

These release notes are intended for administrators of institutions installing MediaSpace and for MediaSpace developers.

Build 4.5.17 addresses bug fixes for customers. For full release details, see [Version 4.5, Build 4.5.15][1].

 [1]: #Build_4_5_15

<span class="mce-heading-4">Resolved Issues </span>

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Issue</strong>
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableHeading">
          <strong>Fix</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="198">
        The pager does not display correctly when the cache is not clean.
      </td>
      
      <td valign="top" width="372">
        The pager always displays correctly.
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        When embedding a video in MediaSpace, size selection does not work with IE7 and IE8.
      </td>
      
      <td valign="top" width="372">
        When embedding a video in MediaSpace, size selection works with all supported browsers.
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        [OTN] - When a user logs in as a guest, the following MediaSpace API error is displayed: Must use filters or categories. 
      </td>
      
      <td valign="top" width="372">
        [OTN] - When a user logs in as a guest, no error is displayed. 
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        [MediaSpace 4] Custom date fields are not saved correctly - the month always defaults to 01 regardless of what the user enters.
      </td>
      
      <td valign="top" width="372">
        [MediaSpace 4] Custom date fields, including the month, are correctly saved according to what the user enters.
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        The pager on the playlist tab does not function.
      </td>
      
      <td valign="top" width="372">
        The pager on the playlist tab functions correctly.
      </td>
    </tr>
  </tbody>
</table>

<span class="mce-heading-4"><a name="Build_4_5_15"></a>Version 4.5, Build 4.5.15</span>

These release notes pertain to MediaSpace version 4.5, released November 2012.

These release notes are intended for administrators of institutions installing MediaSpace and for MediaSpace developers.

<p class="mce-heading-4">
  What's New in this Release?
</p>

<table style="width: 570px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          <strong>MediaSpace SaaS</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        <ul>
          <li>
            <strong>Custom Module</strong> – Allow a customer to deploy custom modules to the Kaltura hosted environment. The custom modules will be available only for the customer's MediaSpace instance. <br />Requires professional services development and testing. For more information, please contact your Account Manager or Project Manager. 
          </li>
          <li>
            <strong>Custom Theme</strong> – Allow a customer to deploy custom themes to the Kaltura hosted environment. The custom themes will be available only for the customer's MediaSpace instance. <br />Requires professional services development and testing. For more information, please contact your Account Manager or Project Manager. 
          </li>
          <li>
            <strong>Custom SSO</strong> – Allow a customer to deploy a custom SSO gateway to the Kaltura hosted environment. The custom SSO gateway will be available only for the customer's MediaSpace instance.
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <strong>Comments</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        <ul>
          <li>
            Allow MediaSpace users to comment on media entries. 
          </li>
          <li>
            Allow the Comments feature to be enabled or disabled for a site.
          </li>
          <li>
            Allow a channel manager to override and disable comments for a specific channel.
          </li>
          <li>
            Allow a media entry owner to disable or close comments for a specific media entry.
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          <strong>Screen Recorder</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        <p>
          Allow MediaSpace users to create a screencast and automatically post it to MediaSpace. The screencast can include:
        </p>
        
        <ul>
          <li>
            A desktop recording
          </li>
          <li>
            Audio
          </li>
          <li>
            (Optional) Web cam 
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p>
          <strong>Captions</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        <ul>
          <li>
            Allow a content owner to upload caption files to a video in MediaSpace, instead of using the KMC.
          </li>
          <li>
            Allow MediaSpace users to:
          </li>
          <ul>
            <li>
              Search throughout MediaSpace for text that appears in captions (in addition to searching metadata).
            </li>
            <li>
              Automatically play any video that includes the caption text from the point where the text appears.
            </li>
          </ul>
          
          <li>
            Allow MediaSpace users to search a specific video for text that appears in captions and to automatically play the video from the point where the text appears.
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
   Known Issues
</p>

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="131">
        <p class="TableHeading">
          <strong>ID</strong>
        </p>
      </td>
      
      <td width="148">
        <p class="TableHeading">
          <strong>Module</strong>
        </p>
      </td>
      
      <td width="330">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="131">
        <p style="text-align: left;">
          1774 
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Webcam record description 
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        The description of a recording is saved only after the recording is saved.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        4511 
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Channels 
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p>
          When a channel is an Open channel type, the channel embed playlist is not displayed to users by default.  Displaying the channel embed playlist to users requires changing the Content Privacy of the channel's category to No Restriction in the KMC.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5292
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Media upload
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p>
          When media is added from a gallery page or channel page, the media overlap each other.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5350 
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Screen capture
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p>
          The screen capture widget cannot be dragged to the extend screen.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5551
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Likes
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p>
          Sorting by Likes is displayed even when the module is disabled.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5604 
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Comments
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p style="text-align: left;">
          Sorting by comment is displayed in a channel even when the module is disabled in the channel.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  Limitations
</p>

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="131">
        <p class="TableHeading">
          <strong>ID</strong>
        </p>
      </td>
      
      <td width="148">
        <p class="TableHeading">
          <strong>Module</strong>
        </p>
      </td>
      
      <td width="330">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          4224
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Devices-Android
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Only the device volume button can control the volume in a Flash player on Android.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          3332
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Devices-Android (Galaxy)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          My Playlists: Scrolling long playlists with two fingers is not possible.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          3861
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Search
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Live search: When starting to type a media name that exists, all of the media in the galleries disappears until the name is completely typed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          2570
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Search
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Entering a channel or gallery search string with numbers returns all the items.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          2599
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Categories
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Categories with long names are presented inadequately in the More drill down menu in the top navigation bar.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          3999
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Configuration-Roles
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Role name cannot be left empty. An empty role name causes a fatal error.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          4174
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Presentations
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Presentations may be displayed inadequately, depending on the UI size.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          3173
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          iPad
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          When navigating between pages, some elements from the previous page are displayed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          4268
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Android Xoom
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          In the bulk publish window, the display of sub‑categories is not straight.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p class="TableBodyText">
          4131
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          External and Internal Webcam  Use
        </p>
      </td>
      
      <td valign="top" width="330">
        <p class="TableBodyText" style="text-align: left;">
          Switching between an external and internal camera is not supported.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p>
          5130
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Comments
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        Sorting by comment does not work properly.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p>
          5153
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Comments
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        entryCommentsCountProfileId does not choose the correct profile ID.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        <p>
          5205
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Captions
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        Searching in certain languages, such as Hebrew and Japanese, fails.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5309
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Login 
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p>
          The minimum six-character requirement for the KMS login is not compatible with third party authentication methods such as LDAP. The password length should be configurable.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5342
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Screen capture
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        Camera recording overlays the screen capture and hides part of the screen.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5372
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Screen capture 
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        The recording area changes while the user is capturing the screen.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5593
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Devices-iPhone 
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        After performing a search for a keyword in captions, the user cannot play the entry.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5600
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        HTML5 
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        When switching between media, the loaded media plays only audio and the video is black.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5608
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Captions 
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        Caption search results cannot be displayed in a collapsed results format.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="131">
        5623
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        Upgrade 
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        Custom metadata - Channel topics are not saved after an upgrade.
      </td>
    </tr>
  </tbody>
</table>

<span class="mce-heading-4">Resolved Issues </span>

<table style="width: 570px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Issue</strong>
        </p>
      </td>
      
      <td valign="top" width="372">
        <p class="TableHeading">
          <strong>Fix</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          Enable header style>light currently is not supported. 
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        Enable header style>light is supported. 
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          The number of channel members in the Members tab of the channel's Settings page does not match the exact number of members in the channel. 
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        The number of channel members in the Members tab of the channel's Settings page correctly matches the number of members in the channel. 
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableBodyText">
          On an iPad: When My Media or an existing playlist have entries, adding media causes the entries to be displayed inadequately. 
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="372">
        On an iPad: When My Media or an existing playlist have entries,  the entries are displayed correctly when media is added. 
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  Tested Browsers
</p>

The following desktop browsers were tested for this release:

*   Firefox  13.0.1
*   Chrome latest
*   Safari 5.1.6
*   IE9
*   IE7 

<p class="mce-heading-4">
  Tested Operating Systems
</p>

The following Operating Systems were tested for this release:

*   Windows XP
*   Windows 7
*   iOS Mac

<p class="mce-heading-4">
  Tested Devices
</p>

<table style="width: 609px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="131">
        <p class="TableHeading">
          <strong>Platform</strong>
        </p>
      </td>
      
      <td width="148">
        <p class="TableHeading">
          <strong>Version</strong>
        </p>
      </td>
      
      <td width="330">
        <p class="TableHeading">
          <strong>Reference Device</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td rowspan="2" valign="top" width="131">
        <p class="TableBodyText" style="text-align: left;">
          iOS
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          5.0.1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          iPad 2
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          5.1.1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          iPhone 4
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="131">
        <p class="TableBodyText" style="text-align: left;">
          Blackberry
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Torch
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Blackberry Torch
        </p>
      </td>
    </tr>
    
    <tr>
      <td rowspan="4" valign="top" width="131">
        <p class="TableBodyText" style="text-align: left;">
          Android
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          HTML5 version 4 and later is supported.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          Version 3 supports Flash.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          4.0.2
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Galaxy Nexus
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          3.1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Motorola Xoom
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          2.3.3
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Galaxy 1, Galaxy 2
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          3.2
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="330">
        <p class="TableBodyText">
          Samsung Tab
        </p>
      </td>
    </tr>
  </tbody>
</table>