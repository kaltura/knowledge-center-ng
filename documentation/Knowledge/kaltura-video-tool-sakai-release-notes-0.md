---
layout: page
title: "Kaltura Video Tool for Sakai Release Notes "
date: 2016-01-28 13:50:40
---

<h2 class="mce-heading-1">
    <span style="font-size: 22pt;"><a name="v4.0.4"></a>Version 4.0.4</span>
  </h2>
  
  <p>
    These release notes pertain to the Kaltura Video Tool for Sakai, released August 2016.
  </p>
  
  <p>
    The Kaltura Video Tool for Sakai supports Sakai version 10.x.
  </p>
  
  <p class="mce-heading-1">
    <span style="color: #828a8c; font-size: 14pt;">Resolved Issues</span>
  </p>
  
  <table border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          <p>
            Issue
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            Description
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-98
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            The default auth code expiration has been updated from 1 min, to 40 min, to reduce timeout while preserving security,
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-94 
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            Kaltura.authorization.override.code was added to sakai.properties for the admin auth code to provide user enrollment data for publishing in a more secure manner.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-111
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            When antisamy is not configured correctly, the media embedded in the CKeditor will display: No Media with a tooltip to check your antisamy configuration. This replaces the HTTP 500 error,
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
             SAK-112
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
             An inherent cross-domain issue is correctly marked as an exception instead of error.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p style="text-align: left;">
    <span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Known Issues</span>
  </p>
  
  <table border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          Issue
        </td>
        
        <td style="text-align: left;">
          Description
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          SAK-89
        </td>
        
        <td style="text-align: left;">
          You may not be able to scroll down on some iOS devices when using the Browseandembed(BSE) module. 
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    There is a known Sakai issue https://jira.sakaiproject.org/browse/SAK-21129 that causes LTI launches to break on mobile devices. 
  </p>
  
  <p class="mce-procedure">
    To bypass this issue you may do the following:
  </p>
  
  <ol>
    <li>
      Add the following to sakai.properties: portal.pda.autoredirect=false
    </li>
    <li>
      Restart the Sakai server.
    </li>
    <li>
      On your mobile device, enable 3rd party cookies by going to Settings -> Safari -> Block Cookies -> Always Allow.<span style="font-weight: bold;"> </span>
    </li>
  </ol>
  
  <h2 class="mce-heading-1">
    <a name="v_4.0.3"></a>Version 4.0.3
  </h2>
  
  <p>
    These release notes pertain to the Kaltura Video Tool for Sakai, released March 2016.
  </p>
  
  <p>
    The Kaltura Video Tool for Sakai supports Sakai version 10.x.
  </p>
  
  <h3 class="mce-heading-3">
    Resolved Issues
  </h3>
  
  <table border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          Issue
        </td>
        
        <td style="text-align: left;">
          Description
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          SAK-90
        </td>
        
        <td style="text-align: left;">
          The CK editor integration security issue has been resolved.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
           
        </td>
        
        <td style="text-align: left;">
          Spelling was fixed for "expiration_date" in SQL scripts
        </td>
      </tr>
    </tbody>
  </table>
  
  <h3 class="mce-heading-3" style="text-align: left;">
    Known Issues
  </h3>
  
  <table border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          <strong>Issue</strong>
        </td>
        
        <td style="text-align: left;">
          <strong>Description</strong>
        </td>
      </tr>
      
      <tr>
        <td>
          <p>
            SAK-89
          </p>
        </td>
        
        <td>
          <p>
            You may not be able to scroll down on some iOS devices when using the Browseandembed(BSE) module. 
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    There is a known Sakai issue https://jira.sakaiproject.org/browse/SAK-21129 that causes LTI launches to break on mobile devices. 
  </p>
  
  <p class="mce-procedure">
    To bypass this issue you may do the following:
  </p>
  
  <ol>
    <li>
      Add the following to sakai.properties: portal.pda.autoredirect=false
    </li>
    <li>
      Restart the Sakai server.
    </li>
    <li>
      On your mobile device, enable 3rd party cookies by going to Settings -> Safari -> Block Cookies -> Always Allow.
    </li>
  </ol>
  
  <h2 class="mce-heading-1">
    Version 4.0.2
  </h2>
  
  <p>
    These release notes pertain to the Kaltura Video Tool for Sakai, released March 2016.
  </p>
  
  <p>
    The Kaltura Video Tool for Sakai supports Sakai version 10.x.
  </p>
  
  <h3 class="mce-heading-3">
    <span>Resolved Issues</span>
  </h3>
  
  <table style="width: 579px;" border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          <strong>Issue</strong>
        </td>
        
        <td style="text-align: left;">
          <strong>Description</strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-90
          </p>
        </td>
        
        <td style="text-align: left;">
          The CK editor integration security issue has been resolved.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
           
        </td>
        
        <td style="text-align: left;">
          The "Kaltura My Media" module has been renamed to "My Media".
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
           
        </td>
        
        <td style="text-align: left;">
          The issue causing My Media not to be added to "My Workspace" for existing users has been resolved.
        </td>
      </tr>
    </tbody>
  </table>
  
  <h3 class="mce-heading-3">
    <span>Known Issues</span>
  </h3>
  
  <table style="width: 579px;" border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          <strong>Issue</strong>
        </td>
        
        <td style="text-align: left;">
          <strong>Description</strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-89
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            You may not be able to scroll down on some iOS devices when using the Browseandembed(BSE) module. 
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    There is a known Sakai issue https://jira.sakaiproject.org/browse/SAK-21129 that causes LTI launches to break on mobile devices. 
  </p>
  
  <p class="mce-procedure">
    To bypass this issue you may do the following:
  </p>
  
  <ol>
    <li>
      Add the following to sakai.properties: portal.pda.autoredirect=false
    </li>
    <li>
      Restart the Sakai server.
    </li>
    <li>
      On your mobile device, enable 3rd party cookies by going to Settings -> Safari -> Block Cookies -> Always Allow.
    </li>
  </ol>
  
  <table style="width: 579px;" border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          <strong>Issue</strong>
        </td>
        
        <td style="text-align: left;">
          <strong>Description</strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-76
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            Due to the Sakai Site cache TTL, it may take time for sites to appear when publishing from My Media.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-86
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            The CK editor appears in edit mode in assignments. To preview the embedded media you will need to select the Preview button on the assignment page.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <h2 class="mce-heading-1">
    Version 4.0.1
  </h2>
  
  <p>
    These release notes pertain to the Kaltura Video Tool for Sakai, released January 2016.
  </p>
  
  <p>
    <span>The Kaltura Video Tool for Sakai supports Sakai version 10.x.</span>
  </p>
  
  <p>
    This release is the first Kaltura Video Tool for Sakai that is based on KAF. We recommend that you read the updated Kaltura Video Tool for Sakai documentation.
  </p>
  
  <h3 class="mce-heading-3">
    <span style="font-size: 1.17em;">Known Issues</span>
  </h3>
  
  <table style="width: 579px;" border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          <strong>Issue</strong>
        </td>
        
        <td style="text-align: left;">
          <strong>Description</strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-89
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            You may not be able to scroll down on some iOS devices when using the Browseandembed(BSE) module. 
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    There is a known Sakai issue https://jira.sakaiproject.org/browse/SAK-21129 that causes LTI launches to break on mobile devices. 
  </p>
  
  <p class="mce-procedure">
    To bypass this issue you may do the following:
  </p>
  
  <ol>
    <li>
      Add the following to sakai.properties: portal.pda.autoredirect=false
    </li>
    <li>
      Restart the Sakai server.
    </li>
    <li>
      On your mobile device, enable 3rd party cookies by going to Settings -> Safari -> Block Cookies -> Always Allow.
    </li>
  </ol>
  
  <table style="width: 579px;" border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          <strong>Issue</strong>
        </td>
        
        <td style="text-align: left;">
          <strong>Description</strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-76
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            Due to the Sakai Site cache TTL, it may take time for sites to appear when publishing from My Media.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SAK-86
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            The CK editor appears in edit mode in assignments. To preview the embedded media you will need to select the preview button on the assignment page.
          </p>
        </td>
      </tr>
    </tbody>
  </table>