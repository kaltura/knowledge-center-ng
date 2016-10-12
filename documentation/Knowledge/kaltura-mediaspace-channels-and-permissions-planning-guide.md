---
layout: page
title: "Kaltura MediaSpace Channels and Permissions Planning Guide"
date: 2012-11-04 08:52:54
---

This article describes how to plan and implement Kaltura MediaSpace™ (KMS) channels and channel permissions based on data managed in organizational information systems.

<p class="mce-note-graphic">
  NOTE: You perform some steps in the Kaltura MediaSpace Administration Area and in the Kaltura Management Console (KMC).
</p>

<p class="mce-heading-2">
  Audience
</p>

This guide is intended for MediaSpace infrastructure support staff and developers who want to understand the options for creating and updating channels and channel permissions. To understand the document, you must be familiar with channel functionality in MediaSpace and related [terminology][1].

 [1]: #Terminology

This guide may be useful to:

*   **MediaSpace site administrators:** Responsible for supporting the organizational media portal
*   **IT and identity management experts:** Responsible for integrating organizational group membership information with entitlements to media channels in the media portal

<p class="mce-heading-1">
  Organizational Strategy for MediaSpace Channels and Permissions: Overview
</p>

When creating an organizational video portal with MediaSpace, MediaSpace channels and their respective user permissions can be set and maintained in different ways. When channels serve organizational units and groups, it may be possible to create the channels and maintain the channel permissions based on data managed in the organization’s information system (for example, identity management systems and group management systems).

This article addresses:

*   [How to plan the organizational operations and integrations related to managing channels and channel user permissions][2]
*   [How to create channels in bulk for groups managed in the organizational information systems][3]
*   [How to create and maintain channel user permissions based on groups managed in the organizational information systems][4]
*   [How to create and maintain the Add Members auto-complete list for adding channel members manually][5]

 [2]: #PlanningManageChannelsChannelPermissions
 [3]: #CreatingMediaSpaceChannels
 [4]: #CreatingUpdatingChannelPermissions
 [5]: #CreatingUpdatingAddMembersAutoCompleteList

These tasks can be accomplished in different ways since every organization has different needs and requirements, deploys and supports different information systems, and has different levels of IT capabilities and resources. The guidelines in this article can be adapted to fit each organization’s needs and capabilities. 

<p class="mce-heading-2">
  <a name="Terminology"></a>Terminology
</p>

**User ID** – A user’s unique identifier in your organization’s information systems. The same ID is used in Kaltura as a unique identifier of the user in a specific partner account.

**Group ID** – A unique identifier in your organizational information system representing an actual organizational unit or an ad-hoc security group. A user can be a member of multiple groups and may hold a different organizational role in each group. The organizational role of a user within a unit/group may or may not be represented within the organization information system.

**MediaSpace Channel** – An open/private/restricted channel in MediaSpace that a specific group of users (channel members) is able to access. The list of people with permissions to access the group channel may derive from user membership in a specific organizational group or may be defined manually by the channel manager with no relation to organizational structure and units.

<p class="mce-note-graphic">
  NOTE: <strong>MediaSpace Galleries</strong> also may be assigned specific entitlements and user permissions. When needed, these can be derived from the information system, similar to <strong>MediaSpace Channels</strong>.
</p>

**Kaltura User** – A Kaltura backend object that holds information about a specific user and is identified by the **User ID**. Kaltura supports the management of different user attributes. The **user ID** is a mandatory attribute, the user’s first name, last name, and screen name (by default, the user’s full name) are required to enable convenient end-user management in MediaSpace and in the KMC. **Kaltura User** objects are automatically created in Kaltura for different scenarios. For user management purposes, **Kaltura User** objects also may be created manually from the KMC or using bulk services. The **Kaltura User** object is used for managing both KMC admins and application end‑users. Only KMC administrators have a special attribute granting access to the KMC account.

**Kaltura Category** – A Kaltura backend object for managing media collections and the end‑user entitlements to access and manage these media collections in MediaSpace. This backend entity manages both **MediaSpace Channels** and **Galleries**.

**Kaltura Category ID** – A Kaltura internal unique identifier of a single **Kaltura Category** Object.

**Kaltura Category Reference ID** – A **Kaltura Category** attribute designed to hold and connect the category to an external identifier such as the **Group ID**. Uniqueness of the Category reference ID is not enforced by Kaltura.

**Kaltura’s End-User Entitlements **(Channel Permissions) – A permission level that enables a specific end‑user to access, contribute to, or manage a specific channel. In the Kaltura backend, end‑user entitlements are managed in Kaltura’s categoryUser object, which manages the relationship between a specific end‑user and a specific category. 

<p class="mce-heading-1">
  <a name="PlanningManageChannelsChannelPermissions"></a>Planning How to Manage Channels and Channel Permissions
</p>

<p class="mce-heading-2">
  <a name="UnderstandingPlanningConsiderations"></a>Understanding Planning Considerations
</p>

Consider the following questions when you plan the organizational process for managing MediaSpace channels and channel memberships.

<span class="mce-sub-heading">What types of channels will be in your video portal?</span>

*   Education Examples
*   Course channels  
    For media-rich courses, faculty can create a course channel in MediaSpace in a simple, feature-rich environment.
*   School/Department channels  
    Each school/department has its own managed channel that shows content that either is accessible only to the school/department or is open to all.
*   Workgroup channels  
    Not bound by a strict learning management system (LMS) structure, faculty and students can create cross-course ad hoc groups for research, projects, and more.
*   Portfolio Channel  
    Allow faculty and any authorized users to create their own portfolio channel, with recordings of public speaking, awards and events, lectures, video work, and more. Typically, the channels are public under the university roof, but also can be restricted to a specific set of users within the organization.

*   Enterprise Examples
*   Department channel  
    Each department head manages the department channel that shows content that either is accessible only to the department or is accessible to all employees.
*   Community channels  
    All employees are empowered to create their own channels, and can either invite specific co‑workers to join or can enable open access. For each channel, the creator can control who can contribute and whether moderation is required.

<p class="mce-sub-heading">
  For which units in your organization do you want to create a MediaSpace channel?
</p>

Examples:

*   For all groups of a specific type (for example, all departments or all schools)
*   For only a few groups within the organization (for example, a few departments or media‑related courses only)
*   For a few communities/work groups within the organization
*   Every user will be able to open a channel.

<p class="mce-sub-heading">
  What should be the typical/default privacy level required for channels of each type?
</p>

*   Open  
    All users in the organization are entitled to access the channel and contribute content.
*   Restricted  
    All users in the organization are entitled to access the channel, but only specific users are entitled to contribute content.
*   Private  
    Only specific users in the organization are entitled to access the channel and contribute content.

<p class="mce-sub-heading">
  What changes in your organization should require an update to channel user permissions?
</p>

Examples:

*   Someone joined/left an organizational group.
*   Someone's role in organizational groups changed.
*   Someone joined or left the organization.

<p class="mce-sub-heading">
  What is the frequency and volume of the relevant organizational changes?
</p>

*   How often do the changes happen?
*   How many users/groups are affected?

<p class="mce-sub-heading">
  What is the acceptable lag time for channel permissions to be updated in MediaSpace following an organizational change?
</p>

How promptly must organizational changes be reflected within MediaSpace channels and channel permissions? For example, immediately, within a few hours, on the next day.

<p class="mce-sub-heading">
  How available is your organizational IT Department?
</p>

Do you have resources for developing and maintaining an automated update of channel permissions based on changes in your organizational information systems?

<p class="mce-heading-2">
  Understanding Channel Management Types
</p>

Based on your evaluation of the [planning consideration questions][6], decide on the best way to manage channels and channel memberships in your organization. You can select one of the following options or combine options to manage different types of channels.

 [6]: #UnderstandingPlanningConsiderations

<table style="width: 1026px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td rowspan="2" valign="top" width="90">
        <p>
          <strong>Channel Management Type</strong>
        </p>
      </td>
      
      <td rowspan="2" valign="top" width="78">
        <p>
          <strong>Integration Effort </strong>
        </p>
      </td>
      
      <td colspan="4" width="858">
        <p align="center">
          <strong>Channel Management</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
           
        </p>
      </td>
      
      <td valign="top" width="288">
        <p align="center">
          <span style="color: #ff6600;"><strong>Channel Creation </strong></span>
        </p>
      </td>
      
      <td valign="top" width="276">
        <p align="center">
          <span style="color: #ff6600;"><strong>Channel Permissions — Initial Setup</strong></span>
        </p>
      </td>
      
      <td valign="top" width="240">
        <p align="center">
          <span style="color: #ff6600;"><strong>Channel Permissions — Ongoing Updates</strong></span>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td rowspan="3" valign="top" width="90">
        <p>
          <span style="color: #ff6600;"><strong>Self-Created</strong></span>
        </p>
        
        <p>
           
        </p>
      </td>
      
      <td rowspan="3" valign="top" width="78">
        <p>
          <strong>Very Low</strong>
        </p>
        
        <p align="center">
           
        </p>
      </td>
      
      <td valign="top" width="54">
        <p>
          <strong>Who?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          Organizational unit/group managers or anyone authorized by the organization to create a MediaSpace channel
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          Channel Managers
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          Channel Managers
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
          <strong>When?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          Whenever a new channel is needed
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          Upon channel creation
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          When needed
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
          <strong>How?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          On the MediaSpace site
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          On the MediaSpace site
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          On the MediaSpace site
        </p>
      </td>
    </tr>
    
    <tr>
      <td rowspan="3" valign="top" width="90">
        <p>
          <span style="color: #ff6600;"><strong>Centrally Assigned </strong></span>
        </p>
      </td>
      
      <td rowspan="3" valign="top" width="78">
        <p>
          <strong>Low–Medium</strong>
        </p>
      </td>
      
      <td valign="top" width="54">
        <p>
          <strong>Who?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          Video portal administrators, with or without IT department assistance
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          Channel Managers
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          Channel Managers
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
          <strong>When?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          Upon initial set up of video portal channels, upon major organizational changes, when a new channel is needed
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          Upon channel creation
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          When needed
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
          <strong>How?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          <a href="#CreatingChannelsCentrallybyAdministrators">In the KMC: manual or bulk CSV-based creation</a>
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          On the MediaSpace site
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          On the MediaSpace site
        </p>
      </td>
    </tr>
    
    <tr>
      <td rowspan="3" valign="top" width="90">
        <p>
          <span style="color: #ff6600;"><strong>Centrally Prepared</strong></span>
        </p>
      </td>
      
      <td rowspan="3" valign="top" width="78">
        <p>
          <strong>Medium </strong>
        </p>
      </td>
      
      <td valign="top" width="54">
        <p>
          <strong>Who?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          Video portal administrators, with or without IT department assistance
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          Video portal administrators, with or without IT department assistance
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          Organizational unit managers and/or their assistants.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
          <strong>When?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          Upon initial set up of video portal channels, upon major organizational changes, when a new channel is needed
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          Upon channel creation
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          When needed
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
          <strong>How?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          <a href="#CreatingChannelsCentrallybyAdministrators">In the KMC: manual or bulk CSV-based creation</a>
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          <a href="#SettingUpChannelPermissionsCentrally">In the KMC: manual or bulk CSV-based setup</a>
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          On the MediaSpace Site
        </p>
      </td>
    </tr>
    
    <tr>
      <td rowspan="3" valign="top" width="90">
        <p>
          <span style="color: #ff6600;"><strong>Automatically Maintained</strong></span>
        </p>
      </td>
      
      <td rowspan="3" valign="top" width="78">
        <p>
          <strong>High</strong>
        </p>
      </td>
      
      <td valign="top" width="54">
        <p>
          <strong>Who?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          Video portal administrators, with or without IT department assistance
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          Video portal administrators, with or without IT department assistance
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          Scheduled automated update process or based on information system’s triggers
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
          <strong>When?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          Upon initial set up of video portal channels, upon major organizational changes, when a new channel is needed
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          Upon initial set up of video portal channels, upon major organizational changes, when a new channel is needed
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          Scheduled as needed or triggered in real-time upon group membership modifications
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="54">
        <p>
          <strong>How?</strong>
        </p>
      </td>
      
      <td valign="top" width="288">
        <p>
          <a href="#CreatingChannelsCentrallybyAdministrators">In the KMC: manual or bulk CSV-based creation</a>
        </p>
      </td>
      
      <td valign="top" width="276">
        <p>
          <a href="#SettingUpChannelPermissionsCentrally">In the KMC: manual or bulk CSV-based setup</a>
        </p>
      </td>
      
      <td valign="top" width="240">
        <p>
          See <a href="#AutomaticallyUpdatingChannelPermissions">Automatically Updating Channel Permissions</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-1">
  <a name="CreatingMediaSpaceChannels"></a>Creating MediaSpace Channels
</p>

<p class="mce-heading-2">
  Creating Channels in MediaSpace – by Users
</p>

Organizational group managers or anyone authorized by the organization to create channels in MediaSpace can create a channel on the MediaSpace site and manually select the channel’s settings and member permissions.

Users who create channels in MediaSpace require a MediaSpace application role that enables channel creation. To learn more, refer to Setting Permissions for Creating a MediaSpace Channel in the [Kaltura MediaSpace Setup Guide][7].

 [7]: http://knowledge.kaltura.com/node/559/attachment/field_media

To learn more about channel creation and management, refer to Creating and Managing a Channel in the [Kaltura MediaSpace User Manual][8].

 [8]: http://knowledge.kaltura.com/node/560/attachment/field_media

<p class="mce-heading-2">
  <a name="CreatingChannelsCentrallybyAdministrators"></a>Creating Channels Centrally – by Administrators
</p>

Video portal administrators can create channels, with or without the assistance of the organizational IT department.

<p class="mce-heading-3">
  Creating MediaSpace Channels in Bulk
</p>

You may need to create channels in bulk, either at the initial setup or upon major organizational changes that trigger the creation of numerous channels. We recommend creating channels in bulk using Kaltura’s bulk services with [Kaltura’s Categories CSV][9].

 [9]: http://knowledge.kaltura.com/node/465

<p class="mce-procedure">
  <a name="TocreateMediaSpaceChannelsinbulk"></a>To create MediaSpace Channels in bulk
</p>

1.  Prepare the initial list of groups that will use the new MediaSpace Channels. You can prepare the list manually or export the list from the organizational information system. Include at least the following information from your organizational information system:  
    - For groups managed in your organizational information system, include the **Group ID** of each organizational group/unit.  
    - If a group manager plans to create the channel members list and permissions in MediaSpace, specify the **User ID** of the group manager. This sets the group manager as the channel owner and enables the group manager immediate access to the group channel settings in MediaSpace.  
    - If a friendly group name is available in your information system, you can export the friendly group name to use as the channel name.
2.  Edit the basic group list in a spreadsheet editor or programmatically to comply with [Kaltura’s Categories CSV format][9]. Insert the following information to create channels in MediaSpace with relevant channel settings (see example below).  
    - Enter the relative category path to your MediaSpace Channels category.  
    - When relevant, set each **Group ID** as the **reference ID** of its respective category. This enables you to refer to the category based on the **Group ID**,when needed (for example, for automated channel membership creation).  
    -  Enter the channel name. You can use the group name exported from your information system, the **Group ID**, or any name you select. The name will be displayed as the channel name in MediaSpace.  
    - For the category owner, enter the **User ID** of the user who will initially manage the channel (for example, the **User ID** of the unit/group manager).  
    - Enter the category entitlement settings according to the type of channel (open/restricted/private).  
    - You can add additional information, such as channel description, tags, and any custom channel classification or topic managed by the category’s custom data. The channel owner also can manually enter this information in MediaSpace after the channel is created.  
    - Insert the Categories CSV headers for fields that are populated in your CSV.  
    <img src="{{site.url}}/assets/791">
    *Categories CSV for creating different types of MediaSpace Channels*  
    **NOTE:** While there is no limit on the number of lines in the CSV, the processing time of each CSV is affected by the number of lines in the CSV. Therefore, we recommend splitting the CSV into manageable chunks for convenient editing, processing, and tracking. 
3.  On the KMC Upload tab, upload the Categories CSV.  
    Bulk processing in Kaltura is handled in an asynchronous batch process. Track the completion status of the bulk job in the KMC on the Bulk Upload Log page or using email notifications set by Kaltura for your account.

<p class="mce-heading-3">
  Creating MediaSpace Channels Individually
</p>

Occasionally you may need to create a single channel or a few channels. We recommend creating and configuring individual channels in the KMC Edit Category window.

To learn more, refer to Managing Categories in the [Kaltura Management Console (KMC) User Manual][10] and Understanding Channel Types in the [Kaltura MediaSpace Setup Guide][7].

 [10]: http://knowledge.kaltura.com/node/561/attachment/field_media

<p class="mce-heading-1">
  <a name="CreatingUpdatingChannelPermissions"></a>Creating and Updating Channel Permissions
</p>

<p class="mce-heading-2">
  Assigning Channel Permissions
</p>

<p class="mce-heading-3">
  Setting Up Channel Members and Permissions Manually in MediaSpace
</p>

Channel managers can manually add members to their channels, assign and update member permission levels, and remove members. A channel manager manages channel members and permissions on the Channel Settings page in MediaSpace.

To learn more, refer to Creating and Managing a Channel in the [Kaltura MediaSpace User Manual][8].

<p class="mce-heading-3">
  <a name="SettingUpChannelPermissionsCentrally"></a>Setting Up Channel Permissions Centrally
</p>

Channel permissions can be initially assigned by the video portal administrator in the KMC for channels related to organizational units. The organizational IT department usually needs to assist setting up group channel permissions by exporting the organizational group membership data from the organization’s information systems.

<p class="mce-heading-4">
  Setting Up Channel Permission in Bulk
</p>

Channel permissions should be assigned in bulk for a large number of new channels, either at the initial setup or upon major organizational changes that trigger the creation of numerous channels. We recommend assigning channel permissions in bulk using Kaltura’s bulk services with [Kaltura’s End-User Entitlements CSV][11].

 [11]: http://knowledge.kaltura.com/node/466

<p class="mce-note-graphic">
  NOTE: You must assign channel permissions in bulk after creatingthe channels. Assigning channel permissions in bulk requires first setting the <strong>Group ID</strong> value as the channel <strong>Category’s Reference ID</strong>. See the procedure <a href="#TocreateMediaSpaceChannelsinbulk">To create MediaSpace Channels in bulk</a>.
</p>

<p class="mce-procedure">
  To create memberships and permissions in bulk for new channels
</p>

1.  For all new channels for which you are assigning permissions, prepare an initial list of organizational user/group membership pairs with the required channel permission levels.  
    <img src="{{site.url}}/assets/792">
    *Initial list of group memberships*  
    - When you export group memberships from your organizational information system for the list, you may need to separately query all group managers, all group members, and so on. This is to ensure that different channel permission levels are assigned according to the user’s organization role within a specific group.  
    - If you want the channel to be self-managed in MediaSpace and did not assign a channel owner when creating the channel, assign a Manager permission level to at least one user.
2.  Edit the basic group membership list in a spreadsheet editor or programmatically to comply with [Kaltura’s End-User Entitlements CSV format][11]. Specifically, insert the CSV field headers, specify the CSV add action (action =1), and specify the numeric value of each permission level according to Kaltura’s specifications.  
    You may assign permissions for multiple channels within one CSV file.  
    <img src="{{site.url}}/assets/793">
    *Channel memberships formatted in Kaltura's End-User Entitlements CSV*  
    **NOTE:** While there is no limit on the number of lines in the CSV, the processing time of each CSV is affected by the number of lines in the CSV. Therefore, we recommend splitting the CSV into manageable chunks for convenient editing, processing, and tracking.
3.  On the KMC Upload tab, upload the End-User Entitlements CSV.  
    Bulk processing in Kaltura is handled in an asynchronous batch process. Track the completion status of the bulk job in the KMC on the Bulk Upload Log page or using email notifications set by Kaltura for your account.

<p class="mce-heading-4">
  Setting Up Channel Permissions Individually
</p>

Occasionally the video portal administrator may need to assign individual channel membership and permissions. We recommend assigning individual channel membership and permissions in the KMC Edit Category window.

To learn more, refer to Managing Categories in the [Kaltura Management Console (KMC) User Manual][10].

<p class="mce-heading-2">
  <a name="AutomaticallyUpdatingChannelPermissions"></a>Automatically Updating Channel Permissions
</p>

Following the initial setup of channels and channel permissions, you can automate the updating of channel permissions to reflect relevant changes in your organization (user joined/left an organizational group; User joined/left the organization, and so on).

Automated updating of MediaSpace channel permissions based on changes made in your organizational information system is very useful for big organizations. Automatic channel permission updates help when organizational group memberships are updated frequently and when you want to eliminate the need for each channel manager to manually manage permissions in MediaSpace.

Automating ongoing updates of channel permissions requires the expertise and full involvement of the organizational IT department and requires your organizational information system to support one of the following modes:

*   [**Automated periodic export of changes**  
    ][12]Audit, query, report, or export changes in your information systems for a specific time period (for example, day or week) to prepare and submit a scheduled bulk update using [Kaltura’s End-User Entitlements CSV][11] or Kaltura's API.

 [12]: #Todevelopautomatedprocessperiodicallyupdatingchannelmembershippermissions

*   [**Real-time triggers**  
    ][13]Trigger real-time update calls from your information system or from related applications to Kaltura using Kaltura’s API when every relevant change occurs in your system.

 [13]: #Todeveloptriggerprocessupdatingchannelmembershippermissions

<p class="mce-note-graphic">
  NOTE: The following procedures provide general guidelines and rely on your IT experts and/or developers to tailor the automation process based on the capabilities of your organizational information system and related applications. Kaltura’s professional services team may provide assistance in designing and developing the automated updating process and will provide all information required for utilizing Kaltura’s bulk services and API for automation.
</p>

<p class="mce-procedure">
  <a name="Todevelopautomatedprocessperiodicallyupdatingchannelmembershippermissions"></a>To develop an automated process for periodically updating channel membership permissions
</p>

1.  Define how frequently to schedule the update.  
    Decide how often you need to update the channel membership permissions, and schedule the frequency of the update process accordingly.
2.  Develop an automated process that includes the following steps and logic:
<ol style="list-style-type: lower-alpha;">
  <li>
    List the required channel permissions modifications.<br />Based on your information system audit, querying, and export capabilities, retrieve the list of users who — within a specific time range — joined or left groups within your organization, or changed their organizational role in specific groups.<br />You may rely on direct audit information available in your information system or develop a query and sync process that implements the following logic:
  </li>
  <ol style="list-style-type: lower-roman;">
    <li>
      List every user whose record was created/modified/deleted within a specific time range (for example, from the last update until now).
    </li>
    <li>
      For each user in this list:
    </li>
    <ol style="list-style-type: upper-alpha;">
      <li>
        Query your information system to get the list of groups that the user currently belongs to (possibly with the specific role in each group)
      </li>
      <li>
        Query Kaltura for the list of channels that the user currently is a member of.
      </li>
    </ol>
    
    <li>
      Compare the two lists (based on the Group ID and Category reference ID) and implement the logic for determining the channels for which the specific user’s permission should be created, updated, or deleted. Format this as an initial list of channel permission actions (add, update, delete).<br /><br />This logic assumes that changes in user group memberships affect the modification date of the user’s record. When changes in user group memberships affect the modification date of the group’s record, implement an equivalent logic that is oriented toward synchronizing the list of channel members instead of synchronizing the list of channels that the user is a member of.<br /><br /><strong>NOTES:</strong><br />- An attempt to create/update/delete user permission in a channel’s category that does not exist yet in Kaltura will fail. You may extend the logic for automatic creation of new channels when the first relevant group membership is set in Kaltura. Note that such an addition may cause uncontrolled channel creation and may result in a large number of empty channels, which is not recommended when channel browsing is enabled in your site.<br />- An attempt to create a user permission in a channel’s category when the user record is not yet in Kaltura will cause the automatic creation of the user’s record in Kaltura with the specified User ID.<br />- The category’s reference ID is a standard way to map a single organizational group to a single channel. To automatically assign permissions for a single channel to users of multiple organizational groups, you may tailor a synchronization logic that relies on a category custom data schema that enables multiple Group IDs to be assigned specific permission levels to a single category. Contact Kaltura professional services for assistance if necessary.
    </li>
  </ol>
  
  <li>
    Prepare the End-User Entitlements CSV.<br />Transform the initial list of channel permission actions (add, update, delete) to comply with <a href="http://knowledge.kaltura.com/node/466">Kaltura’s End-User Entitlements CSV format</a>. Insert the CSV field headers and specify the permission levels and actions.<br />To add a user permission, use the CSV add action (action = 1).<br />To update a user permission or create a new one as a fallback in case the permission you attempt to update was not yet set, use the CSV add or update action (action = 6).<br />To delete a user permission, use the CSV delete action (action = 3).<br /><img src="{{site.url}}/assets/794">
  </li>
  <li>
    Submit the End-User Entitlements CSV.<br />When the End-User Entitlements CSV is available, submit it to Kaltura using the Kaltura API: Call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=categoryUser&action=addfrombulkupload">categoryUser.addfrombulkupload</a> API action.<br />Bulk processing in Kaltura is handled in an asynchronous batch process. Track the completion status of the bulk job in the KMC on the Bulk Upload Log page or using email notifications set by Kaltura for your account.
  </li>
</ol>

<p class="mce-procedure">
  <a name="Todeveloptriggerprocessupdatingchannelmembershippermissions"></a>To develop a trigger-based process for updating channel membership permissions
</p>

<p class="mce-note-graphic">
  NOTE: For changes in your information system to trigger real-time updates to channel membership permissions, your information system or related applications must support real-time triggering of notifications to other systems.
</p>

Develop the following:

1.  Trigger an Add Channel Permission call  
    Create a script that implements the following Kaltura API requests when a new group membership is created for a user in your information system (a user joins an organizational group).
<ol style="list-style-type: lower-alpha;">
  <li>
    Call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=category&action=list">category.list</a> API action to retrieve the channel’s category object. In the list filter, include the <strong>Group ID</strong> set as the <strong>Category’s Reference ID</strong> attribute.
  </li>
  <li>
    When the category is found, call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=categoryEntry&action=add">categoryUser.add</a> API action to create a new permission for the user in the specific channel with the proper permission level.
  </li>
</ol>

2.  Trigger a Delete Channel Membership call  
    Create a script that implements the following Kaltura API requests when an existing group membership is removed from a user in your information system (a user leaves an organizational group).
<ol style="list-style-type: lower-alpha;">
  <li>
    Call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=category&action=list">category.list</a> API action to retrieve the channel’s category object. In the list filter, include the <strong>Group ID</strong> set as the <strong>Category’s Reference ID</strong> attribute.
  </li>
  <li>
    When the category is found, call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=categoryEntry&action=delete">categoryUser.delete</a> API action to delete the user's existing channel membership.
  </li>
</ol>

3.  Trigger an Update Channel Membership call  
    Create a script that implements the following Kaltura API requests when an existing group membership type in your information system is changed in a way that impacts the relevant channel permission level (for example, a user's role within a group changes and the user should be set as a channel manager).
<ol style="list-style-type: lower-alpha;">
  <li>
    Call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=category&action=list">category.list</a> API action to retrieve the channel’s category object. In the list filter, include the <strong>Group ID</strong> set as the <strong>Category’s Reference ID</strong> attribute.
  </li>
  <li>
    When the category is found, call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=categoryUser&action=update">categoryUser.update</a> API action to adjust the user’s permission level in the group’s channel.
  </li>
</ol>

<p class="mce-note-graphic">
  NOTE: In the previous steps you may skip step A, which lists the category with the specified Reference ID, if you store the <strong>Kaltura Category ID</strong> in your information system’s group record.
</p>

<p class="mce-heading-3">
  Enabling Manual Overrides of Automatically Updated Channel Permissions
</p>

When channel permissions are assigned and automatically updated based on organizational group memberships, you may want to allow channel managers and video portal administrators the flexibility to assign different channel permissions in specific cases.

Examples:

*   In a company departmental channel, you want one of the employees to be the channel *moderator*, while all employees in the department are assigned only the channel *member* permission level.
*   In a course channel, you want to assign contribution privileges to one of the students, while all other students are assigned only the channel *member* permission.
*   In a company business unit channel, you want the unit’s administrative assistant to be the channel manager but there is no attribute within your organizational information system that you can use to assign this permission level automatically.

The Update Method attribute of channel permissions enables manual overrides to a channel’s user permission levels that will not be updated by the automatic update process. You can set the Update Method as *automatic* or *manual*.

Call the [categoryUser.update][14] Kaltura API action to enable a controlled override of permission levels that were set or updated manually in MediaSpace or the KMC. Use the *override* parameter to indicate whether to override a permission level that is set manually.

 [14]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=categoryUser&action=update

Using this API action enables you to implement a logic that prevents manually created or updated channel permission levels from being updated by automated processes or that allows the channel permission levels to be updated only in specific cases.

By default, end-user permissions created in bulk using a CSV use the *automatic update* method and will not override manual updates to channel permission levels.

Any channel member added in MediaSpace is set to the *manual update* method. In addition, any permission level change to existing members by a MediaSpace channel manager sets the channel permission to *manual update*.

You can view and fully control the permission level update method in the KMC Category Edit window.

<p class="mce-heading-2">
  Deleting MediaSpace Channels
</p>

MediaSpace Channels can be deleted:

*   By the channel owner in MediaSpace
*   By the video portal administrators in the KMC
*   With a bulk service, using [Kaltura’s Categories CSV][9]
*   With a script that calls the [category.delete][15] Kaltura API action

 [15]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=category&action=delete

When a category is deleted, the media entries in the category (including sub-category entries) are not deleted. The media entries lose the association with the deleted category, including any privacy setting defined in the deleted category.

To plan channel deletions and to ensure that access to content in deleted channels is controlled according to your organizational needs, note that:

1.  When a channel is deleted in MediaSpace, a media entry in the channel that is not associated with any other channel or gallery becomes private (associated with the MediaSpace private category).
2.  When categories are deleted manually in the KMC or using the Categories CSV, the media entries in the category automatically are associated with the deleted category's parent category. Before deleting a category, you may want to associate the category's entries with new categories using the entry bulk actions available in the KMC (Edit Categories, Add to New Category).
3.  When a category is deleted using the [category.delete][15] Kaltura API action, you can control whether the deleted category's media entries automatically are assigned to the parent category. In addition, you can programmatically associate the entries with other categories before the category is deleted, according to the logic you want to implement.

<p class="mce-heading-2">
  Deactivating Channel Memberships
</p>

Deactivating MediaSpace channel memberships may be useful when you want to block channel members from accessing a channel’s content while retaining the option to reactivate their memberships later.

<p class="mce-procedure-text mce-procedure">
  To deactivate and reactivate channel memberships
</p>

You can do either of the following:

*   In the KMC Edit Category window, apply the deactivate/activate action to selected channel members.
*   Prepare a [Kaltura End-User Entitlements CSV][11]:
*   To deactivate a user's channel membership, use the CSV update action (action = 2) with status = 3.
*   To activate a user's channel membership, use the CSV update action (action = 2) with status = 1.  
    <img src="{{site.url}}/assets/795">
    *Deactivating channel's members (status = 3)*  
    <img src="{{site.url}}/assets/796">
    *Reactivating channel's members (status=1)*

<p class="mce-heading-1">
  <a name="CreatingUpdatingAddMembersAutoCompleteList"></a>Creating and Updating the Add Members Auto-Complete List
</p>

A channel manager can add end-users as members of a channel in MediaSpace on the Members tab of the Channel Settings page. The channel manager can conveniently select members using an auto-complete feature. In the Add Member window under Enter user name, the channel manager starts typing a user name or user ID. Suggested user names are displayed after three characters are entered, and the channel manager can select a member to add. To learn more about editing channel members, refer to Editing Channel Users in the [Kaltura MediaSpace User Manual][8].

By default, the auto-complete list includes only users who already are listed in Kaltura.

When authorizing access to MediaSpace through integration with SSO/LDAP, a user's record in Kaltura is not necessarily created prior to the user’s first login to MediaSpace.

To populate the auto-complete list with all users who potentially can use MediaSpace (and not only those who already are logged-in), you may pre-provision the user records in Kaltura.

** The Workflow for Creating and Updating the Add Members Auto-Complete List:**

1.  [Setting Up the Initial Add Members Auto-Complete List][16]
2.  [Updating the Add Members Auto-Complete List][17]

 [16]: #SettingUpInitialAddMembersAutoCompleteList
 [17]: #UpdatingAddMembersAutoCompleteList

<p class="mce-note-graphic">
  NOTE: When you use Kaltura to authorize access to MediaSpace, it is assumed that all user accounts are pre-provisioned in Kaltura. Therefore, the auto-complete list includes all potential MediaSpace users.
</p>

<p class="mce-heading-2">
  <a name="SettingUpInitialAddMembersAutoCompleteList"></a>Setting Up the Initial Add Members Auto-Complete List
</p>

<span class="mce-procedure">To populate the Add Members auto-complete user list in bulk</span>

1.  Prepare the initial list of users in your organization who will be eligible to access MediaSpace. You can prepare the list manually or export the list from your organizational information system. Include at least the following information:  
    - User ID  
    - User’s first name  
    - User's last name
2.  Edit the initial users list in a spreadsheet editor or programmatically to comply with [Kaltura’s end-users CSV format][18].
<ol style="list-style-type: lower-alpha;">
  <li>
    Use the CSV <em>add</em> or <em>update</em> action (action = 6) to update any existing user record that includes only the user ID with the user’s first and last names, or to create new records.
  </li>
  <li>
    (Optional) Combine the first and last names into an additional field called <em>screenName</em>, which also is used in the KMC and applications.<br /><img src="{{site.url}}/assets/797">
  </li>
</ol>

3.  On the KMC Upload tab upload the End-Users CSV.  
    Bulk processing in Kaltura is handled in an asynchronous batch process. Track the completion status of the bulk job in the KMC on the Bulk Upload Log page or using email notifications set by Kaltura for your account.

 [18]: http://knowledge.kaltura.com/node/464

<p class="mce-heading-2">
  <a name="UpdatingAddMembersAutoCompleteList"></a>Updating the Add Members Auto-Complete List
</p>

You may need to update the Add Members auto-complete list when users join or leave your organization.

To add or delete users, you can:

*   Manually update the users list and submit the End-Users CSV.
*   [Develop an automated process for periodically updating the Add Members auto-complete users list][19].
*   [Develop a trigger-based process for updating the Add Members auto-complete user list.][20]

 [19]: #TodevelopautomatedprocessperiodicallyupdatingAddMembersautocompleteuserslist
 [20]: #TodeveloptriggerbasedprocessupdatingAddMembersautocompleteuserslist

<p class="mce-note-graphic">
  NOTE: Deleted users are also removed from all channels in which they are members. Content ownership and analytics information of the deleted user are not deleted.
</p>

<p class="mce-note-graphic">
  NOTE: Since user records are shared by all Kaltura applications running on the same account, we recommend that you delete records only of users who left the organization.
</p>

<p class="mce-note-graphic">
  NOTE: Integrating the Add Members auto-complete feature directly with your information system to enable a real-time search of users may be possible as custom work. The integration requires real-time access and search capabilities based on user ID and user name. To learn more, contact Kaltura.
</p>

<p class="mce-procedure">
  <a name="TodevelopautomatedprocessperiodicallyupdatingAddMembersautocompleteuserslist"></a>To develop an automated process for periodically updating the Add Members auto-complete users list
</p>

1.  Define how frequently to schedule the update.  
    Decide how often you need to update the Add Members auto-complete users list, and schedule the frequency of the update process accordingly.
2.  Develop an automated process that includes:
<ol style="list-style-type: lower-alpha;">
  <li>
    List the users to add or delete in the Add Members auto-complete users list.<br />Create the list of users to be added or deleted, based on your information system audit, querying, and export capabilities.
  </li>
  <li>
    Prepare the End-User CSV.<br />Transform your update data to comply with the <a href="http://knowledge.kaltura.com/node/464">Kaltura’s end-users CSV format</a> for adding/deleting users from the user list. Insert the CSV field headers and specify the actions.<br />To add a user, use the CSV <em>add</em> or <em>update</em> action (action = 6). To delete a user, use the CSV <em>delete</em> action (action = 3). <br /><img src="{{site.url}}/assets/798">
  </li>
  <li>
    Submit the End-User CSV.<br />When the End-Users CSV is available, submit it to Kaltura using the Kaltura API: Call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=addfrombulkupload">user.addfrombulkupload</a> API action.<br />Bulk processing in Kaltura is handled in an asynchronous batch process. Track the completion status of the bulk job in the KMC on the Bulk Upload Log page or using email notifications set by Kaltura for your account.
  </li>
</ol>

<p class="mce-note-graphic">
  NOTE: For the updating process, you can use direct Kaltura API calls (<a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=add">user.add</a>, <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=delete">user.delete</a>) instead of the CSV.
</p>

<p class="mce-procedure">
  <a name="TodeveloptriggerbasedprocessupdatingAddMembersautocompleteuserslist"></a>To develop a trigger-based process for updating the Add Members auto-complete users list
</p>

<p class="mce-note-graphic">
  NOTE: For changes in your information system to trigger real-time updates to the Add Members auto-complete users list, your information system or related applications must support real-time triggering of notifications to other systems.
</p>

Develop the following:

1.  Trigger an Add User notification.  
    Create a script that implements the following Kaltura API requests when a new user who is eligible to access MediaSpace is added to your information system.  
    - Call the [user.add][21] API action to create a new user record. Specify at least the following:  
    *       User ID  
    *       User’s first name  
    *       User’s last name  
    *       screenName (Combine the first and last names.)
2.  Trigger a Delete User notification.  
    Create a script that implements the following Kaltura API requests when a MediaSpace user leaves your organization.  
    - Call the [user.delete ][22]API action to delete the user’s record from Kaltura.  
    Specify the User ID.
3.  Trigger an Update User notification.  
    Create a script that implements the following Kaltura API request when an existing MediaSpace user's name changes in your information system.  
    - Call the [user.update][23] API action to update the user record. Specify the following:  
    *       User ID  
    *       Updated values for: User’s first name, User’s last name, screenName (Combine the first and last names.)

 [21]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=add
 [22]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=delete
 [23]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=update