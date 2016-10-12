---
layout: page
title: "Kaltura Admin Console User Manual"
date: 2012-10-29 16:21:35
---

*   <a name="top" href="#overview"></a>[Overview of the Kaltura Administration Console][1]
*   [Publisher Management][2]
*   [Users Management][3]
*   [UI ConfsTab][4]
*   [Batch Process Control Tab][5]
*   [Monitoring Tab][6]
*   [Developer Tab][7]
*   [Adjusting the Usage Packages Menu][8]

 [1]: #overview
 [2]: #pub_mng
 [3]: #users_management
 [4]: #UI_Confs_Tab
 [5]: #batch_processes
 [6]: #monitoring_tab
 [7]: #developer_tab
 [8]: #adjusting

<h1 class="mce-heading-2">
  <a name="overview"></a>Overview of the Kaltura Administration Console
</h1>

The Kaltura Administration Console provides organizations deploying a self-hosted instance of the Kaltura online video platform with full administrative control over the deployment, configuration, management, and monitoring of their Kaltura system.  The Admin Console is targeted toward IT and support oriented personnel, enabling administrators to set up, monitor and maintain the Kaltura online video platform. The Admin Console also includes management level usage reports and tools that help provide tier-1 customer support.  For optimal security it is recommended to deploy the Kaltura Admin Console behind the network firewall.

The following functionality is included in the Kaltura Administration Console:

*   [Publisher Account Management][9]
*   [Publisher Account Usage Reports][10]
*   [Admin Console User Management ][11]
*   [Batch Processing Control][12]
*   [Monitoring and Alerting System][13]
*   [Developer Tools][14]

 [9]: #p_acct_man
 [10]: #p_acct_usage
 [11]: #admin_console_usr
 [12]: #batch_proc
 [13]: #monitoring
 [14]: #dev_tools

## <a name="p_acct_man"></a>Publisher Account Management

From the Admin Console, site administrators are able to view immediate information about the publisher accounts on the system.  In addition, administrators can create new publisher accounts or block and delete accounts when necessary. Administrators are also able to set specific configuration parameters for publisher account settings, and to seamlessly access each publisher’s specific Kaltura Management Console to assist publishers with their content management, publishing flow settings, etc. For more information see [Publisher Management][15].

 [15]: https://portal.kaltura.com/community-team/Shared%20Documents/Knowledge%20Management/Work%20in%20Progress/Kaltura%20OnPrem/Admin_Console/Kaltura_Admin_Console_User_Manual_Falcon.docx#_Publisher_Management

## <a name="p_acct_usage"></a>Publisher Account Usage Reports

The Admin Console allows administrators to generate and export comprehensive usage reports, summarizing the aggregated activities and usage for each publisher account on the system in any given time period. The usage reports include information on number of plays, number of player impressions (views), number of content entries (total and by file type), streaming usage and storage usage. The generated reports can be exported to a CSV formatted file for further analysis or as a basis for billing calculations.

## <a name="admin_console_usr"></a>Admin Console User Management

To meet the needs of large enterprise IT departments, the Kaltura Admin Console can be operated by more than one administrator. Each administrator is assigned login credentials. Administrators with User Management permissions, can add, block and delete users, and edit user credentials. An Admin Console user can edit their credentials when needed. The default/first administrator account cannot be changed, blocked or deleted.

## <a name="batch_proc"></a>Batch Processing Control

The core of the Kaltura platform internal processing is orchestrated by Kaltura’s centralized batch module entities.  The Kaltura batch module is specifically responsible for the internal flow of content ingestion as well as for other real-time/offline server processes. From within the Administration Console, administrators are able to view and control the internal processing queues. They are able to conveniently cancel or abort pending tasks or tasks already in progress and to troubleshoot and retry task failures. In order to provide immediate tier -1 customer support, administrators can use the batch processing tools and information to understand the internal steps related to a specific content ingestion action, and to drill down into detailed information about a specific content entry for in-depth troubleshooting. Administrators can also adjust the setup of the Kaltura batch module components to fit their specific set-up requirements.

## <a name="monitoring"></a>Monitoring and Alerting System

Within the Admin Console, Kaltura provides an out-of-the-box solution for system monitoring and alerting.  The monitoring solution provided by Kaltura enables administrators to be notified in real-time about applicative problems and hardware/network related issues. Administrators can drill down into detailed information about any specific component being monitored.

## <a name="dev_tools"></a>Developer Tools

Kaltura provides an intuitive test console and documentation for working with Kaltura APIs. This full set of API commands enables developers to extend the functionality provided by Kaltura for their specific needs, for both site administration and web integration.

# <a name="getting_started"></a>Getting Started

<p class="Procedure mce-procedure">
  To login to the Kaltura Admin Console
</p>

1.  Go to the Kaltura Admin Console at the URL configured in your site deployment (the common URL is: www.yourdomain/admin_console).  
    <img src="{{site.url}}/assets/357">
2.  Enter your Kaltura Admin Console user credentials.
3.  Check the "Remember Me" box for the system to complete your password automatically after you typed in your user name.
4.  Click the Reset Password link to send a password reset link to your email.

The Admin Console user login credentials are set to a unified user account in the system. Only one set of credentials is kept for a specific user (uniquely defined by the user email address). The same set of credentials is applicable to both the Kaltura Admin Console and the Kaltura Management Console (KMC). The Admin Console allows for granular control to the accounts users have access to. See [Accessing Specific Publishers][16] for more information.

 [16]: #Accessing_Specific_Publishers

[Back to Top][17]

 [17]: #top

# <a name="pub_mng"></a>Publisher Management

Use the Publisher’s tab to review and fully control the publishers that are registered on your Kaltura video platform deployment. You can display the publishers' details and their usage information. Additionally, you can manage your publishers’ content accounts, create new publishers, block publishers, remove publishers, and change their settings. The Publishers tab contains three functionality pages: [][18]

 [18]: https://portal.kaltura.com/community-team/Shared%20Documents/Knowledge%20Management/Work%20in%20Progress/Kaltura%20OnPrem/Admin_Console/Kaltura_Admin_Console_User_Manual_Falcon.docx#_Publishers_Management

*   [Publisher Management Page][19]
*   [Add New Publisher Page][20]
*   [Publisher Usage Page][21]

 [19]: #pub_mng_page
 [20]: #add_new_pub_page
 [21]: #pub_usage_page

## <a name="pub_mng_page"></a>Publisher Management Page

Use the Publisher Management Page to manage all of your publisher’s features and to search for a specific publisher.

<p class="mce-procedure">
  T<a name="search_reg_pubs"></a>o search and view the details of registered publishers
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Use the Search By drop down menu and select the search criteria based on either:  
    *   Publisher ID
    *   Publisher Name
    *   Free-form text
    
    The search is applied to the publisher description, publisher URL or publisher’s administrator email address.

3.  Click Search.<img src="{{site.url}}/assets/765">

### <a name="pubs_actions"></a>Publisher Actions

You can perform the following actions to each publisher account from the Actions column in the publisher’s information table.  

<p class="mce-note-graphic">
  The drop down action list is available only for a partner that is assigned to this user.
</p>

*   [**Manage**][22] – enables full access to the specific publisher KMC account. From the publisher KMC account, you can monitor and control all of the publisher’s account activities and fully support publishers in any questions or problems they might be experiencing.
*   [**KMC Users**][23] – opens list of users associated with a specific KMC account, and allows you to login to the selected KMC account as a specific user, and to manually reset the password.
*   [**Configure**][24] **– **allows you to control your publishers’ account settings.
*   [**Block**][25]** - **allows you to block a user.
*   [**Remove**][26]** – **allows you to remove a publisher account.
*   [**MA Login**][27] – allows you to log in to the publisher’s Multi-Account Console account.<span style="text-decoration: underline;"></span>

 [22]: #manage
 [23]: #users
 [24]: #cfg
 [25]: #block
 [26]: #remove
 [27]: #multi-acct

<p class="mce-note-graphic">
  The Multi-account option is only visible for Group Parent or VAR parent partners.
</p>

<p class="mce-procedure">
  <a name="manage"></a>T<a name="manage_pubs"></a>o manage/access a publisher’s KMC account
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account you want to manage.
3.  Select Manage from the Actions dropdown menu.  
      
    The specific publisher’s Kaltura Management Console (KMC) information is displayed in a separate window. <img src="{{site.url}}/assets/766">

<p class="Procedure">
  <a name="users"></a><span class="mce-procedure">T<a name="access_thru_KMC_login"></a>o access a KMC account using a specific KMC user login</span>
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account that contains the user you want to manage.
3.  Select KMC Users from the Actions dropdown menu.<img src="{{site.url}}/assets/767">
      
    The specific Publisher’s User’s List is displayed.
4.  Select Login from the Actions drop down menu, to login into the KMC user you want to manage. You can view and manage the KMC features that are granted to the selected user according to their KMC role.
5.  Select Reset Password from the Actions drop down menu to reset the user’s password, if needed.

<p class="Procedure">
  <a name="multi-acct"></a><span class="mce-procedure">To <a name="ma_acct_mng"></a>access a Multi-account Management Console</span>
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account whose Multi- account Management Console account you are interested in viewing.
3.  From the “actions” drop-down menu, select “MA Login”.<img src="{{site.url}}/assets/768">

### Configuration Options

#### <a name="Publisher_Specific_Configuration"></a>Publisher Specific Configuration Management

This window contains options to configure settings for a publisher and contains the following sections:

*   [General Information][28]
*   [Multi-Account Group Related Info][29]
*   [Publisher Specific Delivery][30]
*   [Remote Storage Policy][31]
*   [Advanced Notification Settings][32]
*   [Content Ingestion Options][33]
*   [Password Security][34]
*   [New Account Options][35]
*   [Included Usage][36]
*   [Live Stream Config][37]
*   [Enable/Disable Features][38]

 [28]: #genl_info
 [29]: #multi_acct_group_rel
 [30]: #Publisher_Specific_Delivery
 [31]: #remote_storage
 [32]: #adv_notifications
 [33]: #content_ingestion
 [34]: #pwd_security
 [35]: #new_acct
 [36]: #included_usage
 [37]: #live_stream_cfg
 [38]: #enable_disable

<p class="Procedure mce-procedure">
   <a name="cfg"></a>To configure publisher specific settings
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account that contains the user you want to configure.
3.  Select Configure from the Actions dropdown menu.  
      
    The Publisher Specific Configuration window is displayed.<img src="{{site.url}}/assets/769">
4.  Configure the settings.
5.  Click Save.

#### <a name="genl_info"></a>Publisher Specific Configuration – General information

This section is used to manage generic information. All fields except the Publisher Name and Description are non-editable and are usually provided by the publisher or generated by the system at signup.<img src="{{site.url}}/assets/770">

#### <a name="multi_acct_group_rel"></a>Publisher Specific Configuration – Multi-Account Group Related Info

Publishers can be part of groups when several publisher accounts are established for the same organization, or for a service reseller that manages several accounts. Publisher groups can be defined for aggregated billing (usage and billing are set to the entire group) or to non-aggregated billing, where each account is billed separately. You can define a specific account as the parent of a group, or define the account as a plain Publisher account, with or without association to its group Parent Account ID, for the purpose of aggregated billing.<img src="{{site.url}}/assets/771">

The Parent Account ID is only relevant (=enabled) when the account type is Publisher Account.

#### <a name="Publisher_Specific_Delivery"></a>Publisher Specific Configuration – Publisher Specific Delivery

You can assign the following to your publishers:

*   Service Host Name - a specific API Host URL
*   Specific  CDN HTTP Deliver URL -  host URLs:
    *   RTMP or Thumbnail can be delivered from different specific CDNs
    *   Delivery Restrictions (for example, secured delivery only)  
        <img src="{{site.url}}/assets/772">

#### <a name="remote_storage"></a>Publisher Specific Configuration  - Remote Storage Policy

Use this section to manage remote storage global account settings, if enabled for the account. See [Enable/Disable Features][38]. The delivery of the content can be from Kaltura only, from the remote storage only, or try one and failover to the other. In addition, you can define specific actions, such as deleting the exported storage, etc.<img src="{{site.url}}/assets/773">

#### <a name="adv_notifications"></a>Publisher Specific Configuration – Advanced Notification Settings

Advanced notification configuration can be set from here. In most cases, standard notification configuration is sufficient and can be edited from the KMC. Contact Kaltura if advanced notification configuration is required.<img src="{{site.url}}/assets/799">

To learn more about Event Notification configuration, see [Event Notifications][39].

 [39]: #event_notifications

#### <a name="content_ingestion"></a>Publisher Specific Configuration – Content Ingestion Options

Options for content ingestion are grouped in this section.

*   Default Thumbnail Offset – defines the second in the media the default thumbnail is captured from.
*   Default Thumbnail Density – the DPI for the default thumbnail.
*   Enable/disable for:
*   Content moderation – if checked, by default all ingested content has to pass moderation.
*   Entry Replacement Manual Approval – if checked, entry media replacement requires approval.
*   Manual Drop Folder Matching –use to enable/disable the manual Match Drop Folder button in the KMC, in the Flavors tab per entry. This kind of configuration (hiding the button) is useful when working in a fully automated drop folder ingestion workflow, for example when ingesting XML files.
*   Bulk Upload Notifications Email–  email address to send a report of the bulk upload ingestion

<img src="{{site.url}}/assets/800">

#### <a name="pwd_security"></a>Publisher Specific Configuration – Password Security

Use this section to define the number of password attempts and the password replacement/retention policy.<img src="{{site.url}}/assets/801">

#### <a name="services_pkgs"></a>Publisher Specific Configuration – Service Packages

Use this section to set different service classes, editable through local XML files. This feature displays different service level indications in reports such as Publisher Usage and Publisher Management.<img src="{{site.url}}/assets/802">

#### <a name="new_acct"></a>Publisher Specific Configuration – New Account Options

Use this section to enable and control new publishers, and allow, for example, a free trial for a limited duration (assuming your free trial model is limited usage based).<img src="{{site.url}}/assets/803">

#### <a name="included_usage"></a>Publisher Specific Configuration – Included Usage

For a usage based service user, use this section to set quotas per account, for example, the amount of usage (combined streaming and storage, or separate), KMC users, streams, end users (specifically, video uploaders) and total videos. These settings allow you to provide different classes of service to different publisher accounts.

<p class="mce-note-graphic">
  <span>The Kaltura platform does not automatically block accounts when the quota values are exceeded, (excluding the number of KMC users), but only provides the infrastructure for developing usage overage reports.</span>  
</p>

<img src="{{site.url}}/assets/804">

#### <a name="live_stream_cfg"></a>Publisher Specific Configuration – Live Stream Config

Use this section to configure the source of live streams. Currently, the Kaltura platform comes with Akamai built-in; other live stream sources are possible with an integration effort).<img src="{{site.url}}/assets/805">

#### <a name="enable_disable"></a>Publisher Specific Configuration – Enable/Disable Features

Use this section to enable/disable specific features per partner. Some options have additional configuration tasks as noted.

<img src="{{site.url}}/assets/806">

## Publisher Specific Configuration Features - Additional Tasks

This section provides the additional tasks you are required to perform to configure Publisher Specific Configuration options.

## Publisher-Specific Objects and Profiles

<p class="BodyTextKWN">
  This section covers the profiles and objects that can be defined per-publisher, by using the publisher’s “Profiles” drop-down menu:<img src="{{site.url}}/assets/807">
</p>

### Widgets

<p class="Procedure mce-procedure">
  To <a name="widgets"></a>configure UI Confs (Widgets) for a publisher
</p>

<p class="mce-note-graphic">
  <span>The UI Confs tab is not available by default to On-Prem customers.</span>
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account that you want to configure.
3.  Select Widgets from the Profiles dropdown menu.  
    <img src="{{site.url}}/assets/779">
      
    The specific Publisher’s UI Confs Management page is displayed.  
    <img src="{{site.url}}/assets/352">

See the [UI Confs Management Page][40] for more information.

 [40]: #UI_Confs_Management_Page

### Remote Storage

You can define and set a remote storage and delivery profile for a specific publisher account by checking the Remote Storage option in the Publisher Management Page- Enable Disable Features section.  The remote storage and delivery solution can be used to enable storage and delivery of video assets from a network storage location that is external to the Kaltura Platform.  This feature is commonly used to leverage a publisher’s CDN network storage solution (for example, <a href="http://www.akamai.com/html/technology/products/netstorage.html" target="_blank">Akamai’s NetStorage</a>). Selecting this option will lead you to the Remote Storage Profiles page for creating or editing publisher specific Remote Storage profiles. Access to the remove storage profiles is also possible through the Publisher Management Page- Enable Disable Features Remote Storage feature “config” link.

<p class="Procedure mce-procedure">
  <a name="cfg_remote_storage_profile"></a>To configure a publisher’s remote storage and delivery profile
</p>

1.  [Configure the publisher specific settings][24].
2.  Check Remote Storage in the Enable/Disable Features section and click the config link or alternatively<ol style="list-style-type: lower-alpha;">
      <li>
        Go to the Publishers tab and select Publisher Management.
      </li>
      <li>
        Select the publisher account that you want to configure.
      </li>
      <li>
        Select Remote Storage from the Profiles dropdown menu.<br />The specific Publisher’s Remote Storage Profile is displayed.<img src="{{site.url}}/assets/808">
      </li>
    </ol>

<p class="Procedure mce-procedure">
  To <a name="create_remote_storage_profile"></a>create a remote storage profile
</p>

1.  [Configure a publisher’s remote storage and delivery profile.][41]
2.  Click Create New.<img src="{{site.url}}/assets/809">
      
    The Storage Specific Setup window is displayed.
3.  Set the configuration options and click Save.

 [41]: #cfg_remote_storage_profile

**General:** The Related Publisher ID is the Publisher ID. This field is auto-filled if triggered from a specific publisher. The Remote Storage Name is the name for this storage profile. Both fields are mandatory.

**Export Details**: Use these fields to set the access information required for exporting assets from the Kaltura server to the remote storage location following the video transcoding process.  Provide a Storage URL, Storage Base Directory and Transfer Protocol information. Select ‘Kaltura Path’ for constructing storage hierarchy according to Kaltura’s default path structure, or contact Kaltura for instructions on how to customize storage structuring to a specific storage path definition.

**Delivery Details: ** Use these fields to set the delivery related information that enables direct delivery of content from the defined remote storage to a Kaltura player. The HTTP Delivery Base URL is mandatory; all other listed delivery methods are optional.

**Export Policy**: Use these fields to set different export delivery policy options for (selective) export to the remote storage location. It is possible to use the Remote Storage feature to store/deliver only assets that are bigger than/smaller than a specific file size. Use the Export Policy Advanced options to store/deliver only specific transcoding flavors and with or without the source file, or to push assets to remote storage only after moderator approval.

Additional remote storage account setting options are available from the publisher configuration window. These options apply to all storage profiles that may be in use by the publisher account. See [Publisher specific configuration – Remote storage policy][31].

### Virus Scan profiles

<p class="Procedure mce-procedure">
  To <a name="configure-anti_virus"></a>configure anti-virus scanning for a publisher
</p>

You can scan entries (per type) with an external virus scanning engine.

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account that you want to configure.
3.  Select Virus Scan from the Profiles drop down menu.<img src="{{site.url}}/assets/810">
    The Virus Scan Profiles page is displayed.

<span><span class="mce-note-graphic">This feature requires the purchase and installation of a virus scan service. Kaltura supports the Symantec engine, however, specific installation and configuration is required to enable the feature</span>.</span> 

You can configure scanning one or several data, media or document files.<img src="{{site.url}}/assets/811">

You can delete, or attempt to clean (failing over to deleting) an entry.

### Generic Distribution Providers

This option allows you to control Content Distribution. The Distribution module enables publishers to automate the distribution of video packages, directly from within the KMC.  Distribution partners who enable automatic submission of content to their sites and expose specifications for such automatic submission can automate distribution. The exposed specifications may include requirements for video qualities, different sizes of thumbnails, metadata, scheduling data, supported submission actions and other parameters.

Kaltura provides a robust infrastructure UI for enabling the content distribution workflow. Distribution connectors can be developed as Kaltura server plugins according to the specifications of each distribution partner on how to submit video packages into their sites. When a distribution plugin is enabled in the system, publisher’s Distribution Profiles can be set from the Admin Console for each publisher account. For further technical information on Kaltura’s Distribution module, please refer to the *Creating a Custom Distribution Destination Using Kaltura Infrastructure* document. Generic Providers

Generic Distribution Provider settings include the required transcoding flavors for distribution target, the required thumbnails for distribution target and required parameters of each specific distribution action. You may utilize the Generic Distribution Provider settings to set multiple Distribution Profiles according to your needs.

<img src="{{site.url}}/assets/814">

<p class="Procedure mce-procedure">
  To create and configure a Generic Provider
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account that you want to configure.
3.  Select Generic Providers from the Profiles dropdown menu.  
    The Generic Distribution Provider Profiles configuration is displayed.  
    <img src="{{site.url}}/assets/816">
4.  Click Create New.
5.  Select Configure from the Action drop down menu to modify an existing Generic Distribution Provider profile.  
    The Generic Provider Specific Setup Configuration window is displayed.  
    <img src="{{site.url}}/assets/817">
6.  Fill in the required generic provider identifiers. 
<ol style="list-style-type: lower-alpha;">
  <li>
    To enable settings for all publisher accounts, define the Publisher ID as 0.
  </li>
  <li>
    To enable setting for a specific publisher account, define the specific Publisher ID.
  </li>
  <li>
    To define the default generic provider, check the "Is Default" box.
  </li>
</ol>

7.  Scroll down and toggle on additional options.
8.  To add a thumbnail, click the "Add Thumbnail" button and fill in the thumbnail values.<img src="{{site.url}}/assets/813">
9.  ** **To enable a Submit, Update, Delete or FetchReport action, click Enabled and enter the action values.

### Drop Folders

Information related to the configuration and use of the Drop-Folder functionality can be found [here][42].

 [42]: http://cdnknowledge.kaltura.com/sites/default/files/Kaltura_Drop_Folder_Service_for_Content_Ingestion_0.pdf

### <a name="event_notifications"></a>Event Notifications

<p class="Procedure mce-procedure">
  To create an Event Notification Template
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account that you want to configure.
3.  Select “Event Notifications” from the Profiles drop down menu.  
      
    The Event Notification screen is displayed.<img src="{{site.url}}/assets/821">

<p class="mce-note-graphic">
  The Event Notification feature requires the purchase and installation of the Event Notification service. Contact your Kaltura Account manager for more information.
</p>

In the Event Notifications Template screen, you can add new Event Notification templates for the publisher. For this release only, the Email Notification Template is available.

<img src="{{site.url}}/assets/825">

<p class="Procedure">
  <a name="block"></a><span class="mce-procedure">To block/unblock a publisher account</span>
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account you want to block.
3.  Select Block from the Actions dropdown menu.

A prompt opens for your confirmation.  

A blocked account may be unblocked by an admin at any time from the publisher actions menu.

The publisher’s content will not be displayed; however, the publisher will still be able to login to the Kaltura Management Console.<img src="{{site.url}}/assets/826">

<p class="Procedure">
  <a name="remove"></a><span class="mce-procedure">To remove a publisher account</span>
</p>

1.  Go to the Publishers tab and select Publisher Management.
2.  Select the publisher account you want to remove.
3.  Select Remove from the Actions dropdown menu.

A prompt opens for your confirmation.  

When you remove a publisher, the publisher’s content can be displayed in the publishers table, when the removed status filter is checked. However, you cannot apply any actions to the publisher account. You can see that the publisher has been removed. The publisher can no longer login to the Kaltura Management Console.

<p class="mce-note-graphic">
  <span>Account removal is permanent.</span>
</p>

<img src="{{site.url}}/assets/827">

## <a name="add_new_pub_page"></a>Add New Publisher Page

Use this page to add a new publisher account.

<p class="Procedure mce-procedure">
  To add a new publisher account
</p>

1.  Go to the Publishers tab and select Add New Publisher.<img src="{{site.url}}/assets/828">
2.  Enter the publisher's details: Name, Company Administrator, Administrator email address and Administrator Phone number.
3.  The Publisher’s Service Edition Type may be selected to assign a specific service level indication to the new publisher. If the usage package selection is not relevant, you can select the N/A option.  For instructions on how to adjust the “Usage Packages” menu, see [Usage Packages][8].

Once the publisher is created in the system, the publisher's administrator will receive an email containing their credentials to access the Kaltura Management Console (KMC).

Admin Console users are able to create multiple KMC accounts for any purpose while using the email address used for their Kaltura Admin Console user account. However, actual publisher accounts that are not associated with an Admin Console user are limited to enable one KMC account per email address. This limitation is set mainly to secure the credentials of publisher account owners.

## <a name="pub_usage_page"></a>Publisher Usage Page

Use the Publisher Usage Page to display all the information about the publisher's usage, including number of entries, number of views, total bandwidth usage, storage usage and more.

You can search for specific publishers  by entering publisher ID, name or free text, or you can filter the list of publishers by selecting a specific status (active, blocked, removed) or by date range of account creation.

<p class="Procedure mce-procedure">
  To retrieve and export publisher usage information
</p>

1.  Go to the Publishers tab and select Publishers’ Usage
2.  Enter search criteria for the publisher account that would like to obtain information for and click Search.

The Usage information is displayed.

<p class="Procedure mce-procedure">
  To export publisher usage information
</p>

1.  Go to the Publishers tab and select Publishers’ Usage
2.  Enter search criteria for the publisher account that would like to obtain information for and click Search.
3.  Click Export to CSV (located at the bottom of the page) to export the information to a CSV formatted file, for further analysis and/or for billing purposes.  
    <img src="{{site.url}}/assets/831">

### Distribution Profiles Page

Use the Distribution Profiles Page to manage the distribution profiles for publisher accounts, and to create new distribution profiles.

To allow a specific publisher to distribute content to a certain distribution partner, an administrator must create a distribution profile for the specific distribution partner for the specific publisher’s KMC account.

<p class="Procedure mce-procedure">
  To search for and view the details of a distribution profile
</p>

1.  Enter a Publisher ID, Publisher Name or free text.
2.  After you choose your search criteria, click Search.
3.  Select Configure from the Actions drop down menu.
4.  In the Publisher Specific Configuration page, enable the Content Distribution Model and click config.  
      
    The Distribution Profile page is displayed.<img src="{{site.url}}/assets/833">

<p class="Procedure mce-procedure">
  How to create a distribution profile
</p>

1.  Enter a Publisher ID, Publisher Name or free text.
2.  After you choose your search criteria, click Search.
3.  Select Configure from the Actions drop down menu.
4.  In the Publisher Specific Configuration page, enable the Content Distribution Model and click config.  
      
    The Distribution Profile page is displayed.
5.  Enter the publisher ID.
6.  Select the provider type and click Create New.<img src="{{site.url}}/assets/774">
      
    The Profile Setup Configuration window opens.<img src="{{site.url}}/assets/775">
7.  Configure the values and scroll down for more options.<img src="{{site.url}}/assets/834">
8.  To set the status for a Submit, Update, Delete or Report action, select the "Enabled" value.
9.  To add a thumbnail, click "Add Thumbnail" and fill in the thumbnail values.<img src="{{site.url}}/assets/777">
10. To configure an existing distribution profile, choose the profile from the list and select the "Configure" action.<img src="{{site.url}}/assets/778">

 [Back to Top][17]

<div class="WordSection1">
  <h1>
    <a name="users_management"></a>Users Management
  </h1>
  
  <p>
    Use the Users tab to configure the system administrator users in your site. The Users tab contains the following functionality pages:
  </p>
  
  <ul>
    <li>
      <a href="#User_Management_Page">User Management</a>
    </li>
    <li>
      <a href="#Add_User_Page">Add User</a>
    </li>
    <li>
      <a href="#Change_My_Settings_Page">Change My Settings</a>
    </li>
    <li>
      <a href="#User_Roles_Page">User Roles</a>
    </li>
  </ul><img src="{{site.url}}/assets/835">
  
  <br /><h2>
    <a name="User_Management_Page"></a>User Management Page
  </h2>
  
  <p>
    The User Management Page displays all the administrator users authorized to use the Kaltura Admin Console. From the Actions menu you are able to:
  </p>
  
  <ul>
    <li>
      Block a Kaltura Admin Console user for temporary denial of access to the Admin Console
    </li>
    <li>
      Permanently remove a user
    </li>
    <li>
      Change the user's role
    </li>
    <li>
      Assign Partners – see <a href="#Accessing_Specific_Publishers">Accessing Specific Publishers</a>
    </li>
  </ul>
  
  <p class="mce-note-graphic">
    You cannot apply any action on your own user or on the primary administrator of the platform.
  </p>
  
  <p class="mce-note-graphic">
    <img src="{{site.url}}/assets/836">
  </p>
  
  <h2>
    <a name="Add_User_Page"></a>Add User Page
  </h2>
  
  <p>
    Use the Add User page to add a new administrator/user to the site.
  </p>
  
  <p class="mce-procedure">
    To add a System Administrator/user
  </p>
  
  <ol>
    <li>
      Go to the User tab and select Add User.
    </li>
    <li>
      Fill in the new user details.
    </li>
    <li>
      Select System Administrator/or other user role from the Role drop down menu.
    </li>
    <li>
      Click Create. The new user will receive an email with credentials for the Kaltura Admin Console.<img src="{{site.url}}/assets/837">
    </li>
  </ol>
  
  <p>
    For a description of users and roles, see <a href="#Admin_Users_and_Roles">Admin Users and Roles</a>.
  </p>
  
  <p class="mce-procedure">
    To change the role of an existing Admin Console user
  </p>
  
  <ol>
    <li>
      Go to the Users tab and select User Management.
    </li>
    <li>
      Select a user and then select Change role from the Action drop down menu.<br /><br />The Change Role window is displayed.<img src="{{site.url}}/assets/838">
    </li>
    <li>
      Select a Role from the drop down menu and click Save.<img src="{{site.url}}/assets/839">
    </li>
  </ol>
  
  <p>
    <a name="Accessing_Specific_Publishers"></a><span class="mce-heading-3">Accessing Specific Publishers</span>
  </p>
  
  <p class="mce-procedure">
    To allow administrators to access a specific publisher
  </p>
  
  <ol>
    <li>
      Go to the Users tab and select User Management.
    </li>
    <li>
      Select a user.
    </li>
    <li>
      Select Assign partners from the Action drop down menu.<img src="{{site.url}}/assets/840">
    </li>
    <li>
      Assign Partners. There are three options to assign  partners:<ul>
        <li>
          by Partner Id
        </li>
        <li>
          by Partner Service Edition
        </li>
        <li>
          both Partner Id  and Partner Service Edition
        </li>
      </ul>
      
      <p>
        You can set a specific Partner Ids, assign multiple Partner Ids or enter “*” (asterisk) for all partners. The Partner Ids list should be separated by comma.
      </p>
    </li>
    
    <li>
      Select the Publisher Service Edition you want this administrator to have access to.
    </li>
    <li>
      Click Save.<img src="{{site.url}}/assets/841">
    </li>
  </ol>
  
  <h2>
    <a name="Change_My_Settings_Page"></a>Change My Settings Page
  </h2>
  
  <p>
    Use the Change My Settings Page to change your Admin Console login credentials. After you change your credentials, an email is sent to you with the new login credential’s information. Changes to the user’s credentials also apply to the KMC user account that the user is associated with.<img src="{{site.url}}/assets/842">
  </p>
  
  <h2>
    <a name="User_Roles_Page"></a>User Roles Page
  </h2>
  
  <p>
    Use the User Roles page to configure specific permissions for admin user roles. Selecting “configure” for a specific role grants you granular control over specific permissions for that role within the admin console.
  </p>
  
  <h3>
    <a name="Admin_Users_and_Roles"></a>Admin Users and Roles
  </h3>
  
  <p>
    The Kaltura Admin Console includes the following default Admin Console user roles:
  </p>
  
  <ul>
    <li>
      <strong>System Administrator</strong> - has full permission for all Admin Console functionalities
    </li>
    <li>
      <strong>Support Manager</strong> - has the following permissions:
    </li>
    <ul>
      <li>
        Publisher Management
      </li>
      <li>
        Add Publisher
      </li>
      <li>
        Publishers’ Usage
      </li>
      <li>
        Batch Process Control (view only)
      </li>
      <li>
        Distribution Profiles
      </li>
      <li>
        Developer
      </li>
    </ul>
    
    <li>
      <strong>Publisher Administrator</strong> - has the following permissions:
    </li>
    <ul>
      <li>
        Publisher Management
      </li>
      <li>
        Add Publisher
      </li>
      <li>
        Publishers’ Usage
      </li>
      <li>
        Developer
      </li>
    </ul>
    
    <li>
      <strong>Guest</strong> - is pre-defined role with no access to any of the Admin Console functionalities. The Guest role is reserved to enable tailored permission settings according to specific needs.
    </li>
  </ul>
  
  <p>
    You should assign a role to each user to permit access to Admin Console functionality based on their organizational responsibilities.<img src="{{site.url}}/assets/843">
  </p>
  
  <p class="mce-procedure">
    To assign permissions to a role
  </p>
  
  <ol>
    <li>
      Go to the Users tab and select User Roles.
    </li>
    <li>
      Click on a Name and then select Configure from the Action drop down menu.<br /><br />The User Role Configuration window is displayed.<img src="{{site.url}}/assets/844">
    </li>
    <li>
      Check the permissions and click Save.
    </li>
  </ol>
  
  <a href="#top">Back to Top</a>
</div>

<div class="WordSection2" style="text-align: left;" dir="RTL">
  <h1 dir="LTR">
    <a name="UI_Confs_Tab"></a>UI Confs Tab
  </h1>
  
  <p dir="LTR">
    The UI Confs tab is disabled by default on the On-Prem<sup>TM</sup> installation and enabled in CE.
  </p>
  
  <h2 dir="LTR">
    <a name="UI_Confs_Management_Page"></a>UI Confs Management Page
  </h2>
  
  <p dir="LTR">
    Use this page to manage all the UI Configuration objects in your deployment. You can edit the definition for any flash widget/application - including the KMC, installed for the selected publisher account. You can directly edit the UI Conf using a built in editor using the XML definition file for the Flash player selected.
  </p>
  
  <p dir="LTR">
    UI Confs objects that are associated with Publisher 0 are applicable to all accounts in your platform.  UI Confs objects associated with Publisher 99 are used as templates and cloned upon the creation of new accounts.
  </p>
  
  <p class="mce-note-graphic" dir="LTR">
    <span>Any change to existing UI Confs objects might negatively affect your platform's UI functionality. We recommend that you duplicate and keep a backup copy of the UI Conf object you want to edit.</span>
  </p>
  
  <span class="mce-procedure">To manage a UI Conf object</span> 
</div>

1.  Go to the UI Confs tab.  
    The UI Confs Management page is displayed.
2.  Select a Filter and then click Search.<img src="{{site.url}}/assets/845">

3.  Select a row and then select an Action from the drop down menu.
*   Edit opens the Edit UI Confs window.
*   Edit External opens the XML definition file for the Flash player selected.

4.  Modify the UI Confs parameters and Save.

<p class="mce-procedure">
  <span>To add a UI Conf object</span>
</p>

1.  Go to the UI Confs tab.  
      
    The UI Confs Management page is displayed.
2.  Click Create New.  
    <img src="{{site.url}}/assets/846">
      
    The Add UI Conf window is displayed.
3.  Enter values for the fields and Save.

 [Back to Top][17]

# <a name="batch_processes"></a>Batch Process Control Tab

Use the Batch Process Control tab to control the Kaltura platform batch processes. The Batch Process Control tab contains the following pages:

 

*   [In-Progress Tasks][43]
*   [Failed Tasks][44]
*   [Setup Page][45]
*   [Entry Lifecycle ][46]
*   [Entry Investigation][47]

 [43]: #in_progress
 [44]: #failed_tasks
 [45]: #setup_page
 [46]: #entry_lifecycle
 [47]: #entry_investigation

<img src="{{site.url}}/assets/847">

## <a name="in_progress"></a>In-Progress Tasks Page

Use the In-Progress Tasks page to display all ongoing batch tasks in your site. The information is constantly updated so that you can better understand your system’s batch processing behavior.

The In-Progress Tasks page contains two tables:

*   In-Queue Tasks table - lists the batch tasks that are waiting to be processed.
*   In-Progress tasks table -  lists the batch tasks that are currently processed

Both tables contain useful information on the characteristics of each batch task. An option to cancel a batch task currently in queue, or abort a batch task currently in progress, is provided.

<p class="mce-note-graphic">
  <span>An action that you take on a ‘parent’ entry affects its ‘children’ entries as well.</span> 
</p>

<p class="Procedure mce-procedure">
  To filter and view In-Progress Tasks
</p>

1.  Go to the Batch Control tab and select in Progress Tasks.  
      
    The In-Progress Tasks page is displayed.
2.  Select a Filter and then click Search.   
      
    You can filter tasks by date range, Entry ID, Publisher ID or a specific task type. The filters are applied to both of the tables on the page.
3.  Click on a Task ID to display additional information about the specific batch task parameters.
4.  Click on an Entry Name to display the Entry Lifecycle page.

The In-Progress Tasks page refreshes every 30 seconds. You may pause and resume the automatic refresh, or refresh the page manually by clicking Refresh Now.<img src="{{site.url}}/assets/848">

 

## <a name="failed_tasks"></a>Failed Tasks Page

Use the Failed Tasks page to display failed batch tasks (including aborted tasks). You can delete or retry a failed task or initiate a troubleshooting process. You can filter the failed tasks using several filters. For example, you can filter tasks by date range, Entry ID, Publisher ID or a specific reason of failure. You can hover over the Failure Reason information in the table, to understand the specific error type and code. Specific error types have a link with a more detailed error description.

Click the Entry Name to display entry ingestion related failures. An Advanced Entry Investigation page is displayed.

The screen refreshes every 30 seconds (The duration can be adjusted). You may pause and resume the automatic refresh or refresh manually by clicking e "Refresh Now".

## <a name="setup_page"></a>Setup Page

Use the Setup page to may manage the batch services that are configured in the site.

<p class="Procedure mce-procedure">
  To view the specific configuration of each batch service
</p>

1.  Go to the Batch Control Process tab and select Setup.
2.  Click on a Name in the Configure Batch Services Table and then select an action from the Action drop down menu. 

You can start/stop, enable/disable or set the start-up type of each batch service.<img src="{{site.url}}/assets/851">

 

## <a name="entry_lifecycle"></a>Entry Lifecycle Page

Use the Entry Lifecycle Page to see the full process that a specific entry has gone through during its ingestion to the Kaltura platform. The processes may include import related tasks as well as transcoding related tasks. By tracking the lifecycle for a specific entry you can spot entry specific and general problems in the system.

<p class="Procedure mce-procedure">
  To view the batch processing lifecycle of a specific media entry
</p>

1.  Go to the Batch Control Process tab and select Entry Lifecycle.
2.  Select By  Entry ID to search by Entry ID and enter the Entry ID or  
      
    Select By Flavor Asset ID and enter the Flavor Asset ID.
3.  Click Search.

You can also access this page by clicking any Entry Name in the [In-Progress Tasks Page.  ][48] Click the Entry Name to display the Advanced Entry Investigation page. Click on the Account link to access the publisher KMC account.<img src="{{site.url}}/assets/850">

 [48]: file:///C:/Users/Debbie/Documents/On_Prem/Falcon/Admin_Console/Falcon/Kaltura_Admin_Console_User_Manual_Falcon.docx#_In_Progress_Tasks

## <a name="entry_investigation"></a>Entry Investigation Page

Use the Entry Investigation page to research a specific entry and view detailed information about its parameters, its batch processing history, the information related to its transcoding flavors and the actual files on disk related to it.  The Entry Investigation page is the place for Kaltura platform experts to go to; to fully investigate what problems occurred during the entry ingestion process. You can export this page to an external file and send it to the Kaltura support team as input for further investigation by Kaltura experts.<img src="{{site.url}}/assets/849">

[Back to Top][17]

<div class="WordSection2" style="text-align: left;" dir="RTL">
  <h1>
    Monitoring Tab<a name="monitoring_tab"></a>
  </h1>
</div>

<div class="WordSection1" dir="RTL">
  <p dir="LTR">
    Use the Monitoring tab to display a graphical monitoring overview of your servers. Each row represents the monitoring checks configured for a single server in your site. The Monitoring Status page provides a quick view of the platform hosts and services. Green icons indicate that the status is OK for the specific check. Orange and Red icons represent a critical or almost critical state that requires the attention of the site administrator. Orange and red states are usually accompanied by a real-time alert message. From the Monitoring Status page you can drill down to the history and trend information of each check in each server.<img src="{{site.url}}/assets/337">
  </p>
  
  <p dir="LTR">
    You can run the Xymon based monitoring functionality directly from the Xymon application GUI to include some advanced monitoring functionalities that are not available within the Kaltura Admin Console. The common URL for the Xymon application is http://www.your domainname/xymon.
  </p>
  
  <p dir="LTR">
    <a href="#top">Back to Top</a>
  </p>
</div>

<h1 dir="LTR">
  <a name="developer_tab"></a>Developer Tab
</h1>

<p class="WordSection2" style="text-align: left;" dir="RTL">
  :This section describes the following<br /><a href="#test_console">Test Console</a><br /><a href="#api_doc">API Documentation</a><br /><a href="#apc">APC</a><br /><a href="#api_clientlib">API Client Libraries</a><br /><a href="#system_helper">System Helper</a>
</p>

<h2 dir="LTR">
  <a name="test_console"></a>Test Console
</h2>

<p dir="LTR">
  Use the Test Console menu to test the different Kaltura REST API methods available. Automatic code generation for:
</p>

*   <a href="http://www.kaltura.co.cc/api_v3/testme/?hideMenu=true" target="_blank">PHP</a>
*   <a href="http://www.kaltura.co.cc/api_v3/testme/?hideMenu=true" target="_blank">Java</a>
*   <a href="http://www.kaltura.co.cc/api_v3/testme/?hideMenu=true" target="_blank">C#</a>
*   <a href="http://www.kaltura.co.cc/api_v3/testme/?hideMenu=true" target="_blank">Python</a>
*   <a href="http://www.kaltura.co.cc/api_v3/testme/?hideMenu=true" target="_blank">JavaScript</a>

<p dir="LTR">
  is included. Click <a href="http://www.kaltura.co.cc/api_v3/testme/?hideMenu=true" target="_blank">Show Code Example</a> to display the selected code.
</p>

<p dir="LTR">
  You can select specific API services and actions and the relevant code is automatically generated to simply copy-and-paste into your work.
</p>

<p class="Procedure mce-procedure" dir="LTR">
  To access the Test Console
</p>

*   Go to the Developer tab and select Test Console.  
      
    For more information about the Test Console features and functionality see [here][49].

 [49]: http://knowledge.kaltura.com/using-kalturas-api-test-console-introduction

<h2 dir="LTR">
  <a name="api_doc"></a>API Documentation
</h2>

<p dir="LTR">
  Use the API Documentation page to learn about the different Kaltura REST API methods available, either for extending the services offered in your site or for advanced integration of any website with your online video platform.
</p>

<p class="Procedure" dir="LTR">
       To access the API Documentation
</p>

*   Go to the Developer tab and select API Documentation. For more information, see [here][50].<img src="{{site.url}}/assets/852">

 [50]: http://knowledge.kaltura.com/kaltura-api-documentation-set

<h2 dir="LTR">
  <a name="apc"></a>APC
</h2>

<p dir="LTR">
  Use the APC menu to cache management statistics for a <strong>single server</strong> deployment. This feature is useful during development and testing.
</p>

<p class="Procedure mce-procedure" dir="LTR">
  To clean the APC cache
</p>

*   Click “Clear opcode cache” at the top right corner.<img src="{{site.url}}/assets/853">

<h2 dir="LTR">
  <a name="api_clientlib"></a>API Client Libraries
</h2>

<p dir="LTR">
  Use the API Client Libraries menu to download the API Client libraries in different programming languages.
</p>

<p class="Procedure mce-procedure" dir="LTR">
  To access the API Client Libraries
</p>

*   Go to the Developer tab and select API Client Libraries. For more information, see [here][51].<img src="{{site.url}}/assets/855">

 [51]: http://knowledge.kaltura.com/introduction-kaltura-client-libraries

<h2 dir="LTR">
  <a name="system_helper"></a>System Helper
</h2>

<p dir="LTR">
  Use the System Helper tools in this section to debug Kaltura Sessions (KS), test the IP to Country and other encoding/decoding functions.<img src="{{site.url}}/assets/856">
</p>

<p dir="LTR">
  <a href="#top">Back to Top</a>
</p>

<h1 dir="LTR">
  <a name="adjusting"></a>Adjusting the Usage Packages Menu
</h1>

<p dir="LTR">
  You can adjust the names of the Usage Packages assigned to the publishers registered in your site to better fit the packages offered by your business unit. 
</p>

<p class="Procedure mce-procedure" dir="LTR">
  To adjust the Usage Packages options
</p>

1.  Edit the patnerPackages.xml file available at the following location.  
      
    <a href="file:///C:/opt/kaltura/app/alpha/apps/kaltura/config/partnerPackages.xml" target="_blank">/opt/kaltura/app/alpha/apps/kaltura/config/partnerPackages.xml </a>
2.  <a href="file:///C:/opt/kaltura/app/alpha/apps/kaltura/config/partnerPackages.xml" target="_blank"></a>Update your changes on each server on your site that runs a Kaltura application code. We recommend that you consult with the Kaltura technical team before applying your changes.