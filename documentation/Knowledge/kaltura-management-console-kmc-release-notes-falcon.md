---
layout: page
title: "Kaltura Management Console (KMC) Release Notes - Falcon"
date: 2012-07-25 14:18:53
---

Version:<span style="background-color: #ffffff; color: #ff0000;"><span style="color: #000000;">Falcon</span> </span>Build: 5.19

These release notes pertain to the Kaltura Managment Console, released July 2012. These release notes are intended for content managers and Kaltura Management Console users and also contain the latest information for developers, integrators, and operations and site administrators using the Kaltura platform. 

#### What's New in this Release?

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Feature</strong>
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText" style="text-align: left;">
          Enanced User Interface 
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          A more effective and robust UI has been developed for content and category management in the KMC. You can manage a list of end users and groups, as well as their permissions per each category (channel), including integration with external user management via SAML and LDAP.
        </p>
        
        <p>
          The new UI includes:
        </p>
        
        <ul>
          <li>
            Better visibility and control for content and category filters.
          </li>
          <li>
            Tag setting for entries and categories that is assisted by an auto suggestion list based on tags that are already available in the system.
          </li>
          <li>
            Category setting for entries is now possible by selecting categories from a tree view within the Edit Entry window.
          </li>
          <li>
            Additional bulk actions are available through the bulk actions menu, including: adding/removing multiple entries to/from multiple categories (replacing the previous drag and drop option that was limited for adding entries to a single category only), immediate creation of a new category to hold the set of selected entries and bulk assignment of multiple entries to a specific owner for supporting different applicative and UGC flows.
          </li>
          <li>
            Unified metadata and custom data settings are available from the Edit Entry metadata tab
          </li>
          <li>
            New categories filter preferences to enable the preferred category filtering option  (displays entries associated directly with the specific category or all entries under a specific category level)
          </li>
          <li>
            Additional categories management page in the Content tab has been added where you can set metadata to categories and manage large volumes of categories using filters and bulk action options.
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText" style="text-align: left;">
          <span>KMC End-User Entitlement Settings</span> 
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText" style="text-align: left;">
          <span><span>Category Entitlement Options may be set to Private, where the respective access level is based on specific end-user permissions.  User permissions to a category and content associated it may be set through 4 permission levels: Member, Contributor, Moderator, and Manager. </span><br /></span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText" style="text-align: left;">
          <span><span>KMC Category Enhancements</span></span>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        Custom data per category makes the category a more robust grouping object. For example,  metadata of a channel or a TV series that applies to all videos, can be saved in the category level. 
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText" style="text-align: left;">
          <span><span>KMC User Level Analytics</span></span>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          User level analytics provide reports per user, for the duration viewed and the content viewed. For example which video was watched in the time frame and for how long; and per content - which users  watched the content and for how long. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText" style="text-align: left;">
          <span><span><span>KMC Usage Reports Improvements</span></span></span>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          New usage reports have been added that provide clearer visibility into the usage and insight about billing, including:
        </p>
        
        <ul>
          <li>
            Easy way to see historical data, broken by month or day, for a standard time range (Current / previous month / week / year) or a custom one (any two dates).
          </li>
          <li>
            Easy way to separate between streaming and storage, as well as aggregate them together.
          </li>
          <li>
            Breakdown calculations of the storage level – average, peak and added during the given timeframe. Easy way to export detailed report to excel format for further investigation.
          </li>
          <li>
            Tracking storage at the user level 
          </li>
          <li>
            Feature Description about how much each end user (Student / Employee / etc.) is storing.
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <span>Player New Flash Player Templates</span>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <span>Additional player templates have been added with a new user interface, layout and look. The player templates are available for selection and customization via the application studio.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <span>Player 508 Player Enhancements</span>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <span>The new 508 player is now more flexible and configurable, including configurations available through the application studio, and smoother workflows for captions upload.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <span><span>Player Related Videos</span></span>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <p>
          <span>The Kaltura related videos module is configured to appear at the end of the video and includes a countdown option that invokes the user to take action in a limited time.  The default related videos algorithm may be one of the following: </span>
        </p>
        
        <p>
          <span>1. Related via the Manual playlist, allowing the administrator to manually define the “related videos” for each video that are applicable</span>
        </p>
        
        <p>
          <span> 2. Related videos automatically discovered by the system. Can be extended per customer requirements as professional services.</span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <span>On Line Help</span>
      </td>
      
      <td style="text-align: left;" valign="top" width="435">
        <span>Embeded on-line help is available in the application’s interface. The on-line help provides topic-oriented, procedural and reference information and is accessed by clicking on the question mark icon in the GUI.</span>
      </td>
    </tr>
  </tbody>
</table>

 

#### Known Issues

<table style="width: 762px;" border="1" cellspacing="0" cellpadding="0">
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
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          5102
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When creating a category using the Bulk Actions drop down menu, (Add Category option), a Flash error message is displayed when assigning the new entry to the category.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          5083
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When exporting a report to CSV using the Playback Context filter, data is exported unfiltered.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          5148
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Server
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When creating a ui conf via the Test Me Console, several fields may not be updated.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4826
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Core
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          If the Event notification is set when performing a bulk upload, a PHP error occurs.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4887
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Playlist
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When filtering Rule-Based Playlists according to Custom Data filters, errors may occur.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4917
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When using a foreign locale tab titles and the bulk actions drop down, are not do not display in the foreign language.-
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4921
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Entry Drill Down
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          Entry scheduling cannot be cancelled once set.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4974
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Core
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When you change a thumbnail through bulk xml upload and set it as the default, the thumbnail is updated but is not set as the default. .
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          3978
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Connectors
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          The DailyMotion connector returns an error when trying to distribute content, when restrictions are not defined in the KMC Access Control profile. This error occurs when using "Access Control" type geo-blocking.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          3901
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Manage
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          Clipped entries may not be presented in the Contents page when filtering by a source flavor.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4088
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Core
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          A clip created from a rotated video may not be rotated.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          2694
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Entry Drill Down
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          While a video is playing in the clipping tool, the End Time runs backwards and the player freezes when clicking "Set In".
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4327
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Manage
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When setting a manual drop folder in the Admin Console<a href="file:///C:/Users/Debbie/Documents/Defect%20IDdzoct10.docx#_msocom_1">[CF1]</a> , and 'Matching from KMC'=TRUE, the “Match From Drop Folder” button is not presented in the entry drill down.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4510
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Core
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When filtering data by the “to Date” option, and setting the last day of month to the Date, the next month is also displayed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4583
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Player
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When previewing a flavor from the Flavors tab, the player is not aligned to the Preview Flavors page. (in Explorer only)
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          2430
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When exporting data to a CSV from the 'Users &Community' Top Syndications reports, erroneous data is added to the CSV.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          2882
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Moderate
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When trying to search for categories in the Categories tree, in the Moderation tab, the suggestion box is not displayed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          2961
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Entry Drill Down
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          The following characters are invalid: € £ ¢ for custom data values, if you are trying to save an entry which also contains special characters in the name or description.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          2984
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Content
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          Filtering does not persist after refreshing the page from the browser.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          3390
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          In the Publisher Bandwidth & Usage report, data is displayed in a different time unit than the selected time unit.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          3449
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          KCW
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          A Flash error occurs when importing photos from the web, when selecting the "Search your photo" from Flicker option.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          2561
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Entry Drill Down
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          For auto-completion; when the suggestions list is short (up to 3 items), the first suggestion is displayed twice and the arrow key is disabled.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          2818
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          KMC
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          In the Entry drill down, the Tags suggestion box displays incorrectly when the tags are more than a row’s length.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          2410
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Entry Drill Down
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When uploading content to a draft entry, the Metadata tab is not refreshed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4245
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          In the Publisher & Bandwidth Storage report, when setting the Date Range to "This week", details for Saturday of the previous week are also included and calculated.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4314
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          The columns in the totals and the detailed tables are not aligned.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          4520
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Front
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When the value of a custom data field is a long expression, the value may not display correctly.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          3709
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          In some reports, the columns in the detailed table are not sortable.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          3673
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Core
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          When bulk uploading users or categories with custom data, the custom data field values are not presented in the log file.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          3979
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Connectors
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          After distributing content using an "Access Control Profile, changing the Access Control settings (changing the limitations in the used profile or changing the user access control profile for the entry) does not trigger a manual or automatic updat
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="118">
        <p class="TableBodyText">
          4965
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Analytics
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          In some cases, erroneous dates are sent in the Analytics reports:
        </p>
        
        <ul>
          <li>
            When selecting a Date Range "This week" while current day is Sunday, to Date is sent as the previous Saturday. Therefore, the “to Date” value is prior to the “from Date” value.
          </li>
          <li>
            When selecting the Date Range "This month" while the current date is the first of the month, “to Date” = “from Date”.
          </li>
          <li>
            When selecting the Date Range as the “Last 12 months" while the current date is the first of the month, details for 13 months are reported, and not 12.
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="118">
        <p class="TableBodyText">
          4890
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Core
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="525">
        <p class="TableBodyText">
          You cannot update a User ID of a KMC user.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="118">
        <p class="TableBodyText">
          5129
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Entry Drill Down
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          In the entry drill down, the Entry-Id list is saved when closing the window without saving.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom" width="118">
        <p class="TableBodyText">
          3762
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="119">
        <p class="TableBodyText">
          Entry Drill Down
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom" width="525">
        <p class="TableBodyText">
          Categories without entitlement settings erroneously display the tooltip as if they are categories with entitlement settings. This may occur when hovering over old categories.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<div>
  <div>
    <p>
       
    </p>
  </div>
</div>

#### Tested Browsers

The following browsers were tested for this release (recommended resolution 1024x768):

*   Chrome 19
*   FF 13
*   IE9 on Windows 7