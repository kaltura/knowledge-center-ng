---
layout: page
title: "Kaltura Simple Uploader (KSU) Customization"
date: 2012-04-15 13:14:12
---

<p class="mce-heading-2">
  Customizing the KSU
</p>

This article explains how integrators and project managers can customize the KSU.

The KSU does not load locales or skins.

<p class="mce-heading-3">
  Changing Configuration Values
</p>

The index.template.html file (under the [KSU project][1] -> html-template) contains JavaScript and FlashVars. To adapt the KSU to your needs, you can change the following FlashVars: 

 [1]: http://www.kaltura.org/kalorg/ksu/trunk/

<div align="center">
  <table border="1" cellspacing="0" cellpadding="0">
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          <strong>Variable</strong>
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          <strong>Description</strong>
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          <strong>uiConf</strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          ks
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          A unique string that represents the user. Valid for 24 hours.
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          uid
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          The internal identifier of the end user
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          partnerId
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          The identifier of the partner
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          entryId
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          The kshow to which the new entries will be added
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          host
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          The host of the application
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          jsDelegate
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          A JavaScript object that contains callback functions
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          externalInterfaceDisabled
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          Determines whether external interface functions are called
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          Groupid
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          The identifier of the group
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          partnerdata
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          Custom data, passed from the partner, to be attached to each entry that is added
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          uiconfid
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          The uiConf that will be used
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          siteUrl
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          The URL of the credits site
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          screenName
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          Name of the Credits screen
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          quickedit
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          Boolean flag. Indicates whether the contributed media files are added automatically to the end of the roughcut. The default value is 1.
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          maxFileSize
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          Maximum size of a file
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          Yes
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          maxTotalSize
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          Maximum size of all files
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          Yes
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          maxUploads
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          Maximum number of uploads
        </td>
        
        <td style="text-align: left;" valign="top" width="79">
          Yes
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="194">
          conversionProfile
        </td>
        
        <td style="text-align: left;" valign="top" width="317">
          The identifier of the conversion profile
        </td>
        
        <td valign="top" width="79">
          <p style="text-align: left;">
            Yes
          </p>
        </td>
      </tr>
    </tbody>
  </table>
</div>

<p class="mce-heading-3">
  Understanding the uiConf
</p>

You customize the KSU by modifying properties in the uiConf. 

The uiConf is the user interface configuration file. uiConf is a general name for XML files that enable customizing the KSU for specific needs.

You can use the KSU uiConf to configure your media filters and file restrictions.

<p class="mce-heading-3">
  Creating a uiConf for the KSU
</p>

See [Sample KSU confile][2] for a complete uiConf sample file.

 [2]: #KSUConfileExample

<p class="mce-procedure">
  To create a uiConf
</p>

Use the uiconf.add API call with the following parameters:

*   creationMode = ADVANCED
*   name = [a name that you assign]
*   confile: See [KSU confile format][3].

 [3]: #FormatoftheKSUconfile

<p class="mce-heading-4">
  <a name="FormatoftheKSUconfile"></a>KSU confile format
</p>

The configuration file for the KSU is an XML file with the following format:{syntaxhighlighter brush: xml;fontsize: 100; first-line: 1; }<KUploadConfiguration> <fileFilters> <fileFilter/> </fileFilters> <limits/> </KUploadConfiguration> {/syntaxhighlighter}

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="53">
        <strong>#</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="158">
        <strong>Node</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="129">
        <strong>Attributes</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        <strong>Data type</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="75">
        <strong>Values</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="153">
        <strong>Description</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="53">
        1
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="158">
        KUploadConfiguration
      </td>
      
      <td style="text-align: left;" valign="top" width="129">
        conversionProfile
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        Int
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="75">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="153">
        The identifier of the conversion profile
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="53">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="158">
        fileFilters
      </td>
      
      <td style="text-align: left;" valign="top" width="129">
        default
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        string
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="75">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="153">
        Contains an XML list of file filters
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="53">
        3
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="158">
        fileFilter
      </td>
      
      <td style="text-align: left;" valign="top" width="129">
        <p>
          id
        </p>
        
        <p>
          description
        </p>
        
        <p>
          extension
        </p>
        
        <p>
          sentryType
        </p>
        
        <p>
          mediaType
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        <p>
          string
        </p>
        
        <p>
          string
        </p>
        
        <p>
          string
        </p>
        
        <p>
          enum
        </p>
        
        <p>
          enum
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="75">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="153">
        Describes a filter
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="53">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="158">
        limits
      </td>
      
      <td style="text-align: left;" valign="top" width="129">
        <p>
          maxUploads
        </p>
        
        <p>
          maxFileSize
        </p>
        
        <p>
          maxTotalSize
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        <p>
          int
        </p>
        
        <p>
          int
        </p>
        
        <p>
          int
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="75">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="153">
        Sets restrictions on uploaded data
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <a name="KSUConfileExample"></a>Sample KSU confile
</p>{syntaxhighlighter brush: xml;fontsize: 100; first-line: 1; }<KUploadConfiguration conversionProfile="2"> <fileFilters default="image"> <fileFilter id="image" description="images" extensions="\*.jpg;\*.jpeg;\*.bmp;\*.png;\*.gif;\*.tif;*.tiff" entryType="1" mediaType="2" /> <fileFilter id="video" description="videos" extensions="\*.flv;\*.asf;\*.qt;\*.mov;\*.mpg;\*.mpeg;\*.avi;\*.wmv;\*.mp4;\*.m4v;*.3gp" type="1" entryType="1" mediaType="1" /> <fileFilter id="audio" description="audio" extensions="\*.flv;\*.asf;\*.wmv;\*.qt;\*.mov;\*.mpg;\*.avi;\*.mp3;\*.wav;\*.mp4;\*.wma;\*.3gp" entryType="1" mediaType="5" /> <fileFilter id="media" description="images/videos/audio" extensions="\*.qt;\*.mov;\*.mpg;\*.avi;\*.mp3;\*.wav;\*.mp4;\*.wma;\*.flv;\*.asf;\*.qt;\*.mov;\*.mpeg;\*.avi;\*.wmv;\*.m4v;\*.3gp;\*.jpg;\*.jpeg;\*.bmp;\*.png;\*.gif;\*.tif;\*.tiff" entryType="1" mediaType="-1" /> <fileFilter id="documents" description="documents" extensions="\*.csv;\*.doc;\*.docx;\*.txt;\*.xls;\*.xlsx;\*.ppt;\*.pptx;\*.pdf;\*.rtf;\*.tab;\*.gif;\*.jpg;\*.jpeg;\*.art;\*.bmp;*.tif" entryType="10" mediaType="-1" /> <fileFilter id="Any" description="documents/images/videos/audio" extensions="\*.csv;\*.doc;\*.docx;\*.txt;\*.xls;\*.xlsx;\*.ppt;\*.pptx;\*.pdf;\*.rtf;\*.tab;\*.mov;\*.mpg;\*.avi;\*.mp3;\*.wav;\*.mp4;\*.wma;\*.flv;\*.asf;\*.qt;\*.mov;\*.mpg;\*.mpeg;\*.avi;\*.wmv;\*.m4v;\*.3gp;\*.wav;\*.mp4;\*.jpg;\*.jpeg;\*.art;\*.bmp;\*.png;\*.gif;\*.tif;\*.tiff" entryType="-1" mediaType="-1" /> </fileFilters> <limits maxUploads="60" maxFileSize="200" maxTotalSize="9999999999" /> </KUploadConfiguration>{/syntaxhighlighter}