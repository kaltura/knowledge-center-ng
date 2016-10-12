---
layout: page
title: "Categories CSV - Usage and Schema Description "
date: 2012-06-06 14:08:40
---

# Categories CSV

The Categories CSV may be used for creating, updating or deletion of, a large amount of categories.

## Purpose and Usage

The categories CSV for bulk operation may be useful for:

*   Creating multiple categories for any applicative use. For example:
*   Creating multiple categories for the initial setup of Media Space’s galleries and channels
*   Creating multiple categories for a Kaltura based website integration
*   An on-going scheduled process for the syncing categories managed in Kaltura with a respective external structure. For example:
*   A scheduled daily sync process for syncing MediaSpace group channels with groups managed in the organization.
*   An automatic sync of Kaltura’s categories with the taxonomy of an external CMS 

 

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="68">
        <span>NOTE: </span> 
      </td>
      
      <td style="text-align: left;" valign="top" width="541">
        <p class="Note" style="text-align: left;">
          For an efficient on-going CSV based sync processes, only new categories and categories that require updating or deletion should be included within the CSV
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
        <p class="Note">
          Content entitlement related attributes can be populated via the CSV only in accounts that are set to support entitlements and for categories under a category tree branch that is set to have entitlement settings.
        </p>
      </td>
    </tr>
  </tbody>
</table>

## General Guidelines

*   Lines that begin with a # character will not be processed.
*   The first line for processing (fields’ definition line) should start with an * sign and should include the field names to be populated via the CSV, according to the defined schema of each CSV format. Mandatory fields must be present. The field order may be set as needed.
*   Each line for processing within the CSV should include a comma separated list of values ordered by the field ordering set in the fields’ definition line.
*   Each line for processing within the CSV will apply an action on a single Kaltura object. For example: each line in the categories CSV will apply the action to a single category.  
*   The CSV may be submitted from the KMC (through the Upload menu) or via a script, by utilizing Kaltura’s API.
*   Prior to processing the CSV file, its format is validated. When a mandatory field is missing, the bulk job will fail and processing will not start.
*   Bulk job tracking as well as downloading bulk job related files (the original CSV and log files) are done through the KMC using the **Bulk Upload Log** feature under the **Upload Control **page.
*   Email notifications on the completion of bulk upload processing - including completion status and a direct link to the log file, can be configured by Kaltura per request.
*   There is no limitation on the supported number of lines within each CSV.  The overall processing time of each CSV file is affected by the number of lines included in it. 
*   The following special characters can be populated within text fields via the CSV file :

           - _ % ? . :  ;  &  > @ ! $ ^ ~  = [ ] { } |  < 

        See special exceptions within each schema description.

The CSV examples included in this guide are displayed in screens from MS Excel for better clarity.

## <a name="_Toc329270838"></a><span>Schema Description for Categories CSV</span><span></span>

<table style="width: 936px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="126">
        <p class="TableHeading">
          <strong>Parameter Name</strong>
        </p>
      </td>
      
      <td valign="top" width="90">
        <p class="TableHeading">
          <strong>Mandatory/ Optional</strong>
        </p>
      </td>
      
      <td valign="top" width="414">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
        
        <p class="TableHeading">
          <strong> </strong>
        </p>
      </td>
      
      <td valign="top" width="84">
        <p class="TableHeading">
          <strong>Default</strong>
        </p>
        
        <p class="TableHeading">
          <strong> </strong>
        </p>
      </td>
      
      <td valign="top" width="222">
        <p class="TableHeading">
          <strong>Type and Restrictions</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          action
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          Kaltura’s numeric value for the action to apply on a specific category.
        </p>
        
        <p class="TableBodyText">
          CSV lines with different actions can be combined into a single CSV file. Only fields that are relevant to the CSV action will be used.
        </p>
        
        <p class="TableBodyText">
          The supported action types and their numeric values are:
        </p>
        
        <p class="TableBodyText">
          1=Add - to add a category
        </p>
        
        <p class="TableBodyText">
          2=Update – to update an existing category
        </p>
        
        <p class="TableBodyText">
          3=Delete – to delete an existing category
        </p>
        
        <p class="TableBodyText">
          6=Add or Update – to add or update a category when the given categoryId or referenceId are already available in Kaltura.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          1= Add
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaBulkUploadAction">KalturaBulkUploadAction</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          name
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Mandatory in <strong>add</strong> actions
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The name of the category. When the category name includes the > character it will automatically be replaced with _ (underscore character).
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          Text Field. Maximum length: 60 Characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          relativePath
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The category-tree path in which the category is located or should be created. Each category level within the path should be separated by the ‘> ‘character.  
        </p>
        
        <p class="TableBodyText">
          <strong>Note:</strong> The provided path must exist prior to processing  the CSV line, or created in a higher CSV line.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          Text Field. Unlimited length
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          categoryId
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The Kaltura internal and unique identifier of the category.  The categoryId field is used in the CSV for identifying a category that requires updating or needs to be deleted.
        </p>
        
        <p class="TableBodyText">
          In an ‘update’ or a ‘delete’ action, either the categoryId or the referenceId field must be provided for identifying the category to which the action should apply.
        </p>
        
        <p class="TableBodyText">
          In ‘add’ actions the categoryId field will be ignored.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          Integer 
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          referenceId
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          A possible identifier of the category based on an identifier from an external system that can relate the category to an external entity it represents or related to.
        </p>
        
        <p class="TableBodyText">
          In an ‘update’ or a ‘delete’ action, either the categoryId or the referenceId field must be provided for identifying the category to which the action should apply.
        </p>
        
        <p class="TableBodyText">
          In ‘add’ actions the referenceId will be populated into the new category.
        </p>
        
        <p class="TableBodyText">
          Note: The uniqueness of the referenceId field is not verified nor managed in Kaltura.  It is recommended to use logic that maintains this uniqueness for being able to reference bulk actions and API calls to a specific category.
        </p>
        
        <p class="TableBodyText">
          In case multiple categories with the same referenceId exist in the account, any update/delete action will be committed only to a single category.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          Text Field. Maximum length: 512 Characters
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          tags
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The tags to be added to the category. Multiple tags can be separated by commas, while the entire field should be wrapped with double quotation marks (e.g. “tag1, tag2). When the CSV is created in a simple text editor or by a script - the wrapping quotation marks should be added explicitly.  When CSV is created with a spread sheet editor (e.g. MS Excel) this wrapping is automatically generated when saving to a CSV format with no need for manual editing.
        </p>
        
        <p class="TableBodyText">
          Tag values cannot include commas.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          Text Field. Unlimited length
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          description
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          A description of the category and its applicative/administrative purpose.
        </p>
        
        <p class="TableBodyText">
          When the CSV is created in a simple text editor or by a script – adding wrapping quotation marks is recommended for cases in which the description includes commas
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          <em> </em>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          Text Field. Unlimited length
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          Custom Data
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          Custom data fields that are set to extend the Kaltura Category object can be populated into a category by defining the fields in the following formats:
        </p>
        
        <p class="TableBodyText">
          metadata::the-schema-system-name::the-schema-field-name
        </p>
        
        <p class="TableBodyText">
          With this format multiple custom data schemas and fields can be populated via the CSV.
        </p>
        
        <p class="TableBodyText">
          Custom data schema and fields system names are available in the custom data setting page in the KMC.
        </p>
        
        <p class="TableBodyText">
          Values of custom data fields that have multiple values should be separated with a the following delimiter:   |,|
        </p>
        
        <p class="TableBodyText">
          Note: When updating custom data fields to an existing category, a new metadata XML is automatically created. For preventing overriding existing values, all custom data fields that are set for the user should be provided in the CSV as part of the update action.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          <em> </em>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" colspan="5" valign="top" width="936">
        <p class="TableBodyText">
          <strong>Entitlements Settings</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          privacy
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The numeric value of the Content Privacy option to set for the category as part of its entitlements settings.
        </p>
        
        <p class="TableBodyText">
          This option is enabled only in accounts that are configured to support end-user entitlements to content and for categories that were set to have entitlement settings.
        </p>
        
        <p class="TableBodyText">
          The supported action types and their numeric values are:
        </p>
        
        <p class="TableBodyText">
          1= No Restriction
        </p>
        
        <p class="TableBodyText">
          2 =Requires Authentication
        </p>
        
        <p class="TableBodyText">
          3= Private
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          1 = No Restriction
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaPrivacyType">KalturaPrivacyType</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          appearInList
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The numeric value of the Category Listing option to set for the category as part of its entitlements settings.
        </p>
        
        <p class="TableBodyText">
          The setting of this option is enabled only in accounts that were configured to support Content Entitlements and in categories that have entitlement settings.
        </p>
        
        <p class="TableBodyText">
          The supported action types and their numeric values are:
        </p>
        
        <p class="TableBodyText">
          1= No Restriction
        </p>
        
        <p class="TableBodyText">
          3= Private
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          1 = No Restriction
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaAppearInListType">KalturaAppearInListType</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          contributionPolicy
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The numeric value of the ContributionPolicy option (who can add content to the category) to set for the category as part of its entitlements settings.
        </p>
        
        <p class="TableBodyText">
          The setting of this option is enabled only in accounts that were configured to support Content Entitlements and in categories that have entitlement settings.
        </p>
        
        <p class="TableBodyText">
          The supported action types and their numeric values are:
        </p>
        
        <p class="TableBodyText">
          1= No Restriction
        </p>
        
        <p class="TableBodyText">
          2= Private
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          1 = No Restriction
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaContributionPolicyType">KalturaContributionPolicyType</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          inheritanceType
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The numeric value of user permissions inheritance option (Inherit End-User Specific Permissions from Parent Category) to set for the category as part of its entitlements settings.
        </p>
        
        <p class="TableBodyText">
          The setting of this option is enabled only in accounts that were configured to support Content Entitlements and in categories that have entitlement settings.
        </p>
        
        <p class="TableBodyText">
          The supported action types and their numeric values are:
        </p>
        
        <p class="TableBodyText">
          1= Yes.  inherit specific end-user permissions from  parent category
        </p>
        
        <p class="TableBodyText">
          3= No.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          2=No
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaInheritanceType">KalturaInheritanceType</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          owner
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The userId of the category's owner.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
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
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          defaultPermissionLevel
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          The numeric value of the default permission Level the end-users should be granted for the specific category (unless other permission level was specified explicitly via CSV or API). The supported values are:
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
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          3=Member
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaCategoryUserPermissionLevel">KalturaCategoryUserPermissionLevel</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="126">
        <p class="TableBodyText">
          moderation
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p class="TableBodyText">
          Optional
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="414">
        <p class="TableBodyText">
          Indicates whether content should be moderated in the application before it is added to the category.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="84">
        <p class="TableBodyText">
          0=moderation is not required
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="222">
        <p class="TableBodyText">
          Boolean
        </p>
      </td>
    </tr>
  </tbody>
</table>

## Examples of the Categories CSV

### Bulk Creation of Categories – Basic Metadata Only

<img src="{{site.url}}/assets/531">

### Updating Existing Categories with a Few Entitlement Settings

This example uses the referenceId as the category identifier.

<p class="TableHeading">
  <img src="{{site.url}}/assets/532">
</p>