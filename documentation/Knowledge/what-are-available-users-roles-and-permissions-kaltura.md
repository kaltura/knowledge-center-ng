---
layout: page
title: "What are the available Users, Roles and Permissions in Kaltura?"
date: 2012-10-22 13:26:24
---

## Roles and Permissions

Roles and permissions enable organizations to define a user's ability to perform actions based on the user's responsibilities. Only users with admin permissions can add users, create roles and define permissions.

A publisher uses the roles and permissions infrastructure to specify actions that a user is allowed to perform. User roles define permissions granted to the user for the different KMC functionalities.

### Adding a User

The following table lists the information that should be provided for adding a new KMC admin user. Please note that a limited number of users are allocated by default to each KMC account. If you reached the KMC users quota for your account and need to set additional users, please contact Kaltura with a <a href="http://site.kaltura.com/Request-Users.html" target="_blank">request for additional KMC admin users</a>.

<table style="width: 633px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Field</strong>
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
      <td valign="top" width="198">
        <p class="TableBodyText">
          <strong>Email address</strong> 
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          The user’s email address serves as a unique identifier of the user in the Kaltura system, as the user login username and as a recipient address for system-generated messages. Upon the creation of a new user account, a welcome email notification will be sent to this email address with a link for setting the initial password.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          <strong>First name, Last name</strong> 
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          User’s name
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          <strong>Publisher ID (Optional)</strong> 
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          A unique identifier that may be in use by the publisher in different systems. This will serve as the KMC user identifier as content contributor in all KMC-related locations. When a publisher ID is not provided, the user email address will be used as a default value.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          <strong>User Role</strong> 
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          Defines the set of permissions granted to the user for the different KMC functionalities. This role should be set according to the tasks that the user needs to work on and the functionalities that the user needs access to within the KMC. The different KMC user roles are set (by users who are granted with permission to do so) from the KMC Roles page (under the Administration tab).
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-procedure">
  To add a user
</p>

1.  Go to the Administration tab and select the Users tab.
2.  Click Add User, and fill in the details in the Add User window.  
    <img src="../../assets/755.img">
3.  Select a User Role from the drop-down menu. The choices are:  
    *   Publisher Administrator
    *   Manager
    *   Content Uploader
    *   Content Moderator
    *   Player Designer
4.  (Optional) Click Add Role to create a custom role. See <a href="{{site.url}}/documentation/Knowledge/how-create-custom-roles-kaltura-management-console.html" target="_blank">Creating Custom Roles.</a>
5.  [][1]Click Save.

 [1]: file:///C:/Users/Debbie/Documents/KMC/Gemini/Kaltura_Management_Console_(KMC)_User_Manual_gemini.docx#_Creating_Custom_Roles

When a user is created, an email will be sent to the specified email address containing a link to set the account password. 