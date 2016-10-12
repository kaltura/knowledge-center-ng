---
layout: page
title: "Kaltura Distribution Module"
date: 2012-02-24 01:15:50
---

Kaltura’s Distribution Module allows you to reach your users on the web and across any mobile device. The module provides a streamlined and simple workflow so you can distribute your content to distribution partners, such as YouTube, Hulu, Comcast, MySpace, MSN or an FTP drop folder, directly from within the KMC.

### Key Benefits:

*   Full control over where and when the content is presented.
*   Manage all of your distribution partners through a single user-friendly interface
*   Deliver assets automatically as they are added to your Kaltura account, or require a manual review, at your discretion
*   Seamlessly push updates to distributed content from a central dashboard
*   Control scheduling sunrise and sunset per asset and per distribution partner
*   Track your content across all distribution partners
*   Simple and straightforward pricing, with no hidden fees or “guesstimates”
*   Kaltura’s system validates content to make sure it’s ready to be distributed to each distributor, and alerts about any errors that need to be fixed prior to distribution (missing thumbnails, missing metadata, etc.)
*   Successful delivery to each distribution partner is confirmed for each asset (if supported by the partner)

## <a name="distribution_work"></a>How Does Distribution Work?

Distribution ensures that your content is viewed by as many customers as possible across multiple video destination sites and improves total views for your content. Kaltura pushes the actual contents of the video assets to distribution partners for them to host on their sites.  Each distribution channel is unique and depends on the distributor’s capabilities and the extent of their desired exposure.

The Kaltura Distribution Module supports several workflows. You can configure simple as well as complex asset information to distribute. For example, simple asset information may include the entry name, description and tags, or metadata alone, that may be used for example, to configure ads based on metadata. More complex distribution data is configurable by your project manager and depends on the distributor’s capabilities.

You can define the destinations for each video package and control aspects such as the video qualities, number and size of thumbnails, metadata, and scheduling data for each distribution destination.

You can display distributors for each entry, the distribution start and end dates, submission status.

<p class="mce-note-graphic">
  <span style="font-size: x-small;">NOTE: You can distribute ALL videos to be pushed automatically to the destination or you can distribute selected entries MANUALLY to be sent to the destination.</span>
</p>

<p class="mce-note-graphic">
  <span style="font-size: x-small;">NOTE: Tag based or Rule Based distribution options are currently not available. You can either distribute ALL entries or NONE. If none, you can manually select which entries will be distributed to the destination.</span>
</p>

A sample distribution configuration may contain the following components for an entry: video, metadata, thumbnail, scheduling, content availability by Kaltura and removal of distributed content.

The Distribution Module can be configured to update distributed content for metadata, so that the most updated information is propagated to the distribution site. Other customizable parameters may be configured for distribution. The Distribution Module also can be configured to remove distributed content for metadata, so that information that was propagated to the distribution site can be retracted.

With the Kaltura Distribution Module, administrators can control the destinations for each video package, and for each distribution destination. In addition, administrators can control video transcodes, multiple thumbnails in different sizes, metadata translations, scheduling data, and more.

The Distribution Module is an add-on module to the KMC, and incurs additional fees based on the amount of distribution destinations supported for your account. Additional connectors to distribution destinations can also be developed as custom work.  Contact your Kaltura project manager or sales representative for complete pricing.

### Adding a Distributor to an Entry

<p class="Note mce-note-graphic">
  <span style="font-size: x-small;">NOTE: To enable automatic distribution of all new entries, <a href="http://corp.kaltura.com/about/contact">contact us</a>, or call +1-800-871-5224. To add more distribution destinations, contact your project manager.</span>
</p>

<p class="Procedure">
  <span class="mce-procedure"><a name="select_distributors"></a>To select distributors</span>
</p>

1.  Check the distributors from the Distributor list.  Click All or None at the top of the column to select or clear all the items in a column.
2.  Check the Distribute Automatically column to distribute an entry as soon as it is ready. Click All or None at the top of the column to select or clear all the items in a column. <span style="text-align: left;">All includes all distributors. For example, if you have configured Daily Motion and YouTube as distributors, content will be distributed to both destinations.</span>
3.  Click Apply to save your changes and return to the Distribution tab.
4.  Click Save Changes to complete the process.

## Scheduling a Video Package

By default, an entry's general scheduling is inherited by all distributors. The instructions here are for setting scheduling for a specific distributor. A Remote ID is the ID assigned to the distributed content in the distributor, and is only available after content has been distributed. The Remote ID may be used as a response from the distributor as well as a reference, for example, to reach the page where the distributed content appears in the distributor.

<p class="Procedure">
  <span class="mce-procedure"><a name="schedule"></a>To schedule when an entry should be distributed</span>
</p>

1.  Select the Content tab and select the Manage menu.
2.  In the Entries Table, click the name of the entry that you want to schedule.
3.  In the Edit Entry window, select the Distribution tab and then select the name of a distributor. The Distribution Details window is displayed.
4.  Set the Start Date and End Date and enter the hour.
5.  Click Save to return to the Distribution menu.
6.  Click Save and Close to complete the process.

### Validating a Video Package

Errors may occur when you specify a video package distributor.

<p class="Procedure mce-procedure">
  To find and resolve errors
</p>

1.  Go to the Content tab and select Manage from the menu.
2.  In the Entries Table, click the name of an entry for which you added a distributor.
3.  In the Edit Entry window, go to the Distribution tab and click the error name in the Submission Status column to display a description of the error. You can also click on the Distributor in the Distribution tab, and then click the error name in the Distribution Details window.
4.  Follow the instructions in the error description.

The following errors may occur:

<p class="Sub-Heading">
  <strong>Missing Flavor Error</strong>
</p>

<p class="Procedure">
  <span class="mce-procedure">To add a flavor</span>
</p>

<p class="Procedure" style="padding-left: 30px;">
  If you click "Go to Flavors Tab" in the error description, skip to step 4.
</p>

1.  Go to the Content tab and select the Manage menu.
2.  In the Entries Table, click the name of the entry that is missing a flavor.
3.  In the Edit Entry window, go to the Flavors tab.
4.  In the Action column, click Convert or Reconvert for each transcoding flavor specified in the error description, and click Save Changes.

<p class="Subheading">
  <strong>Metadata Error</strong>
</p>

<p class="Procedure mce-procedure">
  To correct metadata
</p>

<p style="padding-left: 30px;">
  If you click "Go to Metadata Tab" in the error description, skip to step 4.
</p>

1.  Go to the Content tab and select the Manage menu.
2.  In the Entries Table, click the name of the entry that has a metadata error.
3.  In the Edit Entry window, go to the Metadata tab or the Custom Data tab.
4.  Modify the information in the metadata field specified in the error description, and click Save and Close. If the submission status error is still displayed in the Edit Entry window's Distribution tab: go back to the Edit Entry window, and select the Custom Data tab.
5.  Add the missing information specified in the error description, and click Save and Close.

<p class="Subheading">
  <strong>Missing Thumbnail Error</strong>
</p>

<p class="Procedure mce-procedure">
  To add a thumbnail
</p>

1.  Go to the Content tab and select the Manage menu.
2.  In the Entries Table, click the name of the entry that is missing a thumbnail.
3.  In the Edit Entry window, go to the Thumbnails tab.
4.  Click Add Thumbnail and select Grab from Video.
5.  If you have a thumbnail file, select Upload, specify the file location and name, and click Open.
6.  Play the video, pause on the frame you want, and click the thumbnail capture buon.A thumbnail will be captured from the highest quality video flavor.
7.  Exit to return to the Thumbnails window.

<p class="Procedure">
  <span class="mce-procedure">To modify the thumbnail dimensions</span>
</p>

1.  In the Edit Entry window, click **Add Thumbnail** and‎ select New Crop.
2.  Select the Thumbnail to modify.
3.  Check the Lock aspect ratio and scale to option and select the values specified in the error description.
4.  Adjust the display area with the handles on the image.
5.  Click Generate Thumbnail, and exit to return to the Thumbnails window.Click Save Changes to complete the process.

#### Filtering Distributed Content

<p class="Procedure mce-procedure">
  To display distributed content in the Entries Table
</p>

1.  Go to the Content tab and select the Manage menu.
2.  ** **Select the Distribution filter and click a destination you want to display. Only entries that are active for the selected destination are displayed in the Entries Table.

 

<p class="Procedure mce-procedure">
  To clear the distribution filter
</p>

*   Click the destination name in the Distribution filter again.

### <a name="remove"></a>Removing a Distributor from a Video Package

You may want to change your distribution destinations for video packages.

<p class="Procedure mce-procedure">
      To remove a distributor from a video package
</p>

1.  Go to the Content tab and select the Manage menu.
2.  In the Entries Table, click the name of the entry with a distributor that you want to remove.
3.  In the "Edit Entry" window, go to the "Distribution" tab and click "Add / Remove Distributors".
4.  In the "Add / Remove Distributors" window, clear a distributor checkbox. To clear all items in a column, click "None" at the top of the column.
5.  Click Apply to save your changes and return to the Distribution tab.
6.  Click Save Changes to complete the process.

### Managing Distributor Details

<p class="Procedure mce-procedure">
      To manage an entry's distributor details
</p>

1.  Click the distributor's name on the "Distribution" tab.  In the "Distribution Details" window, you can see the distributor's distribution details (status, remote ID and schedule), the entry's metadata details, the available thumbnails and the video flavors.
2.  In the "Distribution Details" section:
3.  To fix an error, click the error name to display an error description and follow the instructions.
4.  To schedule when an entry is available at the distributor, set the start and end dates and times, and click "Save".  You can set scheduling separately for each distribution so that the same content may have a different schedule depending on the distributor.
5.  In the "Thumbnails" section, Thumbnails are matched to the distribution point's required thumbnail size.  If you have multiple thumbnails of the same size, click "Swap" to manually select the one you want.
6.  In the "Video Flavors" section, to preview the entry in a specific flavor, click "Preview" and play the entry in the "Flavor Preview" window.