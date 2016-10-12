---
layout: page
title: "Kaltura Contribution Wizard (KCW) Customization"
date: 2012-04-15 09:44:59
---

<p class="mce-heading-2">
  <span style="text-align: left;">Customizing KCW Look and Feel</span>
</p>

This article explains how integrators and project managers can customize the KCW.

<p class="mce-heading-3">
  Changing Configuration Values
</p>

The index.template.html file (under the [KCW project][1]->html-template) contains JavaScript and FlashVars. To adapt the KCW to your needs, you can change the following FlashVars:

 [1]: http://kaltura.org/kalorg/kcw/trunk

<div align="center">
  <table border="1" cellspacing="0" cellpadding="0">
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          <strong>Variable</strong>
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          <strong>Description</strong>
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          <strong>uiConf</strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          sessionId
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          A unique string that represents the user. Valid for 24 hours.
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          protocol
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The protocol that the application uses
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          uid
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The internal identifier of the end user
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          isanonymous
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          If true, the user is anonymous. The KCW allows an anonymous user to enter a screen name and source URL (a reference to where the media is from) before submitting entries.
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          partnerid
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The identifier of the partner
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          kshowid
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The kshow to which the new entries will be added
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          host
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The host of the application
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          Terms_of_use
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          A URL for the partner terms of service. The link is displayed when the user is required to approve compliance with the site's terms of use.
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          afteraddentry
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          JavaScript function called when new entries are added
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          close
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          JavaScript function called when the user closes the wizard
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          wizardreadyhandler
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          JavaScript function called when the KCW completes loading and awaits user input.
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          Groupid
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The identifier of the group
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          partnerdata
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Custom data, passed from the partner, to be attached to each entry that is added
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          filesystemmode
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          If true, loads locale and skin
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          uiconfid
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The uiConf that is used
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          showclosebutton
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Determines whether to display the contribution Close button
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          Yes
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          showcategories
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Determines whether to display the Categories combo box in the tagging screen
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          Yes
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          showdescription
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Determines whether to display the Description field in the tagging screen
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          Yes
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          showtags
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Determines whether to display the Tags field in the tagging screen
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          Yes
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          quickedit
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Boolean flag. Indicates whether the contributed media files are added automatically to the end of the roughcut. The default value is 1.
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          uploadurl
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The URL that is called on upload
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          categoriesrootid
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          The root category identifier for the tagging screen. All children of the root category are displayed as optional categories. The default value is 0.
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          enforceCategory
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Defining the full name of a category allows all uploads to be automatically placed under the specified category. Works with uiConf v2.1.8 and upwards.
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          additionalfield
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Locale key for an additional field that is displayed in the tagging screen. If there is no matching locale string, the field is not displayed.
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          No
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          limitations.upload.*
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Sets limitations on uploaded files. Can be used as follows:<ul>
            <li>
              limitations.upload.singleFileSize.min
            </li>
            <li>
              limitations.upload.singleFileSize.max
            </li>
            <li>
              limitations.upload.totalFileSize.min
            </li>
            <li>
              limitations.upload. totalFileSize.max
            </li>
            <li>
              limitations.upload.numFiles.min
            </li>
            <li>
              limitations.upload. numFiles.max
            </li>
          </ul>
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          Yes
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          limitations.search.*
        </td>
        
        <td style="text-align: left;" valign="top" width="527">
          Sets limitations on imported files. Can be used as follows:<ul>
            <li>
              limitations.search.numFiles.min
            </li>
            <li>
              limitations.search.numFiles.max
            </li>
          </ul>
        </td>
        
        <td style="text-align: left;" valign="top" width="268">
          Yes
        </td>
      </tr>
    </tbody>
  </table>
</div>

<p class="mce-heading-3">
  Understanding the uiConf
</p>

The uiConf is the user interface configuration file. uiConf is a general name for XML files that enable customizing the KCW for a specific need, layout, and design.

The uiConf affects:

*   The functionality of the KCW. You can configure:
    *   Media types (video/audio/image/swf)
    *   Data providers (for example, upload/user content/webcam/flickr)
    *   Restrictions on the uploaded data (for example, maximum file size to upload)
*   The appearance of the KCW. You can select the screens to display, such as an introduction screen and a finish screen.
*   Look and Feel: Defined in a compiled swf skin file that is linked in the uiConf file.

<p class="mce-heading-3">
  Creating a uiConf for the KCW
</p>

See [Sample KCW confile][2] for a complete uiConf sample file.

 [2]: #KCWConfileExmaple

<p class="mce-procedure">
  To create a uiConf
</p>

Use the uiconf.add API call with the following parameters:

*   objType = CONTRIBUTION_WIZARD
*   creationMode = ADVANCED
*   swfUrlVersion = [version number, for example: 2.1.4] <span>It is important to <strong>leave the swfUrlVersion blank.  </strong></span>
*   name = [a name that you assign]
*   confile: See [KCW confile format][3].

 [3]: #FormatoftheKCWconfile

<p class="mce-heading-4 mce-heading-3">
  <a name="FormatoftheKCWconfile"></a>KCW confile format
</p>

The configuration file for the KCW is an XML file with the following format:

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;ContributionWizard&gt;
	&lt;UIConfigList&gt;
	&lt;/UIConfigList&gt;

	&lt;MediaTypes&gt;
	&lt;/MediaTypes&gt;
 
	&lt;StartupDefaults&gt;
	&lt;/StartupDefaults&gt;

	&lt;limitations&gt;
	&lt;/limitations&gt;
&lt;/ContributionWizard&gt;</pre>

<p class="mce-heading-4">
  UIConfigList
</p>

The **UIConfigList** section describes the skin and locale used for the media provider types. Each media provider can have a specific UIConfig node. A UIConfig node may be defined within a service node. In that case, it overrides a UIConfig defined in the UIConfigList. 

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;UIConfig&gt;
    &lt;target&gt;
      ContributionWizard.swf
    &lt;/target&gt;
    &lt;cssUrl /&gt;
    &lt;localeUrl /&gt;
  &lt;/UIConfig&gt;</pre>

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="37">
        <strong>#</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        <strong>Node</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <strong>Attributes</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        <strong>Data type</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        <strong>Values</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="172">
        <strong>Description</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="37">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        target
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        string
      </td>
      
      <td style="text-align: left;" valign="top" width="172">
        Defines the Flex module to which the skin and locale info relate. Usually, instead of providing specific skin info for every media provider, one CSS swf file is provided for the whole KCW.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="37">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        cssUrl
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        string
      </td>
      
      <td style="text-align: left;" valign="top" width="172">
        The path of the skin swf file
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="37">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        localeUrl
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="172">
        The path of the locale swf file
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  MediaTypes
</p>

The **MediaTypes** section defines the media providers that are available to the user. Each media type has its own media providers. A media provider is a source for importing media. Examples include *Kaltura*, *Upload*, and *Webcam*.

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;mediaTypes&gt;

    &lt;media type="video"&gt;
&lt;provider id="upload" name="upload" code="1"&gt;
        		&lt;authMethodList&gt;
          			&lt;authMethod type="1"/&gt;
        		&lt;/authMethodList&gt;
        		&lt;moduleUrl&gt;UploadView.swf&lt;/moduleUrl&gt;
        		&lt;fileFilters&gt;
          	&lt;filter type="video"&gt;
            	&lt;allowedTypes&gt;flv,asf,qt,mov,mpg,avi,wmv,mp4,3gp,f4v,m4v&lt;/allowedTypes&gt;
         	     	 &lt;/filter&gt;
        		&lt;/fileFilters&gt;
      	&lt;/provider&gt;
	…&nbsp;</pre>

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="48">
        <strong>#</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="126">
        <strong>Node</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <strong>Attributes</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        <strong>Data type</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        <strong>Values</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        <strong>Description</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="48">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="126">
        provider
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        IdNameCode
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        StringStringInt
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        Describes one data provider.Code can be:<ul>
          <li>
            FLICKR = 3
          </li>
          <li>
            YOUTUBE = 4
          </li>
          <li>
            MYSPACE = 7
          </li>
          <li>
            PHOTOBUCKET = 8
          </li>
          <li>
            JAMENDO = 9
          </li>
          <li>
            CCMIXTER = 10
          </li>
          <li>
            NYPL = 11
          </li>
          <li>
            CURRENT = 12
          </li>
          <li>
            MEDIA_COMMONS = 13
          </li>
          <li>
            KALTURA = 20
          </li>
          <li>
            KALTURA_USER_CLIPS = 21
          </li>
          <li>
            ARCHIVE_ORG = 22;
          </li>
          <li>
            KALTURA_PARTNER = 23
          </li>
          <li>
            METACAFE = 24
          </li>
          <li>
            SEARCH_PROXY = 28
          </li>
          <li>
            PARTNER_SPECIFIC = 100
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="48">
        3
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="126">
        authMethodList
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        Lists the available authorization modes used to access the media provider
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="48">
        3
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="126">
        moduleUrl
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        Determines where the specific Flex component is located
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="48">
        3
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="126">
        fileFilters
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="84">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        Lists filters for the media from the data provider
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  StartupDefaults
</p>

The **StartupDefaults** section defines default values and behaviors for the wizard. 

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;StartupDefaults&gt;
    &lt;SingleContribution&gt;false&lt;/SingleContribution&gt;
    &lt;showLogoImage&gt;false&lt;/showLogoImage&gt;
    &lt;NavigationProperties&gt;
      &lt;showCloseButton&gt;true&lt;/showCloseButton&gt;
      &lt;enableIntroScreen&gt;false&lt;/enableIntroScreen&gt;
      &lt;enableTagging&gt;true&lt;/enableTagging&gt;
    &lt;/NavigationProperties&gt;
    &lt;gotoScreen&gt;
      &lt;mediaType&gt;video&lt;/mediaType&gt;
      &lt;mediaProviderName&gt;upload&lt;/mediaProviderName&gt;
 &lt;/gotoScreen&gt;
  &lt;/StartupDefaults&gt;&nbsp;</pre>

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        <strong>#</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        <strong>Node</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        <strong>Attributes</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        <strong>Data type</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        <strong>Values</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        <strong>Description</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        SingleContribution
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        Boolean
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        Controls the way the wizard ends its flow. If true, the wizard displays its last "waiting..." message after submitting the contribution, and calls the defined JavaScript callback function notifying that entries were added. The JavaScript function should redirect the browser or close the modal window that displays the KCW.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        showLogoImage
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        Boolean
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        Determines whether the Kaltura logo is displayed in the KCW footer
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        NavigationProperties
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        Contains properties that control which screen to display or hide
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        gotoScreen
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        Defines a default media provider
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        enableTOU 
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        Boolean
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        The default value is false. If false, the TOU is not displayed in any form.If not false, the TOU is displayed according to the value of <em>autoTOUConfirmation</em>.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        autoTOUConfirmation
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        Boolean
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        <p>
          If true, the <em>TOU</em> footer is displayed. If not true, a <em>TOU</em> popup is displayed before uploading.  
        </p>
        
        <p>
          If <em>enableTOU</em> is false, the <em>autoTOUConfirmation</em> parameter has no effect.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        showCategories 
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        Boolean
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        The default value is true. If true, the Categories combo box is displayed in the tagging screen.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        showTags
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        The default value is true. If true, the Tags field is displayed in the tagging screen.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="157">
        showDescription
      </td>
      
      <td style="text-align: left;" valign="top" width="95">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="48">
        Boolean
      </td>
      
      <td style="text-align: left;" valign="top" width="256">
        The default value is true. If true, the Description field is displayed in the tagging screen.
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-4">
  Limitations
</p>

The **limitations** section defines limitations on uploaded and imported files.

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;limitations&gt;
    &lt;upload&gt;
      &lt;singleFileSize min="-1" max="-1"/&gt;
      &lt;numFiles min="-1" max="100"/&gt;
      &lt;totalFileSize min="-1" max="-1"/&gt;
    &lt;/upload&gt;
    &lt;search&gt;
      	&lt;numFiles min="-1" max="-1"/&gt;
    &lt;/search&gt;
  &lt;/limitations&gt;&nbsp;</pre>

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        <strong>#</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        <strong>Node</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="96">
        <strong>Attributes</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        <strong>Data type</strong>
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        <strong>Values</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="244">
        <strong>Description</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        upload
      </td>
      
      <td style="text-align: left;" valign="top" width="96">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="244">
        Contains all limitations regarding the upload action
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        3
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        singleFileSize
      </td>
      
      <td style="text-align: left;" valign="top" width="96">
        minmax
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        Int
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="244">
        Determines the maximum and minimum size of a single file to upload
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        3
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        numFiles
      </td>
      
      <td style="text-align: left;" valign="top" width="96">
        minmax
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        Int
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="244">
        Determines how many files the user can upload/import at once
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        3
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        totalFileSize
      </td>
      
      <td style="text-align: left;" valign="top" width="96">
        minmax
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        Int
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="244">
        Restricts the total file size a user can upload
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="42">
        2
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="150">
        search
      </td>
      
      <td style="text-align: left;" valign="top" width="96">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="78">
        --
      </td>
      
      <td style="text-align: left;" valign="top" nowrap="nowrap" width="66">
        --
      </td>
      
      <td style="text-align: left;" valign="top" width="244">
        Contains all limitations regarding the search action
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Applying Skins and Styles
</p>

You can skin the KCW with a swf file that the uiConf points to (in the cssUrl tag).

Each KCW component is associated with a specific style. The figure shows the components and associated styles.<img src="{{site.url}}/assets/438">

<p class="mce-heading-3">
  Defining Locales
</p>

You can compile a new locale and point to it in the uiConf (in the localeUrl tag).

The locales folder is under the KCW workspace (refer to <http://www.kaltura.org/kalorg/kcw/trunk>) -> Locales\_Kaltura\_ContributionWizard -> locale -> en_US

Note: you must compile a new locale in the en_US folder.

<p class="mce-procedure">
  To compile a new locale
</p>

1.  In the command line, set the root under the Locales\_Kaltura\_ContributionWizard project.
2.  Run the following command (replace the variables with your values):  
    <pre class="brush: xml;fontsize: 100; first-line: 1; ">mxmlc -locale=en_US -source-path=locale/{locale} -include-resource-bundles=[list your properties files] -output=[name of the output swf file]&nbsp;</pre>

The figure shows an example of defining a new locale. 

<img src="{{site.url}}/assets/439">

<span class="mce-heading-2"><a name="KCWConfileExmaple"></a>Sample KCW confile </span>

The following is the uiConf XML file for the default KCW. 

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;kcw&gt;

  &lt;UIConfigList&gt;
    	&lt;UIConfig&gt;
      		&lt;target&gt;ContributionWizard.swf&lt;/target&gt;
     		 &lt;cssUrl&gt;/content/uiconf/kaltura/kmc/kcw/v2.1.4/styles.swf&lt;/cssUrl&gt;
      		&lt;localeUrl&gt;/content/uiconf/kaltura/kmc/kcw/v2.1.4/en_US_ContributionWizard_kaltura.swf&lt;/localeUrl&gt;
    	&lt;/UIConfig&gt;
  &lt;/UIConfigList&gt;

  &lt;ImportTypesConfig&gt;
    	&lt;taggingConfig&gt;
      		&lt;minTitleLen&gt;1&lt;/minTitleLen&gt;
      		&lt;maxTitleLen&gt;2000&lt;/maxTitleLen&gt;
      		&lt;minTagsLen&gt;0&lt;/minTagsLen&gt;
     		 &lt;maxTagsLen&gt;2000&lt;/maxTagsLen&gt;
    	&lt;/taggingConfig&gt;
  &lt;/ImportTypesConfig&gt;

  &lt;webcamParams&gt;
    &lt;keyFrameInterval/&gt;
    &lt;width/&gt;
    &lt;height/&gt;
    &lt;framerate/&gt;
    &lt;favorArea/&gt;
    &lt;bandwidth/&gt;
    &lt;quality/&gt;
  &lt;/webcamParams&gt;

  &lt;limitations&gt;
    &lt;upload&gt;
      &lt;singleFileSize min="-1" max="-1"/&gt;
      &lt;numFiles min="-1" max="100"/&gt;
      &lt;totalFileSize min="-1" max="-1"/&gt;
    &lt;/upload&gt;
    &lt;search&gt;
      	&lt;numFiles min="-1" max="-1"/&gt;
    &lt;/search&gt;
  &lt;/limitations&gt;

  &lt;mediaTypes&gt;

    &lt;media type="video"&gt;
&lt;provider id="upload" name="upload" code="1"&gt;
        		&lt;authMethodList&gt;
          			&lt;authMethod type="1"/&gt;
        		&lt;/authMethodList&gt;
        		&lt;moduleUrl&gt;UploadView.swf&lt;/moduleUrl&gt;
        		&lt;fileFilters&gt;
          	&lt;filter type="video"&gt;
            	&lt;allowedTypes&gt;flv,asf,qt,mov,mpg,avi,wmv,mp4,3gp,f4v,m4v&lt;/allowedTypes&gt;
         	     	 &lt;/filter&gt;
        		&lt;/fileFilters&gt;
      	&lt;/provider&gt;

      	&lt;provider id="webcam" name="webcam" code="2"&gt;
        		&lt;authMethodList&gt;
         		 	&lt;authMethod type="1"/&gt;
        		&lt;/authMethodList&gt;
      		 &lt;moduleUrl&gt;WebcamView.swf&lt;/moduleUrl&gt;
        		&lt;customData&gt;
          			&lt;serverUrl&gt;rtmp://{HOST_NAME}/oflaDemo&lt;/serverUrl&gt;
        		&lt;/customData&gt;
     	 &lt;/provider&gt;

      	&lt;provider id="metacafe" name="metacafe" code="24"&gt;
       		 &lt;moduleUrl&gt;SearchView.swf&lt;/moduleUrl&gt;
       		 &lt;authMethodList&gt;
         			 &lt;authMethod type="1"/&gt;
        		&lt;/authMethodList&gt;
      	&lt;/provider&gt;

     	&lt;provider id="thissite" name="thissite" code="23" addsearch="true"&gt;
       		 &lt;moduleUrl&gt;SearchView.swf&lt;/moduleUrl&gt;
       		 &lt;authMethodList&gt;
         			 &lt;authMethod type="1"/&gt;
        		&lt;/authMethodList&gt;
        		&lt;tokens&gt;
          			&lt;token&gt;
           				 &lt;name&gt;extra_data&lt;/name&gt;
            			&lt;value&gt;$partner_id&lt;/value&gt;
          			&lt;/token&gt;
        		&lt;/tokens&gt;
      	&lt;/provider&gt;
    &lt;/media&gt;
    
    &lt;media type="audio"&gt;
     	 &lt;provider id="upload" name="upload" code="1"&gt;
       		 &lt;authMethodList&gt;
        			  &lt;authMethod type="1"/&gt;
       		 &lt;/authMethodList&gt;
        		&lt;moduleUrl&gt;UploadView.swf&lt;/moduleUrl&gt;
        		&lt;fileFilters&gt;
          			&lt;filter type="audio"&gt;
           			 	&lt;allowedTypes&gt;flv,asf,wmv,qt,mov,mpg,avi,mp3,wav&lt;/allowedTypes&gt;
         			 &lt;/filter&gt;
       		 &lt;/fileFilters&gt;
      	&lt;/provider&gt;

      	&lt;provider id="ccmixter" name="ccmixter" code="10"&gt;
       		 &lt;moduleUrl&gt;SearchView.swf&lt;/moduleUrl&gt;
       		 &lt;authMethodList&gt;
          			&lt;authMethod type="1"/&gt;
          			&lt;authMethod type="3"/&gt;
        		&lt;/authMethodList&gt;
      	&lt;/provider&gt;
	  
&lt;provider id="thissite" name="thissite" code="23"&gt;
&lt;moduleUrl&gt;SearchView.swf&lt;/moduleUrl&gt;
        	&lt;authMethodList&gt;
          		&lt;authMethod type="1"/&gt;
        	&lt;/authMethodList&gt;
       	 &lt;tokens&gt;
          		&lt;token&gt;
            		&lt;name&gt;extra_data&lt;/name&gt;
           		 	&lt;value&gt;$partner_id&lt;/value&gt;
         		 &lt;/token&gt;
        	&lt;/tokens&gt;
 &lt;/provider&gt;
	  
    &lt;/media&gt;

   &lt;media type="image"&gt;

      	&lt;provider id="upload" name="upload" code="1"&gt;
       	 &lt;authMethodList&gt;
         		 &lt;authMethod type="1"/&gt;
        	&lt;/authMethodList&gt;
       	 &lt;moduleUrl&gt;UploadView.swf&lt;/moduleUrl&gt;
        	&lt;fileFilters&gt;
          		&lt;filter type="image"&gt;
            		&lt;allowedTypes&gt;jpg,bmp,png,gif,tiff&lt;/allowedTypes&gt;
         	 	&lt;/filter&gt;
        	&lt;/fileFilters&gt;
      	&lt;/provider&gt;

      	&lt;provider id="flickr" name="flickr" code="3"&gt;
        		&lt;moduleUrl&gt;SearchView.swf&lt;/moduleUrl&gt;
       		 &lt;authMethodList&gt;
          		&lt;authMethod type="1"/&gt;
        		  	&lt;authMethod type="4" searchable="false"/&gt;
        		&lt;/authMethodList&gt;
     	 &lt;/provider&gt;

      	&lt;provider id="nypl" name="nypl" code="11"&gt;
       		 &lt;moduleUrl&gt;SearchView.swf&lt;/moduleUrl&gt;
       		 &lt;authMethodList&gt;
          			&lt;authMethod type="1"/&gt;
       		 &lt;/authMethodList&gt;
      	&lt;/provider&gt;
      
     	 &lt;provider id="thissite" name="thissite" code="23" addsearch="true"&gt;
       		 &lt;moduleUrl&gt;SearchView.swf&lt;/moduleUrl&gt;
        		&lt;authMethodList&gt;
          			&lt;authMethod type="1"/&gt;
       		 &lt;/authMethodList&gt;
        		&lt;tokens&gt;
          			&lt;token&gt;
            		&lt;name&gt;extra_data&lt;/name&gt;
            		&lt;value&gt;$partner_id&lt;/value&gt;
          			&lt;/token&gt;
       		 &lt;/tokens&gt;
      	&lt;/provider&gt;
    &lt;/media&gt;
  &lt;/mediaTypes&gt;

  &lt;StartupDefaults&gt;
    &lt;SingleContribution&gt;false&lt;/SingleContribution&gt;
    &lt;showLogoImage&gt;false&lt;/showLogoImage&gt;
    &lt;NavigationProperties&gt;
      &lt;showCloseButton&gt;true&lt;/showCloseButton&gt;
      &lt;enableIntroScreen&gt;false&lt;/enableIntroScreen&gt;
      &lt;enableTagging&gt;true&lt;/enableTagging&gt;
    &lt;/NavigationProperties&gt;
    &lt;gotoScreen&gt;
      &lt;mediaType&gt;video&lt;/mediaType&gt;
      &lt;mediaProviderName&gt;upload&lt;/mediaProviderName&gt;
 &lt;/gotoScreen&gt;
  &lt;/StartupDefaults&gt;
&lt;/kcw&gt;</pre>