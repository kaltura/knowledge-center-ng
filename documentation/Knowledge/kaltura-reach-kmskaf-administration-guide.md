---
layout: page
title: "Kaltura REACH KMS/KAF Administration Guide"
date: 2016-02-09 13:50:42
---

<h2 id="KalturaWebcastingAdministration-ActivatingtheKalturaWebcastingFeatureinKalturaMediaSpace">
    Activating Kaltura REACH in Kaltura MediaSpace or in your KAF Instance
  </h2>
  
  <p>
    The REACH module in KMS/KAF, allows users to have access to a full suite of workflows (fidelity, turnaround time, foreign transcription/translation) directly in the Kaltura platform. These workflows are completely customizable within the plugin and control of completed caption access, caption requests, and caption moderation can be granted on a user-to-user basis.
  </p>
  
  <p>
    You must have a provisioned REACH module before use. For information about getting your account setup see <a href="{{site.url}}/documentation/Knowledge/kaltura-reach-setup-and-walkthrough-guide.html" target="_blank">here</a>.
  </p>
  
  <p>
    The following tasks are described:
  </p>
  
  <ul>
    <li>
      <a href="http://knowledge.kaltura.com/node/1531/revisions/7672/view#events"></a><a href="#configure_reach">Configure the REACH Module</a>
    </li>
    <li>
      <a href="#verify">Verify that REACH is Activated</a>
    </li>
  </ul>
  
  <h2>
    <a name="configure_reach"></a>Configure the REACH Module in KMS or in the KAF Instance
  </h2>
  
  <p>
    The configuration page dedicated to REACH is accessed from the <strong>Configuration Management</strong> page under the category, Modules.
  </p>
  
  <p class="mce-procedure">
    <strong>To configure the REACH module in KMS or in the KAF Admin Console</strong>
  </p>
  
  <ol>
    <li>
      Login to Kaltura MediaSpace or the KAF Admin Console and go to the Configuration Management window.
    </li>
    <li>
      Scroll down and click the REACH module in the Modules section.<br /><img src="../../assets/3487.img">
    </li>
    <li>
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb">In the Enabled field, select Yes to enable the module.<br /><img src="../../assets/3037.img">
    </li>
    <li>
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb">Enter values for the relevant fields and click Save. <br /><br /></span></span><div align="center">
        <table border="1" cellspacing="0" cellpadding="0" align="left">
          <tbody>
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  <strong>Field</strong>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  <strong>Definition</strong>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  <strong>Description</strong>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  <strong>Variable</strong>
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  userName
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  The username of your cielo24 account.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  This is provided directly from cielo24 or provisioned through “<a href="{{site.url}}/documentation/Knowledge/kaltura-reach-setup-and-walkthrough-guide.html">auto-provisioning</a>”.  If you do not have a username or password, please reach out to your Kaltura rep or cielo24 at <a href="mailto:sales@cielo24.com">sales@cielo24.com</a>.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  <a name="pwd"></a>password
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  The password of your cielo24 account. 
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  This will be provided along with the cielo24 username. If you are using an apiKey, you do not require a password.  Please see userName description for details around procuring a password.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  apiKey
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  API Key for secure (instead of password)
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  This is used as an alternative to the <a href="#pwd">password</a>.  Also provided by cielo24.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  serverUrl
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  cielo24 Server URL.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  <a href="https://api.cielo24.com">https://api.cielo24.com</a>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  https://api.cielo24.com
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  logo
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  cielo24 Logo
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Hide or show the cielo24 logo on Order Captions screen.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Show
                </p>
                
                <p>
                  Hide
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  orderCaptionScreenText
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Display info text on Order Caption screen.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  There is a100 character limit. This feature can be used to communicate simple messages to users on the order captions panel, typically instructive or descriptive.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  AllowOrdering
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Select User Roles to set who is able to request captions.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Users who are logged in with an enabled permission role, will have the “Order Captions” button available.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  allowOrderingSpeakerName
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Select User Roles to enable adding speaker identification.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Users who are logged in with an enabled permission role, will to add Speaker name identification to caption order requests
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  requireRequestsAuthorization
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  If enabled, caption requests must be approved before processing. 
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Captions submissions are not sent into moderation prior to processing. The request will require “Approval” or “Rejection” from an administrator role.  While approving the request, the moderator also has the capability to adjust request parameters for fidelity and turnaround time prior to approving.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Yes
                </p>
                
                <p>
                  No
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  requireAuthMechanicalFidelity
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  If enabled, mechanical caption requests must be approved before processing begins.
                </p>
                
                <p>
                   
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  If disabled and requireRequestsAuthorization is enabled, mechanical caption requests will be processed automatically without approval. <span>If enabled, Mechanical caption requests must also be authorized by user.</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Yes
                </p>
                
                <p>
                  No
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  allowAuthorize
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  <span>User Roles selected will be able to authorize and delete caption requests.  </span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  This setting is tied directly to requireRequestsAuthorization and requireAuthMechanicalFidelity configurations.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  <span>receieveAuthNotificationEmail</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  <span>Email addresses added to this field will receive a notification about caption requests pending authorization (if authorization is enabled).</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Users can add specific email addresses by clicking “Add recieveAuthNotificationEmail” and inputting email addresses to receive an email notification when caption requests are pending authorization.
                </p>
                
                <p>
                  To remove an email address select “Delete”.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                 
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  allowEdit
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Users enabled will be able to edit completed captions using the Customer Edit Tool.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  For permitted User Roles ‘Edit Captions’ will be available from the ‘Actions’ drop down of the media entry. Please find instructions for using the customer edit tool <a href="https://www.youtube.com/watch?v=tAMEvawJ5sk&feature=youtu.be">here</a>.
                </p>
                
                <p>
                   
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  allowView
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  <span>User Roles selected will be able to view all caption requests for an entry.</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  For permitted User Roles ‘View Captions’ will be available from the ‘Actions’ drop down of the media entry.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  language
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Language set will be the default language for all caption requests.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                   
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  languageOverride
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  <span>User Roles selected will be allowed to adjust the source language of caption requests.</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  This provides the ability for users to select native foreign language processing i.e. (Spanish audio into Spanish captions/transcripts)
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  additionalLanguage
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  <span>User Roles selected will be allowed to request foreign language translation when ordering captions.  </span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  cielo24 supports English into 15 supported languages, as well any of the listed languages into English. Custom translation will need to be requested directly from cielo24 by contacting <a href="mailto:support@cielo24.com">support@cielo24.com</a>. Translation requests will automatically perform native transcription first, and then translation from native transcription to requested language. For example, if ‘Request Foreign Language Translation’ is enabled and you select a language to translate (e.g. Source Media Language = English and Target Translation Language = Hebrew) the request will process in two parts automatically A) Native Transcription (return English captions) B) Foreign Translation (return Hebrew captions).
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  fidelity
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Set value is default fidelity for caption requests.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Choose the default accuracy options (Professional, Premium, Mechanical)
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Professional (99%)
                </p>
                
                <p>
                  Premium (94 to 96%)
                </p>
                
                <p>
                  Mechanical (70 to 80%)
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  fidelityOverride
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Select User Roles enabled to change the requested fidelity of caption requests.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Allows users to select the various accuracy options (Professional, Premium, Mechanical)
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  fidelityChoices
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Enabled options will be available fidelity choices when ordering captions.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Configures the fidelity options permitted users are able to choose from when selecting  accuracy levels.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Professional (99%)
                </p>
                
                <p>
                  Premium (94 to 96%)
                </p>
                
                <p>
                  Mechanical (70 to 80%)
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  turnaroundTime
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Default value for turnaround time of caption requests.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Choose the default turnaround time for English transcription requests.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Standard (7 days)
                </p>
                
                <p>
                  Standard (48 hours)
                </p>
                
                <p>
                  Priority (24 hours)
                </p>
                
                <p>
                  Critical (6 hours)
                </p>
                
                <p>
                  Critical (3 hours)
                </p>
                
                <p>
                  Custom
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  turnaroundTimeChoices
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Enabled options will be available turnaround time choices when ordering caption.s
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Configures the turnaround options permitted users are able to choose from when changing processing times.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Standard (7 days)
                </p>
                
                <p>
                  Standard (48 hours)
                </p>
                
                <p>
                  Priority (24 hours)
                </p>
                
                <p>
                  Critical (6 hours)
                </p>
                
                <p>
                  Critical (3 hours)
                </p>
                
                <p>
                  Custom
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  turnaroundTimeOverride
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Select User Roles enabled to choose turnaround time value when ordering captions.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Allows users to select the various turnaround options (24 hours, 48 hours, 7 days, etc.)
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  format
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  File format of returned caption file to KMC.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Default is DFXP.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  DFXP
                </p>
                
                <p>
                  SRT
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  showMediaDataAsTags
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Allow media data to appear as tags on entries that have been processed
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  cielo24 provides media data (keywords, topic, entities, speaker names, etc.) about a given media file. By enabling this setting these outputs are displayed at Tags.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  progressiveReturn
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Select User Roles enabled to set progressive return
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  <a name="prog_return"></a>Progressive return is the interim delivery of all three fidelities (accuracies) cielo24 provides.  Media will initially be processed at the Machine output and data will be populated within Mechanical SLA, followed by the Premium fidelity, ending in the Professional quality.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  progressiveReturnDefault
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  If enabled, progressive return will be turned on my default
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Videos selected at Professional fidelity will be processed with Progressive Return (see <a href="#prog_return">progressiveReturn </a>) workflow by default.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Yes
                </p>
                
                <p>
                  No
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  allowNotes
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  <span>User Roles selected are enabled to add special notes to transcriptionists when ordering captions for a specific entry.</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Notes serve as a resource for cielo24’s transcription team to aid with difficult technical terminology, domain information, and names.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  glossary
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  This text will be shown as notes to transcriptionists for ALL caption requests from your account.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  Glossaries can be added on an account level to provide a rolodex of terminology, genres, names, etc  to cielo24’s transcription team.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  cielo24ProfileId
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  Custom metadata profile ID for cielo24.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  This will be set automatically when the plugin is enabled.
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                   
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <p>
                  <span>privateCustomerEditTool</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <p>
                  <span>Allows user to set the Customer Edit link for captions to private so only authenticated users can access the edit tool.</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <p>
                  <span>If enabled, Customer Edit links will only be accessible in KMS. If set to ‘No” then the Customer Edit link can be shared publicly and accessed without authentication.</span>
                </p>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                <p>
                  Yes 
                </p>
                
                <p>
                  No
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" valign="top" width="172">
                <span>publicCustomerEditLifetime</span>
              </td>
              
              <td style="text-align: left;" valign="top" width="263">
                <span>Allows user to specify amount of minutes before the Public Customer Edit link URL expires,</span>
              </td>
              
              <td style="text-align: left;" valign="top" width="179">
                <span>Public links to the Customer Edit Tool for captions will expire after the specified amount of minutes. Leave blank if you would like the Customer Edit link URL to never expire.</span>
              </td>
              
              <td style="text-align: left;" valign="top" width="113">
                 
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
      
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"></span></span><p>
         
      </p>
    </li>
  </ol>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
    <a href="http://knowledge.kaltura.com/node/1531/revisions/7672/top">Back to Top</a>
  </p>
  
  <h2>
    <strong><a name="verify"></a>Verify that you have activated the REACH Feature in KMS or in your KAF instance</strong>
  </h2>
  
  <p>
    <strong class="mce-procedure">To verify that you can order captions</strong><a href="https://kaltura.sharepoint.com/community-team/Shared%20Documents/Knowledge%20Management/Work%20in%20Progress/Kaltura%20Webcasting/Setup/Kaltura_Webcasting_Admin_Guide_KC.docx#_msocom_1"><br /></a>
  </p>
  
  <ol start="1">
    <li>
      Login to Kaltura MediaSpace or your KAF instance.
    </li>
    <li>
      Select a video and click Edit. <br />The Order Captions should appear in the Actions drop down menu.<br /><img src="../../assets/3031.img">
    </li>
  </ol>
  
  <p>
    <a href="http://knowledge.kaltura.com/node/1531/revisions/7672/top">Back to Top</a>
  </p>