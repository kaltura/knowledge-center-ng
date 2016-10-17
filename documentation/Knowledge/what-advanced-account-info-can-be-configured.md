---
layout: page
title: "What advanced account info can be configured?"
date: 2011-12-25 00:52:26
---

<p class="mce-heading-2">
  Entry Managment
</p>

1.  Go the the Settings tab and select Integration Settings.
2.  In the Entry Management pane click Advanced Settings.

<img src="../../assets/90.img">

The following table describes the fields for the Miscellaneous options.

<table style="width: 735px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="248">
        <p class="TableHeading">
          <strong>Field</strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="248">
        <p class="TableBodyText" style="text-align: left;">
          User Page URL format
        </p>
      </td>
      
      <td valign="top" width="487">
        <p class="TableBodyText" style="text-align: left;">
          When Kaltura Media Entries are played in the Kaltura Player, a variable named “userLandingPage” will be created for every played entry. That variable will hold a link to the user page of the user who created that media entry.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          To determine the URL to which the userLandingPage variable will point to, enter the base URL in this field, followed by the following token:
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          {uid} – The User Id who created the media.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          For example: http://mysite.com/users/{uid}
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="248">
        <p class="TableBodyText" style="text-align: left;">
          Media Page URL format
        </p>
      </td>
      
      <td valign="top" width="487">
        <p class="TableBodyText" style="text-align: left;">
          When Kaltura Media Entries are played in the Kaltura Player, a variable named “partnerLandingPage” will be created for every played entry. That variable will hold a link to a media page of that entry on the publisher site.<strong></strong>
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          To determine the URL to which the partnerLandingPage variable will point to, enter the base URL in this field, followed by the following token:<strong></strong>
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          {id} – The Media Entry Id.<strong></strong>
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          For example: http://mysite.com/media/{id}
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="248">
        <p class="TableBodyText" style="text-align: left;">
          User Upload Limit
        </p>
      </td>
      
      <td valign="top" width="487">
        <p class="TableBodyText" style="text-align: left;">
          By default, Kaltura allows users to upload files up to 150 MB per file. Use this option to change the file upload limit. You cannot upload more than 1GB per upload session. For example, setting the upload limit to 100MB allows users to upload up to 10 files at a time.<strong></strong>
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          If you require higher settings, please contact Kaltura’s Support.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  Notifications
</p>

When creating Kaltura applications or integrating various Kaltura features into existing applications or sites, it is often required that the application be notified of various actions that occurred in Kaltura. For example: When a user on your site uploads a new video file, you might want your site code to be notified of when Kaltura has finished processing the video file and made it ready for publishing.

While it is possible to easily query the Kaltura API periodically, Kaltura’s API Notifications utilize a “push” methodology where a code on your site will be called automatically by Kaltura whenever a certain actions occur like video upload or media status changes.

Kaltura provide two types of Notifications: 

<a href="http://www.kaltura.org/kaltura-terminology#kaltura-client-notifications" target="_blank">Kaltura Client Notifications</a><a href="http://www.kaltura.org/kaltura-terminology#kaltura-client-notifications" target="_blank"> </a>– Notifications that are sent from the Kaltura widget (e.g. Kaltura Contribution Wizard) when a user performs an action like uploading a new video file. The notification will be called from the Kaltura widget directly to the publisher’s notification handler code hosted on the publisher’s server.

<a href="http://www.kaltura.org/kaltura-terminology#kaltura-server-notifications" target="_blank">Kaltura Server Notifications</a><a href="http://www.kaltura.org/kaltura-terminology#kaltura-server-notifications" target="_blank"> </a>– Notifications that are sent from the Kaltura server to the publisher’s server using http post requests. The publisher is expected to host a notification handler script on his server, to which the Kaltura server will call providing information about the actions that occurred.

<p class="mce-procedure">
  To setup client and/or server notifications 
</p>

1.  Enter the Notification URL.
2.  Select the type of notifications from the displayed list. <img src="../../assets/92.img">

<p class="MsoBodyText" style="margin: 6pt 0in 0pt;">
  For more information about the various notifications and how to implement a notification handler script on your server, refer to: <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?page=notifications"><span style="color: #0fa2bb; font-family: arial, helvetica, sans-serif;">API Notifications.</span></a>
</p>

 

 

 

 

 

 