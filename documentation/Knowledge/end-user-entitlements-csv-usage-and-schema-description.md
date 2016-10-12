---
layout: page
title: "End-User Entitlements CSV - Usage and Schema Description "
date: 2012-06-06 14:10:01
---

# End-User Entitlements CSV

The End-User Entitlements CSV is used for setting, updating or deleting specific end-user permissions to categories. The end-user permission to a category is set to a specific user ID and with a defined permission level. End-user entitlements can be set to multiple categories through a single CSV file.

## Purpose and Usage

The End-user entitlements bulk operation may be useful for the following cases:

*   Creating multiple end-user permissions for the initial setup of MediaSpace group channels based on users’ membership in organizational units.
*   An on-going scheduled process for syncing end-user permissions to MediaSpace group channels with group membership’s information saved in an organizational system.
*   All user permissions created via this bulk service are set to an automatic “update method”. When an on-going sync process is activated on a regular basis - it is possible to manually override the automatically created user permissions from the KMC or MediaSpace for granting different permission levels to some users in the group. In this case the specific user permissions will be set to a manual “update method”, for example, group managers, and will not be overridden by upcoming executions of the end-user entitlements bulk service.

<table style="width: 638px;" border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="68">
        <span>NOTE:</span> 
      </td>
      
      <td valign="top" width="570">
        <p class="Note" style="text-align: left;">
          For an efficient on-going CSV based sync processes - it is recommended that only new user permissions and user permissions that require updating or deletion, based on recent changes in organizational structure will be included within the CSV and not the entire group directory
        </p>
      </td>
    </tr>
  </tbody>
</table>

## General Guidelines

*   Lines that begin with a # character will not be processed.
*   The first line for processing (fields’ definition line) should start with an * sign and should include the field names to be populated via the CSV, according to the defined schema of each CSV format. Mandatory fields must be present. The field order may be set as needed.
*   Each line for processing within the CSV should include a comma separated list of values ordered by the field ordering set in the fields’ definition line.
*   Each line for processing within the CSV will apply an action on a single Kaltura object. For example: each line in the End-User Entitlements CSV will apply the action to a single end-user permission to a category..  
*   The CSV may be submitted from the KMC (through the Upload menu) or via a script, by utilizing Kaltura’s API.
*   Prior to processing the CSV file, its format is validated. When a mandatory field is missing, the bulk job will fail and processing will not start.
*   Bulk job tracking as well as downloading bulk job related files (the original CSV and log files) are done through the KMC using the **Bulk Upload Log** feature under the **Upload Control **page.
*   Email notifications on the completion of bulk upload processing - including completion status and a direct link to the log file, can be configured by Kaltura per request.
*   There is no limitation on the supported number of lines within each CSV.  The overall processing time of each CSV file is affected by the number of lines included in it. 
*   The following special characters can be populated within text fields via the CSV file :

         - _ % ? . :  ;  &  > @ ! $ ^ ~  = [ ] { } |  < 

        See special exceptions within each schema description.

The CSV examples included in this guide are displayed in screens from MS Excel for better clarity. 

## Schema Description for End-User Entitlements CSV

The following table includes descriptions for all end-user attributes supported by Kaltura. CSV examples targeted to MediaSpace user-management only are available below. 

<table style="width: 936px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="144">
        <p class="TableHeading">
          <strong>Parameter Name</strong>
        </p>
      </td>
      
      <td valign="top" width="90">
        <p class="TableHeading">
          <strong>Mandatory/ Optional</strong>
        </p>
      </td>
      
      <td valign="top" width="396">
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
      <td style="text-align: left;" valign="top" width="144">
        <p class="TableBodyText">
          action
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="396">
        <p class="TableBodyText">
          Kaltura’s numeric value for the action to apply for specific end-user permission to a category.
        </p>
        
        <p class="TableBodyText">
          CSV lines with different actions can be combined into a single CSV file. Only fields that are relevant to the CSV action will be used.
        </p>
        
        <p class="TableBodyText">
          The supported action types and their numeric values are:
        </p>
        
        <p class="TableBodyText">
          1=Add - to add specific end-user permission to a category
        </p>
        
        <p class="TableBodyText">
          2=Update – to update a specific end-user permission to a category
        </p>
        
        <p class="TableBodyText">
          3=Delete – to delete a new specific end-user permission to a category
        </p>
        
        <p class="TableBodyText">
          6=Add or Update – to add or update a specific end-user permission to a category.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          1= Add
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaBulkUploadAction">KalturaBulkUploadAction</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="144">
        <p class="TableBodyText">
          categoryId
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="396">
        <p class="TableBodyText">
          The Kaltura internal and unique identifier of the category.  The categoryId field is used in the CSV for identifying the category to which the specific end-user permission should be added/updated/deleted.
        </p>
        
        <p class="TableBodyText">
          This field is optional but either the categoryId or the referenceId fields must be provided for identifying the category to which the action should apply.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Integer
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="144">
        <p class="TableBodyText">
          categoryReferenceId
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="396">
        <p class="TableBodyText">
          A possible identifier of the category from an external system.  The categoryReferenceId field is used in the CSV for identifying the category to which the specific end-user permission should be added/updated/deleted.
        </p>
        
        <p class="TableBodyText">
          This field is optional, but either the categoryId or the categoryReferenceId fields must be provided for identifying the category to which the action should apply.
        </p>
        
        <p class="TableBodyText">
          The uniqueness of categoryReferenceId field is not verified nor managed in Kaltura.  It is recommended to use a logic that maintains this uniqueness for being able to reference bulk actions and API calls to a specific category.
        </p>
        
        <p class="TableBodyText">
          In case of multiple categories with the same categoryReferenceId exist in the account, CSV update/delete actions will be committed only to a single category.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          Text Field. Maximum length: 512 Characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="144">
        <p class="TableBodyText">
          userId
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Mandatory
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="396">
        <p class="TableBodyText">
          The identifier of the end-user to which the category permission should be added/updated/deleted for.
        </p>
        
        <p class="TableBodyText">
          When the user account is not yet set in Kaltura it will be created as part of this bulk service with the given userId
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
        
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="144">
        <p class="TableBodyText">
          permissionLevel
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="396">
        <p class="TableBodyText">
          The numeric value of the permission Level the end-user should be granted for the specific category. The supported values are:
        </p>
        
        <p class="TableBodyText">
          0=Manager
        </p>
        
        <p class="TableBodyText">
          1=Moderator
        </p>
        
        <p class="TableBodyText">
          2=Contributor
        </p>
        
        <p class="TableBodyText">
          3=Member
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          3=Member
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaCategoryUserPermissionLevel">KalturaCategoryUserPermissionLevel</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="144">
        <p class="TableBodyText">
          updateMethod
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="396">
        <p class="TableBodyText">
          The numeric value of the update method the end-user permission to the category should be updated. The supported values are:
        </p>
        
        <p class="TableBodyText">
          0=Manual
        </p>
        
        <p class="TableBodyText">
          1=Automatic
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          1=Automatic
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaUpdateMethodType">KalturaUpdateMethodType</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="144">
        <p class="TableBodyText">
          status
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="396">
        <p class="TableBodyText">
          The numeric value of the status of the end-user permission to the category. The supported values are:
        </p>
        
        <p class="TableBodyText">
          1=Active
        </p>
        
        <p class="TableBodyText">
          3=Deactivated (update actions only)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="102">
        <p class="TableBodyText">
          1=Active
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="204">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaCategoryUserStatus">KalturaCategoryUserStatus</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

## Examples of End-User Entitlements CSV

### Adding/Updating Permissions to 2 Categories

This example uses the referenceId as the category identifier.

<img src="{{site.url}}/assets/533">

### Deleting End-user Permissions from Specific Categories

This example uses the referenceId as the category identifier.

 <img src="{{site.url}}/assets/535">