---
layout: page
title: "How to set entitlement settings in the KMC"
date: 2012-09-16 15:09:21
---

<span style="color: #484848; font-size: 18pt; font-weight: bold;">Setting the Entitlement Settings</span>

Perform the tasks in the <a href="http://knowledge.kaltura.com/faq/what-categorys-entitlement-tab-used-kmc#workflow_entitlement" target="_blank">workflow</a> to configure the KMC with Entitlement Settings.

The possible entitlement combination settings for different channel/category/gallery types are also provided [here][1].

 [1]: #combo

<p class="mce-procedure">
  To set Entitlement Settings
</p>

1.  Set the Content Privacy. See <a href="{{site.url}}/documentation/Knowledge/how-determine-content-privacy-kmc-0.html" target="_blank">Content Privacy.</a>
2.  Select the <a href="http://knowledge.kaltura.com/faq/what-are-categorys-listing-options-kmc-and-kms" target="_blank">Category Listing</a>.
3.  Select the <a href="http://knowledge.kaltura.com/faq/how-define-contribution-policy-kmc-and-kms" target="_blank">Contribution Policy</a>.
4.  Select whether to inherit specific end-user permissions.
5.  Set <a href="http://knowledge.kaltura.com/faq/what-are-specific-end-user-permissions-kmc-and-kms" target="_blank">Specific End User Permissions</a>.
<ol style="list-style-type: lower-alpha;">
  <li>
    <a href="http://knowledge.kaltura.com/faq/how-change-category-owner-kmc-or-kms" target="_blank">Change Owner.</a>
  </li>
  <li>
    Click <a href="{{site.url}}/documentation/Knowledge/how-manage-categories-specific-end-user-permissions.html" target="_blank">Manage </a>to manage end-user permissions.
  </li>
  <li>
    Configure <a href="{{site.url}}/documentation/Knowledge/how-change-category-owner-kmc-or-kms.html" target="_blank">Additional Category Entitlement Settings</a>.
  </li>
</ol>

6.  Click Save & Close. <img src="../../assets/697">

<p class="mce-heading-3">
  <a name="combo"></a>KMS Galleries / Channels Entitlements
</p>

The following information describes how Channels/Galleries work in context to KMS application roles.

Please familiarize yourself with the information in the article <a href="{{site.url}}/documentation/Knowledge/kaltura-mediaspacekaltura-application-framework-kaf-roles-and-permissions.html" target="_blank">Kaltura MediaSpace/Kaltura Application Framework (KAF) Roles and Permissions</a> before you set entitlement settings for KMS.

**<span>If the settings do not align with a behavior you are seeing in KMS, you may have misconfigured  the gallery / channel entitlements in the KMC configuration</span>**. 

<span class="mce-note-graphic">KMS Galleries / Channels entitlements settings should NEVER be modified through the KMC. Changes to entitlements of KMS galleries / channels should be made through KMS ONLY.</span>

KMS Galleries / channels are manifested with the following entitlements combinations in KMC :

<div class="table-wrap">
  <table class="confluenceTable">
    <tbody>
      <tr>
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            <strong>Gallery type / permission</strong>
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            <strong>Content Privacy</strong>
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            <strong>Category listing</strong>
          </p>
          
          <p align="center">
            <strong> </strong>
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            <strong>Who can add content to gallery</strong>
          </p>
        </td>
      </tr>
      
      <tr>
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            Open
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            No restriction
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            No restriction
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            No restriction
          </p>
        </td>
      </tr>
      
      <tr>
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            Restricted
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            Requires authentication
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            No restriction
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            Private
          </p>
        </td>
      </tr>
      
      <tr>
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            Private
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            Private
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            Private
          </p>
        </td>
        
        <td class="highlight-green confluenceTd" data-highlight-colour="green">
          <p>
            Private
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
     
  </p>
</div>

<div class="table-wrap">
  <table class="confluenceTable">
    <tbody>
      <tr>
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            <strong>Channel type / permission</strong>
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            <strong>Content Privacy</strong>
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            <strong>Category listing</strong>
          </p>
          
          <p align="center">
            <strong> </strong>
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            <strong>Who can add content to gallery</strong>
          </p>
        </td>
      </tr>
      
      <tr>
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Public
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            No restriction
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            No restriction
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Private
          </p>
        </td>
      </tr>
      
      <tr>
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Open
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Requires authentication
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            No restriction
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            No restriction
          </p>
        </td>
      </tr>
      
      <tr>
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Restricted
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Requires authentication
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            No restriction
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Private
          </p>
        </td>
      </tr>
      
      <tr>
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Private
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Private
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Private
          </p>
        </td>
        
        <td class="highlight-red confluenceTd" data-highlight-colour="red">
          <p>
            Private
          </p>
        </td>
      </tr>
      
      <tr>
        <td class="highlight-red confluenceTd" colspan="1">
          Shared Repository
        </td>
        
        <td class="highlight-red confluenceTd" colspan="1">
          Private
        </td>
        
        <td class="highlight-red confluenceTd" colspan="1">
          Private
        </td>
        
        <td class="highlight-red confluenceTd" colspan="1">
          Private
        </td>
      </tr>
    </tbody>
  </table>
</div>

 

ANY combination that is set through the KMC and does not align with the above combinations, will not work properly, or as described in the <a href="{{site.url}}/documentation/Knowledge/kaltura-mediaspacekaltura-application-framework-kaf-roles-and-permissions.html" target="_blank">Kaltura MediaSpace/Kaltura Application Framework (KAF) Roles and Permissions</a> article.