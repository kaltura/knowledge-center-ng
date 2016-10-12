---
layout: page
title: "What  types of notifications are there in the KMC?"
date: 2011-12-26 15:59:12
---

While it is possible to easily query the Kaltura API periodically, Kaltura’s API Notifications utilize a “push” methodology where a code on your site will be called automatically by Kaltura whenever a certain actions occur like video upload or media status changes.

<div>
  <p>
    Kaltura provide two types of Notifications: 
  </p>
  
  <p>
    Kaltura Client Notifications – Notifications that are sent from the Kaltura widget (e.g. Kaltura Contribution Wizard) when a user performs an action like uploading a new video file. The notification will be called from the Kaltura widget directly to the publisher’s notification handler code hosted on the publisher’s server.
  </p>
  
  <p>
    Kaltura Server Notifications – Notifications that are sent from the Kaltura server to the publisher’s server using http post requests. The publisher is expected to host a notification handler script on their server, to which the Kaltura server will call providing information about the actions that occurred.
  </p>
  
  <p class="mce-procedure">
    To setup client and/or server notifications
  </p>
  
  <ol>
    <li>
      Enter the Notification URL.
    </li>
    <li>
      Select the type of notifications from the displayed list.<br /><img src="{{site.url}}/assets/143">
    </li>
  </ol>
  
  <p>
    For more information about the various notifications and how to implement a notification handler script on your server, refer to:h<a href="https://developer.kaltura.com/api-docs/#/eventNotificationTemplate" target="_blank">ttps://developer.kaltura.com/api-docs/#/eventNotificationTemplate</a>
  </p>
</div>