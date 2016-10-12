---
layout: page
title: "How to add users to KMS using the Bulk Upload Option"
date: 2014-11-17 14:06:47
---

<div data-layout="single">
  <div data-type="normal">
    <div>
      It is possible to add a large list of KMC users via the Kaltura Management Console. You can also add MediaSpace users in bulk.
    </div>
    
    <div>
      <p>
        <em><strong>Note: There is a 5000 user limitation on channel and category members.</strong> If more members are expected, please use Kaltura Groups . See</em> <a href="https://knowledge.kaltura.com/node/1672%20" target="_blank">Group Support in Kaltura Applications and Kaltura Groups FAQ</a> for additional information.
      </p>
    </div>
    
    <div>
       
    </div>
    
    <div>
      To bulk-add MediaSpace users, use the same bulk upload method as for the KMC but add additional attributes required by MediaSpace.
    </div>
    
    <p class="mce-procedure">
      To edit the Users-Bulk-Upload CSV File
    </p>
  </div>
</div>

<div class="columnLayout single" data-layout="single">
  <div class="cell normal" data-type="normal">
    <div class="innerCell" style="padding-left: 30px;">
      <ol style="padding-left: 30px;">
        <li>
          <p>
            <span style="line-height: 16px; background-color: initial;">Click </span><a href="#sample" target="_blank" style="font-weight: bold; line-height: 16px; background-color: initial;" rel="nofollow">here</a><span style="line-height: 16px; background-color: initial;"> to view a sample <em>o</em>f what the Bulk CSV file would look like.<br /><img src="{{site.url}}/assets/2479">
          </p>
        </li>
        
        <li>
          Open the end users example CSV using Excel or similar.
        </li>
        <li>
          Add an "email" column and populate it with email addresses for the MediaSpace users. While not manatory, setting email addresses allows these new users to receive <a href="http://knowledge.kaltura.com/kaltura-mediaspace-46-release-notes#email+notifications">MediaSpace email notifications</a>.
        </li>
        <li>
          Add a column for a MediaSpace role. The format of the column title is "metadata::KMS_USERSCHEMA1_[your_MediaSpace_instance_id]::role", where the instance id is your MediaSpace instance id, found in the Application section of your MediaSpace back office.<br /><img src="{{site.url}}/assets/2483">
        </li>
      </ol>The new column defines the role of the new users to be created, the options depend on the KMS instance. By default, the following roles are available:
      
      <br /><ul>
        <li>
          unmoderatedAdminRole
        </li>
        <li>
          adminRole
        </li>
        <li>
          privateOnlyRole
        </li>
        <li>
          viewerRole
        </li>
        <li>
          anonymousRole
        </li>
      </ul>After adding all the information to the CSV, your file should look as follows:
    </div>
    
    <div class="innerCell" style="padding-left: 30px;">
       
    </div>
    
    <div class="innerCell" style="padding-left: 30px;">
      <img src="{{site.url}}/assets/2481">
        Uploading the CSV file to MediaSpace and Kaltura Management Console
      </h3>
      
      <span class="mce-procedure" style="background-color: #ffffff;">To Upload the CSV via Kaltura Management Console</span>
    </div>
    
    <div class="innerCell" style="padding-left: 30px;">
      <ol>
        <li>
          <span>After saving the CSV file, browse to your </span><a rel="nofollow">Kaltura Management Console </a><a rel="nofollow">(</a><a rel="nofollow">KMC)</a><span>.</span>
        </li>
        <li>
          <span></span><span>Select </span><strong>Upload</strong><span>, then choose </span><strong>Select CSV/XML</strong><span> and choose </span><strong>End-Users CSV</strong><span>.<br /><img src="{{site.url}}/assets/2345">
        </li>
        <li>
          <p>
            <span></span><span>Choose the CSV from the previous step and click </span><strong>Open</strong><span>.<br /><img src="{{site.url}}/assets/2346">
          </p>
          
          <span></span>That's it. The CSV file containing a list of MediaSpace users is uploaded.
        </li>
      </ol>
      
      <p id="HowtobulkuploadKMSusers-UploadingUsers-CSVfromMediaSpaceAdminConsole" class="mce-procedure">
        To Upload the Users-CSV from MediaSpace Admin Console
      </p>
      
      <ol>
        <li>
          Access your MediaSpace Admin Console.
        </li>
        <li>
          Select Manage Users from top navigation bar.<br /><img src="{{site.url}}/assets/2347">
        </li>
        <li>
          <span>To upload the CSV, click  </span><strong>Submit CSV.<br /><strong><strong><strong><img src="{{site.url}}/assets/2348">
        </li>
        <li>
          <span>Click the </span><strong>Choose File</strong><span> button and select the CSV from the previous step and click </span>OK<span>.</span>
        </li>
      </ol>
      
      <p style="padding-left: 30px;">
        <img src="{{site.url}}/assets/2349">
      </p> That's it. Users should now be able to log in to MediaSpace.
    </div>
    
    <div class="innerCell" style="padding-left: 30px;">
       
    </div>
    
    <h2 class="innerCell" style="padding-left: 30px;">
      <a name="sample"></a>Sample of <span>Users-Bulk-Upload CSV File</span>
    </h2>
    
    <div class="innerCell" style="padding-left: 30px;">
       
    </div>
    
    <div class="innerCell" style="padding-left: 30px;">
      <pre class="brush: plain;fontsize: 100; first-line: 1; "># Detailed information on the End-Users CSV, including relevant use cases, complete schema description and examples,
# is available in: http://knowledge.kaltura.com/end-users-csv-usage-and-schema-description
# Note: The submission of end-users CSV enabled only when your account is set to support end-user management
# The CSV should have the following fields for each user record. separated by comma:
# -- action – Optional - Kaltura’s numeric value for the action to apply on a specific user account. Supported action typles and their numeric values: values: 1- add, 2- update, 3- delete, 6- add or update. Default = add
# -- userId - Mandatory - The user's unique identifier.
# -- firstName – Optional (required for MediaSpace) The user's first name
# -- lastName – Optional (required for MediaSpace)- The user's last name
# -- screenName - Optional (required for MediaSpace)- The user's Screen Name as will appear in the KMC.
# -- email – Optional - The user's email address.
# -- tags – Optional - The tags to be added to the user account
# -- gender – Optional - Kaltura's numeric value for gender. Supported values: 0-unknown (default), 1- male, 2- female.
# -- city – Optional - a free text field for populating a user's city
# -- state – Optional - a free text field for populating a user's state
# -- country – Optional - a free text field for populating a user's country
# -- zip – Optional - a free text field for populating a user's zip code
# -- dateOfBirth - Optional - The user's date of birth
# -- partnerData - Optional - a free text field used in the account for applicative use.
# -- Custom metadata (User object) - Optional - field name should be set according to the following format: metadata::[metadataProfileSystemName]::[metadataProfileFieldSystemName]
#
*action userId firstName lastName screenName
1 su1xyz Sample User1 Sample User1
1 su2xyz Sample User2 Sample User2
1 su3xyz Sample User3 Sample User2</pre>
    </div>
  </div>
</div>