---
layout: page
title: "Kaltura’s Support for Ingestion of the WebEx ARF File Format "
date: 2013-07-03 12:13:59
---

 

Information for the following workflows is provided:

*   [Workflow 1 – KMC - Upload Multiple ARF files from Desktop][1]
*   [Workflow 2 – KMC - Import a Single ARF File from WebEx Server][2]
*   [Workflow 3 – KMC - Bulk Upload Multiple ARF Files][3]
*   [Workflow 4 – KMC - Upload Single ARF File using Aspera][4]
*   [Workflow 5 – KMC - Upload Multiple ARF Files Using Drop-folders][5]
*   [Workflow 6 – KMS - Upload a Single ARF File from Desktop][6]
*   [Workflow 7 – Applications - Upload a Single ARF File from Desktop][7][][8]

 [1]: #Workflow1
 [2]: #Workflow2
 [3]: #Workflow3
 [4]: #Workflow4
 [5]: #Workflow5
 [6]: #Workflow6
 [7]: #Workflow7
 [8]: https://portal.kaltura.com/community-team/Shared%20Documents/Knowledge%20Management/Final%20Documents%20-%20Ready%20for%20Publishing/webex/Webex_Workflow_and_Enablement%20_Internal.docx#_Workflow_7_–

<a name="Workflow1"></a><span class="mce-heading-3">Workflow 1 – KMC - Upload Multiple ARF Files from Desktop</span>

1.  In the KMC Upload tab, select Upload from desktop.
2.  Browse to your file.  
    The KMC uploader  supports uploading single or multiple ARF files.

<a name="Workflow2"></a><span class="mce-heading-3">Workflow 2 – KMC - Import a Single ARF File from WebEx Server</span>

1.  Copy the link in the  “<a name="download"></a>Download recording link” from the WebEx server.  
    <img src="http://cdnknowledge.kaltura.com//sites/default/files/styles/large/public/dowload_recording_link.png" border="0" alt="" width="640" height="273" />
2.  Create a media-less entry in the KMC. Select the Upload tab and then select Prepare Video Entry.  
    <img src="http://cdnknowledge.kaltura.com//sites/default/files/styles/large/public/prepare_entry.png" border="0" alt="" width="640" height="331" />
3.  In the New Entry window select the Flavors tab.  
    <img src="http://cdnknowledge.kaltura.com//sites/default/files/styles/large/public/new_entry_flavors_tab.png" border="0" alt="" width="640" height="300" />
4.  Select Import File/s.  
    <img src="http://cdnknowledge.kaltura.com//sites/default/files/styles/large/public/import.png" border="0" alt="" width="640" height="300" />
5.  Paste the URL that you copied from the  “[Download recording link][9]” from the WebEx server and click Import.  
    After the file is imported and transcoding is done, the entry is ready.

 [9]: #download

<a name="Workflow3"></a><span class="mce-heading-3">Workflow 3 – KMC - Bulk Upload Multiple ARF Files</span>

1.  In the KMC Upload tab, select Submit Bulk and  then select CSV/XML.
2.  In the CSV/XML file , insert the URL pointing to the ARF file. The URL may be that you copied from the  “[Download recording link][9]” from the WebEx server or from  another location.
3.  Upload the CSV file as you would in the regular KMC workflow.

<a name="Workflow4"></a><span class="mce-heading-3">Workflow 4 – KMC - Upload a Single ARF File using Aspera</span>

*   The regular KMC Aspera workflow supports ARF files.

<a name="Workflow5"></a><span class="mce-heading-3">Workflow 5 – KMC - Upload Multiple ARF Files Using Drop-folders</span>

*   The regular KMC Drop-folders workflow supports ARF files.

<a name="Workflow6"></a><span class="mce-heading-3">Workflow 6 – KMS - Upload a Single ARF File from Desktop</span>

1.  In the Add New tab choose Media Upload.
2.  Browse to your file and add media.  (Only single files ARF files are supported.)  
    The MediaSpace flow continues normally.  
    This feature is included  by default to new customers running on SaaS KMS 4.6. Existing customers running on SaaS KMS 4.6  will need to request that this feature be enabled for them.   
    When the SaaS KMS 5 is released, this feature will be available to all customers running KMS5.

<a name="Workflow7"></a><span class="mce-heading-3">Workflow 7 – Applications - Upload a Single ARF File from Desktop</span>

*   Upload a single file using the KCW in the application.

The feature is available for the KCW default version in the various Kaltura applications (Blackboard, Sakai, Moodle, Wordpress, Drupal). For non-default KCW versions, this feature may be added, per request.

<p class="mce-heading-3">
  Created Flavors
</p>

The entry will include:

1.  The original ARF file –  the file can playback on the WebEx player and saved for future use. The file does not  have to be hosted on the WebEx server as well.
2.  A Kaltura source file – WMV format, from which the customer can re-transcode to any flavor.
3.  All the customer’s flavors.   
    <img src="http://cdnknowledge.kaltura.com//sites/default/files/styles/large/public/arf_source.png" border="0" alt="" width="640" height="412" />

<p class="mce-heading-3">
  Limitations
</p>

When ingesting from WebEx, only the presentation panel is included in Kaltura’s panel. Other panels such as polling, Video, Chat or file transfer, may be available at a later date.