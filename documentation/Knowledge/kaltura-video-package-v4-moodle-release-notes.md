---
layout: page
title: "Kaltura Video Package V4 for Moodle Release Notes"
date: 2014-09-11 23:00:02
---

<p class="mce-heading-2">
  <a name="top"></a>
</p>

<p class="mce-heading-2">
  <a name="v4.0.10"></a>Version 4.0.10
</p>

<span>These release notes pertain to the Kaltura Video Plugin for Moodle, released July 2016. </span>This version includes added support for Moodle 3.1. This version supports automatic migration of content from version V3 of the package. Please refer to the section on [Content Migration][1] for important information. 

 [1]: #content_migration

<a name="v4.0.10"></a>

<table class="confluenceTable">
  <tbody>
    <tr>
      <td class="confluenceTd">
        <strong>Version</strong>
      </td>
      
      <td class="confluenceTd">
        4.0.10
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd">
        <strong>Release date</strong>
      </td>
      
      <td class="confluenceTd">
        July 2016
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>Supported Moodle Versions</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        <p>
          <span>Moodle 3.1: </span><strong>Kaltura Release 4.0.10 (<span>2016070731</span>)</strong>
        </p>
        
        <p>
          Moodle 3.0: <strong>Kaltura Release 4.0.10 (<span>2016070730</span></strong><strong>)</strong>
        </p>
        
        <p>
          Moodle 2.9: <strong>Kaltura Release 4.0.10 (<span>2016070729</span>)</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>KAF Version</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        5.49.x
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<p class="mce-heading-3">
  Resolved Issues
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-11624
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        Moodle 3.1 verification
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-11854
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        Added support for locally assigned roles and group limited users.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-7324
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The issue causing newly embedded content to not show up when using the old BSE has been resolved.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-7348
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The issue causing a DNS error when updating an entry has been resolved.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-8116 
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The issue causing difficulty with saving changes for feedback on a media assignment submission has been resolved.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-11337
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The plugin is now sending the "launch_presentation_url" parameter in every LTI launch for language detection.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-10750
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The error causing issues with the full screen display has been resolved.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-11871
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The error causing issues with preview and embed of a video resource on IE has been resolved.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-11965
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The error causing issues with scrolling in the BSE window has been resolved.
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>Known Issues
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2542
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A Kaltura video presentation may not be viewed properly on mobile devices. The introduction of the Kaltura HTML5 Video Presentation Player should resolve this issue.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The Shared Repository header displays the repository counter (with a value of 1), instead of displaying "Shared Repository".<strong><br /></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2486
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Changing the text color option in the Edit Entry page is not working properly on Internet Explorer.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2875
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The collapsed view does not react on the Shared Repository tab inside the Browse, Search and Embed module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KAL-DEV-628
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A redundant scroll bar appears when migrating a video in TinyMCE in a Kaltura Video Resource from V3 to V4.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>Limitations
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          FEC-1687
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The full screen button in the small and medium Video Presentations is not visible.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KMS-2487
      </td>
      
      <td style="text-align: left;" valign="top">
        HTML tags appear in the video presentation Description field when creating a new video presentation.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KMS-2547
      </td>
      
      <td style="text-align: left;" valign="top">
        It is not possible to upload captions on mobile devices.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KALDEV-593
      </td>
      
      <td style="text-align: left;" valign="top">
        A Video Resource may be displayed incorrectly when adding media via the TinyMCE and Add Media.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KALDEV-626
      </td>
      
      <td style="text-align: left;" valign="top">
        A video presentation resource may be migrated incorrectly if the video was also added via the TinyMCE.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        SUP-3512
      </td>
      
      <td style="text-align: left;" valign="top">
        Migration to this version may require disabling the 32 category limitation by Kaltura Customer Care and will require a temporary scheduled downtime for non-KAF applications.
      </td>
    </tr>
  </tbody>
</table>

[Back to Top][2]

 [2]: #top

<p class="mce-heading-2">
  <a name="v4.0.07"></a>Version 4.0.08
</p>

This version includes added support for Moodle 3.0. This version supports automatic migration of content from version V3 of the package. Please refer to the section on [Content Migration][1] for important information. 

<a name="v4.0.02"></a>

<table class="confluenceTable">
  <tbody>
    <tr>
      <td class="confluenceTd">
        <strong>Version</strong>
      </td>
      
      <td class="confluenceTd">
        4.0.08
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd">
        <strong>Release date</strong>
      </td>
      
      <td class="confluenceTd">
        December 2015
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>Supported Moodle Versions</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        <p>
          Moodle 3.0: <strong>Kaltura Release 4.0.08 (2015120930</strong><strong>)</strong>
        </p>
        
        <p>
          Moodle 2.9: <strong>Kaltura Release 4.0.08 (2015120909)</strong>
        </p>
        
        <p>
          Moodle 2.8: <strong>Kaltura Release 4.0.08 (2015122708)</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>KAF Version</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        5.37.04
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<p class="mce-heading-3">
  Resolved Issues
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-4063
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The message shown when grading a Kaltura video assignment where no submissions are available yet, has been updated.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-6548
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The issue causing the following error: "<span>Error reading from database" when grading a submission has been resolved.</span>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-6754
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        When grading a Kaltura video assignment, all students will be listed, including students that have not submitted assignments yet.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-9555
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        All the Kaltura Tool's icons have been updated.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-9330
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The video section will be automatically opened in the Kaltura Video Resource page.
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>Known Issues
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2542
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A Kaltura video presentation may not be viewed properly on mobile devices. The introduction of the Kaltura HTML5 Video Presentation Player should resolve this issue.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The Shared Repository header displays the repository counter (with a value of 1), instead of displaying "Shared Repository".<strong><br /></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2486
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Changing the text color option in the Edit Entry page is not working properly on Internet Explorer.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2875
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The collapsed view does not react on the Shared Repository tab inside the Browse, Search and Embed module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KAL-DEV-628
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A redundant scroll bar appears when migrating a video in TinyMCE in a Kaltura Video Resource from V3 to V4.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>Limitations
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          FEC-1687
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The full screen button in the small and medium Video Presentations is not visible.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KMS-2487
      </td>
      
      <td style="text-align: left;" valign="top">
        HTML tags appear in the video presentation Description field when creating a new video presentation.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KMS-2547
      </td>
      
      <td style="text-align: left;" valign="top">
        It is not possible to upload captions on mobile devices.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KALDEV-593
      </td>
      
      <td style="text-align: left;" valign="top">
        A Video Resource may be displayed incorrectly when adding media via the TinyMCE and Add Media.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KALDEV-626
      </td>
      
      <td style="text-align: left;" valign="top">
        A video presentation resource may be migrated incorrectly if the video was also added via the TinyMCE.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        SUP-3512
      </td>
      
      <td style="text-align: left;" valign="top">
        Migratiion to this version may require disabling the 32 category limitation by Kaltura Customer Care and will require a temporary scheduled downtime for non-KAF applications.<br /><br />
      </td>
    </tr>
  </tbody>
</table>

[Back to Top][2]

<p class="mce-heading-2">
  <span><a name="v4.0.07"></a>Version 4.0.07</span>
</p>

This version includes added support for Moodle 2.9. This version supports automatic migration of content from version V3 of the package. Please refer to the section on [Content Migration][1] for important information. 

<a name="v4.0.02"></a>

<table class="confluenceTable">
  <tbody>
    <tr>
      <td class="confluenceTd">
        <strong>Version</strong>
      </td>
      
      <td class="confluenceTd">
        4.0.07
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd">
        <strong>Release date</strong>
      </td>
      
      <td class="confluenceTd">
        September 2015
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>Supported Moodle Versions</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        <p>
          <span>Moodle 2.9: </span><strong>Kaltura Release 4.0.07 (<span>2015091609</span></strong><strong>)</strong>
        </p>
        
        <p>
          Moodle 2.8: <strong>Kaltura Release 4.0.07 (<span>2015090708</span>)</strong>
        </p>
        
        <p>
          Moodle 2.7: <strong>Kaltura Release 4.0.07 (<span>2015090707</span>)</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>KAF Version</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        5.30.05
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<p class="mce-heading-3">
  Resolved Issues
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-3619<a href="https://kaltura.atlassian.net/browse/KMS-4030"></a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue with cross site scripting in IE has been resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-4944
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the error wihen embedding content via the TinyMCE on IE has been resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          SUP-3804
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the "Submit" button to move down the page after submitting a media assignment has been resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-8733
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the full screen not to work for media assignments has been resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-8735
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the "Exit" button to appear out of the media assignment box has been resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-8846
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the "Grade Submission" screen to be cut from the screen has been resolved.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a><span>Known Issues</span>
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2542
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A Kaltura video presentation may not be viewed properly on mobile devices. The introduction of the Kaltura HTML5 Video Presentation Player should resolve this issue.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The Shared Repository header displays the repository counter (with a value of 1), instead of displaying "Shared Repository".<strong><br /></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2486
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Changing  the text color option in the Edit Entry page is not working properly on Internet Explorer.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KMS-2875
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The collapsed view does not react on the Shared Repository tab inside the Browse, Search and Embed module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          KAL-DEV-628
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A redundant scroll bar appears when migrating a video in TinyMCE in a Kaltura Video Resource from V3 to V4.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a><span>Limitations</span>
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          FEC-1687
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The full screen button in the small and medium Video Presentations is not visible.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KMS-2487
      </td>
      
      <td style="text-align: left;" valign="top">
        HTML tags appear in the video presentation Description field when creating a new video presentation.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KMS-2547
      </td>
      
      <td style="text-align: left;" valign="top">
        It is not possible to upload captions on mobile devices.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KALDEV-593
      </td>
      
      <td style="text-align: left;" valign="top">
        A Video Resource may be displayed incorrectly when adding media via the TinyMCE and Add Media.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        KALDEV-626
      </td>
      
      <td style="text-align: left;" valign="top">
        A video presentation resource may be migrated incorrectly if the video was also added via the TinyMCE.
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        SUP-3512
      </td>
      
      <td style="text-align: left;" valign="top">
        The migration might require to disable the 32 category limitation by Kaltura Customer Care and will require a temporary scheduled downtime for non-KAF applications.<br /><br />
      </td>
    </tr>
  </tbody>
</table>

[Back to Top][2]

<p class="mce-heading-2">
  <a name="v4.0.04"></a><span style="font-size: 18pt;">Version 4.0.04</span>
</p>

<a name="v4.0.04"></a>This version now includes added support for Moodle 2.8. This version supports automatic migration of content from version V3 of the package. Please refer to the section on [Content Migration][1] for important information. 

<a name="v4.0.02"></a>

<table class="confluenceTable">
  <tbody>
    <tr>
      <td class="confluenceTd">
        <strong>Version</strong>
      </td>
      
      <td class="confluenceTd">
        4.0.04
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd">
        <strong>Release date</strong>
      </td>
      
      <td class="confluenceTd">
        March 2015
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>Supported Moodle Versions</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        <p>
          <span>Moodle 2.8: </span><strong>Kaltura Release 4.0.04 (<span>2015021108</span>)</strong>
        </p>
        
        <p>
          Moodle 2.7: <strong>Kaltura Release 4.0.04 (<span>2015021107</span>)</strong>
        </p>
        
        <p>
          Moodle 2.6: <strong>Kaltura Release 4.0.04 (<span>2015021106</span>)</strong><a href="https://moodle.org/plugins/download.php/6861/Kaltura_Video_Package_moodle26_2014023000.zip"><br /></a>
        </p>
        
        <p>
          <a href="https://moodle.org/plugins/download.php/6861/Kaltura_Video_Package_moodle26_2014023000.zip"></a>Moodle 2.5: <strong>Kaltura Release 4.0.04 (<span>2015021105</span>)</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>KAF Version</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        5.18.10
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<p class="mce-heading-3">
  Resolved Issues
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          SUP-3539<a href="https://kaltura.atlassian.net/browse/KMS-4030"></a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the following error: "Cannot find data record in database table course_modules" has been resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-6000
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Removed two functions that are being called that have been deprecated in Moodle 2.8.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a><span style="color: #828a8c; font-size: 14pt;">Known Issues</span>
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2542
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A Kaltura video presentation may not be viewed properly on mobile devices. The introduction of the Kaltura HTML5 Video Presentation Player should resolve this issue.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The Shared Repository header displays the repository counter (with a value of 1), instead of displaying "Shared Repository".<strong><br /></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2486
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Changing  the text color option in the Edit Entry page is not working properly on Internet Explorer.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2875
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The collapsed view does not react on the shared repository tab inside the Browse, Search and Embed module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KAL-DEV-628
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A redundant scroll bar appears when migrating a video in TinyMCE in a Kaltura Video Resource from V3 to V4.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a><span style="color: #828a8c; font-size: 14pt;">Limitations</span>
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          FEC-1687
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The full screen button in the small and medium Video Presentations is not visible.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-2487
      </td>
      
      <td style="text-align: left;" valign="top">
        HTML tags appear in the video presentation Description field when creating a new video presentation.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-2547
      </td>
      
      <td style="text-align: left;" valign="top">
        It is not possible to upload captions on mobile devices.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KALDEV-593
      </td>
      
      <td style="text-align: left;" valign="top">
        A Video Resource may be displayed incorrectly when adding media via the TinyMCE and Add Media.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KALDEV-626
      </td>
      
      <td style="text-align: left;" valign="top">
        A video presentation resource may be migrated incorrectly if the video was also added via the TinyMCE.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        SUP-3512
      </td>
      
      <td style="text-align: left;" valign="top">
        The migration might require to disable the 32 category limitation by Kaltura Customer Care and will require a temporary scheduled downtime for non-KAF applications.<br /><br />
      </td>
    </tr>
  </tbody>
</table>

[Back to Top][2]

<p class="mce-heading-2">
  Version 4.0.03
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

This version supports automatic migration of content from version V3 of the package. Please refer to the section on [Content Migration][1] for important information.

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table class="confluenceTable">
  <tbody>
    <tr>
      <td class="confluenceTd">
        <strong>Version</strong>
      </td>
      
      <td class="confluenceTd">
        4.0.03
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd">
        <strong>Release date</strong>
      </td>
      
      <td class="confluenceTd">
        January 2015
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>Supported Moodle Versions</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        <p>
          Moodle 2.7: <strong>Kaltura Release 4.0.03 (<span>2015012507</span>)</strong>
        </p>
        
        <p>
          Moodle 2.6: <strong>Kaltura Release 4.0.03 (<span>(2015012506</span>)</strong><a href="https://moodle.org/plugins/download.php/6861/Kaltura_Video_Package_moodle26_2014023000.zip"><br /></a>
        </p>
        
        <p>
          <a href="https://moodle.org/plugins/download.php/6861/Kaltura_Video_Package_moodle26_2014023000.zip"></a>Moodle 2.5: <strong>Kaltura Release 4.0.03 (<span>2015012505</span>)</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>KAF Version</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        5.17.07
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<p class="mce-heading-3">
  Resolved Issues
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          SUP-3493<a href="https://kaltura.atlassian.net/browse/KMS-4030"></a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the following migration error: "Exception - Invalid entry id" has been resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          SUP-3537
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the following migration error: "Exception - Entry id "3" not found" has been resolved.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          SUP-3519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          The issue causing the following migration error: "Entry already assigned to this category" has been resolved.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<p class="mce-heading-3">
  Known Issues
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2542
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A Kaltura video presentation may not be viewed properly on mobile devices. The introduciton of the Kaltura HTML5 Video Presentation Player should resolve this issue.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The Shared Repository header displays the repository counter (with a value of 1), instead of displaying "Shared Repository".<strong><br /></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2486
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Changing  the text color option in the Edit Entry page is not working properly on Internet Explorer.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2875
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The collapsed view does not react on the shared repository tab inside the Browse, Search and Embed module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KAL-DEV-628
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A redundant scroll bar appears when migrating a video in TinyMCE in a Kaltura Video Resource from V3 to V4.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<p class="mce-heading-3">
  Limitations
</p>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          FEC-1687
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The full screen button in small and medium Video Presentations is not visible.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-2487
      </td>
      
      <td style="text-align: left;" valign="top">
        HTML tags appear in the video presentation description field when creating a new video presentation.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-2547
      </td>
      
      <td style="text-align: left;" valign="top">
        It is not possible to upload captions on mobile devices.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KALDEV-593
      </td>
      
      <td style="text-align: left;" valign="top">
        A Video Resource may be displayed incorrectly when adding media via the TinyMCE and Add Media.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KALDEV-626
      </td>
      
      <td style="text-align: left;" valign="top">
        A video presentation resource may be migrated incorrectly if the video was also added via the TinyMCE.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        SUP-3512
      </td>
      
      <td style="text-align: left;" valign="top">
        The migration might require to disable the 32 category limitation by Kaltura Customer Care and will require a temporary scheduled downtime for non-KAF applications.
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="v4.0.02"></a>
</p>

[Back to top][2]

<p class="mce-heading-2">
  <a name="v4.0.02"></a>Version 4.0.02
</p>

This version supports automatic migration of content from version V3 of the package. Please refer to the section on [Content Migration][1] for important information.

<table class="confluenceTable">
  <tbody>
    <tr>
      <td class="confluenceTd">
        <strong>Version</strong>
      </td>
      
      <td class="confluenceTd">
        <span>4.0.2</span>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd">
        <strong>Release date</strong>
      </td>
      
      <td class="confluenceTd">
        January 2015
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>Supported Moodle Versions</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        <p>
          <span>Moodle 2.7: <strong>Kaltura Release 4.0.02 (<strong>2014121807</strong>)</strong></span>
        </p>
        
        <p>
          <span>Moodle 2.6: <strong>Kaltura Release 4.0.02 (<span>2014121806</span>)</strong></span><a href="https://moodle.org/plugins/download.php/6861/Kaltura_Video_Package_moodle26_2014023000.zip"><br /></a>
        </p>
        
        <p>
          <a href="https://moodle.org/plugins/download.php/6861/Kaltura_Video_Package_moodle26_2014023000.zip"></a><span>Moodle 2.5: <strong>Kaltura Release 4.0.02 (<span>2014121805</span>)</strong></span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" colspan="1">
        <strong>KAF Version</strong>
      </td>
      
      <td class="confluenceTd" colspan="1">
        <span>5.16.10</span>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Resolved Issues
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        SUP-3517
      </td>
      
      <td style="text-align: left;" valign="top">
        <span><span>The issue causing the following migration error: "<span>unable to determine the root category id</span></span><span>" has been resolved.</span></span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-5334
      </td>
      
      <td style="text-align: left;" valign="top">
        The issue causing the video resources to not work after migration has been resolved.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-5210
      </td>
      
      <td style="text-align: left;" valign="top">
        The issue causing the migration to not complete while selecting continue has been resolved.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-5543
      </td>
      
      <td style="text-align: left;" valign="top">
        The issue causing the following error: "<span>Entry should be created by current user or user is not entitled to categories entry is published to" when playing an entry after a second migration, has been resolved.</span>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Known Issues
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          <span></span>KMS-2542
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A Kaltura Video presentation may not be viewed properly on mobile devices. The introduciton of the Kaltura HTML5 Video Presentation Player should resolve this issue.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The Shared Repository header displays the repository counter (with a value of 1), instead of displaying "Shared Repository".<strong><br /></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2486
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Changing  the text color option in the Edit Entry page is not working properly on Internet Explorer.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2875
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          Moodle (KAF)- The collapsed view does not react on the shared repository tab inside the Browse, Search and Embed module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KAL-DEV-628
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p>
          A redundant scroll bar appears when migrating a video in TinyMCE in a Kaltura Video Resource from V3 to V4.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Limitations
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          FEC-1687
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The full screen button in small and medium Video Presentations is not visible.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-2487
      </td>
      
      <td style="text-align: left;" valign="top">
        HTML tags appear in the video presentation description field when creating a new video presentation.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-2547
      </td>
      
      <td style="text-align: left;" valign="top">
        It is not possible to upload captions on mobile devices.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KALDEV-593
      </td>
      
      <td style="text-align: left;" valign="top">
        A Video Resource may be displayed incorrectly when adding media via the TinyMCE and Add Media.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KALDEV-626
      </td>
      
      <td style="text-align: left;" valign="top">
        A video presentation resource may be migrated incorrectly if the video was also added via the TinyMCE.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        SUP-3512
      </td>
      
      <td style="text-align: left;" valign="top">
        The migration might require to disable the 32 category limitation by Kaltura Customer Care and will require a temporary scheduled downtime for non-KAF applications
      </td>
    </tr>
  </tbody>
</table>

[Back to top][2] 

<p class="mce-heading-2">
  <span>Version 4.0</span>
</p>

<span></span>This version supports automatic migration of content from version V3 of the package. Please refer to the section on [Content Migration][1] for important information.

<table class="confluenceTable">
  <tbody>
    <tr>
      <td class="confluenceTd" style="text-align: left;">
        <strong>Version</strong>
      </td>
      
      <td class="confluenceTd" style="text-align: left;">
        <span style="color: #000000;">4.0</span>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" style="text-align: left;">
        <strong>Release date</strong>
      </td>
      
      <td class="confluenceTd" style="text-align: left;">
        October 2014
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" style="text-align: left;" colspan="1">
        <strong>Supported Moodle Versions</strong>
      </td>
      
      <td class="confluenceTd" style="text-align: left;" colspan="1">
        <p>
          <span style="text-align: center;">Moodle 2.7: <strong>Kaltura Release 4.0.01 (2014102807)</strong></span>
        </p>
        
        <p>
          <span style="text-align: center;">Moodle 2.6: <strong>Kaltura Release 4.0.01 (2014102106)</strong></span><a href="https://moodle.org/plugins/download.php/6861/Kaltura_Video_Package_moodle26_2014023000.zip" style="text-align: center;"><br /></a>
        </p>
        
        <p>
          <a href="https://moodle.org/plugins/download.php/6861/Kaltura_Video_Package_moodle26_2014023000.zip" style="text-align: center;"></a><span style="text-align: center;">Moodle 2.5: <strong>Kaltura Release 4.0.01 (2014102105)</strong></span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td class="confluenceTd" style="text-align: left;" colspan="1">
        <strong>KAF Version</strong>
      </td>
      
      <td class="confluenceTd" style="text-align: left;" colspan="1">
        5.11.107
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Resolved Issues
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          <span></span>KMS-4030<a href="https://kaltura.atlassian.net/browse/KMS-4030"></a>
        </p>
      </td>
      
      <td valign="top">
        <p>
          The 'x' icon on the search bar on mobile devices is now working properly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          FEC-1729
        </p>
      </td>
      
      <td valign="top">
        <p style="text-align: left;">
          The full screen display is woring properly for image entries.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Known Issues
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          <span style="text-decoration: line-through;"></span>KMS-2542
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p style="text-align: left;">
          A Kaltura Video presentation may not be viewed properly on mobile devices. The introduciton of the Kaltura HTML5 Video Presentation Player should resolve this issue.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2519
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p style="text-align: left;">
          <span>Moodle (KAF)- The Shared Repository header displays the repository counter (with a value of 1), instead of displaying "Shared Repository".</span><strong><br /></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2486
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p style="text-align: left;">
          Changing  the text color option in the Edit Entry page is not working properly on Internet Explorer.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KMS-2875
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p style="text-align: left;">
          Moodle (KAF)- The collapsed view does not react on the shared repository tab inside the Browse, Search and Embed module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          KAL-DEV-628
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p style="text-align: left;">
          <span>A redundant scroll bar appears when migrating a video in TinyMCE in a Kaltura Video Resource from V3 to V4.</span>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Limitations
</p>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top">
        <p>
          <strong>Ticket Number</strong>
        </p>
      </td>
      
      <td valign="top">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          FEC-1687
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        The full screen button in small and medium Video Presentations is not visible.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-2487
      </td>
      
      <td style="text-align: left;" valign="top">
        <span>HTML tags appear in the video presentation description field when creating a new video presentation.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KMS-2547
      </td>
      
      <td style="text-align: left;" valign="top">
        <span>It is not possible to upload captions on mobile devices.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KALDEV-593
      </td>
      
      <td style="text-align: left;" valign="top">
        <span>A Video Resource may be displayed incorrectly when adding media via the TinyMCE and Add Media.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        KALDEV-626
      </td>
      
      <td style="text-align: left;" valign="top">
        <span>A video presentation resource may be migrated incorrectly if the video was also added via the TinyMCE.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        SUP-3512
      </td>
      
      <td style="text-align: left;" valign="top">
        <span>The migration might require to disable the 32 category limitation by Kaltura Customer Care and will require a temporary scheduled downtime for non-KAF applications</span>
      </td>
    </tr>
  </tbody>
</table>

<a name="content_migration"></a><span class="mce-heading-3">Content Migration</span>

Please make sure to read the<a href="http://knowledge.kaltura.com/node/1170/attachment/field_media" target="_blank"> Kaltura Video Package V4 for Moodle Installation and Upgrade Guide </a>before upgrading from the Kaltura Video Package V3.

Content migration was tested and verified on the following enviornment

*   CentOS 6.5, Apache 2.2.15, PHP 5.3.3
*   CentOS 6.5, Apache 2.2.15, PHP 5.4.23
*   Fedora 19, Apache 2.4.10, PHP 5.5.15

<p class="mce-heading-3">
  Known Issues and Limitation for Migration
</p>

<table border="0">
  <tbody>
    <tr>
      <td>
        KALDEV-632
      </td>
      
      <td style="text-align: left;">
        Entries shared with multiple courses in V3 may not migrate properly when running on PHP versions below 5.3.29.
      </td>
    </tr>
    
    <tr>
      <td>
        KALDEV-626
      </td>
      
      <td style="text-align: left;">
        <span>A video presentation resource migrated incorrectly if  the video was added also via TinyMCE</span>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  Important Configuration Notes
</p>

*   When changing the KAF root category in the KMC, it is mandatory to update the Shared Repository by opening the KAF Admin Consle > Hosted > Shared repository field and clicking the Update button.

*   The default role-mapping settings for Students allow:

*   Accessing and adding media via My Media

*   Publishing media to the Shared Repository (previsouly known as "Shared with Site")

*   Publishing media to courses Media Gallery. Published entries will require moderation by a faculty member.

*   The default settings for Teachers (and administrator) allow:

*   Accessing and adding media via My Media

*   Publishing media to the Shared Repository (previsouly known as "Shared with Site".

*   Publishing media to courses Media Gallery. Published entries will require moderation by a faculty member.

*   Changing Moodle course names: When the name of an active course is changed in Moodle, it is only updated in the KMC (and KAF) after the first time a user accesses the Media Gallery of that course.

[Back to top][2]