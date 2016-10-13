---
layout: page
title: "Kaltura Drop Folders Service For Content Ingestion"
date: 2011-12-19 18:37:52
---

<p class="mce-heading-2">
  Using a Drop Folder
</p>

The Kaltura Drop Folder service constantly watches each drop folder for new content, and activates automatic ingestion of new content to the specific account.

Kaltura offers multiple configuration options for setting each drop folder to a specific workflow.  Contact your Kaltura account manager to learn more about how drop folders can simplify your workflow, and to activate and configure drop folders on your account.

Use the Kaltura Drop Folder service to:

*   Automate or partially automate an on-going content ingestion workflow.
*   Support bulk ingestion of content to Kaltura, either when you set up an account, and to migrate a large amount of existing content, or, on an on-going basis.
*   Work with content providers and operational teams who do not have access to the Kaltura Management Console (KMC) or any other content management application.

Kaltura’s drop folder service is designed to support a variety of integration requirements and business needs, and has flexible configuration options. 

<span class="mce-heading-3">Drop Folder Locations</span>  
A drop folder may be 

*   [Hosted on the Kaltura Cloud][1], publisher pushes the content; 
    
    or

*   [Hosted On-Premise by the Publisher][2], Kaltura pulls the content (with standard FTP/SFTP access and authentication).

 [1]: #KalturaCloud
 [2]: #KalturaOnPrem

<p class="mce-heading-3">
  <a name="KalturaCloud"></a>Hosted on the Kaltura Cloud
</p>

When account-specific drop folders are located on the Kaltura cloud, they are fully  hosted and managed by Kaltura. Publishers are granted FTP/SFTP?Aspera access to one or more account-specific drop folders. Publishers are responsible for uploading their content to the drop folders. Kaltura recommends this option for publishers who prefer a fully-managed drop folder solution, and for publishers whose workflow and security needs are better met by this option.

<p class="mce-heading-3">
  <a name="KalturaOnPrem"></a>Hosted On-Premise by the Publisher
</p>

Kaltura defines a drop folder configuration with the drop folder location and access details. The publisher locates account-specific drop folders at the publisher's premises or on any FTP/SFTP-accessed location.   A Kaltura drop folder watcher constantly checks the drop folder. When content is ready to be ingested, it is downloaded from the drop folder to the Kaltura cloud. Kaltura recommends this option for publishers who already have a network location that they want Kaltura to watch and use for ingestion, and for publishers whose workflow and security needs are better met by this option.

<p class="mce-heading-1">
  Drop Folders Control
</p>

KMC administrators can view and delete media files in the account drop folder on the Drop Folders Control page. The Drop folder input package may be a single source file or a complete media package including multiple flavors and metadata xml. You can create a new entry based on the input package or add to an existing entry 

<p class="mce-heading-2">
  Drop Folder Configuration Options
</p>

*   [Transcoding Profile][3]
*   [File Name Patterns][4]
*   [Ingestion Types][5]
*   [Ingestion from Media Files - Matching Policies][6]
*   [Ingestion from Media Files - Matching Regular Expression][7]

 [3]: #Transcoding
 [4]: #Patterns
 [5]: #Ingestion
 [6]: #MatchingPol
 [7]: #MatchingRE

 

<a name="Transcoding"></a><span class="mce-heading-3">Transcoding Profile</span>

The transcoding profile attached to the drop folder settings defines the transcoding se<a name="MatchingPol"></a>ttings required for content ingested from the drop folder. Consequently, the transcoding profile also determines whether media files in the drop folders are handled as a single file media source or as part of a media package. Kaltura fully transcodes a single file media source, while a media  package consists of multiple bit rate transcoding flavors that are generated by a local  transcoder. A media package is added from the drop folder to a single media entry as one unit.

<a name="Patterns"></a><span class="mce-heading-3">File Name Patterns</span>

By default, drop folders handle all file name patterns. File name patterns to handle. A publisher can define a specific drop folder file name pattern to be handled by the drop folder (white list approach). The file name pattern should be configured when you need to apply a drop folder operation only to files of a specific type or naming structure.

A publisher can define a specific drop folder file name pattern to be ignored by the drop folder (black list approach). The file name pattern should be configured when you need a drop folder  operation to ignore files of a specific type or naming structure. This option is useful when transferring temporary files created by transfer client applications when uploading files to the drop folder. The temporary files usually use a specific name pattern or extension. You can mark to ignore a specific name pattern or extension by the drop folder service.

<a name="Ingestion"></a><span class="mce-heading-3">Ingestion Types</span>

Content ingestion from a drop folder can be triggered from:

Media files - With this ingestion type, only media files are dropped to the drop folder. An automatic ingestion process is triggered for uploading these files to Kaltura. You can conveniently edit the metadata in the KMC. This ingestion type requires setting additional configuration options for specific policies in the drop folder profile. 

A Kaltura MRSS-formatted XML – The XML should include both metadata and references to related media files. With this ingestion type, a Kaltura MRSS-formatted XML is dropped into the drop folder. The XML may include metadata information for multiple media items and references to media files related to each item. The referenced media files can reside within the drop folder itself or on a  remote location. An automatic ingestion process is triggered that creates or updates media entries in Kaltura while populating the metadata fields of the entries from the XML and processing the ingestion and transcoding of referenced media files. When Media files reside within the drop folder, the ingestion process will only start when all files referenced in the XML are found in the drop folder.

<p class="mce-note-graphic">
  <span>NOTE: When a transcoding profile is defined in the XML, it is used. The transcoding profile attached to the drop folder settings are overridden.</span>
</p>

<a name="MatchingPol"></a><span class="mce-heading-3">Ingestion from Media Files - Matching Policies</span>

When a drop folder is set to ingest content from media files, one of the following matching policies should be selected:

**Create an entry from media**– Media files in the drop folder always trigger the creation of a new entry in Kaltura. This option is especially useful when you need a simple content creation workflow that is handled by users who don’t have access to the KMC or for users who are not using the KMC to upload media files. 

Use this policy when you need to automatically upload media files into Kaltura, and when metadata editing can/should be completed after files are uploaded to the system.

<p class="mce-procedure">
  To create an entry from media
</p>

1.  Drop a media file into the drop folder. A new entry in Kaltura is automatically created. This triggers an automatic conversion in  Kaltura according to the transcoding profile settings attached to the drop folder. The title of the new entry is based on the file name.
2.  Edit the new entry metadata in the KMC as needed. A process to automatically replace the media cannot be triggered from a drop folder configured to support this policy.

**Match media to an existing entry** - Media files in the drop folder are automatically matched to an existing entry in Kaltura. The automatic matching is based on a Reference ID. The Reference ID must be part of the media file name. You must set the same Reference ID as an entry metadata item.

Use this policy for fast-paced or complex operational environments that require working simultaneously on metadata and media preparation. 

<p class="mce-procedure">
  <strong>To set up entries in drop folders to match media to existing entries</strong>
</p>

1.  Prepare a new entry in the KMC.
2.  Set metadata for the new entry and set its Reference ID in the Edit Entry's Metadata tab. Reference ID example: MyVideoClip123
3.  Drop a media file in the drop folder and include the Reference ID in the filename. For example: MyVideoClip123.mp4

The MyVideoClip123.mp4 file in the drop folder automatically will be added to an entry with the “MyVideoClip123” string as a Reference ID metadata item. This triggers an automatic conversion in Kaltura according to the Transcoding Profile settings associated with the drop folder. When there is no entry in the system with a matching Reference ID, the media files remain in the drop folder until a matching entry is created.

When the matched entry already is already associated with media, a process is triggered that automatically replaces the media. 

**Match media when entry exists or create a new entry** –The Kaltura system tries to match the media file in the drop folder to an existing entry based on a Reference ID. When the KMC entry does not have a matching Reference ID, a new entry is created in Kaltura. The media file in the drop folder is added to the new entry. A process to automatically replace the media can be triggered from a drop folder configured to support this policy.

Use this policy when

*   You need to automatically upload media files into Kaltura.
*   Metadata editing can/should be completed after files are uploaded to the system.
*   You need to trigger a process from a drop folder to automatically replace media. 

<p class="mce-note-graphic">
  NOTE: When an account is configured to support the use of a local transcoder, multiple bit rate media files also can be automatically added to the entry in the same manner when the files are handled together as a single media package. In this case, uploading the media files and adding them to the entry are triggered only when all media files that are part of the media package are available in the drop folder. 
</p>

<a name="MatchingRE"></a><span class="mce-heading-3">Ingestion from Media Files - Matching Regular Expression</span>

When a drop folder is set to match media files to an existing media entry, the file name must include the Reference ID that is used as a matching key.  By default, the file name itself is treated as a Reference ID.  

Examples: (the Reference ID is <span style="color: #ff0000;">red</span>):

<p style="padding-left: 30px;">
  <code>&lt;span style="color: #ff0000;">MyVideoClip123&lt;/span>.mp4 &nbsp;</code>
</p>

When an account is configured to support the use of a local transcoder and ingestion of multiple bit rate media files to a single media entry, file naming convention must be defined to also include the system name of a specific flavor in the transcoding profile that this file should be matched to.

In the following examples, all media files are added to a single entry and each file is matched to  the appropriate transcoding flavor, according to its system_name definition in the transcoding  profile  (the Reference ID is red, the transcoding flavor system name is <span style="color: #0000ff;">blue</span>):

<p style="padding-left: 30px;">
  <code>&lt;span style="color: #ff0000;">MyVideoClip123&lt;/span>_&lt;span style="color: #0000ff;">HD&lt;/span>.flv</code>
</p>

<p style="padding-left: 30px;">
  <code></code><code>&lt;span style="color: #ff0000;">MyVideoClip123&lt;/span>_&lt;span style="color: #0000ff;">Basic-Small&lt;/span>.flv</code>
</p>

<p style="padding-left: 30px;">
  <code></code><code>&lt;span style="color: #ff0000;">MyVideoClip123&lt;/span>_&lt;span style="color: #0000ff;">Basic-Large&lt;/span>.flv</code>
</p>

<h2 class="mce-heading-1 mce-heading-2">
  Drop Folder File Management Policies
</h2>

A file deletion policy can be defined for a drop folder hosted on-premise by the Publisher. 

The File Deletion policy defines whether files in drop folders are deleted automatically by the Kaltura drop folder service after a successful completion of ingestion processing or are deleted manually by the publisher from the KMC. 

When you select an automatic deletion policy, you must also define the number of days that the files are kept in the drop folder before being deleted. This policy deletes only files that were processed successfully. 

For drop folders hosted in Kaltura, by default, files will be deleted automatically a short time after successful completion of ingestion processing. 

You can perform manual deletion from the drop folders control page in the KMC or by using the Kaltura API. Kaltura does not recommend direct manual deletion of files from the drop folder itself. This is because manual file deletion may impact the synchronization between the status of drop folder files and their representation, which is managed by Kaltura’s drop folder file management service.

With both options, a change to an existing file in the drop folder (such as a change in the file creation date or file size) resets handling of the file. The drop folder service then treats the changed file as a new file.

<p class="mce-heading-2">
  Drop Folder Access Settings
</p>

When a drop folder is managed by Kaltura and is hosted on the Kaltura cloud, Kaltura’s technical support team sets the drop folder location and provides full access and authentication information to the publisher.

When a drop folder is hosted and managed at the publisher's premises, the publisher must provide the following information, per preferred transfer protocol, to Kaltura, to set up the drop folder configuration:

<table class="kaltura-table" align="left">
  <thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 20%;">
        Protocol 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 20%;">
        Access Details
      </th>
      
      <th class="kaltura-table-head-item" style="width: 20%;">
        Authentication Details
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%;">
        FTP<span class="Apple-tab-span" style="white-space: pre;"></span>
      </td>
      
      <td align="left">
        Host, Port, Storage path
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%;">
        Username, Password 
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%;">
        SFTP
      </td>
      
      <td align="left">
        Host, Port, Storage path
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%;">
        Username & Password, or Username &  SSH private/public keys (by default keys will be generated by Kaltura)
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3 mce-heading-2">
   Drop Folder Control Panel
</p>

This section applies only after the Kaltura Drop Folder service is set up. 

In the KMC Content tab, KMC administrators can use a control panel to monitor and troubleshoot media files in drop folders. Access to the Drop Folders control panel can be granted to specific administrators through the administrator's user role definition. 

<img src="/sites/default/files/u16/kmc-drop-folders.png" border="0" width="400" />

The Drop Folders control panel includes the current processing status of each file in the drop folder, and an option to filter the file display for a specific drop folder, status and creation date range. For files that completed their processing, a link to the entry editing window is available as well. 

An additional option to manually delete files from the drop folder can be granted separately only to authorized administrators. 

<p class="mce-heading-2">
  Drop Folders Table
</p>

The Drop Folders Files table in the Drop Folder Control page lists all media and/or XML files currently available in the account’s drop folders. Current details of each file are available within the table. In the filter bar on the left side of the page, you can filter the files by:

*   Search criteria
*   Drop folder
*   File creation date
*   Drop folder File Processing status

If you need to delete files from the drop folder, click Delete.

<p class="mce-heading-2">
  <a name="statuses"></a>Drop Folder Files' Statuses
</p>

The following statuses describe the different stages and possible error cases that may apply to a specific file in the drop folder:

*   **Parsed from XML –** A reference to the media file was parsed from the XML. The media file is expected but is not yet available in the drop folder.
*   **Uploading** – File is currently uploading to the drop folder.
*   **Pending** – File upload is completed - Waiting for drop folder processing to start.
*   **Waiting for Related Files (Formerly “Matched”)** – Processing of this file should continue when all related media files are available in the drop folder (i.e. other files referenced in the same XML or other flavors expected for the same entry).
*   **Waiting for Matched Entry (Formerly “Not Matched”)** – Processing of this file should continue when all related files are available in the drop folder (for example, XML file, other media files referenced in the same XML or other flavors expected for the same entry).
*   **Processing -** Drop folder engine is currently processing this file.
*   **Downloading** - The file is currently importing from the drop folder to Kaltura.(applicable only in drop folders hosted on-premise by customers)
*   **Done** – Drop folder processing was completed for this file.
*   **Error** – Drop folder engine processing failed.
*   **Download  Failed - **Failed to import the file from the drop folder to Kaltura. (applicable only in drop folders hosted on-premises by customers)
*   **Delete Failed** - Failed to delete the file from the drop folder.

 

<p class="mce-heading-2">
  Unsupported file name characters
</p>

When uploading to a dropfolder it is important to note that there are unsupported character in file names that should be avoided when uploading files, below you can find a full list of all unsupported characters.

<table style="width: 20%;" border="0" cellspacing="0" cellpadding="0">
  <colgroup><col span="2" width="64" /> </colgroup><tbody>
    <tr>
      <th class="xl65" style="width: 128px; height: 19px;" colspan="2">
        Unsupported characters
      </th>
    </tr>
    
    <tr>
      <td height="19">
        \ 
      </td>
      
      <td>
        (backslash) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        / 
      </td>
      
      <td>
        (forward slash) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        : 
      </td>
      
      <td>
        (colon) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        ; 
      </td>
      
      <td>
        (semi-colon) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        * 
      </td>
      
      <td>
        (asterisk) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        ? 
      </td>
      
      <td>
        (question mark) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        "
      </td>
      
      <td>
        (double quotes) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        < 
      </td>
      
      <td>
        (left angle bracket) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        > 
      </td>
      
      <td>
        (right angle bracket) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        | 
      </td>
      
      <td>
        (pipe) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        % 
      </td>
      
      <td>
        (percent) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        , 
      </td>
      
      <td>
        (comma) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        # 
      </td>
      
      <td>
        (pound or number) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        $ 
      </td>
      
      <td>
        (dollar) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        ! 
      </td>
      
      <td>
        (exclamation) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        + 
      </td>
      
      <td>
        (plus) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        { 
      </td>
      
      <td>
        (left bracket) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        } 
      </td>
      
      <td>
        (right bracket) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        & 
      </td>
      
      <td>
        (ampersand) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        [ 
      </td>
      
      <td>
        (left square bracket) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        ] 
      </td>
      
      <td>
        (right square bracket) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        • 
      </td>
      
      <td>
        (bullet) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        ' 
      </td>
      
      <td>
        (apostrophe) 
      </td>
    </tr>
    
    <tr>
      <td height="19">
        ` 
      </td>
      
      <td>
        (backtick)
      </td>
    </tr>
  </tbody>
</table>

 