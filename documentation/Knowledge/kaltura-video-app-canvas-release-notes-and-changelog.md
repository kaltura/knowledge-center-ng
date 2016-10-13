---
layout: page
title: "Kaltura Video App for Canvas Release Notes and Changelog"
date: 2014-01-22 16:10:44
---

<a name="top"></a>

<table border="1" cellpadding="0">
  <thead>
    <tr>
      <td>
        <p>
          <strong>Version</strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Date Released</strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Details</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td>
        <p align="center">
          <a href="#v1.1">1.1</a>
        </p>
      </td>
      
      <td>
        <p align="center">
          December, 2015
        </p>
      </td>
      
      <td>
        <p align="center">
          Kaltura Application Framework v 5.37.06
        </p>
      </td>
    </tr>
    
    <tr>
      <td>
        <p align="center">
          <a href="#version1_0">1.0 </a>
        </p>
      </td>
      
      <td>
        <p align="center">
          February, 2014 
        </p>
      </td>
      
      <td>
        <p align="center">
          Kaltura Application Framework v 5.6.04 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <strong><a name="version1_0"></a></strong>
</p>

<p class="mce-heading-2">
  <strong><a name="v1.1"></a>Version 1.1</strong>
</p>

These release notes pertain to the Kaltura Video App for Canvas, released in January, 2015. Added support according to the content item message specification as part of the LTI standard. 

To upgrade you will need to uninstall the Media Gallery app and re-install following the instructions in the <a href="{{site.url}}/documentation/Knowledge/kaltura-video-app-canvas-deployment-guide-0.html" target="_blank">Kaltura Video App for Canvas Deployment Guide.</a>

<p class="mce-heading-3">
  Resolved issues
</p>

<table border="0" frame="border">
  <tbody>
    <tr>
      <td>
        ID
      </td>
      
      <td>
        Details
      </td>
    </tr>
    
    <tr>
      <td>
        KMS-9242
      </td>
      
      <td>
        The rich-text editor integration has been transitioned and now complues with content-item message specification.
      </td>
    </tr>
    
    <tr>
      <td>
        KMS-10344
      </td>
      
      <td>
        You can now use the Create XML generator for the Canvas app installation.
      </td>
    </tr>
    
    <tr>
      <td>
        SUP-6096
      </td>
      
      <td>
        The problem with embbeding Kaltura Media within Canvas Groups that  resulted in an "Access Denied" error has been fixed.
      </td>
    </tr>
  </tbody>
</table>

** Currently, you need to map the LTI role "None" to the  "PrivateOnly Role" to allow embedding content wihtin Canvas Groups. Please note that this will also grant My Media access to users with the "None" role.

<p class="mce-heading-3">
  <strong>Known Issues</strong>
</p>

<table border="1" cellpadding="0">
  <thead>
    <tr>
      <td>
        <p>
          <strong>ID#</strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong> Component      </strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td>
        <p align="center">
          KMS-1932
        </p>
      </td>
      
      <td>
        <p align="center">
          Publish / General UI
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          When publishing a single item via My Media, there is an indication in the course's checkboxes where the item was published.<br />When publishing multiple items, the indication is not displayed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td>
        <p align="center">
          KMS-2104
        </p>
      </td>
      
      <td>
        <p align="center">
          View Media / General UI
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          When vieweing a media item in large screen resolutions (e.g. 1280x800), the video player size does not fit the entire iframe.<br />Workaround: Scroll down to reach the player's control bar.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <strong>Limitations</strong>
</p>

<table border="1" cellpadding="0">
  <thead>
    <tr>
      <td>
        <p>
          <strong>ID#</strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Component       </strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td>
        <p align="center">
           KMS-2068
        </p>
      </td>
      
      <td>
        <p align="center">
          My Media / View Media
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          When an entry is uploaded to a course via Browse, Search & Embed, the following tag is included in the media item's details: 'embedded in course'.<br />After the entry is deleted from the specific embed HTML of the course, the tag 'embedded in course' is still displayed under the entry's details.
        </p>
      </td>
    </tr>
    
    <tr>
      <td>
        <p align="center">
          KMS-1291
        </p>
      </td>
      
      <td>
        <p align="center">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          When deleting a course from Canvas, after a new category was created in Kaltura's end, the deletion is not reflected in Kaltura and the category is not deleted. <br />This issue causes the entry to display all the courses it was published to, even though these courses may have been deleted. 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
   
</p>

<p class="mce-heading-2">
  <strong>Version 1.0</strong>
</p>

These release notes pertain to the Kaltura Video App for Canvas, released in February, 2014

<p class="mce-heading-3">
  <strong>Known Issues</strong>
</p>

<table border="1" cellpadding="0">
  <thead>
    <tr>
      <td>
        <p>
          <strong>ID#</strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong> Component      </strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;">
        <p align="center">
          KMS-1932
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          Publish / General UI
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          When publishing a single item via My Media, there is an indication in the course's checkboxes where the item was published.<br />When publishing multiple items, the indication is not displayed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        <p align="center">
          KMS-2104
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          View Media / General UI
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          When vieweing a media item in large screen resolutions (e.g. 1280x800), the video player size does not fit the entire iframe.<br />Workaround: Scroll down to reach the player's control bar.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <strong>Limitations</strong>
</p>

<table border="1" cellpadding="0">
  <thead>
    <tr>
      <td>
        <p>
          <strong>ID#</strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Component       </strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;">
        <p align="center">
           KMS-2068
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          My Media / View Media
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          When an entry is uploaded to a course via Browse, Search & Embed, the following tag is included in the media item's details: 'embedded in course'.<br />After the entry is deleted from the specific embed HTML of the course, the tag 'embedded in course' is still displayed under the entry's details.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        <p align="center">
          KMS-1291
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          When deleting a course from Canvas, after a new category was created in Kaltura's end, the deletion is not reflected in Kaltura and the category is not deleted. <br /> This issue causes the entry to display all the courses it was published to, even though these courses may have been deleted. 
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <strong>Mobile - Known issues</strong>
</p>

<table border="1" cellpadding="0">
  <thead>
    <tr>
      <td>
        <p>
          <strong>ID#</strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>  Component </strong>
        </p>
      </td>
      
      <td>
        <p>
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td>
        <p align="center">
          KMS-1497 
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          Mobile / Upload 
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          Uploading a new recorded video using an Android device is not supported via Canvas for this release. When uploading a new 'Camcorder' video via an Android device, an error message is displayed in the upload progress.<br /><br />
        </p>
      </td>
    </tr>
    
    <tr>
      <td>
        <p align="center">
          KMS-2087
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          Mobile / General UI
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          Text cannot be added into the Description field of a Media item or Media Gallery via iOS devices. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td>
        <p align="center">
          KMS-2079
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          Mobile / General UI
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          Full screen via iOS devices does not work propely.
        </p>
      </td>
    </tr>
    
    <tr>
      <td>
        <p align="center">
          KMS-2089
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          Mobile / General UI
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          The Browse, Search & Smbed window does not fit to the iOS device screen width and may be inconvenient to control and use via Mobile.
        </p>
      </td>
    </tr>
    
    <tr>
      <td>
        <p align="center">
          KMS-839
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          View Media / Mobile 
        </p>
      </td>
      
      <td style="text-align: left;">
        <p>
          Viewing an image via a Mobile device will open an incorrect player which refers to it as a video.<br />The 'Play' button in the middle of the player is needed to be clicked in order to view the image.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <strong>Tested Browsers and Operating Systems</strong>
</p>

The following desktop browsers were tested for this release:**  
**

*   Firefox, latest
*   Chrome, latest
*   Safari 7
*   IE10, IE11

The following desktop operating systems were tested for this release:

*   Windows 7
*   Mac OS 10.9 - Mavericks

**Tested Mobile Devices**

<table border="1" cellpadding="0">
  <thead>
    <tr>
      <td>
        <p align="center">
          <strong>Platform</strong>
        </p>
      </td>
      
      <td>
        <p align="center">
          <strong>     Version</strong>
        </p>
      </td>
      
      <td>
        <p align="center">
          <strong>Reference Device</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;">
        <p align="center">
          iOS
        </p>
        
        <p align="center">
           
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          6.x / 7.x
        </p>
      </td>
      
      <td style="text-align: left;">
        <ul>
          <li>
            iPhone 4            
          </li>
          <li>
            iPhone 4S
          </li>
          <li>
            iPad 2
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        <p align="center">
          Android
        </p>
      </td>
      
      <td style="text-align: left;">
        <p align="center">
          4.x
        </p>
      </td>
      
      <td style="text-align: left;">
        <ul>
          <li>
            Samsung Galaxy S3
          </li>
          <li>
            Samsung Tab
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

[Back to top][1]

 [1]: #top

 