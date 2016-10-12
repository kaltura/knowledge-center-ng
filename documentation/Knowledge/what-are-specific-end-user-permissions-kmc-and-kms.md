---
layout: page
title: "What are specific end-user permissions in the KMC and KMS"
date: 2012-09-16 14:56:11
---

<div class="WordSection1">
  <h3>
    Specific End-User Permissions
  </h3>
  
  <p>
    When any one of the Category Entitlement Options is set to Private, the respective access level is based on specific end-user permissions.  User permissions to a category and content associated with it are set through 4 permission levels: Member, Contributor, Moderator, and Manager.  The basic access permissions listed below are enforced by the Kaltura server. In MediaSpace the permission levels are used to control the availability of the relevant UI controls and user flows, for example, Channel Settings, Channel’s moderation panel, Publish Module and others.
  </p>
</div>

<table style="width: 618px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="156">
        <p class="TableHeading">
                        Permissions
        </p>
        
        <p class="TableHeading">
           
        </p>
        
        <p class="TableHeading">
          Permission Levels
        </p>
      </td>
      
      <td valign="top" width="84">
        <p class="TableHeading">
          View Content and Category
        </p>
      </td>
      
      <td valign="top" width="78">
        <p class="TableHeading">
          Add  Remove Content to Category
        </p>
        
        <p class="TableHeading">
           
        </p>
      </td>
      
      <td valign="top" width="90">
        <p class="TableHeading">
          Approve Content added to the category
        </p>
      </td>
      
      <td valign="top" width="96">
        <p class="TableHeading">
          Edit Category’s settings, privacy options and user permissions
        </p>
      </td>
      
      <td valign="top" width="114">
        <p class="TableHeading">
          Remove Category
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        <p class="TableBodyText">
          Member
        </p>
      </td>
      
      <td valign="top" width="84">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="78">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="90">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="96">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="114">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        <p class="TableBodyText">
          Contributor
        </p>
      </td>
      
      <td valign="top" width="84">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="78">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="90">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="96">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="114">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        <p class="TableBodyText">
          Moderator
        </p>
      </td>
      
      <td valign="top" width="84">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="78">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="90">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="96">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="114">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        <p class="TableBodyText">
          Manager
        </p>
      </td>
      
      <td valign="top" width="84">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="78">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="90">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="96">
        <p class="TableBodyText">
          X
        </p>
      </td>
      
      <td valign="top" width="114">
        <p class="TableBodyText">
          X
        </p>
      </td>
    </tr>
  </tbody>
</table>

The settings of end-user permissions can be made from the KMC, in Bulk Process via a CSV formatted schema, or via Kaltura APIs.  

**In MediaSpace:**  Channel Managers are able to set their channel’s groups members and may assign different permission levels to members of their group.

**Note:** the content owner has always full access and editing permissions to his own content. He is also able to remove his content from any category, regardless of the category’s settings.

**Tip: **the category end-user permissions may also be used by applications when the category is not set as private – for granting category specific applicative permissions to specific users.  **In MediaSpace:** users that is not set to with an Admin Application Role can still be granted with permission to publish content in specific galleries.  In this case the category’s contribution policy is set to **No Restriction **while ability to publish content in the respective gallery is granted by the application to all MediaSpace **Admin** users, but also to a few specific users that are set as contributors in the category.