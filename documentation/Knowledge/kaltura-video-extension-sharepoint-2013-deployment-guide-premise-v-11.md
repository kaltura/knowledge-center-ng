---
layout: page
title: "Kaltura Video Extension for SharePoint 2013 Deployment Guide for On-Premise v 1.1"
date: 2016-07-24 01:55:40
---

<h2>
    <span>Introduction to the Kaltura Video Extension for SharePoint 2013 for On-Premise</span>
  </h2>
  
  <p>
    The Kaltura Video Extension for SharePoint 2013 allows employees to easily upload and create video content directly from within SharePoint without worrying about file size limitations or various video formats. Employees can then easily embed their contributed videos inside SharePoint pages and workflows, create playlists, make their video searchable and social, and reuse their videos beyond SharePoint in other enterprise applications (CMS, LMS, corporate video portals, etc.). In addition to on-demand video, Kaltura allows you to engage employees by streaming live events directly within SharePoint.
  </p>
  
  <p>
    All of the elements within the Kaltura Extension for SharePoint 2013 are standard SharePoint elements that can be deployed, monitored, isolated and uninstalled by SharePoint. For example, it is possible to deploy the elements into a dedicated web application that will isolate all the solution artefacts from other SharePoint solutions. It is also possible to apply the features only to a specific site collection.
  </p>
  
  <p>
    The following lists the SharePoint elements that the Kaltura Video Extension for SharePoint 2013 includes:
  </p>
  
  <ul>
    <li>
      DLLs - Three DLLs are deployed to the (Global Assembly Cache) GAC, all of which start with the word "Kaltura" and can be easily identified.
    </li>
    <li>
      Farm Feature - A single farm feature that adds a Secure Store Application and a Business Data Connectivity Model.
    </li>
    <li>
      Site collection feature - A site collection level feature that deploys web parts.
    </li>
    <li>
      Design elements- standard SharePoint design manager package and search configuration file which are manually uploaded per site collection.
    </li>
  </ul>
  
  <h3>
    <span style="font-size: 1.5em;">Pre-requisites and Workflow</span>
  </h3>
  
  <p>
    The following components must be configured on your site:
  </p>
  
  <ul>
    <li>
      A Kaltura Application Framework instance. Before Starting the Deployment Process, please contact your Kaltura representative to create a Kaltura Application Framework instance for you.
    </li>
  </ul>
  
  <p>
    You should receive the following:
  </p>
  
  <ul>
    <li>
      The launch point base URL that will be used further in the process.
    </li>
    <li>
      The Administration application login page URL
    </li>
    <li>
      Server Requirements
    </li>
    <li>
      SharePoint 2013 Server (Standard or Enterprise)
    </li>
    <li>
      SharePoint Secure Store Service configured
    </li>
    <li>
      For search purposes only: SharePoint Search Service and SharePoint Business Connectivity Services
    </li>
  </ul>
  
  <h2>
    Tasks to Deploy the Kaltura Video Extension for SharePoint 2013 for On-Premise
  </h2>
  
  <p>
    This section describes the workflow and steps that should be performed to deploy the Kaltura Video Extension for SharePoint 2013 for On-Premise.
  </p>
  
  <p class="Note">
    Workflow:<a name="top"></a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step1">Step 1 - Download the Installation Package</a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step2">Step 2 - Install the Solution (WSP)</a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step3">Step 3 - Deploy the Solution (WSP)</a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step4">Step 4 - Activate the Kaltura Farm Feature</a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step5">Step 5 - (Optional) - Configure the Application Settings in SharePoint’s Secure Store Service</a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step6">Step 6 - Configure the Search Crawler (Connector)</a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step7">Step 7 – Activate the UI Features in One or More Site Collections</a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step8">Step 8 - Optional: Configure the Media Search</a>
  </p>
  
  <p class="TableBodyText">
    <a href="#step9">Step 9 - Assign Permissions to Users</a>
  </p>
  
  <p>
    For additional information, see <a href="http://knowledge.kaltura.com/node/1470">How to gather diagnostic information from a SharePoint 2013 On-Prem site </a>.
  </p>
  
  <h2>
    <a name="step1"></a>Step 1 - Download the Installation Package
  </h2>
  
  <p>
    <strong>Targeted for</strong> - SharePoint administrators
  </p>
  
  <p>
    Description: Download the SharePoint installation package from the KAF admin site. If you already have an installation package (WSP or ZIP file), this step should be skipped.
  </p>
  
  <p class="Procedure mce-procedure">
    To download the installation package
  </p>
  
  <ol>
    <li>
      Browse to KAF admin panel https://[your-kaf-domain]/admin/config/tab/sharepoint.
    </li>
    <li>
      Replace “[your-kaf-domain]” with the URL of your KAF instance.  <br /><img src="{{site.url}}/assets/3329">
    </li>
    <li>
      Click on “Download SharePoint Installation Package”, to initiate the download and save the file to a directory within your SharePoint server.
    </li>
    <li>
      Click on ‘Download Search Installation files” to initiate the download and save the file to a directory within your SharePoint server.<br /><img src="{{site.url}}/assets/3330">
    </li>
  </ol>
  
  <p>
    <a href="#top">Back</a>
  </p>
  
  <h2>
    <a name="step2"></a>Step 2 - Install the Solution (WSP)
  </h2>
  
  <p>
    <strong>Targeted for:</strong> SharePoint administrators
  </p>
  
  <p>
    Description: Add the solution (WSP) to SharePoint solution store using PowerShell. This is a common SharePoint action that uploads the solution to SharePoint to make it available for deployment.
  </p>
  
  <p class="Procedure mce-procedure">
    To install the WSP
  </p>
  
  <ol>
    <li>
      Verify that the user you are now logged-in with, that is being used to install the solution, is using the SharePoint farm account, or is a member of the farm administrator’s group.
    </li>
    <li>
      Open PowerShell Management Shell. Click Start (Windows Icon) -> Type “SharePoint 2013 Management Shell”.
    </li>
    <li>
      Right click on the item “SharePoint 2013 Management Shell” and choose “Run as administrator”. As a result, the PowerShell window opens as displayed.<br /><span><strong>NOTE:</strong> Running the PowerShell shell as administrator is required only if you have “User Access Control” (UAC) activated within Windows. If UAC is disabled then you may open the PowerShell shell by clicking on the “SharePoint 2013 Management Shell” item.<br /><img src="{{site.url}}/assets/3331">
    </li>
    <li>
      Within the PowerShell console, type the following command: <br />Add-SPSolution '{Path To the WSP file}\KalturaSolution.wsp'
    </li>
    <li>
      Replace {Path To the WSP file} with the location where you saved the WSP file. The following screen displays an example of Adding the solution via PowerShell window.<br /><img src="{{site.url}}/assets/3332">
    </li>
  </ol>
  
  <p class="FigureList">
     <a href="#top">Back</a>
  </p>
  
  <h2>
    <a name="step3"></a>Step 3 - Deploy the Solution (WSP)
  </h2>
  
  <p>
    <strong>Targeted for:</strong> SharePoint administrators
  </p>
  
  <p>
    <strong>Description:</strong> Deploy the solution (WSP) within SharePoint so that it becomes available for site owners. This is a common SharePoint action that deploys the solution to one or all SharePoint web applications.
  </p>
  
  <p class="Procedure mce-procedure">
    To deploy the Solution (WSP)
  </p>
  
  <ol>
    <li>
      Browse to SharePoint Solution Store.
    </li>
    <li>
      Navigate to “SharePoint Central Administration” -> select “System Settings” (on the left pane) and then select “Manage farm solutions”. You should now see the solution that was added in <a href="#step2">Step 2</a>: “Kaltura SharePoint Solution.wsp”<br /><img src="{{site.url}}/assets/3333">
    </li>
    <li>
      Deploy the solution. Click on the solution, The “Deploy Solution” screen is displayed.
    </li>
    <li>
      Select “All content web applications” from the “Deploy to?” dropdown menu or pick a specific web application you want to deploy the solution to.
    </li>
    <li>
      Click “OK”. The solution is now deployed.<br /><img src="{{site.url}}/assets/3334">
    </li>
  </ol>
  
  <p class="FigureList">
     <a href="#top">Back</a>
  </p>
  
  <h2>
    <a name="step4"></a>Step 4 - Activate the Kaltura Farm Feature
  </h2>
  
  <p>
    <strong>Targeted for:</strong> SharePoint administrators
  </p>
  
  <p>
    <strong><br /> Description: </strong>Activate the farm feature “Kaltura Backbone” in the Farm Features screen. This feature sets the application backbone: that include the search connector and configuration items that are needed for various components in the solution.
  </p>
  
  <p class="Procedure mce-procedure">
    To activate the Kaltura Farm Feature
  </p>
  
  <ol>
    <li>
      Browse to SharePoint’s Farm Features window. Navigate to “SharePoint Central Administration”, select “System Settings”, then select “Manage Farm Features”.
    </li>
    <li>
      Activate the Kaltura Backbone feature. Locate the feature called “Kaltura Backbone” and click “Active”.<br /><img src="{{site.url}}/assets/3335">
    </li>
  </ol>
  
  <h2>
    <a name="step5"></a>Step 5 - (Optional) - Configure the Application Settings in SharePoint’s Secure Store Service
  </h2>
  
  <p>
    <strong>Targeted for:</strong> SharePoint administrators
  </p>
  
  <p>
    <strong>Optional:</strong> This step should be performed only if the installation package was not downloaded from the KAF admin. If you download the solution file from the KAF admin, this step is automatically implemented by the package.
  </p>
  
  <p>
    <strong>Description: </strong>Configure the credentials and other settings that create the connection between SharePoint and KAF. These settings are kept securely in the SharePoint Secure Store Service.
  </p>
  
  <p class="Procedure mce-procedure">
    To configure the app settings in SharePoint’s Secure Store Service
  </p>
  
  <ol>
    <li>
      Browse to SharePoint Secure Store Service.
    </li>
    <li>
      Navigate to “SharePoint Central Administration” and select “Manage Service Applications” and then select “Secure Store Service” (or the name the Secure Store Service was assigned during installation).
    </li>
    <li>
      Set the application credentials. You should see the Secure Store application named “KalturaStore”. Click on KalturaStore and choose “Set Credentials” from the drop down menu.<br /><span>NOTE: Even if the credentials (Secure Store configuration info) were previously filled, they appear as empty because SharePoint hides this information due to security reasons. Consequently, when the need arises to edit a single field – you are required to fill-in all of the fields.<br /><img src="{{site.url}}/assets/3336">
    </li>
    <li>
      Fill in the following Kaltura app credentials and settings within the Secure Store: <br /><img src="{{site.url}}/assets/3346">
    </li>
  </ol>
  
  <ul>
    <li>
      Admin Secret – The admin secret of your Kaltura account. The secret can be obtained from your KMC, under Settings > Integration Settings.
    </li>
    <li>
      Server URL – If a value is not specified it will default to https://www.kaltura.com
    </li>
    <li>
      Partner ID – Your Kaltura Partner ID. The partner ID can be obtained from your KMC, under Settings > Integration Settings.
    </li>
    <li>
      Root category – The name of the media category within KAF. By default the root category is “sharepoint”.
    </li>
    <li>
      KAF URL – The Kaltura Application Framework launch point. You can obtain this value from your Kaltura representative. If a value is not specified it will default to https://{kaltura.partner.id}.kaf.kaltura.com.
    </li>
    <li>
      metadata Profile Id – The ID of an automatically created profile by the KAF instance. This information is found in the KMC under settings/custom data/system name = CategoryAdditionalInfo.
    </li>
    <li>
      KS UserId field sets the value of SPUser object that the Kaltura solution will use.<br />Enter either<strong> loginname or email </strong>(input one of these words in the field). If you want users logging-in to your SharePoint solution to have the same “My Media” when they log-in to another Kaltura Application (MediaSpace for example), the user name login method should be the same in both solutions.<br />For example:<br />loginname –JohnDoe<br />email – Email address : JohnDoe@company.com<br />or for users using KMS, you could choose "email" in SP, and email in the value from ADFS SAML response.
    </li>
    <li>
      Use user Domain – Use to determine whether the domain will be removed from  the  userLoginName or not (Foe example: either domain\johndoe or just johndoe). Valid parameters in this field are yes, no, true, or false.
    </li>
  </ul>
  
  <p class="FigureList">
     <a href="#top">Back</a>
  </p>
  
  <h2>
    <a name="step6"></a>Step 6 - Configure the Search Crawler (Connector)
  </h2>
  
  <p>
    <strong>Targeted for:</strong> SharePoint administrators, Search administrators
  </p>
  
  <p>
    <strong>Description: </strong>Within the SharePoint search service, define a new result source and new result type to enable Kaltura media to result within the SharePoint search results.
  </p>
  
  <p class="Procedure mce-procedure">
    To configure the search crawler
  </p>
  
  <ol>
    <li>
      Authorize the search service to approach Kaltura media items: Navigate to Business Connectivity Services (BCS) - Browse to “SharePoint Central Administration” and select “Manage Service Applications” then select “Business Data Connectivity” (or any other name the business connectivity services was assigned during installation).
    </li>
    <li>
      Ensure that the item “KalturaEntity” exists on the list.
    </li>
    <li>
      Assign the search service permissions to query using this Business Data Connectivity item.
    </li>
    <ol style="list-style-type: lower-alpha;">
      <li>
        Select the item “KalturaEntity”, on the top ribbon and click “Set Object Permissions”.
      </li>
      <li>
        Add the Farm Account which is used for crawling external data (The Farm Account was chosen during the farm installation. If you are not sure how to identify the Farm Account, please refer to the Microsoft article <a href="https://technet.microsoft.com/en-us/library/cc263445.aspx" target="_blank">Plan for administrative and service accounts in SharePoint 2013</a> ), then check the following Permissions’ check-boxes: “Edit”, “Execute”, and “Set Permissions”.<br /><img src="{{site.url}}/assets/3338">
      </li>
    </ol>
    
    <li>
      Install the search schema (also known as ‘Managed Properties’).<br /><ol style="list-style-type: lower-alpha;">
        <li>
          Locate the file “Kaltura SharePoint Solution”.
        </li>
        <li>
          Search Schema Installer.ps1” which you downloaded in <a href="file:///Z:/Final%20Documents%20-%20Ready%20for%20Publishing/Kaltura%20Video%20Extension%20for%20SharePoint/SharePoint_2013/Deployment_Guide/OnPrem/Kaltura_Video_Extension_for_SharePoint_2013_Deployment_Guide_for_On_Premise_v1_1.docx#_Step_1:_Download">step 1</a>.
        </li>
        <li>
          Right click on the file and choose “Run with PowerShell”. A console window is displayed.
        </li>
        <li>
          Create the search schema and display the success message. If an error message appears on the screen, dismiss it, it should not affect the process.
        </li>
      </ol>
    </li>
    
    <li>
      Add a new content source. Navigate to Search Service Application- Browse to “SharePoint Central Administration” and select “Manage Service Applications” and then select “Search Service Application” (or any other name the search service was assigned during installation).
    </li>
    <li>
      Fill in the following information in the Add Content Source window as displayed in the following screens.<br /><img src="{{site.url}}/assets/3340">
    </li>
    <li>
      Verify that the new content source can crawl Kaltura media successfully.
    </li>
  </ol>
  
  <ol>
    <ol style="list-style-type: lower-alpha;">
      <li>
        Click on the content source that was added in <a href="file:///Z:/Final%20Documents%20-%20Ready%20for%20Publishing/Kaltura%20Video%20Extension%20for%20SharePoint/SharePoint_2013/Deployment_Guide/OnPrem/Kaltura_Video_Extension_for_SharePoint_2013_Deployment_Guide_for_On_Premise_v1_1.docx#add_content_source">step 6</a>.
      </li>
      <li>
        Select “Start full crawl”. Wait for the crawling to complete and then click on the content source again.
      </li>
      <li>
        Select “View crawl log” and then ensure that no error appears on the last crawl report.<br /><img src="{{site.url}}/assets/3341">
      </li>
    </ol>
  </ol>
  
  <p class="FigureList">
    <a href="#top">Back</a> 
  </p>
  
  <h2>
    <a name="step7"></a>Step 7 - Activate the UI Feature in One or More Site Collections
  </h2>
  
  <p>
    <strong>Targeted for:</strong> SharePoint administrators, Site owners, Site designers
  </p>
  
  <p>
    <strong>Description:</strong> Activate Kaltura features within site collections where you plan to use Kaltura widgets or perform a Kaltura search. This is a common SharePoint action which is regularly done in SharePoint sites to add new functionality.
  </p>
  
  <p class="Procedure mce-procedure">
    To activate UI features in site collections
  </p>
  
  <ol>
    <li>
      Navigate to a site collection settings screen<strong>. </strong>Browse to a site collection where you want to apply Kaltura functionality. Enter the Site collection settings screen, then choose “Site Collection Features”.<br /><img src="{{site.url}}/assets/3342">
    </li>
    <li>
      Activate the widgets feature. To use Kaltura Widgets web parts (Media Gallery, My Media and Browse Search and Embed) in the site collection, activate the feature “Kaltura Widgets” by selecting the feature and clicking “Active”.<img src="{{site.url}}/assets/3343">
    </li>
  </ol>
  
  <p class="FigureList">
    <a href="#top">Back</a>
  </p>
  
  <h2>
    <a name="step8"></a>Step 8 – (Optional) - Configure the Media Search
  </h2>
  
  <p>
    <strong>Targeted for</strong> – Site collection administrators
  </p>
  
  <p>
    <strong>Applicable for</strong> - SharePoint On-Premise only. Not applicable for the SharePoint for MS Office 365 environment.
  </p>
  
  <p>
    <strong>Description </strong>– Use to customize the media items look and feel within the search result, after applying the search customization media items will have unique logo and hover panel for preview.
  </p>
  
  <p class="mce-procedure">
    To configure the media search within SharePoint
  </p>
  
  <ol>
    <li>
      Login to the site collection where you want to customize the search result as a site collection administrator.<br /><span>NOTE: SharePoint will fail to import the search configuration if you are logged-in with the farm admin or application pool user account. Please ensure that the user who is logged-in is a site collection administrator and does not have higher privileges.</span>
    </li>
    <li>
      Enter the site settings screen by clicking on the gear icon (appears on the top corner of the site) and then choose “Site Settings.
    </li>
    <li>
      Activate the related SharePoint features.<ol style="list-style-type: lower-alpha;">
        <li>
          Within the site settings page, navigate to “Site Collection Features” and activate the feature “SharePoint Server Publishing Infrastructure”.
        </li>
        <li>
          Within the site settings page, navigate to “Manage Site Features” and activate the following features: “Search Config Data Content Types” and “Search Config List Instance Feature”.
        </li>
      </ol>
    </li>
    
    <li>
      Upload the search UI design files to SharePoint “Design Manager”: Within the site settings page, navigate to “Design Manager”.
    </li>
    <li>
      Within the Design Manager home screen, choose “Import a complete design package”.<br /><img src="{{site.url}}/assets/3327">
    </li>
    <ol style="list-style-type: lower-alpha;">
      <li>
        Browse and locate the file “Kaltura SharePoint Solution - Design Artifacts.wsp” that you downloaded with all the other installation files.
      </li>
      <li>
        Confirm to upload the file.
      </li>
      <li>
        Verify that a successful confirmation message appears on the screen: “Import of package "Kaltura SharePoint Solution - Design Artifacts.wsp" succeeded.”
      </li>
    </ol>
    
    <li>
      Import the search configuration file.<ol style="list-style-type: lower-alpha;">
        <li>
          Navigate to “Import Configuration”. The link appears under the menu “Site Collection Settings”.
        </li>
        <li>
          Upload the file “Kaltura SharePoint Solution - Search UI Configuration.xml” using the file Upload button that appears in the screen and then confirm by clicking “Import”.<br /><img src="{{site.url}}/assets/3328">
        </li>
      </ol>
    </li>
    
    <li>
      Verify that the new configuration file was imported successfully. You should see a list of the configuration import files. The column “Status’ should display the value “Imported successfully”.
    </li>
    <li>
      To test the new search configuration, perform a search in the same site collection to which you uploaded the configuration file. Type a phrase that matches some media items that were uploaded to the Media Gallery. You may also put your mouse cursor over some media item, and hover panel with media thumbnail should popup.<br /><span>NOTE: The user who performs a search must have read permissions in the site collection root site. This requirement holds true for every SharePoint solution that makes use of master pages and design files.</span>
    </li>
  </ol>
  
  <h2>
    Examples of Search Experience and Applications
  </h2>
  
  <p>
    By now you have configured the SharePoint search server to index Kaltura media items. This section describes how to expose the search content to the user. The SharePoint search is a rich platform that includes many components and potential applications. You may design your own search solutions using SharePoint tools. The following examples do not teach you how to craft search applications but provides a few popular examples of how you may expose media items using the SharePoint search UI with links to Microsoft’s documentation.
  </p>
  
  <h3>
    Embed Kaltura Content within any Site Search
  </h3>
  
  <p>
    Every SharePoint site template comes with a search box that allows you to search within the local site content. By default, only content of the current site is displayed. Consequently, Kaltura media items will not appear in the search result. However, using the SharePoint search configuration, you may display Kaltura content along the local site content. This can be technically achieved by creating a new search result page (or search result center), configuring it to display items from the local SharePoint content and Kaltura media items and then changing the site settings to refer all searches to the new page. For more information, please refer to the Microsoft article <a href="https://support.office.com/en-ie/article/Specify-search-settings-for-a-site-collection-or-a-site-99da1d77-f42b-4f56-b48a-24e87f336e91?ui=en-US&rs=en-IE&ad=IE" target="_blank">Specify search settings for a site collection or a site</a>. 
  </p>
  
  <h3>
    Leverage Kaltura Content in an Enterprise Search Center
  </h3>
  
  <p>
    Search centers are SharePoint sites that are designed for rich search experience. They are pre-configured to perform organization-wide searches and contain various search UI elements to boost the search experience like verticals (tabs), refiners (filters) and others. If you already have a search center, Kaltura media items will be displayed within the search results. You may improve the user experience by providing a “Kaltura Vertical”. This is a tab within the search result that will narrow the search content to display Kaltura media items only. Using this tool you can focus on media items only in your search. For more information see Microsoft’s documentation on <a href="http://blogs.technet.com/b/tothesharepoint/archive/2013/11/13/how-to-add-a-customized-search-vertical-to-your-search-results-page-in-sharepoint-2013.aspx" target="_blank">How to add a custom search vertical to your search results page in SharePoint 2013</a>.
  </p>
  
  <h3>
    Creating a Custom Search Driven Application
  </h3>
  
  <p style="padding-left: 30px;">
    Microsoft has coined the term <a href="http://blogs.technet.com/b/searchguys/archive/2014/04/08/building-a-search-driven-sharepoint-app-i-setting-a-foundation.aspx" target="_blank">‘Search Driven Application’</a> to describe the richness and flexibility of the search platform. Using the various search tools, you my craft a custom search solution, for example:
  </p>
  
  <ul>
    <li>
      <strong>Show all the organizational media on a topic. </strong>
    </li>
  </ul>
  
  <p style="padding-left: 30px;">
    Based on some user interaction (for example, selecting a topic from a list), display all the related organization media, Kaltura items and local media mixed together, using the <a href="https://support.office.com/en-in/article/Configure-a-Content-Search-Web-Part-in-SharePoint-0dc16de1-dbe4-462b-babb-bf8338c36c9a" target="_blank">search result web part</a>. You may apply similar formatting to all the media items regardless of their type, group important items and more.
  </p>
  
  <ul>
    <li>
      <strong>Show recommended content within your team sites.</strong>
    </li>
  </ul>
  
  <p style="padding-left: 30px;">
    You may add a widget within your team site that displays new, updated and recommended content for the team so they can explore and reveal content of interest regarding a specific topic or in general. To achieve this functionality, you may use the built-in web parts: <a href="http://blogs.technet.com/b/tothesharepoint/archive/2014/01/22/add-and-configure-the-recommended-items-and-popular-items-web-part-in-sharepoint-server-2013.aspx" target="_blank">Recommended Items and Popular Items Web Part</a>.
  </p>
  
  <ul>
    <li>
      <strong>Display related media within your catalog product page.</strong>
    </li>
  </ul>
  
  <p style="padding-left: 30px;">
    SharePoint 2013 contains special treatment for catalog items (cross-organizational entities like products). The product page usually displays various information about the product, using the <a href="http://blogs.technet.com/b/tothesharepoint/archive/2013/05/23/stage-10-configure-the-query-in-a-content-search-web-part-on-a-catalog-item-page.aspx">search result web part in a product page</a>. It is possible to display all the content which is related to this product, local content and Kaltura media mixed together in a list.
  </p>
  
  <p>
    <a href="#top">Back</a>
  </p>
  
  <h2>
    <a name="step9"></a>Step 9 - Assign Permissions to Users
  </h2>
  
  <p>
    <strong>Targeted for:</strong> SharePoint administrators, Site owner, Site designers
  </p>
  
  <p>
    <strong>Description:</strong> Kaltura widgets inherit their permission from SharePoint and display the content according to the user’s permission. This step enables you to use SharePoint built-in security groups and permissions to set what the user is allowed to see and do.
  </p>
  
  <p>
    Similar to any other content solution in SharePoint, users must be added to site groups that have some associated permission level. If your site users are already added to the built-in SharePoint groups – no other actions are required. Kaltura widgets take into account the SharePoint user permissions and authorize users accordingly.
  </p>
  
  <p>
    By default, without changing the SharePoint out-of-the-box permission’s settings and Kaltura Application Framework settings, the following security principles are applied:
  </p>
  
  <ul>
    <li>
      Users that are part of the “<em>Site Name</em> Members” group are assigned the Kaltura “Contributor” contextual role.
    </li>
    <li>
      Users that are part of the “<em>Site Name</em> Visitors” group are assigned the Kaltura “Member” contextual role.
    </li>
    <li>
      Users that are part of the “<em>Site Name</em> Owners” group are assigned the Kaltura “Manager” contextual role.
    </li>
  </ul>
  
  <p class="Procedure mce-procedure">
    To assign permissions to users
  </p>
  
  <ol>
    <li>
      Add users to groups in SharePoint.
    </li>
    <li>
      Change the default SharePoint-KAF permission mapping.
    </li>
  </ol>
  
  <p style="padding-left: 30px;">
    Typically, you do not need to change the default permission settings to satisfy your security requirements. However, for some complex scenarios, you may want to granularly set, for example, which permission (for example, role) in SharePoint is mapped to which KAF (Kaltura Application Framework) role. Should you want to achieve that level of control, it is possible to do so via the KAF admin console, under the ‘SharePoint’ tab. We recommend that you contact your Kaltura representative to get further technical assistance.
  </p>
  
  <h3>
    Default Mapping from SharePoint Groups to Kaltura Roles
  </h3>
  
  <p>
    The following table lists the default mapping from SharePoint groups and their permission levels to the Kaltura Application and Contextual roles.
  </p>
  
  <table border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="120">
          <p class="TableHeading">
            SharePoint Group
          </p>
        </td>
        
        <td valign="top" width="120">
          <p class="TableHeading">
            SharePoint Permission Level
          </p>
        </td>
        
        <td valign="top" width="144">
          <p class="TableHeading">
            SharePoint Permission
          </p>
        </td>
        
        <td valign="top" width="210">
          <p class="TableHeading">
            Kaltura Role
          </p>
        </td>
        
        <td valign="top" width="113">
          <p class="TableHeading">
            Kaltura Contextual Role
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td valign="top" width="120">
          <p class="TableBodyText">
            Members
          </p>
        </td>
        
        <td valign="top" width="120">
          <p class="TableBodyText">
            Edit
          </p>
        </td>
        
        <td valign="top" width="144">
          <p class="TableBodyText">
            ViewListItems
          </p>
        </td>
        
        <td valign="top" width="210">
          <p class="TableBodyText">
            viewerRole
          </p>
        </td>
        
        <td valign="top" width="113">
          <p class="TableBodyText">
            Contributor
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="120">
          <p class="TableBodyText">
            Visitors
          </p>
        </td>
        
        <td valign="top" width="120">
          <p class="TableBodyText">
            Read
          </p>
        </td>
        
        <td valign="top" width="144">
          <p class="TableBodyText">
            AddListItems
          </p>
        </td>
        
        <td valign="top" width="210">
          <p class="TableBodyText">
            privateOnlyRole
          </p>
        </td>
        
        <td valign="top" width="113">
          <p class="TableBodyText">
            Member
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="120">
          <p class="TableBodyText">
            Owners
          </p>
        </td>
        
        <td valign="top" width="120">
          <p class="TableBodyText">
            Full Control
          </p>
        </td>
        
        <td valign="top" width="144">
          <p class="TableBodyText">
            ApproveItems
          </p>
        </td>
        
        <td valign="top" width="210">
          <p class="TableBodyText">
            privateOnlyRole
          </p>
        </td>
        
        <td valign="top" width="113">
          <p class="TableBodyText">
            Manager
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="120">
          <p class="TableBodyText">
            Designers
          </p>
        </td>
        
        <td valign="top" width="120">
          <p class="TableBodyText">
            Design
          </p>
        </td>
        
        <td valign="top" width="144">
          <p class="TableBodyText">
            CancelCheckout
          </p>
        </td>
        
        <td valign="top" width="210">
          <p class="TableBodyText">
            unmoderatedAdminRole
          </p>
        </td>
        
        <td valign="top" width="113">
          <p class="TableBodyText">
            Manager
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    Kaltura differentiates between application roles and contextual roles.
  </p>
  
  <h3>
    Application Roles
  </h3>
  
  <p>
    KAF application roles apply globally and include:
  </p>
  
  <ul>
    <li>
      <strong>anonymousRole</strong> – Can browse your site anonymously until trying to access pages/actions that require login: My Media, My Playlists, and Add New.
    </li>
    <li>
      <strong>viewerRole</strong>
    </li>
    <ul>
      <li>
        Not authorized to upload new content
      </li>
      <li>
        Does not have a My Media page
      </li>
    </ul>
    
    <li>
      <strong>privateOnlyRole</strong>
    </li>
    <ul>
      <li>
        Can upload content to My Media
      </li>
      <li>
        Can add media
      </li>
    </ul>
    
    <li>
      <strong>adminRole</strong>
    </li>
    <ul>
      <li>
        Can publish content
      </li>
      <li>
        Can upload content
      </li>
    </ul>
    
    <li>
      <strong>unmoderatedAdminRole</strong> – Can upload content and bypass moderation (when moderation is enabled for an account)
    </li>
  </ul>
  
  <h3>
    Contextual Roles
  </h3>
  
  <p>
    Contextual roles apply to actions that are in relevant to a media gallery widget.
  </p>
  
  <ul>
    <li>
      <strong>Member</strong>: Can access a media gallery but cannot add a new content
    </li>
    <li>
      <strong>Contributor</strong>: Can add content to a media gallery
    </li>
    <li>
      <strong>Moderator</strong>: In addition to the Contributor permission, can moderate content.
    </li>
    <li>
      <strong>Manager</strong>: In addition to the Contributor permission, can moderate content and access settings, including change metadata, edit members, change appearance, and delete channel.
    </li>
  </ul>
  
  <p>
    For more information see <a href="http://knowledge.kaltura.com/node/987" target="_blank">Kaltura MediaSpace/Kaltura Application Framework (KAF) Roles and Permissions</a>. 
  </p>
  
  <p>
    <a href="#top"><span>Back</span></a>
  </p>