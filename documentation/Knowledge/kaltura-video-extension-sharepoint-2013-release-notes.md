---
layout: page
title: "Kaltura Video Extension for SharePoint 2013 Release Notes "
date: 2015-03-01 20:21:15
---

<span style="color: #000000;">Version: 1.0</span>

These release notes pertain to the Kaltura Video Extension for SharePoint 2013 for Microsoft Office 365 and Kaltura On-Premise,  released March 2015. These release notes are intended for content managers and SharePolint users and administrators and also contain the latest information for developers, integrators, and operations and site administrators using the Kaltura platform. 

<p class="mce-heading-3">
  What's New in this Release?
</p>

This version of Kaltura Video Extension for SharePoint 2013 includes the following functionality:

*   **My Media** – An App/web part that exposes users’ personal repository of media they own, manage and edit.
*   **Media Gallery** – An App/web part that creates a collection of media associated with a certain site or sub-site. Media can be viewed, shared and added.
*   **BSE** (Browse Serach and Embed) – An App/web part that enables users to browse media from available repositories, search for media and embed media in pages.
*   **Integrated Search** (for SP13 On-Premise only) - a connector that enable SharePoint to crawle the videos and surface it as integral part of search results, seamlessly to the user.

 <strong style="color: #828a8c; font-size: 14pt;"><span style="font-size: 1em;">Known Issues</span></strong>

<table style="width: 650px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="118">
        <p class="TableHeading">
          <strong>Defect ID</strong>
        </p>
      </td>
      
      <td valign="bottom" width="119">
        <p class="TableHeading">
          <strong>Component</strong>
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" align="left" valign="top">
        <p>
          KMS-5886
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        Media Gallery
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p>
          Publishing to the Media Gallery is not be possible for the following unique case: It is not possible to publish media to a Media Gallery, if the Media Gallery and the BSE web/app parts are on the same page and were configured on the same window of a fresh installation. After choosing media to publish and clicking on the Publish button, media is not published.
        </p>
        
        <p>
          Workaround: After entering the Media Gallery link on a different window, publishing is possible.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" align="left" valign="top">
        KMS-5955
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        BSE Module
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p>
          The previous/old BSE module is not supported. It's not possible to embed media with the previous BSE. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" align="left" valign="top">
        KMS-5893<a href="https://kaltura.atlassian.net/browse/KMS-5893"></a> 
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        UI
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        The 'Go to Channel' button is erroneous. <p>
          After uploading an entry to the Media Gallery web/app part, a 'Go to channel' button appears. The button should read 'Go to Media Gallery'.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<div>
  <p class="mce-heading-3">
    <strong>Limitations</strong>
  </p>
  
  <table style="width: 650px;" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="bottom" width="119">
          <p class="TableHeading">
            <strong>Component</strong>
          </p>
        </td>
        
        <td valign="bottom" width="525">
          <p class="TableHeading">
            <strong>Summary</strong>
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="119">
          Single Browse-Search-And-Embed Web/App part can be located within a single row.
        </td>
        
        <td style="text-align: left;" valign="bottom" width="525">
          Although not a very common case, you may want to position a few browse-search-and-embed web parts stacked horizontally in a web part page. This cannot be achieved since the web part requires most of the screen's horizontal estate (i.e. 900 pixels). In general, for a proper user-experience, it’s recommended to stack a single video in a row.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="119">
          SharePoint permissions are not precisely equivalent to Kaltura permissions
        </td>
        
        <td style="text-align: left;" valign="bottom" width="525">
          <p>
            The Kaltura Video Solution for SharePoint allows the site owner to define user permissions within SharePoint using the familiar SharePoint permissions screens. Users can be added to SharePoint groups or assigned to permission levels and the Kaltura experience will provide the relvant permissions accordingly. For example a user who is part of the ‘Site Visitors’ group won’t be able to upload new media to the site gallery. However, technically under the hood, for every group or permission level SharePoint has granular permissions, for example: Add Items, Delete Items and many others. These granular permissions are not precisely applied over Kaltura media items. For example, if you create a custom permission level where adding items is allowed but deleting items is not, assigning this permission level to ‘Site Members’ group won’t prevent the group members from deleting items. The granular and detailed allowed operations are determined using the Kaltura Application Framework (KAF) roles. It’s possible to map different SharePoint granular permissions to KAF roles. This topic is greatly described within the deployment document in the section ‘Step 9 - Assign Permissions to Users’.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="119">
          <p>
            Kaltura widgets refresh automatically when changing the page’s style
          </p>
        </td>
        
        <td style="text-align: left;" valign="bottom" width="525">
          <p>
            When the user changes the page style – Kaltura widgets are reloading. Typically in every SharePoint Wiki page, when you edit the page and apply different styles to the page (usually in the page’s ribbon – the top menu), for example by changing the text formatting, all the elements in the page are re-arranged. In this case, Kaltura widgets will refresh and render from Kaltura platform.<span style="color: #ff0000;"><br /></span>
          </p>
        </td>
      </tr>
    </tbody>
  </table>
</div>

<h2 class="mce-heading-3">
  Known Issues for the Kaltura Solution for SP13 On-Premise Only
</h2>

<table style="width: 650px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td align="left" valign="top">
        KMS-5846
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        BSE Module
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p>
          There is a redundant 'Back' button on search results entry page. When clicking on it nothing happens. The video opens in a new window and there's no where to get back to.
        </p>
      </td>
    </tr>
    
    <tr>
      <td align="left" valign="top">
        KMS-5192
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p>
           BSE Module
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p>
          All Kaltura video results are surfaced on the Kaltura vertical even before a search is executed. After you got the Kaltura Search Result page or search for anything, and click on the kaltura vertical (if configured)  in the results page, all kaltura media is disaplyed and the search box is empty.
        </p>
      </td>
    </tr>
    
    <tr>
      <td align="left" valign="top">
        KMS-6107 
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        Metadata
      </td>
      
      <td valign="bottom" width="525">
        <p style="text-align: left;">
          A video may only have one site’s metadata though it appears in multiple sites. When working on two different Sharepoint sites in parallel on different tabs in the same browser, uploading media to one of the sites may cause the metadata to be saved under the second site's metadata.
        </p>
        
        <p style="text-align: left;">
          Workaround: Refresh the tab.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<h2 class="mce-heading-3">
  Limitations in the Kaltura Solution for SP13 On-Premise Only
</h2>

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="119">
        <p class="TableHeading">
          <strong>Component</strong>
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="119">
        <p>
          A search result may not apply the security trimming.
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p>
          When users perform a search within SharePoint, although they may not have permissions to view the media item, the item title and metadata will appear in the search result. The user will not be able to play the media and see its content, only the title and other metadata (e.g. description, tags) are displayed. For example, if a media item “Green Organization.mp4” is uploaded to a SharePoint site, and the users don’t have any permission  to view content on this site, they will be able to search for the phrase “Green Organization” and see the media item “Green Organization.mp4” title and description in the search result view. If they clickon the mediea to play the item – the system will block the operation and an “Access Denied” message will be displayed. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="119">
        <p>
          Search results are based on basic metadata.
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p style="text-align: left;">
          The search connector (content crawler) is indexing text of the media’s name, description and tags. Search results will surface based on this metadata only and not for example based on custom metadata or transcription. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="119">
        The Search result is not scoped to a single site.
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        When users perform a search within a SharePoint site, the result items are originated from all the SP sites in the farm. Though this behavior might be satisfactory and desirable for a cross-organizational search, for example within a search center, it might be an issue for a team site that is searching for an in-site contextual search. <a href="https://kaltura.atlassian.net/browse/KMS-5886"><br /></a>
      </td>
    </tr>
  </tbody>
</table>

<h4 class="mce-heading-3">
  <a name="troubleshooting"></a>Troubleshooting and Important Notes!
</h4>

1.  The root category in the KAF admin configuration must be named "Sharepoint".
2.  The app/cab that was downloaded from the KAF admin to install the Kaltura Video Extension in SharePoint contains metadata: profiles ids, root category name, admin secret, server url, and partner ids. If the metadata was changed in the KAF admin, and the app/cab was not re-deployed in the SharePoint environment, it is possible you' may encounter unexpected issues.
3.  The Kaltura Video Extension for SharePoint only works with the new Browse Search and Embed (BSE) module in KAF. Be certain that it is enabled. The UiConf is found in KAF admin Browseandembed module. If during run-time the old Browse Search and Embed UI is displayed, you are probably missing a metadata profile. Workaround: Try disabling the new BSE UI and enable it again.
4.  The Kaltura Video Extension for SharePoint should not have the Publish action available from the My Media/entry page. If it is there, it may cause issues. Make sure that the manPublish field is disabled (both in the Hosted and Publish modules in the KAF admin). 
5.  For SharePoint developers: SharePoint embedding works with a unique id that is sent from SharePoint to KAF and its value is saved on the entry. If after embedding an entry and refreshing the page, the  BSE UI is displayed instead of the embedded entry, the unique id was either not sent properly or not saved. Workaround: Try checking the entry's metadata in the KMC to see if the value is there. If not, check if the value is sent from SharePoint when loading the page, or when trying to embed the media.
6.  The search connector (our WSP code) is currently not supportting proxy.
7.  It was noticed that in some cases when the Kaltura feature is activated, it is not working properly. Once clearing the existing objects and re-activating it works well. Try this if you encounter any problems.

 

<h4 class="mce-heading-3">
  Tested Browsers
</h4>

The following browsers were tested for this release (recommended resolution 1024x768):<span style="color: #ff0000;"> </span>

*   Microsoft Windws 7,8, 8.1: Internet Explorer 10 and 11; latest versions of Safari (8.0.2 and up), Chrome (40.0.2214.115 and up), and Firefox (35.0.1 and up)
*   Mac 10.7 and up: Latest versions of Safari (8.0.2 and up) and Chrome (40.0.2214.115 and up)
*   iOS 8 and up
*   Android 4.2 and up
*   Kaltura widgets in mobile browser - When oppening SP13 in mobile browser, kaltura widget and player (being HTML5 and responsive design) were verified to be working but not fully tested.