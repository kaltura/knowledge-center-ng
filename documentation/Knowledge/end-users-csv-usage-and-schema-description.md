---
layout: page
title: "End-Users CSV  - Usage and Schema Description "
date: 2012-06-06 14:05:12
---

# End-Users CSV

The End-Users CSV may be used for the provisioning, updating or deleting a large amount of end-user accounts in Kaltura.

<h2 class="mce-heading-4 mce-heading-2">
  Purpose and Usage
</h2>

The end-users CSV for bulk operation may be useful for:

*   Creating multiple end-user accounts. For example:
*   Pre-provisioning of MediaSpace user accounts when user authentication and/or user authorization to access MediaSpace with a specific role should be controlled and managed in Kaltura and not through a SSO/authentication integration.
*   Creating a user list for enabling the selection of MediaSpace’s Channel members from a full list of users managed in Kaltura.
*   An on-going scheduled process for synchronizing the user accounts managed in Kaltura with the organization user directory.

<table style="width: 609px;" border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="68">
        <span>NOTE:</span> 
      </td>
      
      <td style="text-align: left;" valign="top" width="541">
        <p>
          For an efficient on-going CSV based synchronization process, only new user accounts and user accounts that require updating or deletion should be included within the CSV.
        </p>
      </td>
    </tr>
  </tbody>
</table>

 

<table style="width: 609px;" border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="68">
         <span>NOTE: </span>
      </td>
      
      <td style="text-align: left;" valign="top" width="541">
        <p>
          The end-users CSV is designed for managing end-user accounts. KMC user accounts are managed separately via the KMC Administration tab.
        </p>
      </td>
    </tr>
  </tbody>
</table>

## General Guidelines

*   Lines that begin with a # character will not be processed.
*   The first line for processing (fields’ definition line) should start with an * sign and should include the field names to be populated via the CSV, according to the defined schema of each CSV format. Mandatory fields must be present. The field order may be set as needed.
*   Each line for processing within the CSV should include a comma separated list of values ordered by the field ordering set in the fields’ definition line.
*   Each line for processing within the CSV will apply an action on a single Kaltura object. For example: each line in the End-Users CSV will apply the action to a single end-user.  
*   The CSV may be submitted from the KMC (through the Upload menu) or via a script, by utilizing Kaltura’s API.
*   Prior to processing the CSV file, its format is validated. When a mandatory field is missing, the bulk job will fail and processing will not start.
*   Bulk job tracking as well as downloading bulk job related files (the original CSV and log files) are done through the KMC using the **Bulk Upload Log** feature under the **Upload Control **page.
*   Email notifications on the completion of bulk upload processing - including completion status and a direct link to the log file, can be configured by Kaltura per request.
*   There is no limitation on the supported number of lines within each CSV.  The overall processing time of each CSV file is affected by the number of lines included in it. 
*   The following special characters can be populated within text fields via the CSV file :

           - _ % ? . :  ;  &  > @ ! $ ^ ~  = [ ] { } |  < 

       See special exceptions within each schema description.

The CSV examples included in this guide are displayed in screens from MS Excel for better clarity.

## <a name="_Toc330415471"></a><span>Schema Description for the End-Users CSV</span><span></span>

<table style="width: 936px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="120">
        <p class="TableHeading">
          <strong>Parameter Name</strong>
        </p>
      </td>
      
      <td valign="top" width="90">
        <p class="TableHeading">
          <strong>Mandatory/ Optional</strong>
        </p>
      </td>
      
      <td valign="top" width="420">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
        
        <p class="TableHeading">
          <strong> </strong>
        </p>
      </td>
      
      <td valign="top" width="102">
        <p class="TableHeading">
          <strong>Default</strong>
        </p>
        
        <p class="TableHeading">
          <strong> </strong>
        </p>
      </td>
      
      <td valign="top" width="204">
        <p class="TableHeading">
          <strong>Type and Restrictions</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          action
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          Kaltura’s numeric value for the action to apply on a specific user account.
        </p>
        
        <p class="TableBodyText">
          CSV lines with different actions can be combined into a single CSV file. Only fields that are relevant to the CSV action will be used.
        </p>
        
        <p class="TableBodyText">
          The supported action types and their numeric values are:
        </p>
        
        <p class="TableBodyText">
          1=Add - to add a new user account
        </p>
        
        <p class="TableBodyText">
          2=Update – to update an existing user account
        </p>
        
        <p class="TableBodyText">
          3=Delete – to delete an existing user account
        </p>
        
        <p class="TableBodyText">
          6=Add or Update – to add a new user account or update an existing account when the provided user ID is already available in Kaltura.  User accounts may be automatically created in Kaltura upon different cases. It is therefore recommended to use option 6 when adding new user accounts.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          1= Add
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          <a href="https://vpaas.kaltura.com/documentation/Media-Ingest-and-Preperation/Bulk-Content-Ingestion.html#">KalturaBulkUploadAction</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          userId
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Mandatory
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          The user’s unique identifier.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text Field.
        </p>
        
        <p class="TableBodyText">
          Minimum length: 3 characters Maximum length: 100 Characters
        </p>
        
        <p class="TableBodyText">
          Only the following special characters are supported as part of the userId:
        </p>
        
        <p class="TableBodyText">
          . _ @ -
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          firstName
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          The user’s first name.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text Field. Maximum length: 40 Characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          lastName
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          The user’s last name.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          <em> </em>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text field. Maximum length: 40 Characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          screenName
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          The user’s Screen Name as it will appear in the KMC.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          <em> </em>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text field. Maximum length: 100 Characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          email
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          The user’s email address.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text field. Maximum length: 100 Characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          tags
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          The tags to be added to the user account. Multiple tags can be separated by commas, while the entire field should be wrapped with double quotation marks (for example: “tag1, tag2). When the CSV is created in a simple text editor or by a script - the wrapping quotation marks should be added explicitly.  When CSV is created with a spread sheet editor (for example: MS Excel) this wrapping is automatically generated when saving to a CSV format with no need for manual editing.
        </p>
        
        <p class="TableBodyText">
          The tag values cannot include commas.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text Field
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          gender
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          Kaltura’s numeric value for gender
        </p>
        
        <p class="TableBodyText">
          1=Male
        </p>
        
        <p class="TableBodyText">
          2=Female
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          KalturaGender
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          country
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          A free text field for populating a user’s country.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text field. No format validation. Maximum length: 16 Characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          state
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          A free text field for populating a user’s state.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text field. No format validation. Maximum length: 2 Characters
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          city
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          A free text field for populating a user’s city.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text Field. No format validation. Maximum length:  30 characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          zip
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          A free text field for populating a user’s zip code.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text Field. No format validation. Maximum length:  10 characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          dateOfBirth
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          The users date of birth.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          YYYY-MM-DD
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          partnerData
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          The partnerData user attribute is managed only via API.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text field
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          Custom Data
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          Custom data fields that are set to extend the Kaltura User object can be populated via the CSV by defining the fields in the following formats:
        </p>
        
        <p class="TableBodyText">
          metadata::<em>the-schema-system-name</em>::<em>the-schema-field-name</em>
        </p>
        
        <p class="TableBodyText">
          Multiple custom data schemas and fields can be populated via the CSV.
        </p>
        
        <p class="TableBodyText">
          Values of custom data fields that have multiple values should be separated with a the following delimiter:   |,|
        </p>
        
        <p class="TableBodyText">
          Note: When updating custom data fields to an existing user account, a new metadata XML is automatically created. For preventing overriding existing values, all custom data fields that are set for the user should be provided in the CSV as part of the update action.
        </p>
        
        <p class="TableBodyText">
          Custom data schemas and fields that apply to the KalturaUser Object are managed only via the Kaltura API.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          <em> </em>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" colspan="5" valign="top" width="936">
        <p class="TableHeading">
          <strong>MediaSpace Specific User Values</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          MediaSpace User Role (MediaSpace 5.0)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          This field is applicable only when a user is authorized to a specific MediaSpace role through Kaltura and <span style="text-decoration: underline;">not</span> through SSO/authentication integration.
        </p>
        
        <p class="TableBodyText">
          The MediaSpace user role is managed as a user custom data in a standard MediaSpace custom data schema created automatically when MediaSpace is installed.
        </p>
        
        <p class="TableBodyText">
          The system name of  MediaSpace Custom data schema is :
        </p>
        
        <p class="TableBodyText">
          KMS_USERSCHEMA1_<em>Your MediaSpace InstanceId</em>
        </p>
        
        <p class="TableBodyText">
          The name of the role field within this schema is: role
        </p>
        
        <p class="TableBodyText">
          The populated values that should be the same as defined in the MediaSpace configuration.
        </p>
        
        <p class="TableBodyText">
          Example: when the MediaSpace InstanceId is set to: “MyVideoPortal”
        </p>
        
        <p class="TableBodyText">
          and one of the standard MediaSpace roles was named: “viewerRole”
        </p>
        
        <p class="TableBodyText">
          The custom data field name in the CSV should be:
        </p>
        
        <p class="TableBodyText">
          metadata::KMS_USERSCHEMA1_MyVideoPortal::role
        </p>
        
        <p class="TableBodyText">
          and the populated value for view only MediaSpace users should be set to : “viewerRole”
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          <em> </em>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="120">
        <p class="TableBodyText">
          MediaSpace User password
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="420">
        <p class="TableBodyText">
          This field is applicable only when user authentication is handled by Kaltura and <span style="text-decoration: underline;">not</span> through SSO/authentication integration.
        </p>
        
        <p class="TableBodyText">
          For setting a user password as part of the bulk creation of MediaSpace user accounts, a <a href="http://en.wikipedia.org/wiki/SHA-1">sha1</a> hashed password should be populated as part of the partnerData field.
        </p>
        
        <p class="TableBodyText">
          The MediaSpace password should include at least 6 characters.
        </p>
        
        <p class="TableBodyText">
          Example: when a user’s password should be set to:  MyPass123%, the following value should be populated into the partnerData field within the CSV for the user’s record: 
        </p>
        
        <p class="TableBodyText">
          pw=ecc94cd2e13ec3ae3ea30bda01e4fe715f9f9d20
        </p>
        
        <p class="TableBodyText">
          You can also set the password manually from the User Management page in the MediaSpace configuration panel.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          <em> </em>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

## Examples of End-Users CSV

### Bulk Provisioning/updating of Media Space’s User Accounts with a Role*

<img src="../../assets/3450.img">

* Users are authenticated through SSO integration. Authorization to access to MediaSpace with a specific role is managed by Kaltura. The role’s metadata field name and possible values are specific per MediaSpace configuration.

### Bulk Deletion of Specific MediaSpace User Accounts

<img src="../../assets/530.img">