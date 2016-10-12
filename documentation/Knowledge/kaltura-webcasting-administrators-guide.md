---
layout: page
title: "Kaltura Webcasting Administrator's Guide"
date: 2015-10-25 01:00:47
---

<h2 id="KalturaWebcastingAdministration-ActivatingtheKalturaWebcastingFeatureinKalturaMediaSpace">
    <a name="top"></a>Activating the Kaltura Webcasting Feature in Kaltura MediaSpace or in your KAF Instance
  </h2>
  
  <p>
    Kaltura Webcasting is managed by Kaltura MediaSpace system administrators in the Admin area accessed from <Base_URL>/admin. Kaltura Webcasting can also be enabled via the KAF admin console in the same manner. If you do not see the kWebcast module, contact your account manager.
  </p>
  
  <p class="mce-note-graphic">
    Before activating the kWebcast Module be certain that the Events Module is active and that the LiveEntry module is disabled.
  </p>
  
  <p>
    The following tasks are described:
  </p>
  
  <ul>
    <li>
      <a href="#events">Configure the Kaltura Events Module</a>
    </li>
    <li>
      <a href="#events"></a><a href="#kwebcast">Configure the Kwebcast Module</a>
    </li>
    <li>
      <a href="#verify">Verify that Webcasting is Activated</a>
    </li>
  </ul>
  
  <h2>
    <a name="events"></a>Configure the Kaltura Events Module in KMS or in the KAF Instance
  </h2>
  
  <p>
    The events module allows you to add the events date for scheduling and timing webcasts.
  </p>
  
  <p class="Procedure mce-procedure">
    To configure the Events module in KMS and in the KAF Admin Console
  </p>
  
  <ol>
    <li>
      Go to the Kaltura MediaSpace Configuration Management window or the KAF Admin Console and go to the Configuration Management window.
    </li>
    <li>
      Select the Events module in the Modules/Custom/core section.<br /><img src="{{site.url}}/assets/2897">
    </li>
    <li>
      Select Yes to enable the module.<br /><table border="1" cellspacing="0" cellpadding="0">
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
                Enable the Events module.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
    </li>
    
    <li>
      Click Save. 
    </li>
  </ol>
  
  <p>
    <a href="top">Back to Top</a>
  </p>
  
  <h2>
    <a name="kwebcast"></a>Configure the Kwebcast Module in KMS or in the KAF Instance
  </h2>
  
  <p>
    The configuration page dedicated to Webcasting is accessed from the <strong>Configuration Management</strong> page from the menu on the right under the category, <strong>Modules<span class="inline-comment-marker" data-ref="b32ef097-97de-4032-9795-c3fa7d924cda">C</span>ustom/core</strong> sub-category <strong>Kwebc</strong><strong>ast</strong>.
  </p>
  
  <p class="mce-procedure">
    <strong>To configure the Kwebcast module in KMS or in the KAF Admin Console</strong>
  </p>
  
  <ol>
    <li>
      Login to Kaltura MediaSpace or the KAF Admin Console and go to the Configuration Management window.
    </li>
    <li>
      Scroll down and click the <strong>Kwebcast</strong> module in the ModulesCustom/core section.<span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><br /><img src="{{site.url}}/assets/2983">
    </li>
    <li>
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb">In the Enabled field, select Yes to enable the Kwebcast module.<br /><img src="{{site.url}}/assets/2500">
    </li>
    <li>
      Select or enter values for the relevant fields and click Save.<br /><table style="width: 640px;" border="0" cellspacing="0" cellpadding="0">
        <thead>
          <tr>
            <td valign="bottom" width="31%">
              <p>
                <strong>Field</strong>
              </p>
            </td>
            
            <td valign="bottom" width="68%">
              <p>
                <strong>Description</strong>
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                enabled
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                Enable the Kwebcast module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                applicationName
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                Define the applicationName.  This configuration value is passed to the webcast application.  If left empty the default value is used.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                applicationLogoUrl
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                Define the applicationLogoUrl. Provide the URL to a logo image which is passed to the webcast application. If left empty the default logo is used.   
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                transcodingProfile
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p class="TableBodyText">
                This list of transcoding profiles is taken from the Kaltura Management Console and is based on the available transcoding profiles there. The transcoding profile is applied to all webcast events created after this field is set (You cannot change previous entries’ transcoding profiles here. See the article <a href="http://knowledge.kaltura.com/node/1499">Adaptive Bit Rate Settings</a> for more information.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                liveBroadcasterRole
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                Limit Webcast Event creation to a certain user or user role. If a role is selected, any role with higher permissions than the role selected will be allowed to create Webcast Events.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                WinProducerAppUiConfID
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                This value is automatically assigned by the system upon save. ID of the UIConf for the Windows Kwebcast application.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                MacProducerAppUiConfID
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                This value is automatically assigned by the system upon save.This is the ID of the UIConf for the Mac Kwebcast application
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                SupportSelfServe
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                Determine whether to allow self-serve scenario. This field is a beta feature and should be turned off to no.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                PlayerUiconfId
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                This value is automatically assigned by the system upon save. This is the UIConf for the player used for Webcasting events.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                BSEPlayerUIConfID
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                This value is automatically assigned by the system upon save. ID of the UIConf for the BSE Kwebcast player. This field is only relevant for KAF administrators. See the article <a href="http://knowledge.kaltura.com/node/1272">New Browse Search and Embed (BSE) Layout</a> for more information.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                <a name="enable_qna"></a>EnableQnA
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <p>
                Enable or disable running moderated Q&A sessions during live webcasts. 
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <p>
         
      </p>
    </li>
  </ol>
  
  <p>
    <a href="top">Back to Top</a>
  </p>
  
  <h2>
    <strong><a name="verify"></a>Verify that you have activated the Kaltura Webcasting Feature in KMS or in your KAF instance</strong>
  </h2>
  
  <p class="mce-note-graphic">
    Be certain that you have included yourself in the Webcasting permissions to verify that the module is enabled.
  </p>
  
  <p>
    <strong class="mce-procedure">To verify that you can create a webcast event</strong><a href="https://kaltura.sharepoint.com/community-team/Shared%20Documents/Knowledge%20Management/Work%20in%20Progress/Kaltura%20Webcasting/Setup/Kaltura_Webcasting_Admin_Guide_KC.docx#_msocom_1"><br /></a>
  </p>
  
  <ol start="1">
    <li>
      Login to Kaltura MediaSpace or your KAF based application.
    </li>
    <li>
      Select Add New. <br />Webcast Event should display as one of the Add New options.<br /><img src="{{site.url}}/assets/2938">
    </li>
  </ol>
  
  <p>
    <a href="top">Back to Top</a>
  </p>