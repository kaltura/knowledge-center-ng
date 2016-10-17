---
layout: page
title: "Kaltura Interactive Video Quizzes Administrator's Guide"
date: 2016-01-21 15:58:34
---

<h2>
    <a name="verify_quiz"></a>Activating the Kaltura Interactive Video Quiz Feature in Kaltura MediaSpace or in your KAF Instance
  </h2>
  
  <p>
    Kaltura Interactive Video Quizzes are managed by Kaltura MediaSpace system administrators in the Admin area accessed from <Base_URL>/admin. Kaltura Interactive Video Quizzes (IVQ) can also be enabled via the KAF admin console in the same manner. If you do not see the Quiz module, contact your account manager.
  </p>
  
  <p>
    The following tasks are described:
  </p>
  
  <ul>
    <li>
      <a href="#cfg_quiz">Configure the Quiz Module</a>
    </li>
    <li>
      <a href="#verify_IVQ">Verify that Interactive Video Quizzes are Activated</a>
    </li>
  </ul>
  
  <h2>
    <a name="cfg_quiz"></a>Configure the Quiz Module in KMS or in the KAF Instance
  </h2>
  
  <p>
    The configuration page dedicated to Interactive Video Quizzes is accessed from the <strong>Configuration Management</strong> page from the menu on the right under the category, Modules Custom/Core/entryTypes.
  </p>
  
  <p class="mce-procedure">
    <strong>To configure the Quiz module in KMS or in the KAF Admin Console</strong>
  </p>
  
  <ol>
    <li>
      Login to Kaltura MediaSpace or the KAF Admin Console and go to the Configuration Management window.
    </li>
    <li>
      Scroll down and click the Quiz module in the Modules/Custom/core section.<span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb"><br /><img src="../../assets/2951.img">
    </li>
    <li>
      <span class="inline-comment-marker valid" data-ref="6781e562-ffd5-40da-9f18-a3863046f3fb">In the Enabled field, select Yes to enable the Kwebcast module.<br /><img src="../../assets/2952.img">
    </li>
    <li>
      You can leave all other parameter values as they are or enter values for the relevant fields and click Save. <br /><br /><table style="width: 650px;" border="0" cellspacing="0" cellpadding="0">
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
                Enable the Quiz module.
              </p>
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                <span>quizPlayerId</span> 
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <span>What is the player ID (uiConf ID) of the player that plays quizzes?</span> 
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                 <span>playerBarHeightPixels</span>
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <span>The height (in pixels) of the player ui which is not part of the actual video (for example - the bottom bar). Leave blank to use the default player value.</span> 
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                 <span>playerVideoRatioPercent</span>
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <span>The ratio (in percent) of the video inside the player. Standard values: 16:9 = 56.25 , 4:3 = 75 , 16:10 = 62.5. Leave blank to use the default player value.</span> 
            </td>
          </tr>
          
          <tr>
            <td style="text-align: left;" valign="bottom" width="31%">
              <p>
                 <span>BSEPlayerId</span>
              </p>
            </td>
            
            <td style="text-align: left;" valign="bottom" width="68%">
              <span>What is the player ID (uiConf ID) of the player that used to play quizzes in BSE? Uiconf should have the infoScreen plugin enabled</span> 
            </td>
          </tr>
        </tbody>
      </table>
      
      <p>
        <a href="#top">Back to Top</a>
      </p>
    </li>
  </ol>
  
  <h2>
    <strong><a name="verify_IVQ"></a>Verify that you have activated the Interactive Video Quizzes Feature in KMS or in your KAF instance</strong>
  </h2>
  
  <p>
    <strong class="mce-procedure">To verify that you can create a quiz</strong><a href="https://kaltura.sharepoint.com/community-team/Shared%20Documents/Knowledge%20Management/Work%20in%20Progress/Kaltura%20Webcasting/Setup/Kaltura_Webcasting_Admin_Guide_KC.docx#_msocom_1"><br /></a>
  </p>
  
  <ol start="1">
    <li>
      Login to Kaltura MediaSpace or your KAF instance.
    </li>
    <li>
      Select Add New. <br />Quiz should display as one of the Add New options.<br /><img src="../../assets/2953.img">
    </li>
  </ol>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <p class="mce-note-graphic">
    Be certain to activate the Userreports module in KMS or in your KAF instance to ensure that you can display the IVQ analytics.
  </p>