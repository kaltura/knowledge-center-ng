---
layout: page
title: "Kaltura Media Fields for the Drupal Video Module"
date: 2012-05-13 16:12:12
---

<h1 class="mce-heading-2">
  Kaltura Media Fields
</h1>

Kaltura integrates with Drupal 7 at a field level, providing the granularity for integration with a variety of Drupal implementations. . As other fields in Drupal, the Kaltura Media Field may be added to content types, comments, user profiles and all other types of blocks of content.

The Kaltura Media field may be configured to allow certain media types (i.e. video, audio, image), for different display options, and for different media contribution options. These configuration options synergize with Drupal’s innate field and content types configuration, like permissions and displays, and together enable easily building of media use-cases that apply to you.

<h2 class="mce-heading-3">
  Using the Kaltura Media Field in a Content Type
</h2>

This section contains the following topics:

*   [Adding the Kaltura Media Field][1]
*   [Configuring Settings for the Kaltura Media Field][2]
*   [Kaltura Media Field Contribution Elements][3]
*   [Managing the Content Type Display][4]
*   [Populating Kaltura Media Fields with Content][5]

 [1]: #adding_KMF
 [2]: #configuring
 [3]: #contribution
 [4]: #managing
 [5]: #populating

## <a name="adding_KMF"></a><span class="mce-heading-3">Adding the Kaltura Media Field</span>

<p class="Procedure mce-procedure">
  To add the Kaltura Media Field
</p>

1.  Select the Structure tab and in the Label column, select a Content type.
2.  In the Operations column, select manage fields. The Manage Fields tab is displayed.
3.  Enter a field name in the Add new field box.
4.  In the Name column, enter the name of the field in lower case. This is the field name that Drupal will identify.
5.  In the Field column, select **Kaltura Media field.**
6.  Select a widget from the Widget column drop down. See [Widget Types.][6] The widget you select forms the appropriate element to edit your data.
7.  Click Save and continue to configure the settings for the Kaltura Media field. Depending on your widget choice, a configuration window for the field is displayed.

 [6]: #widget

The following is an example of a Kaltura Media field created for uploading video only.

<img src="{{site.url}}/assets/471">

<p class="mce-heading-3">
   <a name="configuring"></a>Configuring Settings for the Kaltura Media Field
</p>

This section describes the options and settings for the Kaltura Media field. All Kaltura features such as setting the conversion profile and CDN configuration work for out of the box and can be set within the Kaltura Management Console. See the [KMC User Manual][7] for more information.

 [7]: http://knowledge.kaltura.com/sites/default/files/Kaltura_Management_Console_%28KMC%29_User_Manual_3.pdf

<h3 class="mce-heading-4">
  <a name="contribution"></a>Kaltura Media Field Contribution Elements
</h3>

You can define two types of contribution elements for the Kaltura Media field:

*   [Widget Types][6]
*   [Add Media Settings ][8]

 [8]: #add_media

### <a name="widget"></a><span class="mce-heading-4">Widget Types</span>

The widget determines the types of media you can propagate to the Kaltura Media field. This applies to both uploading new content from the Kaltura Contribution Wizard and re-using existing content. The following lists the types of widgets that you can set for a Kaltura Media Field.

*   [Video Only][9] – allows you to upload only videos through the Kaltura Contribution Wizard. Use only when the Add Media Settings are set to Add new media.
*   [Audio Only][10] - allows you to upload only audio files through the Kaltura Contribution Wizard. Use only when the Add Media Settings are set to Add new media.
*   [Image Only][11] - allows you to upload only image files through the Kaltura Contribution Wizard. Use only when the Add Media Settings are set to Add new media.
*   [All Media Types][12] - allows you to upload all three types of content, video audio,  and image through the Kaltura Contribution Wizard
*   [Webcam][13] – allows you to record from webcam only. Note that when using this type of widget it is recommended to set the field to “add new media” only, for obvious reasons.

 [9]: #video_only
 [10]: #audio_only
 [11]: #image_only
 [12]: #all_media
 [13]: #webcam

See the article on [Kaltura Contribution Wizard (KCW)][14] for more information and supported formats.

 [14]: http://knowledge.kaltura.com/kaltura-contribution-wizard-kcw

### <a name="add_media"></a><span class="mce-heading-4">Add Media Settings</span>

The Add Media Settings options are dependent on the widget type selected when you define the Kaltura Media field. The following settings are available:

*   **Add new media only **- allows you to upload new media only
*   **Use existing media only **- allows you to choose from uploaded and synced content only
*   **Use existing media and add new media **– allows you to upload new media and choose from existing uploaded content

When you add new media, content is uploaded to your Kaltura account as well as synced to the Drupal database

<p class="Procedure mce-procedure">
  To change the widget type
</p>

1.  Select the Structure tab and then select a content type.
2.  In the Operations column, select manage fields.
3.  In the Widget column, click on the widget type. The Change Widget panel is displayed.  
     <img src="{{site.url}}/assets/473">
4.  Change the Widget type and click Continue.

<h3 class="mce-heading-4">
  <a name="video_only"></a>Video Only
</h3>

<p class="Procedure mce-procedure">
  To configure the Kaltura Media Field settings for the video only widget
</p>

1.  In the Manage Fields tab, click on edit in the Operations column.
2.  Configure the following field settings:  
    **[PLAYER SETTINGS][15]  
    ******[THUMBNAIL SETTINGS][16]  
    [**CONTENT INGESTION** ][17]****
3.  Click Save field settings.

 [15]: #player_settings
 [16]: #thumbnail_settings
 [17]: #content_ingestion

**<a name="player_settings"></a>PLAYER SETTINGS**

**<img src="{{site.url}}/assets/479">

**<img src="{{site.url}}/assets/480">

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="139">
        <p class="TableHeading">
          <strong>Name</strong>
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableHeading">
          <strong>Comments</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          Video Player
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          Select a player from the list of players that are configured in your KMC.
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          Create new player
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          Click to create a new player in the KMC.
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          You will be prompted for your Kaltura credentials to access you KMC account.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          Player Width
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          You can change the player Width to accommodate your display per field.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          Default value: 400<em></em>
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          Sets the default value for this field. This value may be overridden in the display settings per field instance,
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          Player Height
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          You can change the player Height to accommodate your display per field.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          Default value: 330
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          Sets the default value for this field. This value may be overridden in the display settings per field instance,
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          Delivery Type
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          Select from the dropdown options:
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          <img src="{{site.url}}/assets/481">
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          See the <a href="http://knowledge.kaltura.com/sites/default/files/Kaltura_Management_Console_%28KMC%29_User_Manual_3.pdf">KMC User Manual </a>for more information.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          ADVANCED
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          Click Advanced to choose a player that is not configured in your Kaltura account. The Advanced option opens the Custom Player UI_Conf field where you can enter the UIconf ID for the player you want to use.
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          This option is intended for advanced Kaltura users and for Kaltura support and administrators.
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

**<a name="thumbnail_settings"></a>THUMBNAIL SETTINGS**

**<img src="{{site.url}}/assets/482">

This section is relevant when selecting a thumbnail display for the Kaltura Media field. See [Managing the Content Type Display][4].

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="139">
        <p class="TableHeading" style="text-align: left;">
          <strong>Name</strong>
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableHeading" style="text-align: left;">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableHeading" style="text-align: left;">
          <strong>Comments</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          Thumbnail Width
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          Enter the thumbnail width.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          Default value: 80
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          Sets the default value for this field. Per field instance it can be overridden in the display settings.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          Thumbnail Height
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          Enter the thumbnail height.
        </p>
        
        <p class="TableBodyText" style="text-align: left;">
          Default value: 45
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          Sets the default value for this field. Per field instance it can be overridden in the display settings.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="139">
        <p class="TableBodyText" style="text-align: left;">
          Rotate Thumbnails for  Video Items
        </p>
      </td>
      
      <td valign="top" width="257">
        <p class="TableBodyText" style="text-align: left;">
          Check to show a thumbnail slideshow preview of the video when hovering over the thumbnail
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

**<a name="content_ingestion"></a>CONTENT INGESTION**

**<img src="{{site.url}}/assets/483">

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="173">
        <p class="TableHeading">
          <strong>Name</strong>
        </p>
      </td>
      
      <td valign="top" width="223">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableHeading">
          <strong>Comments</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="173">
        <p class="TableBodyText" style="text-align: left;">
          Advanced
        </p>
      </td>
      
      <td valign="top" width="223">
        <p class="TableBodyText" style="text-align: left;">
          Enter the Custom uploader widget ui_conf
        </p>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          The Advanced Content Ingestion settings are intended for the use of advanced Kaltura users.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="173">
        <p class="TableBodyText" style="text-align: left;">
          Add Media Settings
        </p>
      </td>
      
      <td valign="top" width="223">
        <p class="TableBodyText" style="text-align: left;">
          Select one of the following options:
        </p>
        
        <ul>
          <li style="text-align: left;">
            Add new media only
          </li>
          <li style="text-align: left;">
            Use existing media only
          </li>
          <li style="text-align: left;">
            Use existing media and add new media
          </li>
        </ul>
      </td>
      
      <td valign="top" width="172">
        <p class="TableBodyText" style="text-align: left;">
          See <a href="#add_media">Add Media Settings</a>.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="173">
        <p class="TableBodyText" style="text-align: left;">
          Add Media Button Label
        </p>
      </td>
      
      <td valign="top" width="223">
        <p class="TableBodyText" style="text-align: left;">
          Enter an intuitive name for the add media button label.
        </p>
      </td>
      
      <td valign="top" width="172">
        <p>
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

<h3 class="mce-heading-4">
  <a name="audio_only"></a>Audio Only
</h3>

<p class="Procedure">
  <span class="mce-procedure">To configure settings for the audio only widget</span>
</p>

1.  In the Manage Fields tab click on edit in the Operations column.
2.  Configure the following settings as for video only:  
    *   [Player Settings][15]
    *   [Content Ingestion][17]
3.  Click Save field settings.

<h3 class="mce-heading-4">
  <a name="image_only"></a>Image Only
</h3>

<p class="Procedure mce-procedure">
  To configure settings for the image only widget
</p>

1.  In the Manage Fields tab click on edit in the Operations column.
2.  Configure the following settings as for video only:  
    *   Image settings
    <blockquote style="margin: 0 0 0 40px; border: none; padding: 0px;">
      Enter the Image width.<br />Enter the Image height.
    </blockquote>
    
    *   [Thumbnail Settings][16]
    *   [Content Ingestion][17]
3.  Click Save field settings.

### <a name="all_media"></a>All Media types

<p class="Procedure mce-procedure">
  To configure settings for the all media types widget
</p>

1.  In the Manage Fields tab click on edit in the Operations column.
2.  Configure the following settings as for video only:****   
    **** 
    *   [Player settings][15]
    *   [Content Ingestion][17]
3.  Click Save field settings.

### <a name="webcam"></a>Webcam

<p class="Procedure mce-procedure">
  To configure settings for the webcam widget
</p>

1.  In the Manage Fields tab click on edit in the Operations column.
2.  Configure the following settings as for video only:  
    *   [Player settings][15]
    *   [Thumbnail settings][16]
    *   [Content Ingestion][17]
3.  Click Save field settings.

## <a name="managing"></a>Managing the Content Type Display

You can change the display of the configured fields from the default, for each instance of the field and for each different custom display.

<img src="{{site.url}}/assets/484">

<p class="Procedure mce-procedure">
  To manage the Kaltura Media field display
</p>

1.  Select the Structure tab and then select Content Types.
2.  Select the content type you want to configure.
3.  In the Operation column, click manage display to configure the display/format options.  
    *   Choose the Drupal Label from the dropdown menu. Select Above, Inline or Hidden.
    *   Choose the <a name="display_format"></a>Display format option for the Kaltura Media Field. For example, the options for video are as follows:  
        <img src="{{site.url}}/assets/485">
4.  [Customize][18] your display (optional).
5.  Click Save.

 [18]: #customize

<p class="Procedure mce-procedure">
  <a name="customize"></a> To customize the display for a specific instance of the field
</p>

1.  Select the Structure tab and then select Content Types.
2.  Select the content type you want to configure.
3.  In the Operation column click manage display to configure the display/format options.
4.  Click Customize Display Settings and check the settings you want for you display modes.  
    The options you select, for example, Teaser, RSS will be displayed in the manage display screen for further customization.** **
5.  Click on the Display mode, for example, Teaser, and then click the  icon to open the instance specific customization fields.  
     <img src="{{site.url}}/assets/486">
6.  Customize the fields.
7.  Click Update.

## <a name="populating"></a>Populating Kaltura Media Fields with Content

After a Kaltura Media Field is created in a content type, each time content of this type is created, the content editor can populate the field with content.

<p class="Procedure mce-procedure">
  To populate the Kaltura Media field
</p>

1.  Select Content and then select Add Content. The label you defined for each Kaltura Media Field is displayed.
2.  Click the relevant label.  
    The options to add content for the specific field are dependent on the type of Add Media Settings that were set for the field. See [Add Media Settings.][8]  
    *   If you selected Add new media, the content editor will only be able to upload new media to populate the field.
    *   If you selected Use existing media only, the content editor will not be able to upload new media content.
    *   If you selected Use existing media and add new media – the content editor will be able to upload new media as well as choose from existing uploaded content  
        The following example displays a label created for adding new and existing media.  
        <span style="color: #0000ff;">Add Media Use existing media and add new media<br /><img src="{{site.url}}/assets/487">
    <span>The label “Add New” (highlighted in the screenshot) appears only when the field is configured to Add new media. Clicking Add New initiates the <span>Kaltura</span> Contribution Wizard flow. See </span>[Adding Media through the Kaltura Contribution Wizard][8]. 
3.  To sort the content, click on the column table headings for Title and Created By.
4.  To search through your media content, enter a text string and click Apply.  
    <span>If</span>** **<span>you selected more than one media type, you can filter the type of content for your search by using the check boxes</span>.  
    <img src="{{site.url}}/assets/488">
5.  After you select/find the media that you want to use in this specific content, click Insert.  
    In the create/edit Content type page, the selected content is displayed as you specified in the [display format][19].<img src="{{site.url}}/assets/489">
    To remove the content for the Kaltura Media field for a video, click on the red x.  
    <img src="{{site.url}}/assets/490">

6.  Click Save.  
    After you save the content, the content is displayed as defined in the field display settings. See[ Managing the Content Type Display.][4]

 [19]: #display_format

## <a name="adding"></a>Adding Media through the Kaltura Contribution Wizard

When adding new media, Kaltura Contribution Wizard (KCW) widget is used. The options available on the KCW depend on the widget type selected for the field.

*   If you selected ‘Video only widget’, only the Video tab will be available.
*   If you selected ‘Audio only widget’, only the Audio tab will be available.
*   If you selected ‘Image only widget’, only the Image tab will be available.
*   If you selected ‘All media types widget’, all three tabs will be available.
*   If you selected Webcam widget, only the Webcam option within the Video tab will be available.

The following example describes how to contribute media using the Kaltura Contribution Wizard to populate a Kaltura Media Field in the Drupal site.

<p class="Procedure mce-procedure">
  To contribute media using the Kaltura Contribution Wizard
</p>

1.  Depending on the options you selected for widgets and adding media, the Kaltura Contribution Wizard is displayed.  
    <img src="{{site.url}}/assets/491">
2.  Select the type of content and source using the different tabs and options.  
    In this example, a video file is used as the sample to upload.  
     <img src="{{site.url}}/assets/494">
3.  Press ‘Upload!’ to upload the content to Kaltura.
4.  Fill in metadata for the content.  
    <img src="{{site.url}}/assets/493">
5.  Press ‘Next’ to finish the process.

<div>
  <div>
    <div>
      <p>
         
      </p>
    </div>
  </div>
  
  <div>
     
  </div>
</div>