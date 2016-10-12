---
layout: page
title: "Specific End-User Permissions"
date: 2012-06-18 02:23:46
---

When any one of the Category Entitlement Options is set to Private, the respective access level is based on specific end-user permissions.  User permissions to a category and content associated with it are set through 4 permission levels: Member, Contributor, Moderator, and Manager.  The basic access permissions listed below are enforced by the Kaltura server. In MediaSpace the permission levels are used to control the availability of the relevant UI controls and user flows. (for example, Channel Settings, Channel’s moderation panel, Publish Module etc.)

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
          PermissionLevels
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
      <td valign="top" width="156">
        <p class="TableBodyText" style="text-align: left;">
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
      <td valign="top" width="156">
        <p class="TableBodyText" style="text-align: left;">
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
      <td valign="top" width="156">
        <p class="TableBodyText" style="text-align: left;">
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
      <td valign="top" width="156">
        <p class="TableBodyText" style="text-align: left;">
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

The settings of end-user permissions can be made from the KMC, in Bulk Process via a CSV formatted schema, or via Kaltura APIs.   In MediaSpace:  Channel Managers are able to set their channel’s groups members and may assign different permission levels to members of their group.

## Category’s End-User Permission Attributes

*   **Status – **indication to the state of the user permission set to the category. This attribute may be used for supporting different applicative flows.
*   **Active** – Access permission is active and enforced
*   **Pending **- Access permission is pending manager approval and is not yet active. (can be approved and activated)
*   **Deactivated **– Access permission is not active anymore. (can be activated again)

*   **Update Method** - indication on how a specific end-user permission is updated, this may be used  for supporting automatic processes for setting permissions to group channels based on organizational systems, while being able to set manual overrides to specific end-user permissions.
*   **Automatic -** user permission is updated via an automatic process (either via a CSV formatted schema or an API based integration). User permission level may be deleted or updated by the automatic process.
*   **Manual – **user permission is updated manually only and will not be deleted or updated by an automatic process.

## Additional End-User Permission Attributes

*   **Category Owner** – a category attribute, for setting one of the channel managers as the channel owner for any applicative need. A channel owner cannot be deleted by other channel managers.
*   **Default Permission Level **– a category attribute for setting a specific default permission level to the category, for supporting different applicative flows.
*   **Moderate Content** - a category attribute, for supporting the moderation of content prior to its publishing in the channel. (Moderation is configured through MediaSpace, by Channel managers or moderators.) 