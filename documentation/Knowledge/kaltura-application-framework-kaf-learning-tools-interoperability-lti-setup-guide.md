---
layout: page
title: "Kaltura Application Framework (KAF) for Learning Tools Interoperability (LTI) Setup Guide"
date: 2015-11-30 23:47:03
---

<p>
    This guide describes how to setup the Kaltura Video integration within your LMS with the Kaltura Application Framework (KAF) settings. Information on how to control user roles and permissions using the Kaltura Application Framework (KAF) Admin Console is also provided.
  </p>
  
  <p>
    <a name="top"></a>The following topics are descriibed:
  </p>
  
  <ul>
    <li>
      <a href="#prereq">Prerequisities</a>
    </li>
    <li>
      <a href="#understanding">Understanding the Setup Process</a>
    </li>
    <li>
      <a href="#RolesandPermissions">Roles and Permissions</a>
    </li>
  </ul>
  
  <h1>
    <a name="prereq"></a>Prerequisites
  </h1>
  
  <div class="WordSection1">
    <p>
      The following items are required to setup the Kaltura Application Framework (KAF) as a tool provider within your LMS.
    </p>
    
    <ul>
      <li>
        Access to a LTI compliant LMS environment with site administrator role.
      </li>
      <li>
        A Kaltura account - Please contact your Kaltura representative for your Kaltura account details.<ul>
          <li>
            * KAF LTI Integration on your LMS environment. For installation/integration instructions, see …
          </li>
          <li>
            KAF Admin Console – please ask your Kaltura representative for credentials to access your KAF Admin Console instance.
          </li>
        </ul>
      </li>
    </ul>
    
    <a href="#top">Back to Top</a>
  </div>
  
  <div class="WordSection1">
    <div class="WordSection5">
      <h1>
        <a name="understanding"></a>Understanding the Setup Process
      </h1>
      
      <p>
        The KAF LTI Integration offers an out-of-the-box solution that enables users to view, record, upload, publish, search, and share video directly from their LMS environment. This translates into time and money saved for your organization, improved student engagement, creativity and learning results, as well as ease of use for students, faculty and teaching assistants
      </p>
      
      <h2>
        The Kaltura Application Framework (KAF) Admin Console
      </h2>
      
      <p>
        The Generic KAF LTI Integration is implemented on top of the Kaltura Application Framework (KAF), a feature rich framework that allows flexible and streamlined integration of Kaltura’s video solutions and products into 3rd party applications. KAF is hosted and served directly from the Kaltura cloud servers and once integrated into your LMS environment, presents different video components and workflows to users.
      </p>
      
      <p>
        At the backend, the Kaltura Application Framework provides a flexible and extensible administration panel, called “KAF Admin Console”. The KAF Admin Console offers full control over the user experience and when interacting with videos inside KAF.
      </p>
      
      <h2>
        KAF Modules
      </h2>
      
      <p>
        Your KAF instance is composed of multiple <strong>KAF modules</strong>, such as “Application”, “Player”, and “Auth”. Each module controls a different aspect of your LMS integration. A KAF module is composed of a set of <strong>configuration fields</strong>. All KAF modules are listed on the left menu in your KAF Admin Console instance.<br /><img src="{{site.url}}/assets/2589">
      </p>
      
      <p class="mce-note-graphic">
        <span>Your KAF Admin Console may display modules and configuration fields that are not listed in this guide, some of which may be disabled. It is important that you do not modify the configuration of the disabled modules (and not enable them) without consulting your Kaltura representative.</span>
      </p>
      
      <p>
        The following KAF modules are required for configuring the Kaltura Application Framework (KAF) LTI integration and are described in this guide:
      </p>
      
      <h3>
        Global
      </h3>
      
      <ul>
        <li>
          <a href="#application">Application</a>
        </li>
        <li>
          <a href="#auth">Auth</a>
        </li>
        <li>
          <a href="#channels">Channels</a>
        </li>
        <li>
          <a href="#client">Client</a>
        </li>
        <li>
          <a href="#debug">Debug</a>
        </li>
        <li>
          <a href="#gallery">Gallery</a>
        </li>
        <li>
          <a href="#metadata">Metadata</a>
        </li>
        <li>
          <a href="#moderation">Moderation</a>
        </li>
        <li>
          <a href="#player">Player</a>
        </li>
        <li>
          <a href="#Security">Security</a>
        </li>
        <li>
          <a href="#widgets">Widgets</a>
        </li>
        <li>
          <a href="#search">Search </a>
        </li>
        <li>
          <a href="#mediacollaboration">MediaCollaboration</a>
        </li>
        <li>
          <a href="#PlaylistPage">PlaylistPage</a>
        </li>
      </ul>
      
      <h3>
        Modules
      </h3>
      
      <ul>
        <li>
          <a href="#addcontent">Addcontent</a>
        </li>
        <li>
          <a href="#Attachments">Attachments</a>
        </li>
        <li>
          <a href="#Captions">Captions</a>
        </li>
        <li>
          <a href="#Clipper">Clipper</a>
        </li>
        <li>
          <a href="#Comments">Comments</a>
        </li>
        <li>
          <a href="#Disclaimer">Disclaimer</a>
        </li>
        <li>
          <a href="#Downloadmedia">Downloadmedia</a>
        </li>
        <li>
          <a href="#Embed">Embed</a>
        </li>
        <li>
          <a href="#Embedplaylist">EmbedPlaylist</a>
        </li>
        <li>
          <a href="#Sidemymedia">Sidemymedia</a>
        </li>
        <li>
          <a href="#Thumbnails">Thumbnails</a>
        </li>
        <li>
          <a href="#Userreports">Userreports</a>
        </li>
      </ul>
      
      <h3>
        Modules/Channels
      </h3>
      
      <ul>
        <li>
          <a href="#Channelmoderation">Channelmoderation</a><a href="https://kaltura.sharepoint.com/community-team/Shared%20Documents/Knowledge%20Management/Final%20Documents%20-%20Ready%20for%20Publishing/KAF/LTI/Setup_Guide/KAF_LTI_Setup_Guide.docx#_Channelmoderation_2"> </a>
        </li>
      </ul>
      
      <h3>
        Modules/Entry Types
      </h3>
      
      <ul>
        <li>
          <a href="#Audioentry">Audioentry</a>
        </li>
        <li>
          <a href="#Imageentry">Imageentry</a>
        </li>
        <li>
          <a href="#Screencapture">Screencapture</a>
        </li>
        <li>
          <a href="#Videopresentations">Videopresentations</a>
        </li>
        <li>
          <a href="#YouTube">Youtube</a>
        </li>
      </ul>
      
      <h3>
        Modules/Custom/Core/KAF
      </h3>
      
      <ul>
        <li>
          <a href="#Ltigeneric">Browseandembed</a>
        </li>
        <li>
          <a href="#Ltigeneric">Ltigeneric</a>
        </li>
        <li>
          <a href="#hosted2">Hosted</a>
        </li>
        <li>
          <a href="#quiz">Quiz</a>
        </li>
      </ul>
      
      <h2>
        KAF Administration: Actions and Configurable Fields
      </h2>
      
      <p>
        Your KAF account comes pre-configured with the following settings. Items marked with * should not be changed.
      </p>
      
      <h3>
        General Settings
      </h3>
      
      <table style="width: 763px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="164">
              <p class="TableHeading">
                Module
              </p>
            </td>
            
            <td valign="top" width="228">
              <p class="TableHeading">
                Fields
              </p>
            </td>
            
            <td valign="top" width="371">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                Application
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                InstanceId, privacyContext, userRoleProfile
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Internal constant identifiers of your KAF instance. Please note that privacyContext should be empty.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                <a name="auth"></a>Auth
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                sslSettings
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                All site (set to None if SSL is not used)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" rowspan="2" width="164">
              <p class="TableBodyText">
                Debug
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                serviceUrl
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                <a href="https://www.kaltura.com/">https://www.kaltura.com</a> (set to http://www.kaltura.com if SSL is not used)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                VerifySLL
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes (set to No if SSL is not used)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                <a name="Security"></a>Security
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                allowLoadInIframe
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                Addcontent
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                Userreports
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                Publish
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                <a name="Browseandembed"></a>Browseandembed
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                Ltigeneric
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" rowspan="8" width="164">
              <p class="TableBodyText">
                <a name="Hosted"></a>Hosted
              </p>
            </td>
            
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enableLike
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes/No
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enableViews
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes/No
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                allowEditPublished
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Set to <em>No</em> if you want to prevent users from editing entries after they have been published to a course Media Gallery or embedded using the Browse, Search and Embed module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                allowDeletePublished
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Set to <em>No</em> if you want to prevent users from deleting entries after they have been published to a course Media Gallery or embedded using the Browse, Search and Embed module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                enableEntryDelete
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Set to <em>No</em> to completely prevent users from deleting entries
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                manPublish
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Yes* (Unless publish plugin was integrated).
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="228">
              <p class="TableBodyText">
                authMethod
              </p>
            </td>
            
            <td style="text-align: left;" width="371">
              <p class="TableBodyText">
                Lti
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h2>
        Configuration Management: Global
      </h2>
      
      <ol class="mce-note-graphic">
        <li>
          Some fields are displayed only when you select a specific value for a different field.
        </li>
        <li>
          The group's configurable fields follow the group name.
        </li>
      </ol>
      
      <p class="Procedure mce-procedure">
        To modify KAF configuration modules
      </p>
      
      <ul>
        <li>
          In the KAF Admin window select the Manage Configuration tab.
        </li>
      </ul>
      
      <strong class="mce-note-graphic">Related KAF modules: </strong><span class="mce-note-graphic">Application, Auth, Client, Security, Categories, Addcontent, Publish, Browseandembed, Ltigeneric, Hosted</span><br /><h3>
        <a name="application"></a><span style="font-size: 1.17em;">Applica</span><span style="font-size: 1.17em;">tion</span>
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="224">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="569">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                instanceId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Unique string to identify that installation of the LMS. This value can be set during installation only.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                privacyContext
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                String used to be set as privacy context on root category. This value can be set during installation only.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                userRoleProfile
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Metadata Profile ID for user's role per KAF installation instance
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                title
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                What is your LMS website title? The website title is displayed in the browser's title bar and usually is displayed in search engine results. Page titles consist of the name of the currently loaded media and the website title. For example, if a page has a video called 'My Video' and 'LMS' is the website title, the page title is: 'My Video – LMS
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                footer
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                What is your LMS footer text?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                language
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Which language should KAF use? Note: Language files are in /locale/kms/{LANG}/default.po. See <a href="{{site.url}}/documentation/Knowledge/what-are-supported-kmc-and-kms-languages.html">here</a> for the list of supported KAF localization languages.
              </p>
              
              <p class="TableBodyText">
                Fr = French
              </p>
              
              <p class="TableBodyText">
                Jp= Japanese
              </p>
              
              <p class="TableBodyText">
                SR= Serbian
              </p>
              
              <p class="TableBodyText">
                Pt-Br Portuguese Brazlian
              </p>
              
              <p class="TableBodyText">
                En = English
              </p>
              
              <p class="TableBodyText">
                Es- Spanish
              </p>
              
              <p class="TableBodyText">
                D2L = custom language for LMS
              </p>
              
              <p class="TableBodyText">
                En_Custom = custom language
              </p>
              
              <p class="TableBodyText">
                Ar = Arabic
              </p>
              
              <p class="TableBodyText">
                De = German
              </p>
              
              <p class="TableBodyText">
                Da - Danish
              </p>
              
              <p class="TableBodyText">
                Ca-es -Catalan
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                enableLike
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Enable the 'Like' feature for entries. This should be configured in the Hosted module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                enableWebcam
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Enable or Disable the Webcam upload.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                enableEntryTitles
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Include the media title in the URL of the media page when browsing the site and sharing a link to the media.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                allowEditPublished
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Enable editing of published entries. This should be configured in the Hosted module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                allowDeletePublished
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Enable deletion of published entries. This should be configured in the Hosted module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                enableEntryDelete
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Enable deleting the media from the LMS. This should be configured in the Hosted module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                enableViews
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Enable showing number of views per entry. This should be configured in the Hosted module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                showPageTitles
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Show page titles. This should be configured in the Hosted module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                enableUnlisted
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Enable setting entries as unlisted. An unlisted entry can be viewed by anyone with the link to the entry page. Unlisted media can be accessed by anyone with a direct link to the media page and will not be displayed in search results. This is not relevant for KAF applications.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                timezone
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Which <a href="http://php.net/manual/en/timezones.php">timezone</a> should The LMS use to present times and dates.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="224">
              <p class="TableBodyText">
                assetConsolidationEnabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="569">
              <p class="TableBodyText">
                Enable assets (js/css) consolidation and minification.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="channels"></a>Channels
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="45%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="54%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="45%">
              <p class="TableBodyText">
                entriesPageSize
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="54%">
              <p class="TableBodyText">
                How many entries can be displayed on each channel/course page? (The default is 15)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="45%">
              <p class="TableBodyText">
                pagerType
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="54%">
              <p class="TableBodyText">
                Which kind of paging mechanism should be used in the channel/course page?
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="client"></a>Client
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                serviceUrl
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                The URL of the service for API calls. Modify the URL if you use the Kaltura On-Prem Edition.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                CDNUrl
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                The CDN regular URL Used for Player and html5lib. Leave empty for default.
              </p>
              
              <p class="TableBodyText">
                You can change the Kaltura Server CDN URL used by the Kaltura HTML5 player and player embeds. The default value is http://cdnapi.kaltura.com. To update your CDN URL, add the URL in this field.
              </p>
              
              <p class="TableBodyText">
                Note: When configuring a KMS site to HTTPS, also change the CDN URL to https://cdnapisec.kaltura.com.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                SecuredCDNUrl
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                The CDN <em>secured</em> URL. Used for Player and html5lib. Leave empty for default.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                partnerId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Copy your Kaltura account's Partner ID from the Kaltura Management Console (KMC): KMC->Settings->Integration Settings.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                secret
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Copy your Kaltura account's user secret from KMC->Settings->Integration Settings (http://www.kaltura.com/index.php/kmc/kmc4#account|integration). Kaltura uses your user secret to create secure sessions to access the Kaltura API.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                adminSecret
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Copy your Kaltura account's administrator secret from KMC->Settings->Integration Settings (http://www.kaltura.com/index.php/kmc/kmc4#account|integration). KAF uses your administrator secret when you need an 'admin' session, which allows more actions than a user secret session.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                verifySSL
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Set to No, if you want to use SSL with a self-signed certificate.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="debug"></a>Debug
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="18%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="81%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="18%">
              <p class="TableBodyText">
                logLevel
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="81%">
              <p class="TableBodyText">
                Debug level of the KAF Log File (logs/kms.log)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="18%">
              <p class="TableBodyText">
                kalturaDebug
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="81%">
              <p class="TableBodyText">
                Enable debug log of requests to the Kaltura API (logs/apidebug.log)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="18%">
              <p class="TableBodyText">
                kalturaStats
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="81%">
              <p class="TableBodyText">
                Enable stats log of requests to the Kaltura API (logs/api.log)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="18%">
              <p class="TableBodyText">
                emailErrors
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="81%">
              <p class="TableBodyText">
                Enable sending emails in case of errors
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="gallery"></a>Gallery
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="19%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="80%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                pageSize
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                How many entries can be displayed on each gallery page? (The default is 10.)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                pageSizeWide
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                How many entries can be displayed on each gallery page in the Wide gallery view (for example, search results, playlists)? (The default is 24.)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                pageCount
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                How many page links can be displayed in the gallery pager? (Dots represent page links that are not displayed.)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                pagerType
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                Which kind of paging mechanism should be used in the gallery page?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                sortMediaBy
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                By default, how should media in the gallery be sorted?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                globalSearchSortMediaBy
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                By default, how should media in the global search be sorted?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                thumbnailRotator
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                Enable thumbnail image rotation on mouse over in galleries
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                categoryDefaultView
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                Default view for categories. You can define optional view modes for media items inside Galleries. Choose from Grid, Collapsed view or Detailed view.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="19%">
              <p class="TableBodyText">
                categoryExplicitDateFormat
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="80%">
              <p class="TableBodyText">
                Explicit date format.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="metadata"></a>Metadata
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="21%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="78%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="21%">
              <p class="TableBodyText">
                descriptionRequired
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="78%">
              <p class="TableBodyText">
                Require users to fill in the 'Description' field when uploading or editing media?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="21%">
              <p class="TableBodyText">
                tagsRequired
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="78%">
              <p class="TableBodyText">
                Require users to fill in the 'Tags' field when uploading or editing media?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="21%">
              <p class="TableBodyText">
                readMoreEnabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="78%">
              <p class="TableBodyText">
                Enable/disable read more for entry description - shortening to 500 characters. <strong><em><span style="text-decoration: underline;">Notice</span></em></strong>: channel and category description is always shortend.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="21%">
              <p class="TableBodyText">
                metaDataInReadMore
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="78%">
              <p class="TableBodyText">
                If enabled metadata is hidden until clicking on 'read more...' works for all descriptions - entry/channel/category
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="21%">
              <p class="TableBodyText">
                basicNameFieldHelperText
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="78%">
              <p class="TableBodyText">
                Tooltip comment for the <strong><em>Name</em></strong> field when uploading or editing an entry.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="21%">
              <p class="TableBodyText">
                basicDescriptionFieldHelperText
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="78%">
              <p class="TableBodyText">
                Tooltip comment for the <strong><em>Description</em></strong> field when uploading or editing an entry.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="21%">
              <p class="TableBodyText">
                basicTagsFieldHelperText
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="78%">
              <p class="TableBodyText">
                Tooltip comment for the <strong><em>Tags</em></strong> field when uploading or editing an entry.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="21%">
              <p class="TableBodyText">
                showDescriptionInTooltipMeta
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="78%">
              <p class="TableBodyText">
                Choose whether to display field's description as a tooltip
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="moderation"></a>Moderation
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="17%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="82%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="17%">
              <p class="TableBodyText">
                reasonSex
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="82%">
              <p class="TableBodyText">
                Please provide the reasons The LMS users can choose for flagging media. (If none are provided, the default Kaltura reasons will be used)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="17%">
              <p class="TableBodyText">
                reasonViolence
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="82%">
              <p class="TableBodyText">
                Please provide the reasons The LMS users can choose for flagging media. (If none are provided, the default Kaltura reasons will be used)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="17%">
              <p class="TableBodyText">
                reasonHarmful
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="82%">
              <p class="TableBodyText">
                Please provide the reasons The LMS users can choose for flagging media. (If none are provided, the default Kaltura reasons will be used)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="17%">
              <p class="TableBodyText">
                reasonSpam
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="82%">
              <p class="TableBodyText">
                Please provide the reasons The LMS a reasons will be used)
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="player"></a>Player
      </h3>
      
      <p>
        Kaltura Application Framework LTI instances are automatically created using the <a href="{{site.url}}/documentation/Knowledge/kaltura-player-toolkit.html">Kaltura v2 Player</a>.
      </p>
      
      <table style="width: 763px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="98">
              <p class="TableHeading">
                Module
              </p>
            </td>
            
            <td valign="top" width="245">
              <p class="TableHeading">
                Fields
              </p>
            </td>
            
            <td valign="top" width="420">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" rowspan="5" width="98">
              <p class="TableBodyText">
                Player
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="245">
              <p class="TableBodyText">
                playerId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="420">
              <p class="TableBodyText">
                What is the player ID (uiConf ID) of the player that plays the embedded video?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="245">
              <p class="TableBodyText">
                playerBarHeightPixels
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="420">
              <p class="TableBodyText">
                The height (in pixels) of the player ui which is not part of the actual video (for example - the bottom bar)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="245">
              <p class="TableBodyText">
                playerVideoRatioPercent
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="420">
              <p class="TableBodyText">
                The ratio (in percent) of the video inside the player. Standard values: 16:9 = 56.25 , 4:3 = 75 , 16:10 = 62.5
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="245">
              <p class="TableBodyText">
                playerEditId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="420">
              <p class="TableBodyText">
                What is the player ID (uiConf ID) of the player that edits entries?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="245">
              <p class="TableBodyText">
                autoPlayOnLoad
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="420">
              <p class="TableBodyText">
                When KAF loads, should the video that is loaded in the player begin playing automatically? Notes: (1) Autoplay is triggered when KAF starts and each time a new page loads, such as when switching from My Playlists to a gallery page. (2) The player always begins playing automatically when a user clicks a video in a gallery, regardless of whether autoPlayOnLoad is enabled.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="98">
              <p class="TableBodyText">
                 
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="245">
              <p class="TableBodyText">
                playback
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="420">
              <p class="TableBodyText">
                Which Playback method should KAF use? Kaltura Auto' is the default playback option for a new KAF instance.
              </p>
              
              <p class="TableBodyText">
                KAF administrators can select additional playback options. From <em>Player > playback</em>, select any of the following options:
              </p>
              
              <ul>
                <li>
                  <strong>Auto</strong> - Kaltura server chooses between HTTP Progressive Download and Akamai’s HTTP Adaptive Streaming, based on entry duration and available flavors. Auto gives you the best video delivery and playback quality for your entry.
                </li>
                <li>
                  <strong>HTTP Progressive Download</strong> – Allows you to pause the video playback and wait for the content to download. Typically used where viewers have very limited bandwidth and might experience more buffering than adaptive bitrate.
                </li>
                <li>
                  <strong>HTTP Streaming (HDS)</strong> - HTTP streaming based on Adobe technology. Allows adaptive bitrate so the player can adjust the video quality on the fly based on network and CPU conditions.
                </li>
                <li>
                  <strong>HTTP Streaming (Akamai HD)</strong> – HTTP streaming based on Akamai’s technology. Allows adaptive bitrate so the player can adjust the video quality on the fly based on network and CPU conditions, formally called Akamai HD.
                </li>
                <li>
                  <strong>RTMP Streaming</strong> – RTMP streaming based on Adobe technology. Allows adaptive bitrate so the player can adjust the video quality on the fly based on network and CPU conditions.
                </li>
                <li>
                  <strong>Secure Transport (RTMPE)</strong> - RTMP encrypted using Adobe's security mechanism which wraps the RTMP session in a lighter-weight encryption layer.
                </li>
              </ul>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="98">
              <p class="TableBodyText">
                 
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="245">
              <p class="TableBodyText">
                playerModerationId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="420">
              <p class="TableBodyText">
                What is the player ID (uiConf ID) of the player shown in moderation pages?
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="widgets"></a>Widgets
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="13%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="86%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="13%">
              <p class="TableBodyText">
                ksuId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="86%">
              <p class="TableBodyText">
                What is the uiConf ID of the Kaltura Simple Uploader (KSU)? KAF uses KSU to upload videos, images, and audio files.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="13%">
              <p class="TableBodyText">
                krecordId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="86%">
              <p class="TableBodyText">
                What is the  uiConf ID of the kRecord widget? KAF uses kRecord to record and upload video from a webcam.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="13%">
              <p class="TableBodyText">
                rtmpUrl
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="86%">
              <p class="TableBodyText">
                What is the URL of your RTMP Server? The URL is required for Webcam recording.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="13%">
              <p class="TableBodyText">
                krecordDefaults
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="86%">
              <p class="TableBodyText">
                Configure recording details. <em>Select Yes</em><em>, to </em>expose additional fields to configure the webcam widget quality.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="13%">
              <p class="TableBodyText">
                emailErrors
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="86%">
              <p class="TableBodyText">
                Enable sending emails in case of errors.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="search"></a>Search
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                entriesPageSize
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                How many entries to show in search results.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                inVideoPageSize
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                How many in-entry search results to show.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="mediacollaboration"></a>MediaCollaboration
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                mediaCollaborationEnabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable MediaCollaboration module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                changeOwnerEnabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p>
                This field is available when the MediaCollaboration module is enabled. The change owner feature has a special configuration for the co-editor/co-publisher and can be set to enable or disable the co-editor or co-publisher without any dependencies.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <p>
        To add a user as co-editor or co-publisher, the user must log in to KAF prior to using this feature.
      </p>
      
      <p>
        Enable this module to change the media owner and edit co-editors and co-publishers.
      </p>
      
      <p class="mce-note-graphic">
        <span>If configuration is set to 'no' after it was set to 'yes' and in the interim, entries were added with co-editors and co-publishers, all co-editors and co-publishers will lose their ability to view, edit or publish those entries.</span>
      </p>
      
      <h2>
        Configuration Management: Modules
      </h2>
      
      <ol class="mce-note-graphic">
        <li>
          Some fields are displayed only when you select a specific value for a different field.
        </li>
        <li>
          Field group names are in bold. The group's configurable fields follow the group name.
        </li>
      </ol>
      
      <h3 class="mce-note-graphic">
        <a name="addcontent"></a>Addcontent
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="17%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="82%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="17%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="82%">
              <p class="TableBodyText">
                Enable the Addcontent module.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Attachments"></a>Attachments
      </h3>
      
      <p>
        Enable this module to:
      </p>
      
      <ul>
        <li>
          allow media owners to attach files of any type to their media,
        </li>
        <li>
          Enable media viewers to download the file before, during or after viewing.
        </li>
      </ul>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="17%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="82%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="17%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="82%">
              <p class="TableBodyText">
                Enable the Attachments module.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Captions"></a>Captions
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Captions module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                captionsKsuId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the uiConf ID of the Kaltura Simple Uploader (KSU) used for captions? KAF uses KSU to upload .SRT and .DFXP caption files.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                thumbnailRotator
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable thumbnail image rotation on mouse over in captions search results
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                entriesPageSize
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p>
                How many entries are displayed as captions search results on each page? (The default is 10)
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                captionsPageSize
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                How many caption lines are displayed for each entry in search results? (The default is 5)
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Clipper"></a>Clipper
      </h3>
      
      <p>
        Enable this module to create a Clip button in the Edit Media page. The Create Clip feature allows media owners to create clips directly from the Edit Media page.
      </p>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p>
                <strong>Field</strong>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p>
                <strong>Description</strong>
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p>
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Clipper module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p>
                showClipAttribution
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Should a clipped entry page contain an attribution to the original entry.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p>
                clipKdpUiconfId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the uiConf ID of the clipper kdp.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p>
                clippAppUiconfId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the uiConf ID of the clipp App.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p>
                clipperProfileId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                The clipper custom data profile id.)
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Comments"></a>Comments
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="38%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="61%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Enable the Comments module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                channelCommentsProfileId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Custom Metadata profile Id for channels
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                entryCommentsProfileId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Custom Metadata profile Id for entries
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                entryCommentsCountProfileId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Custom Metadata profile Id for entry comments count
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                commentsAllowed
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Who can add comments?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                pageSize
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Number of comments to display
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                sort
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Sort comments by newest or oldest first?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                sortReplies
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Sort replies by newest or oldest first?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                allowClose
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Allow content owners to disable/close comments for particular entries
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                showInGalleries
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Enable/disable showing of comments for entries in the gallery page
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                showInChannels
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Enable/disable showing of comments for entries in the channels page
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                showInChannelsOnly
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Show comments on media entries to users only in the context of a channel/gallery. In this case, users will not be able to see media comments if browsing to the media from search results, my media or any other context that doesn't include the context of the channel/gallery. To enable this feature, from the KAF Admin > Comments set showInChannelsOnly to Yes.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                showAddTimedCommentsCheckbox
              </p>
              
              <p class="TableBodyText">
                 
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Show Add comment at mm:ss checkbox.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="38%">
              <p class="TableBodyText">
                showPrivateCommentsConfig
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="61%">
              <p class="TableBodyText">
                Show configuration for setting private comments per gallery/channel
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Disclaimer"></a>Disclaimer
      </h3>
      
      <p>
        KAF administrators can enforce the Terms of Agreement text and checkbox for end-users to review and/or accept before uploading or publishing content.
      </p>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p>
                <strong>Field</strong>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p>
                <strong>Description</strong>
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Disclaimer module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                disclaimerProfileId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                The disclaimer custom data profile id.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                disclaimerField
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Which custom data field is required to be checked when uploading or publishing media?.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                disclaimerText
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Text to show when explaining user the reason for this checkbox.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                agreeText
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                The text to display next to the checkbox that the user accepts the terms of agreements.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                displayArea
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Before Upload - Terms of agreement are displayed to the user before they can contribute content. Only after the user agrees, the upload, launch screen recorder and other buttons are displayed. After checking the box, the button (or other option to upload) is enabled and the checkbox is disabled so it cannot be unchecked.
              </p>
              
              <p class="TableBodyText">
                Before Publish - Terms of agreement are presented as part of metadata in the upload screen and in the edit media screen. The checkbox can be configured as a required field preventing the user from publishing media if the checkbox is not selected (This is the same behavior as when required metadata is not completed). After terms are agreed to by the user (The checkbox is selected and saved) the field turns into view only and select cannot be unchecked,
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                agreeRequired
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                This is relevant only if selected to show before publish. In this case the module displays the text of the terms of agreement and does not display a checkbox for the user to select.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Downloadmedia"></a>Downloadmedia
      </h3>
      
      <p>
        Enable this module to configure downloadable versions of the media for viewers to download from the media page.
      </p>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p>
                <strong>Field</strong>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p>
                <strong>Description</strong>
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Downloadmedia module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                downloadRoles
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Select one or more roles that can use the Downloadmedia module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                downloadFlavors
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Click Add Download Flavors to configure the flavors that will be visible to the media owner to choose from. You, the admin, choose as many flavors as you want from the list of the transcoding profiles, as they appear in the KMC. You then can name the flavors as they should be displayed to the media owner. If no name is given, the flavor default name in Kaltura is used as the default name. The final list that is displayed to the media owner includes the list that was chosen by the admin, the flavors that are actually set (in the KMC) for this KAF instance and all other available flavors on the specific entry. It is advised that the KAF admin will verify with KMC admin what flavors are checked for the account beforehand.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h4>
        Example of Downloadmedia Configuration<br /><img src="{{site.url}}/assets/2590">
      </h4>
      
      <h3>
        <a name="Embed"></a>Embed
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Embed module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                showMediaURL
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Show link to media page.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                emailShare
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Sharing by email
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                allowEmbedIframeShare
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Allow/Restrict sharing using 'iframe'. This configuration is only supported for non v2 supported players
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                embedAllowed
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Select one or more roles that can use the Embed module. Use 'Ctrl' to select multiple roles. His End-users can share Kaltura unlisted and published media via Email. This is available in share tab, like media grab embed and page link. The media will be shared by the default mail client on the machine.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                embedSkins
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Define skins that can be used for embedded players.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                name
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the name of the skin? The skin name is displayed when the user selects an embed skin.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                imgFile
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the relative path to the image file on the server? The image file represents how the skin looks.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                uiConfId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the numerical value of the player ID to use in the embed code?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                embedSizes
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Define sizes that can be used for embedded players. Define the player size in the following format: {width}x{height}
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                large
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                608x402
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                medium
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                400x285
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                small
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                304x231
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Sidemymedia"></a>Sidemymedia
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                 
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
               
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Thumbnails"></a>Thumbnails
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p>
                <strong>Field</strong>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p>
                <strong>Description</strong>
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p>
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p>
                Enable the Thumbnails module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p>
                thumbnailsKsuId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p>
                What is the uiConf ID of the Kaltura Simple Uploader (KSU) used for thumbnails upload? KAF uses KSU to upload thumbnails files.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p>
                extensionWhitelist
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p>
                define allowed extensions, example: jpg, png, jpeg, gif (one item per extension)
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Userreports"></a>Userreports
      </h3>
      
      <p>
        Channel/Course Managers can measure and analyse the user engagement and contribution to their channels/courses. These contextual analytics allow channel/course managers to answer important questions such as: What are the most popular videos in the channel/course? Who are the members that watch the most videos and what is their drop off rate? Who are the members that contribute the most media to the channel/course?
      </p>
      
      <p>
        The mediaAnalytics field should be enabled to display the Analytics page. The Analytics page is accessed from the 'Actions' drop down of the entry page. The Analytics report is identical to the analytics for the entry in the KMC.
      </p>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p>
                <strong>Field</strong>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p>
                <strong>Description</strong>
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Userreports module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                mediaAnalytics
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable media analytics for media owner
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                num_days
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Default number of days
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                page_size
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Default page size
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h2>
        Configuration Management: Channel Modules
      </h2>
      
      <h3>
        <a name="Channelmoderation"></a>Channelmoderation
      </h3>
      
      <p>
        You can define whether new Media Galleries that are created should be moderated by default. In addition, LMS administrators can configure if the moderation option can be disabled by Media Gallery managers, to comply with use cases where moderation must be enforced. In the <em>Channelmoderation</em> module, you can set the <em>moderationDefaultValue</em> to define if the moderation option should be enabled or not by default when Media Galleries are created.
      </p>
      
      <ul>
        <li>
          If forceModeration = None then the moderationDefaultValue comes into play and the default value is set accordingly
        </li>
        <li>
          If forceModeration = Moderated or Not Moderated then this field is the stronger one and sets the default behavior.
        </li>
      </ul>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <tbody>
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableHeading">
                Module
              </p>
            </td>
            
            <td style="text-align: left;" width="317">
              <p class="TableHeading">
                Fields
              </p>
            </td>
            
            <td style="text-align: left;" width="282">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" rowspan="2" width="164">
              <p class="TableBodyText">
                Channelmoderation
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="317">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="282">
              <p class="TableBodyText">
                Enable the Channelmoderation module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="317">
              <p class="TableBodyText">
                forceModeration
              </p>
            </td>
            
            <td style="text-align: left;" width="282">
              <p class="TableBodyText">
                Force moderation on every new Media Gallery creation.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="164">
              <p class="TableBodyText">
                 
              </p>
            </td>
            
            <td style="text-align: left;" width="317">
              <p class="TableBodyText">
                moderationDefaultValue
              </p>
            </td>
            
            <td style="text-align: left;" width="282">
              <p class="TableBodyText">
                Default value when moderation checkbox is enabled
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h2>
        Configuration Management: Entry Type Modules
      </h2>
      
      <h2>
        Authoring Methods
      </h2>
      
      <p class="mce-note-graphic">
        <strong>Related KAF modules: </strong><span>Widgets, Screencapture, Videopresentations, Captions, Metadata</span><strong>, </strong><span>Customdata</span>
      </p>
      
      <p>
        The KAF Admin Console provides great flexibility in configuring different authoring methods users can utilize for creating new content. To date, the following methods are available (with additional methods to be added in the future):
      </p>
      
      <ul>
        <li>
          Uploading media from a  local machine
        </li>
        <li>
          Capturing a video from a webcam using the Kaltura Webcam Recorder (KRecord)
        </li>
        <li>
          Adding a Video Presentation
        </li>
        <li>
          Creating a new screencast using the Kaltura Screen Recorder (KSR)
        </li>
      </ul>
      
      <p>
        Please refer to the <a href="{{site.url}}/documentation/Knowledge/kaltura-application-framework-kaf-learning-tools-interoperability-lti-integration-guide.html" target="_blank">KAF LTI User Guide</a> for more details about each of these methods.<br /><img src="{{site.url}}/assets/2591">
      </p>
      
      <h3>
        <a name="Audioentry"></a>Audioentry
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="44%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="55%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="44%">
              <p class="TableBodyText">
                customPlayerId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="55%">
              <p class="TableBodyText">
                What is the player ID (uiConf ID) of the player that plays audios?  Leave blank to use the default player.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="44%">
              <p class="TableBodyText">
                playerBarHeightPixels
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="55%">
              <p class="TableBodyText">
                The height (in pixels) of the custom player ui which is not part of the actual video (for example - the bottom bar). Leave blank to use the default player value.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="44%">
              <p class="TableBodyText">
                playerVideoRatioPercent
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="55%">
              <p class="TableBodyText">
                The ratio (in percent) of the audio inside the player. Standard values: 16:9 = 56.25 , 4:3 = 75 , 16:10 = 62.5. Leave blank to use the default player value.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="44%">
              <p class="TableBodyText">
                embedSizes
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="55%">
              <p class="TableBodyText">
                Define sizes that can be used for embedded players. Define the player size in the following format: {width}x{height}. This setting requires a custom player. If a custom player is not specified, the audio entry uses the default video player.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Imageentry"></a>Imageentry
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                imagePlayerId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the player ID (uiConf ID) of the player that shows images?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                imageWatermarkUrl
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the URL of the image that should be used as watermark?
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Screencapture"></a>Screencapture
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Screencapture module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                ksrId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the widget ID (uiConf ID) of the Kaltura Screen Recorder Widget (KSR) used in The LMS?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                videoBitrate
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                The video bitrate quality (in kbps) to use for the capture. For example 2000
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                advancedOptionsEnabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the option to select frames per second by the user
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                limitationNoteEnable
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Show limitation note?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                limitationNote
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Configure limitation note.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Videopresentations"></a>Videopresentations
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Videopresentations module
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                sortMediaBy
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                By default, how should media in the gallery be sorted?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                kpwid
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the widget ID (uiConf ID) of the Kaltura Video-Presentation Widget used in the LMS?
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                kvpmDocUploadId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the uiConf ID of the Kaltura Document Upload widget? The Kaltura Document Upload widget is used by the Kaltura Video-Presentation widget.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                kvpmCreationId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                What is the uiConf ID of the Kaltura Video-Presentation widget? The Video-Presentation widget enables users to synchronize video with PowerPoint presentations.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="YouTube"></a>YouTube
      </h3>
      
      <p>
        The LMS users can add YouTube video content and metadata into The LMS. Hosted content on YouTube is played back on the Kaltura V2 player from version 2.13 and above. To update the player to the latest player version, re-save the player settings in the KMC Studio > Universal Studio tab.
      </p>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="32%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="67%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="32%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="67%">
              <p class="TableBodyText">
                Enable the Youtube module
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="32%">
              <p class="TableBodyText">
                previewPlayer
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="67%">
              <p>
                The player uiconf to use for the YouTube entry preview when adding a new entry. Leave blank to use the default KAFplayer.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="32%">
              <p class="TableBodyText">
                replaceYouTubeEntryMessage
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="67%">
              <p class="TableBodyText">
                The message to display when replacing a YouTube entry.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h2>
        <a name="Channelplaylists"></a>Channelplaylists
      </h2>
      
      <p>
        There are three admin modules used to configure the Channel Playlists: For reference, the Channelplaylists modules are used to create and modify course playlists.
      </p>
      
      <ul>
        <li>
          Channelplaylists
        </li>
        <li>
          <a href="#PlaylistPage">PlaylistPage</a>
        </li>
        <li>
          <a href="#Embedplaylist">Embedplaylist</a>
        </li>
      </ul>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the ChannelPlaylists module
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                channelPlaylistsTabName
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                The title of the tab which will be added to the channel (Media Gallery) and will be presented first.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                entriesSource
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Add media to the playlist from the cahnnel gallery itself, from My Media or from all entitled areas in the site.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <p>
        From this page you can:
      </p>
      
      <ul>
        <li>
          <a href="#enable_course_playlists">Enable the Course Playlists feature </a>
        </li>
        <li>
          <a href="#renaming">Rename the Channel Playlists Tab's name</a>
        </li>
      </ul>
      
      <h3>
        <a name="enable_course_playlists"></a>Enabling Course Playlists
      </h3>
      
      <p>
        Course Playlists (Channelplaylists) activated by default for the KAF LTI instances.
      </p>
      
      <p class="Procedure mce-procedure">
        To enable Course Playlists
      </p>
      
      <ol>
        <li>
          From the <strong>Channelplaylists</strong> page change the setting in the <strong>enabled</strong> field from <strong>No</strong> to <strong>Yes</strong>.
        </li>
        <li>
          Click <strong>Save</strong> to apply the changes.
        </li>
      </ol>
      
      <h3>
        <a name="renaming"></a>Renaming the Playlists Tab
      </h3>
      
      <p>
        Admin users can rename the Playlists tab that appears in Media Gallery page:
      </p>
      
      <p class="Procedure mce-procedure">
        To rename the Playlists tab:
      </p>
      
      <ol>
        <li>
          From the <strong>Channelplaylists</strong> page change the setting in the <strong>CoursePlaylistsTabName</strong> field from <strong>Playlists</strong> to any value you want.
        </li>
        <li>
          Click <strong>Save</strong> to apply the changes.
        </li>
      </ol>
      
      <h3>
        <a name="PlaylistPage"></a>PlaylistPage
      </h3>
      
      <p>
        The configuration page dedicated to generating a player ID is accessed from the <strong>Configuration Management</strong> page <strong>Global</strong> sub-category <strong>PlaylistPage </strong>You can generate a player ID or refer to the playlist player ID in this module if you need to use the player ID number.
      </p>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <tbody>
          <tr>
            <td valign="top" width="376">
              <p>
                <strong>Field</strong>
              </p>
            </td>
            
            <td valign="top" width="376">
              <p>
                <strong>Description</strong>
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="376">
              <p>
                playerId
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="376">
              <p>
                Enter the Playlist playerId. The playerId field is initially empty and the following message is displayed: "Create a Playlist player ID (uiConf ID) for playlists dedicated view page".
              </p>
              
              <p>
                Click Create to generate the player ID.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Embedplaylist"></a>Embedplaylist
      </h3>
      
      <p>
        The configuration page dedicated to activating and configuring the Embed Feature is accessed from the <strong>Configuration Management</strong> page <strong>Modules</strong> sub-category <strong>Embedplaylist</strong>.
      </p>
      
      <p>
        Clicking <strong>Embedplaylist</strong> opens the Embed configuration page:
      </p>
      
      <p>
        From this page you can:
      </p>
      
      <ul>
        <li>
          Enable the Embed Feature
        </li>
        <li>
          Define who (what Role) will be able to use the Embed feature by choosing one of the options in the PlaylistEmbedAllowed.
        </li>
        <li>
          Direct users to the SSO Login page by setting the value of autoRedirect to Yes.
        </li>
        <li>
          Define if the redirect for authentication will be in the top of the browser window (for global authentication) or in an iFrame.
        </li>
        <li>
          Create your own redirect message in autoRedirectMessageHTML.
        </li>
        <li>
          Define the HTML text (may include links) to display inside the iFrame in case a user is only allowed to a subset of the playlist content due to entitlements with authorizedForSubsetHTML.
        </li>
        <li>
          Define the HTML text (may include links) to display inside the iFrame if autoRedirect is set to False with notAuthenticatedHTML.
        </li>
        <li>
          Define the HTML text (may include links) to display inside the iFrame in case Kaltura Entitlement authorization fails with notAuthorizedHTML.
        </li>
        <li>
          Specify the URL to an alternate CSS, to allow a customer to customize the iFrame design to fit corporate style guide with overrideCSSURL.
        </li>
        <li>
          View skin colors and positions, V2 player types and player sizes.
        </li>
      </ul>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Enable the Embedplaylist module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                playlistEmbedAllowed
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Select one or more roles that can use the Embedplaylist module. Use 'Ctrl' to select multiple roles.
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                embedSkins
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Define skins that can be used for embedded playlists.
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                light_horizontal
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                 
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                dark_horizontal
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                 
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                light_vertical
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                 
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                dark_vertical
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                 
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                embedSizes
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Define sizes that can be used for embedded playlists.
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                horizontal
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                 
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                vertical
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                 
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h2>
        Custom/Core Modules/KAF
      </h2>
      
      <h3>
        Browseandembed
      </h3>
      
      <p>
        The Broseandembed KAF module is used to enable and configure the Browse, Search and Embed tool in The LMS. This tool is available within the Rich-text (if installed) editor wherever it is available for example:
      </p>
      
      <ul>
        <li>
          Assignments
        </li>
        <li>
          Forums
        </li>
        <li>
          Announcements
        </li>
      </ul>
      
      <p>
        See The <a href="http://knowledge.kaltura.com/node/1577" target="_blank">Kaltura Application Framework (KAF) LTI Integration Guide</a> for more information.
      </p>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="373">
              <p>
                <strong>Fields</strong>
              </p>
            </td>
            
            <td valign="top" width="445">
              <p>
                <strong>Description</strong>
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                enable
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p class="TableBodyText">
                Yes*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                returnUrlMethod
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p class="TableBodyText">
                POST*
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                allowEmbedFromMultipleCourses
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p class="TableBodyText">
                When set to Yes, users will be able to embed videos from Media Galleries of all the courses they have access to. Set to No if you want to limit users to the Media Gallery of the current course only.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                filterTypeAttribute
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p class="TableBodyText">
                custom_filter_type* The LTI attribute the get the filter type from.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                disableAddNewAttribute
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p class="TableBodyText">
                custom_disable_add_new*. The LTI attribute the get the disable-add-new from.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                enableNewBSEUI
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p class="TableBodyText">
                Yes
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                BSEPlayerID
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p class="TableBodyText">
                The default browse and embed player
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                minimalBSERole
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p>
                Minimal KMS Role allowing browsing and embedding media
              </p>
              
              <p class="TableBodyText">
                 
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                embedSizes
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p>
                Define sizes that can be used for embedded players. Define the player size in the following format: {width}x{height}
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p>
                enableAssignmentSubmission
              </p>
              
              <p class="TableBodyText">
                 
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p>
                This feature enables an additional pop up screen when selecting media in Browse, Search and Embed to verify if the user is submitting an assignment. If confirmed, the selected entry will be cloned under a different user name to prevent editing and deletion
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                assignmentSubmissionText
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p>
                Determines the text that will appear on the pop up message when submitting an assignment. In case left empty, the default message will appear.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" width="373">
              <p class="TableBodyText">
                <br /> assignmentSubmissionMaxRole
              </p>
            </td>
            
            <td style="text-align: left;" width="445">
              <p>
                This sets the highest role level which will see the pop up upon selecting an entry in Browse, Search and Embed.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="Ltigeneric"></a>Ltigeneric
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Enables the LTI generic module. This setting is preconfigured and should not be changed
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <h3>
        <a name="hosted2"></a>Hosted
      </h3>
      
      <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                Description
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enables the Hosted module. This should not be changed
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enableLike
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable the 'Like' feature for entries.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                allowEditPublished
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Set to <em>No</em> if you want to prevent users from editing entries after they have been published to a course Media Gallery or embedded using the Browse, Search and Embed module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                allowDeletePublished
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Set to <em>No</em> if you want to prevent users from deleting entries after they have been published to a course Media Gallery or embedded using the Browse, Search and Embed module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                AllowUnpublishPublished
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Set to <em>No</em> if you want to prevent users from setting entries to private after they have been published to a course Media Gallery or embedded using the Browse, Search and Embed Module
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enableEntryDelete
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Set to <em>No</em> to completely prevent users from deleting entries
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                enableViews
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p>
                Enable showing number of views per entry.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                showPageTitles
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Enable showing page titles
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                expandButton
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Player expand button. Auto is on only if there are modules providing an entry sidebar.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                manPublish
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                Yes. This should not be disabled unless publish plugin was integrated
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="top" width="31%">
              <p class="TableBodyText">
                authMethod
              </p>
            </td>
            
            <td style="text-align: left;" valign="top" width="68%">
              <p class="TableBodyText">
                LTI. This should not be disabled
              </p>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    
    <h3 class="SuperHeading">
      <a name="quiz"></a>Quiz
    </h3>
    
    <table style="width: 793px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td valign="top" width="31%">
            <p class="TableHeading">
              Field
            </p>
          </td>
          
          <td valign="top" width="68%">
            <p class="TableHeading">
              Description
            </p>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              enabled
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              Enables the Quiz module. 
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="31%">
            <p class="TableBodyText">
               
            </p>
          </td>
          
          <td valign="top" width="68%">
             
          </td>
        </tr>
      </tbody>
    </table>
    
    <p class="SuperHeading">
      <a href="#top">Back to Top</a>
    </p>
    
    <h1>
      <a name="RolesandPermissions"></a>Roles and Permissions
    </h1>
    
    <p class="mce-note-graphic">
      <strong>Related KAF modules: </strong><a href="https://kaltura.sharepoint.com/community-team/Shared%20Documents/Knowledge%20Management/Final%20Documents%20-%20Ready%20for%20Publishing/KAF/LTI/Setup_Guide/KAF_LTI_Setup_Guide.docx#hosted">Hosted</a>
    </p>
    
    <p>
      See <a href="https://kaltura.sharepoint.com/community-team/Shared%20Documents/Knowledge%20Management/Final%20Documents%20-%20Ready%20for%20Publishing/KAF/LTI/Setup_Guide/KAF_LTI_Setup_Guide.docx#_Common_Use_Cases">Common Use Cases of Role Configuration</a> for recommendations for common role configurations in the Kaltura Application Framework Generic LTI Integration.
    </p>
    
    <h2>
      Introduction to Role Mapping
    </h2>
    
    <p>
      The Kaltura Application Framework Generic LTI Integration implements role mapping from LMS roles to Kaltura roles via <a href="http://www.imsglobal.org/lti/blti/bltiv1p0/ltiBLTIimgv1p0.html" target="_blank">LIS roles</a>. Each role that is assigned to a user in the LMS is mapped to one of the roles defined in the <a href="http://www.imsglobal.org/lti/blti/bltiv1p0/ltiBLTIimgv1p0.html#_Toc261271984" target="_blank">LIS standard.</a> When a user is assigned with a role in a LMS course – Instructor or Learner for example –the LMS translates this role to an LIS role which is then sent to KAF. On KAF’s side, a dedicated module provides flexible mapping between LIS roles and Kaltura roles, allowing a granular control over the behaviour of the different Kaltura Video Package components in the LMS.
    </p>
    
    <p>
      This process is described in the following workflow.
    </p>
    
    <ol>
      <li>
        Users are <a href="#Assigncourse">assigned a LMS</a> course-level role after being assigned to a course.
      </li>
      <li>
        <a href="#send">The LMS sends the corresponding LIS role to Kaltura</a>.
      </li>
      <li>
        <a href="#grant">KAF Grants Permissions</a> according to mapping.
      </li>
    </ol>
    
    <h3>
      <a name="Assigncourse"></a>Assign a LMS Course-level Role
    </h3>
    
    <p>
      Users are assigned a LMS role when added to courses.
    </p>
    
    <h3>
      <a name="send"></a>The LMS Sends the Corresponding LIS Role to Kaltura
    </h3>
    
    <p>
      When a user accesses a Course-level Kaltura module, such as <em>Media Gallery</em> or the <em>Browse, Search and Embed</em>, the LMS sends the corresponding LIS role to Kaltura, according to the following mapping:
    </p>
    
    <table style="width: 411px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td width="231">
            <p class="TableHeading">
              LMS Course-level role
            </p>
          </td>
          
          <td width="180">
            <p class="TableHeading">
              LIS role
            </p>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td style="text-align: left;" width="231">
            <p class="TableBodyText">
              Learner
            </p>
          </td>
          
          <td style="text-align: left;" width="180">
            <p class="TableBodyText">
              Learner
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" width="231">
            <p class="TableBodyText">
              Instructor
            </p>
          </td>
          
          <td style="text-align: left;" width="180">
            <p class="TableBodyText">
              Instructor
            </p>
          </td>
        </tr>
      </tbody>
    </table>
    
    <h3>
      <a name="grant"></a>KAF Grants Permissions According to the Mapping
    </h3>
    
    <p>
      On the KAF Admin Console side, each LIS role can be mapped back to Kaltura roles. KAF grants different permissions according to the mapping provided in the Hosted module in the KAF Admin Console:
    </p>
    
    <p>
      As displayed, each LIS role is mapped in Kaltura to two roles – an <strong>Applicative Role</strong> (kmsRole) and a <strong>Contextual Role (kmsContextualRole)</strong>. These roles correspond to different cases/scenarios in the Kaltura Application Framework Generic LTI Integration. Setting these roles changes the permissions a user has in the following scenarios:
    </p>
    
    <ul>
      <li>
        <strong>Applicative role (KMSRole)</strong> - Defines the user roles and permissions in Kaltura widgets that are out of course context (for example: My Media)
      </li>
      <ul>
        <li>
          <strong>anonymousRole</strong> – Not relevant to the Kaltura Application Framework Generic LTI Integration and should not be used.
        </li>
        <li>
          <strong>viewerRole</strong> – The user will not have access to My Media, and will not be able to upload new content to either My Media, Media Gallery or using the Embed Kaltura Media text-editor button.
        </li>
        <li>
          <strong>privateOnlyRole</strong> – The user will have access to My Media and will have the ability to create new content.
        </li>
        <li>
          <strong>adminRole, unmoderatedAdminRole</strong> – Not relevant to the Kaltura Application Framework Generic LTI Integration and should not be used.
        </li>
      </ul>
      
      <li>
        <strong>Contextual role (KMScontextualrole)</strong> - Defines the user roles and permission in Kaltura widgets when in a course (site) context (for example: Media Gallery)
      </li>
      <ul>
        <li>
          <strong>Member</strong>: The user will be able to view content in Media Galleries of courses to which the user is enrolled, but will not be able to contribute (publish) to the galleries.
        </li>
        <li>
          <strong>Contributor</strong>: The user has Member permissions with the ability to publish content to the Media Gallery.
        </li>
        <li>
          <strong>Moderator</strong>: The user has Contributor permissions with the ability to moderate content added to the Media Gallery.
        </li>
        <li>
          <strong>Manager</strong>: The user has Moderator permissions with the ability edit the Media Gallery settings, and view the course gallery analytics.
        </li>
      </ul>
    </ul>
    
    <p>
       From the Kaltura module’s perspective, the permissions are as follows:
    </p>
    
    <ul>
      <li>
        <strong>My Media</strong>
      </li>
      <ul>
        <li>
          <strong>Applicative role: </strong>If viewerRole, the user will not have access to My Media and will not be able to upload new content. If privateOnlyRole the user will be able to have its own My Media repository to where he can upload his own private content.
        </li>
        <li>
          <strong>Contextual role</strong>: does not impact My Media.
        </li>
      </ul>
      
      <li>
        <strong>Media Gallery</strong>
      </li>
      <ul>
        <li>
          <strong>Applicative role</strong>: If the user has a contextual role that allows publishing/adding content to the Media Gallery (see the following table), and the user has an Applicative role of <strong>privateOnlyRole</strong>, the user will be able to upload new content or contribute content from its own private My Media repository.
        </li>
        <li>
          <strong>Contextual role</strong>: Determines the role of the user inside the Media Gallery (note – users can access a course Media Gallery after they have access to the course page in the LMS, regardless of their Kaltura role.
        </li>
      </ul>
    </ul>
    
    <table style="width: 699px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td valign="top" width="265">
            <p class="TableHeading">
              Role
            </p>
          </td>
          
          <td valign="top" width="434">
            <p class="TableHeading">
              Permissions
            </p>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="265">
            <p class="TableBodyText">
              Member
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="434">
            <p class="TableBodyText">
              If the user has <strong>Member</strong> contextual role, the user will be treated as a “viewer only” in the Media Gallery, and will only be able to view content, and will not be able to contribute content to the Gallery (regardless of the user’s Applicative role).
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="265">
            <p class="TableBodyText">
              Contributor
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="434">
            <p class="TableBodyText">
              Users with <strong>Contributor</strong> role can view Media Gallery entries and upload and contribute entries from My Media (if applicative role is privateOnlyRole). Students are usually assigned Member or Contributor contextual roles.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="265">
            <p class="TableBodyText">
              Moderator
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="434">
            <p class="TableBodyText">
              <strong>Moderator</strong> role allows the users to moderate content published to a Media Gallery (and to contribute new content). Teaching Assistants usually have Moderator contextual roles.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="265">
            <p class="TableBodyText">
              Manager
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="434">
            <p>
              A <strong>Manager</strong> role provides full access to the Media Gallery, including the ability to moderate content, edit the Media Gallery’s settings and metadata, and access the Media Gallery Analytics. Instructors usually have Manager contextual roles
            </p>
          </td>
        </tr>
      </tbody>
    </table>
    
    <ul>
      <li>
        <strong>Browse, Search and Embed </strong>(rich-text editor button)
      </li>
      <ul>
        <li>
          <strong>Applicative role</strong>: If <strong>viewerRole</strong>, the user will not have access to My Media and will not be able to create new content. If <strong>privateOnlyRole</strong> the user will be able to have their own My Media repository to where they can upload their private content.
        </li>
        <li>
          <strong>Contextual role</strong>: does not impact Embed Kaltura Video.
        </li>
      </ul>
    </ul>
    
    <h4>
      Summary of Default LMS -> LIS -> Kaltura Roles Mapping
    </h4>
    
    <table style="width: 690px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td width="179">
            <p class="TableHeading">
              LMS
            </p>
          </td>
          
          <td width="186">
            <p class="TableHeading">
              LIS role
            </p>
          </td>
          
          <td width="137">
            <p class="TableHeading">
              Default Kaltura applicative role (kmsRole)
            </p>
          </td>
          
          <td width="188">
            <p class="TableHeading">
              Default Kaltura contextual role (kmsContextualRole)
            </p>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td style="text-align: left;" width="179">
            <p class="TableBodyText">
              Learner
            </p>
          </td>
          
          <td style="text-align: left;" width="186">
            <p class="TableBodyText">
              Learner
            </p>
          </td>
          
          <td style="text-align: left;" width="137">
            <p class="TableBodyText">
              privateOnlyRole
            </p>
          </td>
          
          <td style="text-align: left;" width="188">
            <p class="TableBodyText">
              CONTRIBUTOR
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" width="179">
            <p class="TableBodyText">
              Instructor
            </p>
          </td>
          
          <td style="text-align: left;" width="186">
            <p class="TableBodyText">
              Instructor
            </p>
          </td>
          
          <td style="text-align: left;" width="137">
            <p class="TableBodyText">
              privateOnlyRole
            </p>
          </td>
          
          <td style="text-align: left;" width="188">
            <p class="TableBodyText">
              MANAGER
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" width="179">
            <p class="TableBodyText">
              Administrator
            </p>
          </td>
          
          <td style="text-align: left;" width="186">
            <p class="TableBodyText">
              Administrator
            </p>
          </td>
          
          <td style="text-align: left;" width="137">
            <p class="TableBodyText">
              privateOnlyRole
            </p>
          </td>
          
          <td style="text-align: left;" width="188">
            <p class="TableBodyText">
              MANAGER
            </p>
          </td>
        </tr>
      </tbody>
    </table>
    
    <h2>
      <a name="common"></a>Common Use Cases of Role Configuration
    </h2>
    
    <p>
      This section provides recommendations for common role configuration in the Kaltura Application Framework Generic LTI Integration.
    </p>
    
    <p>
      The following use cases are described:
    </p>
    
    <ul>
      <li>
        <a href="#allow_students">Allowing Students to Upload Content</a>
      </li>
      <li>
        <a href="#allow_faculty">Allowing Faculty Only to Upload and Create New Content</a>
      </li>
    </ul>
    
    <h3>
      <a name="allow_students"></a>Allowing Students to Upload Content
    </h3>
    
    <p>
      <strong>Description</strong>: Allow all users to author new content (upload, webcam recording, screencast recording, etc.) and publish to courses, Media Galleries, regardless of their contextual role.
    </p>
    
    <h4>
      LMS Side Configuration
    </h4>
    
    <p>
      No special configuration is required on the LMS side for this case.
    </p>
    
    <h4>
      KAF Side Configuration
    </h4>
    
    <p>
      In your KAF instance, configure the following mapping under the Hosted module:
    </p>
    
    <table style="width: 658px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td valign="top" width="193">
            <p class="TableHeading">
              ItiRole
            </p>
          </td>
          
          <td valign="top" width="233">
            <p class="TableHeading">
              kmsRole
            </p>
          </td>
          
          <td valign="top" width="233">
            <p class="TableHeading">
              kmsContextualRole
            </p>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="193">
            <p class="TableBodyText">
              Learner
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="233">
            <p class="TableBodyText">
              privateOnlyRole
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="233">
            <p class="TableBodyText">
              CONTRIBUTOR
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="193">
            <p class="TableBodyText">
              Instructor
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="233">
            <p class="TableBodyText">
              privateOnlyRole
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="233">
            <p class="TableBodyText">
              MANAGER
            </p>
          </td>
        </tr>
      </tbody>
    </table>
    
    <h3>
      <a name="allow_faculty"></a>Allowing Faculty Only to Upload and Create New Content
    </h3>
    
    <p>
      <strong>Description</strong>: Allowonly faculty members to create and upload new media. Students should not have access to My Media and should not be able to contribute to any course Media Gallery.
    </p>
    
    <h4>
      LMS-side Configuration
    </h4>
    
    <p>
      To accomplish this configuration, the My Media link should be hidden to all logged in users but Teachers.
    </p>
    
    <p>
      It is important to hide the My Media link. If students are able to access the My Media link, an “Access Denied” message will be displayed as they are prevented from accessing My Media by the KAF-side configuration (see below).
    </p>
    
    <h4>
      KAF Side Configuration
    </h4>
    
    <p>
      In your KAF instance, configure the following mapping under the Hosted module:
    </p>
    
    <table style="width: 747px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td valign="top" width="220">
            <p class="TableHeading">
              ItiRole
            </p>
          </td>
          
          <td valign="top" width="264">
            <p class="TableHeading">
              kmsRole
            </p>
          </td>
          
          <td valign="top" width="264">
            <p class="TableHeading">
              kmsContextualRole
            </p>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="220">
            <p class="TableBodyText">
              Learner
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="264">
            <p class="TableBodyText">
              viewRole
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="264">
            <p class="TableBodyText">
              MEMBER
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="220">
            <p class="TableBodyText">
              Instructor
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="264">
            <p class="TableBodyText">
              privateOnlyRole
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="264">
            <p class="TableBodyText">
              MANAGER
            </p>
          </td>
        </tr>
      </tbody>
    </table>
    
    <p>
      <a href="#top"> Back to Top</a>
    </p>
  </div>