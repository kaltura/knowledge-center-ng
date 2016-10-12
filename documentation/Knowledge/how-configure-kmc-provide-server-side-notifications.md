---
layout: page
title: "How to configure the KMC to provide server side notifications"
date: 2013-07-28 13:52:38
---

The following are the supported KMC notifications:

<table style="width: 888px;" border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          <strong>Event</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          Entry Add
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          An entry was successfully added the account.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          Entry Block
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          An entry was blocked by a moderator or admin user.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          Entry Delete
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          An entry was deleted.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          Entry Update
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          An entry was updated/modified.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          Entry Update Moderation
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          An entry’s moderation status was changed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          Entry Update Thumbnail
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          The default thumbnail of the entry was replaced.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          Entry Update Permissions
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          An entry’s privacy settings were changed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          User Add
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          A new user was added to the Kaltura account.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="280">
        <p>
          User Ban
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="608">
        <p>
          A user was banned from the Kaltura account.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-procedure">
   To enable the notifications
</p>

1.  In the KMC, select the Settings tab and then select the Integration Settings menu.  
    <img src="{{site.url}}/assets/1096">
2.  Toggle Yes to receive server notifications.
3.  Enter the Notification URL and Save Changes.

For more information about the various notifications and how to implement a notification handler script on your server, refer to: <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?page=notifications" target="_blank" title="API Documentation Notifications">http://www.kaltura.com/api_v3/testmeDoc/index.php?page=notifications</a>

 

 

 