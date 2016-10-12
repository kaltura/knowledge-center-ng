---
layout: page
title: "Setting up MediaSpace"
date: 2012-09-03 15:26:46
---

This article describes how to set up content, galleries and channels, channel user permissions, and HTTPS for MediaSpace.

<p class="mce-heading-2">
  Setting up MediaSpace Content in the KMC
</p>

<p class="mce-procedure">
  <a name="TosetupaMediaSpacecategorytree"></a>To set up a MediaSpace category tree in the KMC
</p>

1.  In the KMC, create a MediaSpace root category.
<ol style="list-style-type: lower-alpha;">
  <li>
    Select the Content tab and then select the Categories tab.
  </li>
  <li>
    Click <strong>Add Category</strong>.
  </li>
  <li>
    On the New Category window, select the position of the root category and save your new category.<br /><img src="{{site.url}}/assets/618">
  </li>
  <li>
    In the New Category window, enter metadata for the new category and click <strong>Save</strong>.<br /><img src="{{site.url}}/assets/619">
  </li>
</ol>

2.  In MediaSpace, define the root category.
<ol style="list-style-type: lower-alpha;">
  <li>
    On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Categories tab.
  </li>
  <li>
    Under <em>rootCategory</em>, select the category that you created, and click <strong>Save</strong>. <br /><img src="{{site.url}}/assets/620">
  </li>
</ol>

3.  In the KMC, verify your root category and sub-categories.
<ol style="list-style-type: lower-alpha;">
  <li>
    Select the Content tab and then select the Categories tab.
  </li>
  <li>
    Verify that the root category is displayed with new sub-categories.<br /><img src="{{site.url}}/assets/621">
  </li>
</ol>

4.  In the KMC, verify that the root category is assigned a Privacy Context.   
    A Privacy Context is defined during MediaSpace installation or using the KMC.

<ol style="list-style-type: lower-alpha;">
  <li>
    In the KMC, select the Content tab and then select the Categories tab.
  </li>
  <li>
    In the Categories table, click the root category name.
  </li>
  <li>
    On the Edit Category window, select the Entitlements tab.
  </li>
  <li>
    Under Privacy Context Label, confirm that a value is displayed. <br /><img src="{{site.url}}/assets/622">
  </li>
</ol>

<p class="mce-heading-2">
  Uploading MediaSpace Content
</p>

<p class="mce-procedure">
  To upload initial content for MediaSpace in the KMC
</p>

In the KMC, select the Upload tab and then do one of the following:

*   Click **Upload from Desktop**.  
    Use this option to upload a small number of files.
*   Under Submit Bulk, select **Entries CSV/XML**.  
    Use this option to upload a large number of files. Using this option, you also import metadata such as categories and tags.  
    <img src="{{site.url}}/assets/626">

 To learn more about uploading and ingestion, refer to the <a href="http://knowledge.kaltura.com/node/888/attachment/field_media" target="_blank">Kaltura Management Console (KMC) User Manual</a>.

<p class="mce-heading-2">
  Setting up MediaSpace Categories in the KMC
</p>

After you [set up a MediaSpace category tree][1], you canyou can create categories and channels.

 [1]: #TosetupaMediaSpacecategorytree

To learn more about Creating and Managing Content Categories, see see [How to Create and Manage Content Categories][2]?

 [2]: http://knowledge.kaltura.com/node/338

<p class="mce-procedure">
  To add MediaSpace categories manually in the KMC
</p>

1.  In the KMC, select the Content tab and then select the Categories tab.
2.  Click **Add Category**.
3.  Add a category  under [MediaSpaceroot]>Site>Galleries, and save your new category.  
    You can create up to seven levels of sub-categories.     

<p class="mce-procedure">
  To create MediaSpace categories in bulk in the KMC
</p>

1.  In the KMC, select the Upload tab and, under Submit Bulk, select **Categories CSV**.
2.  Specify the path for the gallery categories under [MediaSpaceroot]>Site>Galleries.

<p class="mce-procedure">
  To specify the order of MediaSpace gallery categories in the KMC
</p>

<p style="padding-left: 30px;">
  By default, categories in MediaSpace are displayed by creation date (the most recent appears last). To modify the gallery display order in MediaSpace, you specify the order of your gallery categories in the KMC.
</p>

1.  In the KMC, select the Content tab and then select the Categories tab.
2.  Click **galleries **in the Categories table to open the Edit Category window.  
    <img src="{{site.url}}/assets/629">
3.  On the Edit Category window, select the Sub Categories tab (displayed only when there is more than one sub‑category):  
    <img src="{{site.url}}/assets/630">
4.  Specify the order of the sub-categories using the Up and Down arrows, and click **Save**.
5.  Repeat for additional sub-category levels under *galleries*.

<p class="Procedure mce-procedure">
  To set the owner of a category manually in the KMC
</p>

By default, categories in MediaSpace are added without an owner. To delegate the management of a specific category to a MediaSpace user and allow that user to configure that category and manage members, you should assign the appropriate MediaSpace user as the category owner.

1.  In the KMC, select the Content tab and then select the Categories tab.
2.  Search for the category that you want to set the owner for, and open the Edit Category window.
3.  On the Edit Category window, select the Entitlements tab. You will notice that the “Owner” is not specified.  
    <img src="{{site.url}}/assets/1178">
4.  Click Change.
5.  Enter the user name or user ID of the appropriate owner for this category and click Save.

<p style="padding-left: 30px;">
   <img src="{{site.url}}/assets/1179">
</p>

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">A<a name="assigning_content_2cats"></a>ssigning Content to you MediaSpace Categories</span>

After your category structure is set up, you can assign content to your categories.

You can add entries to categories in the KMC on the Upload tab's Submit Bulk menu using the Entries CSV/XML option. Categories that do not exist are created when you submit the file. To display these categories in MediaSpace, specify the [MediaSpace Root]>site>galleries path.

To learn more about Assigning Content to Categories, refer to <a href="http://knowledge.kaltura.com/node/368" target="_blank">How to create Categories and Assign Entries to a Category</a>.

<p class="mce-procedure">
  To manually assign content to a MediaSpace category in the KMC
</p>

1.  In the KMC, select the Content tab and then select the Entries tab.
2.  In the Entries table, select one or more entries and click **Bulk Actions**.
3.  Select Add/Remove Categories and click **Add to Categories**.  
    <img src="{{site.url}}/assets/631">
4.  On the Select Categories window, under the *galleries* category, select one or more categories and click **Apply**:  
    <img src="{{site.url}}/assets/632">
5.  In the Entries table, the entries are displayed for the category you used as a filter.

<p style="padding-left: 30px;">
  <img src="{{site.url}}/assets/633">
</p>

Also see [Assigning MediaSpace Content to Ca][3]tegories.

 [3]: #Assigning_MediaSpace_Content

<p class="mce-procedure">
  To change an entry’s MediaSpace content owner in the KMC
</p>

Usually, the user who uploads content in the KMC is not the administrative content owner of the media entry. 

*   Refer to <a href="http://knowledge.kaltura.com/node/636" target="_blank">How to change the category owner in the KMC or KMS</a>.

<p class="mce-heading-3">
  <a name="Adding_contributors_to_KMS_Galleries"></a>Adding Members and Contributors via the KMC
</p>

<p class="mce-procedure">
  To add a user as a contributor to a MediaSpace gallery in the KMC
</p>

1.  In the KMC, select the Content tab and then select the Categories tab.
2.  In the Categories table, click the category name.
3.  On the Edit Category window, select the Entitlements tab.
4.  Under Specific End-User Permissions, click **Manage**.  
    <img src="{{site.url}}/assets/636">
5.  On the Specific End-User Permissions window, click **Add Users**.  
    <img src="{{site.url}}/assets/637">
6.  On the Add Users window, under Permission Level select **Contributor**.
7.  On the Add Users window, under Select End-Users start typing a user name. A list of suggestions is displayed after you type the third character.  
    <img src="{{site.url}}/assets/638">
8.  On the Add Users window, select a user from the suggestion list and click **Save**.   
    In MediaSpace, the selected user will have the Add Media option for the specified gallery. 

<p class="mce-heading-2">
  Setting up MediaSpace Channels
</p>

Setting up MediaSpace channels in the KMC is similar to setting up categories. To learn about what’s unique for channels, see  [Assigning User Permissions to MediaSpace Channels in the KMC][4].[  
][5]

 [4]: #Assigning_User_Permissions
 [5]: file:///C:/Users/Debbie/Documents/Mediaspace/MediaSpace5/Setup%20Guide/Kaltura_MediaSpace_Setup_Guide_5.0.docx#_Assigning_User_Permissions

<p class="mce-heading-3">
  <span style="font-size: 14pt;">Displaying Channels in MediaSpace</span>
</p>

This section describes the following topics:

<p class="mce-heading-3">
   
</p>

*   [Adding a Link to the Channels Page and My Channels in the Top MediaSpace Navigation][6]
*   [Adding a Link to My Channels in the MediaSpace Header Menu][7]
*   [Associating Channels to Categories][8]

 [6]: #add_a_link
 [7]: #add_a_link_header
 [8]: #associating_channels2cats

<p class="mce-procedure">
  To <a name="add_a_link"></a>add a link to the Channels page and My Channels in the top MediaSpace navigation
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Navigation tab.
2.  Under *pre*:
<ol style="list-style-type: lower-alpha;">
  <li>
    In the <em>type</em> menu, select <strong>Channels Page</strong> or <strong>My Channels</strong>.
  </li>
  <li>
    In the <em>name</em> field, enter the label to display.<br /><img src="{{site.url}}/assets/1194">
  </li>
</ol>

3.  Click **Save **to display the link in the top MediaSpace header menu. 

<p class="mce-procedure">
  To <a name="add_a_link_header"></a>add a link to My Channels in the header menu
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Headermenu tab.
2.  Under *enabled*, select **Yes** to enable the Headermenu module.
3.  Under *menu*:
<ol style="list-style-type: lower-alpha;">
  <li>
    In the <em>type</em> menu, select <strong>My Channels</strong>.
  </li>
  <li>
    In the <em>label</em> field, enter the label to display.<br /><img src="{{site.url}}/assets/641">
  </li>
</ol>

4.  Click **Save **to display the link in the MediaSpace header menu. 

<h4 class="mce-heading-4">
  <a name="associating_channels2cats"></a>Associating Channels to Categories
</h4>

When you create a channel, you can associate a channel to a category. When users navigate to a category page, they will be able to browse the media and also the channels associated with that category.

<p class="mce-procedure">
  To enable associating channels to categories when creating a channel
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Channelcategories tab.
2.  <img src="{{site.url}}/assets/1195">
3.  Under enabled, select Yes to enable the Channelcategories module.
4.  Click Save. 

<p class="mce-heading-3">
  <a name="SettingPermissionsforCreatingMediaSpaceChannel"></a>Setting Permissions for Creating a MediaSpace Channel
</p>

See [Who can create a channel?][9]

 [9]: http://knowledge.kaltura.com/node/615#Whocancreateachannel

<p class="mce-procedure">
  To define a user role with permissions to create a channel
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Channels tab.
2.  Under *channelCreator*, select one of the following roles, and click **Save**.

*   **Sys Admin** – Channels can be created *only* from the KMC by the KMC admin user.
*   **viewerRole** – All authenticated users
*   **privateOnlyRole** – All users with upload permissions
*   **adminRole **– All users with permission to upload and publish to categories
*   **unmoderatedAdmin** – All users with permission to upload and publish to categories and to bypass moderation (if moderation is enabled)  
    <img src="{{site.url}}/assets/642">

We do not recommend enabling a Viewer to create channels since Viewers cannot add content to channels they create.

When a user has permissions to create a channel, a *Create Channel* button is displayed on Channel Listing pages.

<p class="FigureList">
  <img src="{{site.url}}/assets/1196">
</p>

<p class="mce-heading-3">
  <a name="Assigning_MediaSpace_Content"></a>Assigning MediaSpace Content to Channels
</p>

<p class="mce-procedure">
  To manually assign content to a MediaSpace channel in the KMC
</p>

1.  In the KMC, select the Content tab and then select the Entries tab.
2.  In the Entries table, select one or more entries and click **Bulk Actions**.
3.  Select Add/Remove Categories and click **Add Categories**.   
    <img src="{{site.url}}/assets/1197">
4.  On the Select Categories window, under the channels category, select one or more categories and click **Apply.**  
    In the Entries table, the entries are displayed when you filter for a category to which you assigned the entries.  
    Also see [Assigning MediaSpace Content to Categories][10].

 [10]: #assigning_content_2cats

<p class="mce-heading-2">
  Assigning User Permissions to MediaSpace Channels
</p>

To assign user permissions in bulk, use the <a href="http://knowledge.kaltura.com/node/466" target="_blank">End-User Entitlements CSV</a>. To learn more about assigning end user permissions, refer to the [Kaltura Management Console (KMC) User Manual][11].

 [11]: http://knowledge.kaltura.com/node/888/attachment/field_media

To learn more about entitlement services and how they apply to MediaSpace permissions, refer to [Introduction to the Kaltura Entitlement Infrastructure][12].

 [12]: http://knowledge.kaltura.com/node/475

<p class="mce-heading-3">
  <a name="Assigning_User_Permissions"></a>Assigning User Permissions to MediaSpace Channels in the KMC
</p>

By default, a channel that you create in the KMC is restricted to authorized users. Handling permission restrictions for channels is similar to the way you handle permissions for galleries. See [Adding Contributors to MediaSpace Galleries][13].

 [13]: #Adding_contributors_to_KMS_Galleries

In addition, you perform the following important flows related to channels in the KMC:

*   [Assigning Managers to a MediaSpace Channel][14]
*   [][15][Assigning User Permissions to a Channel in MediaSpace][16]

 [14]: #AssigningManagersandModerators
 [15]: #ListingMediaSpaceChannels
 [16]: #assigning_user_permissions

<p class="mce-heading-3">
  <a name="AssigningManagersandModerators"></a>Assigning Managers to a MediaSpace Channel
</p>

To access channel settings in MediaSpace, a user must have Manager or Moderator permissions for the channel. To learn more about channel settings, refer to the [Kaltura MediaSpace User Manual][11].

<p class="mce-procedure">
  To assign a manager to a MediaSpace channel in the KMC
</p>

1.  In the KMC, select the Content tab and then select the Categories tab.
2.  In the Categories table, click the channel category name.
3.  On the Edit Category window, select the Entitlements tab.
4.  Under Specific End-User Permissions, click **Manage**.
5.  On the Specific End-User Permissions window, do one or more of the following:

*   In the user list, select one or more users and change the user permission to Manager.
*   Click **Add Users**.
*   On the Add Users window, under Permission Level select **Manager**.
*   On the Add Users window, under Select End-Users start typing a user name. A list of suggestions is displayed after you type the third character.
*   On the Add Users window, select a user from the suggestion list and click **Save**.

<p class="mce-note-graphic">
  A MediaSpace end user who creates a channel can assign permissions, including adding managers and moderators.
</p>

<span class="mce-heading-3">A<a name="assigning_user_permissions"></a>ssigning User Permissions to a Channel in MediaSpace</span>

Channel managers and owners can add members and change user permissions in MediaSpace.

<p class="mce-procedure">
  To edit channel members and permissions in MediaSpace
</p>

1.  In MediaSpace, on the Channels page or your My Channels page, click a channel to open the channel page, and then click Actions and select Edit.
2.  On the Members tab:

*   To modify the member's permission level, next to the member's Permission column, click the **Pencil **icon, select a new permission, and click **Done**.
*   To remove the member from channel membership, click **X **icon.
*   To add a member and assign a permission level to the new member, click **Add Member, **enter a user name and select a permission, and click **Add**.

<span class="mce-note-graphic">This operation is available to current owner only and will </span><strong class="mce-note-graphic">transfer</strong><span class="mce-note-graphic"> ownership from you to selected member.</span>

<img src="{{site.url}}/assets/1198">

To learn more about editing channel users, refer to the [Kaltura MediaSpace User Manual][17].

 [17]: http://knowledge.kaltura.com/node/918/attachment/field_media

<p class="mce-heading-3">
  Setting up MediaSpace to Run on HTTPS
</p>

You can configure MediaSpace to run on HTTPS.

<p class="mce-procedure">
  To run MediaSpace on HTTPS
</p>

Do one of the following:

*   Use HTTPS for login only.

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.
2.  Under *sslSettings*, select **Login only** and click **Save.**   
    <img src="{{site.url}}/assets/1199">
3.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Client tab.
4.  Under serviceUrl, enter an HTTP URL and click Save.  
    <img src="http://cdnknowledge.kaltura.com//sites/default/files/styles/large/public/KMS4_Setup_serviceUrl_htpp.png" border="0" alt="" width="640" height="71" />

*   Use HTTPS for your MediaSpace site.

NOTE: To run MediaSpace on HTTPS, contact your Kaltura Project Manager or Account Manager for assistance. Do not attempt to run MediaSpace on HTTPS before consulting your Kaltura representative. Implement the following procedure when your Kaltura representative instructs you to do so.

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.
2.  Under *sslSettings*, select **All site** and click **Save**.  
    <img src="{{site.url}}/assets/1201">
3.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Client tab.
4.  Under serviceUrl, enter an HTTPS URL and click Save.   
    <img src="{{site.url}}/assets/1202">