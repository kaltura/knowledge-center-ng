---
layout: page
title: "Understanding the MediaSpace 5.0 Setup"
date: 2013-09-08 14:40:54
---

Kaltura MediaSpace features fine grained governance rules that grant specific permissions to content on the MediaSpace site. To explain your options, setup-related article describe the different site sections, roles, and permissions that you can configure for MediaSpace.

This articles focuses on setups that include user permissions, referred to as entitlement enabled.

To start learning about MediaSpace, refer to the<a href="http://knowledge.kaltura.com/node/888/attachment/field_media" target="_blank"> Kaltura MediaSpace User Manual</a>, which describes channels and user permissions in terms of site features.

<p class="mce-heading-2">
  Enabling User Permissions – Prerequisites
</p>

Contact your Kaltura Project/Account Manager to confirm that the following prerequisites are implemented:

*   Entitlement services are enabled and *enforce entitlement* is set to true in your account settings.
*   (Optional) The *Like* feature is enabled in your account settings.
*   A root category is set up for MediaSpace in the KMC (see <a href="http://knowledge.kaltura.com/node/616#TosetupaMediaSpacecategorytree" target="_blank">To set up a MediaSpace category tree in the KMC</a>)

Assigning user permissions usually is handled in bulk using a comma-separated value (CSV) file. To learn more about the End-User Entitlements CSV, refer to the <a href="http://knowledge.kaltura.com/node/466" target="_blank">End-User Entitlements CSV</a>.

<p class="mce-heading-2">
  Understanding Content Collections
</p>

Content collections in MediaSpace are defined as either catgories or channels. Your MediaSpace instance can include one or both.

<p class="mce-heading-3">
  Understanding Categories
</p>

Categories represent a centrally curated structure and hierarchy that is available from the MediaSpace navigation side panel. Media can be organized around specific topics in either a hierarchal or a flat navigation layout. When MediaSpace is used as a company/institution-wide media portal, categories usually are shared with the entire organization and also may be available to the public on the web.

Categories define the taxonomy and hierarchical structure of your MediaSpace site. You can access categories through the Navigation icon and browse your content according to the categories they are contained in. Each category opens up the list of sub-categories that are pre-configured by your account administrator. 

<p class="mce-heading-3">
  <a name="Understanding_Channels"></a>Understanding Channels
</p>

Channels are media collections that can be accessed by a subset of users (or all authenticated users). Channels can be created and managed by authorized **MediaSpace users** or can be provisioned centrally by a **KMC admin.**

<h3 class="mce-heading-4">
  Categories vs. Channels
</h3>

<table style="width: 624px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top">
        <p class="TableHeading">
           
        </p>
      </td>
      
      <td valign="top">
        <p class="TableHeading">
          <strong>Categories</strong>
        </p>
      </td>
      
      <td valign="top" width="241">
        <p class="TableHeading">
          <strong>Channels</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top">
        <p class="TableBodyText">
          What are they?
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p class="TableBodyText">
          Centrally curated hierarchical structure that defines the taxonomy of your site
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="241">
        <p class="TableBodyText">
          User generated collections that are personally managed
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p class="TableBodyText">
          Who can create?
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p class="TableBodyText">
          KMC user only
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="241">
        <p class="TableBodyText">
          Any MediaSpace user (configurable according to application roles)
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          Where do they appear?
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <p class="TableBodyText">
          Navigation panel
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="241">
        <ul>
          <li>
            My Channels
          </li>
          <li>
            All Channels
          </li>
          <li>
            Inside a category
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top">
        <p>
          Options
        </p>
      </td>
      
      <td style="text-align: left;" valign="top">
        <ul>
          <li>
            Entitlements
          </li>
          <li>
            Moderation
          </li>
          <li>
            Group Offline Synchronization
          </li>
          <li>
            Inherit members from parent category
          </li>
          <li>
            Import members from parent category
          </li>
          <li>
            Entitlements
          </li>
          <li>
            Moderation
          </li>
          <li>
            Group Offline Synchronization
          </li>
        </ul>
      </td>
      
      <td style="text-align: left;" valign="top" width="241">
        <p class="TableListBullet">
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

<h3 class="mce-heading-3">
  Understanding Roles and Permissions for Categories and Channels
</h3>

Entitlement permissions are used to assign permissions to categories or channels (for example, enabling a user to add content to a channel).

[Application Roles ][1]apply globally, while entitlement permissions are contextual. An example of contextual channel permissions is a user with *Manager* permissions for one channel and lower-level *Contributor* permissions for another channel.

 [1]: #application_roles

For a user to perform an action that a permission allows, the action must be allowed by the user's application role. Therefore, you must ensure that a user with a permission of *Contributor* or higher (see [Understanding Permissions][2]) is assigned a role of *privateUploader* or higher (see[ Application Roles][1]). Otherwise, the user is not able to upload content to MediaSpace despite the permission that entitles the user to contribute content.

 [2]: #understanding_entitlement

A Channel Manager can assign permissions in MediaSpace. The channel manager selects the kind of access that users have for the channel. If the [channel type][3] is restricted or private, the channel manager adds members and assigns member permissions. To learn more, refer to the [Kaltura MediaSpace User Manual.][4]

 [3]: file:///C:/Users/Debbie/Documents/Mediaspace/MediaSpace5/Setup%20Guide/Kaltura_MediaSpace_Setup_Guide_5.0.docx#_Understanding_Channel_Types
 [4]: http://knowledge.kaltura.com/node/918/attachment/field_media

<h4 class="mce-heading-4">
  <a name="understanding_privay_types"></a>Understanding Privacy Types
</h4>

MediaSpace supports the following privacy types for categories:

*   **Open: **All users are entitled to access the category (anonymous or authenticated, depending on the configuration of your site) but only specific users are entitled to contribute content
*   **Restricted**: All authenticated users are entitled to access the category, but only specific users are entitled to contribute content.
*   **Private:** Only specific users are entitled to access the channel and to contribute content.

MediaSpace supports the following privacy types for channels:

*   **Open: **All authenticated users are entitled to access the channel and contribute content.
*   **Restricted**: All authenticated users are entitled to access the channel, but only specific users are entitled to contribute content.
*   **Private:** Only specific users are entitled to access the channel and to contribute content.

Channel type definitions are displayed in MediaSpace under Channel Settings>Basic:  
<img src="{{site.url}}/assets/1170">
  


KMC entitlement definitions are displayed in the KMC under Content>Categories>Edit Category window>Entitlements tab:  
<img src="{{site.url}}/assets/1171">
  


<span>If modifications are made in the KMC that do not correspond to one of the channel types, MediaSpace behavior will follow the KMC definition, not the designated type.</span>

For more information, refer to <a href="http://knowledge.kaltura.com/node/637" target="_blank">How to set entitlement settings in the KMC.</a>

<h2 class="mce-heading-3">
  <a name="application_roles"></a>Understanding Application Roles
</h2>

MediaSpace application roles apply globally and include:

*   **anonymousRole** – Can browse your site anonymously until trying to access pages/actions that require login: My Media, My Playlists, and Add New.
*   **viewerRole**
*   Can browse public galleries
*   Is not authorized to upload new content
*   Does not have a My Media page

*   **privateOnlyRole**
*   Can upload content to My Media
*   Cannot publish to galleries
*   Can add media

*   **adminRole**
*   Can contribute content to all categories
*   Can upload content

*   **unmoderatedAdminRole** – Can upload content and bypass moderation (when moderation is enabled for an account)

MediaSpace application roles are backward compatible.

<h3 class="mce-heading-4">
  Modifying Application Role Names
</h3>

You can modify MediaSpace application role names to match your institutional terminology.

<p class="Procedure mce-procedure">
  To modify MediaSpace application role names
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Roles tab.
2.  Modify the label for one or more roles, and click **Save**.

<p class="FigureList">
   <img src="{{site.url}}/assets/1172">
</p>

<h3 class="mce-heading-4">
  Assigning Application Roles to Multiple Users in Bulk
</h3>

You can assign application roles to multiple users with a bulk action. You use an End Users CSV that includes an option to assign roles.

<p class="Procedure mce-procedure">
  To upload an End Users CSV
</p>

Do one of the following:

*   In the KMC, upload the End-Users CSV. Refer to the <a href="http://knowledge.kaltura.com/node/464" target="_blank">End-Users CSV - Usage and Schema Description.</a>
*   On the User Management panel of the Kaltura MediaSpace Administration Area:
*   Click **Submit CSV**.
*   Click **Choose File** to select the CSV file, and click **OK**.  
    <img src="{{site.url}}/assets/1173">

<h2 class="mce-heading-3">
  <a name="understanding_entitlement"></a>Understanding Entitlement Permissions
</h2>

While an application role applies to your **entire** MediaSpace site, some permissions may be category or channel-specific.

You set user permissions to a specific content collection by applying the following permission levels:

*   **Member**: Can access a channel or category but cannot add new content
*   **<a name="contributor"></a>Contributor**: Can add content to a channel or category
*   **Moderator**: In addition to the [Contributor ][5]permission, can moderate content.
*   **Manager**: In addition to the [Contributor][5] permission, can moderate content and access settings, including change metadata, edit members, change appearance, and delete channel. See [Understanding Roles and Permissions][6].

 [5]: #contributor
 [6]: #understanding_rolesandPermissions

In **channels**: All permission levels are relevant for channels.

In **galleries**: Only the Contributor and Member permission levels are relevant to galleries. Assigning a list of users as Members enables the users only to access a gallery. Assigning a list of users as Contributors enables the users to access a gallery and add media. (A user with the Admin application role also can add media.)

<h2 class="mce-heading-3">
  <a name="understanding_rolesandPermissions"></a>Understanding Roles and Permissions
</h2>

<p class="Sub-Heading">
  <strong>Who can upload content to MediaSpace?</strong>
</p>

A user with an application role of privateOnlyRole and higher (adminRole, unmoderatedAdminRole) can upload content to MediaSpace.

<p class="Sub-Heading">
  <strong>Who can view categories?</strong>
</p>

By default, categories can be accessed by all authorized users.

When Anonymous mode is enabled, open categories can also be viewed by anonymous users.

<p class="Procedure mce-procedure">
  To enable Anonymous mode
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.
2.  Under *allowAnonymous*, select **Yes** and click **Save**.  
    <img src="{{site.url}}/assets/1174">

<p class="FigureList">
   
</p>

<p class="Sub-Heading">
  <strong>Who can view or contribute content to a category/channel?</strong>
</p>

The following table describes the different scenarios depending on your KMS configuration and entitlements settings:

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top">
        <p class="TableHeading">
          <strong>Privacy Type</strong>
        </p>
      </td>
      
      <td valign="top">
        <p class="TableHeading">
          <strong>Action</strong>
        </p>
      </td>
      
      <td valign="top">
        <p class="TableHeading">
          <strong>Category</strong>
        </p>
      </td>
      
      <td valign="top">
        <p class="TableHeading">
          <strong>Channel</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td rowspan="2" valign="top">
        <p>
          Open
        </p>
        
        <p>
           
        </p>
      </td>
      
      <td valign="top">
        <p>
          View
        </p>
      </td>
      
      <td valign="top">
        <p>
          Anonymous +
        </p>
        
        <p>
          (if KMS is enabled for anonymous mode)
        </p>
      </td>
      
      <td valign="top">
        <p>
          Any Authenticated User
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          Contribute
        </p>
      </td>
      
      <td valign="top">
        <p>
          Contributor +
        </p>
        
        <p>
          adminRole +
        </p>
      </td>
      
      <td valign="top">
        <p>
          Any Authenticated User
        </p>
      </td>
    </tr>
    
    <tr>
      <td rowspan="2" valign="top">
        <p>
          Restricted
        </p>
        
        <p>
           
        </p>
      </td>
      
      <td valign="top">
        <p>
          View
        </p>
      </td>
      
      <td valign="top">
        <p>
          Any Authenticated User
        </p>
      </td>
      
      <td valign="top">
        <p>
          Any Authenticated User
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          Contribute
        </p>
      </td>
      
      <td valign="top">
        <p>
          Contributor +
        </p>
      </td>
      
      <td valign="top">
        <p>
          Contributor +
        </p>
      </td>
    </tr>
    
    <tr>
      <td rowspan="2" valign="top">
        <p>
          Private
        </p>
        
        <p>
           
        </p>
      </td>
      
      <td valign="top">
        <p>
          View
        </p>
      </td>
      
      <td valign="top">
        <p>
          Member +
        </p>
      </td>
      
      <td valign="top">
        <p>
          Member +
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top">
        <p>
          Contribute
        </p>
      </td>
      
      <td valign="top">
        <p>
          Contributor +
        </p>
      </td>
      
      <td valign="top">
        <p>
          Contributor +
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="Sub-Heading">
  <strong>How does a user become a manager?</strong>
</p>

A user can become a manager in the following ways:

*   The End-User Entitlements CSV includes fields for assigning a manager, contributors, and member permissions for each user and channel.
*   An authorized user who creates a channel is assigned as the channel owner with managerial rights. An owner can add additional managers, contributors, and members to a channel.

<p class="Sub-Heading">
  <strong>How does a user join a channel?</strong>
</p>

An end user cannot join a channel. The sys-admin or channel manager must authorize the user. An authenticated user can access channels that are[ Open][7] or [Restricted][7]**.**

 [7]: #understanding_privay_types

<p class="Sub-Heading">
  <strong>Who can create a channel?</strong>
</p>

A user with a role that is defined as a channel creator can create a channel. You define the user roles that can create a channel. See [Setting Permissions for Creating a MediaSpace Channel][8].

 [8]: file:///C:/Users/Debbie/Documents/Mediaspace/MediaSpace5/Setup%20Guide/Kaltura_MediaSpace_Setup_Guide_5.0.docx#_Setting_Permissions_for

<p class="Sub-Heading">
  <strong>Who can delete a channel?</strong>
</p>

The following are authorized to delete a channel:

*   From MediaSpace: The channel owner/manager
*   From the KMC: A KMC admin