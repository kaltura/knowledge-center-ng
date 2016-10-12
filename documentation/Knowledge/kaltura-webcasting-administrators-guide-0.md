---
layout: page
title: "Kaltura Webcasting - Administrator's Setup Guide"
date: 2015-01-09 01:07:28
---

<p class="mce-heading-2">
  Introduction to Kaltura Webcasting
</p>

<span style="font-family: verdana, geneva; color: #003366;"></span>Kaltura Webcasting is fully integrated with the user's video portal. It supports internal delivery, ingestion from different encoders and source types, archiving of webcasts to your VOD portal and enhanced interactive features. Kaltura’s Webcasting solution allows you to optimize internal communication and increase return on investment for customer facing communications. Kaltura’s Webcasting is delivered behind the firewall and public internet and offers security and flawless playback as well as unicast and multicast streaming.

<h2 id="KalturaWebcastingAdministration-ActivatingtheKalturaWebcastingFeatureinKalturaMediaSpace">
  Activating the Kaltura Webcasting Feature in Kaltura MediaSpace
</h2>

Kaltura Webcasting is managed by Kaltura MediaSpace system administrators in the Admin area accessed from <Base_URL>/admin.

Before activating the Webcasting Module, be certain that the Events Module is enabLed and that the LiveEntry module is disabled.

<p class="mce-heading-3">
  Configure Kaltura Webcasting (Kwebcast Module) in Kaltura MediaSpace
</p>

<p class="mce-procedure">
  To configure the Kwebcast module in KMS
</p>

1.  Login to Kaltura MediaSpace and go to the Kaltura MediaSpace Configuration Management window.
2.  Scroll down and select the Kwebcast module in the Modules/Custom/core section,  
    <img src="{{site.url}}/assets/2412">
    The Webcasting Administration <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb">page is displayed.</span>  
      
    
3.  In the Enabled field, select Yes to enable the Kwebcast module.  
    <img src="{{site.url}}/assets/2413">
4.  <span style="font-family: verdana, geneva; color: #888888;"><span style="font-family: verdana, geneva; color: #888888;">Select or enter values for the relevant fields and click Save.<br /></span></span><table style="width: 100%;" border="1" cellspacing="0" cellpadding="0">
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
              Enable the Kwebcast module.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              applicationName
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              Define the applicationName. This configuration value is passed to the webcast application.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              applicationLogoUrl
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              Define the applicationLogoUrl. Provide the URL to a logo image which is passed to the webcast application.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              multicastStreaming
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              Allow or disallow multicast streaming. Use multicast streaming for Webcast Events (if DVR is enabled, it will be disabled in runtime).
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              transcodingProfile
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              Set the transcodingProfile to Passthrough or Cloud transcode for Webcast Events. This is done to choose the live event's transcoding profile based on the partner IDs and according to your required setup. The transcoding profile selected will be applied to all Webcasting events.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              liveBroadcasterRole
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              Limit Webcast Event creation to a certain user or user role. If a role is selected, any role above the role selected will be allowed to create Webcast Events.
            </p>
            
            <p class="TableBodyText">
               
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              WinProducerAppUiConfID
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              This value is automatically assigned by the system upon save. ID of the UIConf for the Windows Kwebcast application
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              MacProducerAppUiConfID
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              This value is automatically assigned by the system upon save. ID of the UIConf for the Mac Kwebcast application
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              SupportSelfServe
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              Whether to allow self-serve scenario (currently, this feature is not fully supported)
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              PlayerUiconfId
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              This value is automatically assigned by the system upon save. ID of the UIConf for the Kwebcast player
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              BSEPlayerUIConfID
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              This value is automatically assigned by the system upon save. ID of the UIConf for the BSE Kwebcast player
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="31%">
            <p class="TableBodyText">
              EnableQnA
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="68%">
            <p class="TableBodyText">
              Allow or disallow the ability to run QnA sessions during live webcasts. 
            </p>
          </td>
        </tr>
      </tbody>
    </table>

<p id="KalturaWebCasting-LoginintotheKMS" class="mce-heading-3">
  Verify that you have activated the Kaltura Webcasting feature in KMS 
</p>

<p class="mce-procedure">
  <span style="font-family: verdana, geneva; color: #888888;">To verify that you can create a webcast event</span>
</p>

1.  <span style="color: #888888; font-family: verdana, geneva;">Login to Kaltura MediaSpace.</span>
2.  <span style="color: #888888; font-family: verdana, geneva;">Select Add New > Webcast Event should display as one of the Add New options.</span>