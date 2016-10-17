---
layout: page
title: "Additional Integration Points for the Kaltura Video Module for Drupal"
date: 2012-05-13 19:37:54
---

<h1 class="mce-heading-2">
  Additional Integration Points
</h1>

This article describes additional ways to integrate the Kaltura Video Module to Drupal. The following topics are described:

*   [Synchronizing the Kaltura Publisher Account to Drupal][1]
*   [Editing Content Metadata][2]
*   [Configuring Kaltura Module Settings for Mobile][3]
*   [Drupal Views Integration][4]
*   [Integration with the Drupal Permissions][5]

 [1]: #sync
 [2]: #edit
 [3]: #config
 [4]: #views
 [5]: #permissions

<span class="mce-heading-3"><a name="sync"></a>Synchronizing the Kaltura Publisher Account to Drupal</span>

There are several levels of synchronizing your Kaltura publisher account to Drupal.

*   **Automatic** – server side notifications  
    Server side notifications update the Drupal with events occurring in your Kaltura account outside the Drupal site.   
    These events include, for example:  
    *   New entries added
    *   Update of metadata and thumbnail of existing entries
    *   Deletion of existing entries
      
    These notifications are set in your Kaltura account. You can modify the notification settings in the KMC. For more information, see the [Knowledge Center][6].

 [6]: http://knowledge.kaltura.com/faq/what-types-notifications-are-there-kmc

*   **On-demand** – import  
    You can sync content through the Configuration tab. In the Media section, select Kaltura module settings and then select the Importing Entries from Kaltura to Drupal tab.  See [On-demand import][7].

 [7]: #on_demand

*   **Scheduled  
    **You can add Kaltura API calls and actions on the Drupal database to a CRON job. This option is for advanced Drupal users.

Content that is contained in your Kaltura account is the media that is synced to Drupal. Content that is edited (metadata) in Drupal is also synced to Kaltura. See [Editing Content Metadata][2] for more information.

Depending on your workflow, you may select different syncing methods that can be used simultaneously. For example, you may want to have each entry in your Kaltura account synced for use at a later time, regardless where it was uploaded from. To use this type of synching you will need to turn on the relevant notifications in the KMC. Or, for example, you may want to select certain entries from the content in your Kaltura account for Drupal site content editors to use. Select the On-demand option to synchronize this type of scenario.

Another example is you may have existing content on you Kaltura account that was uploaded before you added the Drupal module and would like to use the content. Use the On-demand option and then turn on the automatic process to ensure that all additional content from Kaltura will be uploaded.

<p class="Procedure mce-procedure">
  To import content into Drupal using the <a name="on_demand"></a>On-demand mode
</p>

1.  Go to Configuration.
2.  In the Media section, select Kaltura module settings and then select the Importing Entries from Kaltura to Drupal tab.   
    The list of media entries in your Kaltura account that have not been synced to the Drupal server are displayed.
3.  Check “Check all”, to import all the entries that are on the page, or, check the individual entries you want to import.
4.  Click Import Selected.

<h2 class="mce-heading-3">
  <a name="edit"></a>Editing Content Metadata
</h2>

You may want to edit the metadata for content that you have uploaded and synced to the Drupal site.

<p class="Procedure mce-procedure">
  To edit content metadata in Drupal
</p>

1.  Select the Configuration tab.
2.  In the Media section, select Kaltura module settings and then select the Importing Entries from Kaltura to Drupal tab.
3.  Click on the List of Kaltura Items tab and then click Edit Metadata.
4.  Modify the metadata information. You can edit the Title, Description and Tags fields, and then click** **Submit.

The metadata is synchronized to your KMC content through the Kaltura API.

<h2 class="mce-heading-3">
  <a name="config"></a>Configuring Kaltura Module Settings for Mobile
</h2>

Several mobile platforms do not support Flash plugins and subsequently the video tag is the exclusive mechanism to distribute video in these mobile HTML browsers.

<p class="Procedure">
       <span class="mce-procedure">To configure the Kaltura Media field for HTML5 encoding</span>
</p>

1.  Select the Configuration menu.
2.  In the Media section select Kaltura Module Settings.
3.  Click on the Kaltura Settings tab.
4.  Check the Support iPhone and iPad with HTML5 box and click Submit.

<h2 class="mce-heading-3">
  <a name="views"></a>Drupal Views Integration
</h2>

The Kaltura Module is fully integrated with Drupal Views. You can create a dynamic display of filtered Kaltura content using Drupal Views. Default Views are provided with the Kaltura Module.

The following shows an example of editing a View that is using Kaltura content. This specific example is one of the predefined views where <span>The Filter is set to image, and the sort a criterion is set to created date.<br /><img src="../../assets/495.img">

A View that contains Kaltura content may also be configured and displayed as a block to allow greater design flexibility for your site.

<h2 class="mce-heading-3">
  <a name="permissions"></a>Integration with Drupal Permissions
</h2>

Permissions let you control what users can do and see on your site. There are four Kaltura permissions that are integrated with the Kaltura Drupal Module. 

*   Administer Kaltura
*   Access Kaltura Widgets
*   View Kaltura embed code
*   Edit Kaltura Metadata