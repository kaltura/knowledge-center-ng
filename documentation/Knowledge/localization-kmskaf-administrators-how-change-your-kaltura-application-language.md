---
layout: page
title: "Localization for KMS/KAF Administrators - How to Change Your Kaltura Application Language?"
date: 2016-04-18 16:03:57
---

<p>
    <a name="top"></a>To help ensure a quality user experience, Kaltura MediaSpace and KAF applications provide localization configuration to adapt online content for regional specificity. Using the <em>Application</em> and <em>Languages</em> modules in the Kaltura MediaSpace Admin Console and the <em>Languages</em> module in the KAF Admin Console, the KMS/KAF admin can control the MediaSpace/KAF instance localization features.<span><a name="top"></a></span>
  </p>
  
  <h3>
    KMS
  </h3>
  
  <p class="mce-procedure">
     To configure the KMS language
  </p>
  
  <ol>
    <li>
      Login to MediaSpace Admin Console
    </li>
    <li>
      Select the <em>Application</em> module in the Global section.
    </li>
    <li>
      Set the following:<br /><br /><ul>
        <li>
          <em>languageConfiguration</em> – Set the instance configuration: multi-language instance or single language instance.
        </li>
        <li>
          <em>languageSelection</em> - Choose the default language for a new user in this specific instance.<br /><br /><img src="{{site.url}}/assets/3145">
        </li>
      </ul>
    </li>
    
    <li>
      When the instance is configured to Multi-language, select the languages available from the <em>languageSelection</em> field.
    </li>
  </ol>
  
  <p style="padding-left: 60px;">
    <img src="{{site.url}}/assets/3225">
  </p>
  
  <p>
    The available languages in the <em>languageSelection</em> field are built from the out-of-the-box Kaltura languages in addition to custom languages that were created by the admin previously.
  </p>
  
  <h3>
    <a name="customizing"></a>Customizing Languages for a KMS or KAF Instance
  </h3>
  
  <p>
    Use the <em>Languages</em> module in the KMS Management Console or the KAF Admin Console to create a custom language or change text in an available language. For KAF: Follow the <a href="#kaf_specific">KAF Specific Instructions</a> in addition to the customizing instuctions that follow.
  </p>
  
  <p>
    <span></span>You will need to download the existing application text file and then upload the new/modified file.
  </p>
  
  <p class="mce-procedure">
    To download language texts
  </p>
  
  <ol>
    <li>
      Select the <em>Languages</em> module in the Global section.
    </li>
    <li>
      In the <em>DownloadLocaleText field,</em>click Download Texts to download the latest texts of KMS. <br /><p>
        <img src="{{site.url}}/assets/3096">
      </p>
      
      <p>
        <img src="{{site.url}}/assets/3098">
      </p>
      
      <p>
        <img src="{{site.url}}/assets/3226">
      </p>
    </li>
    
    <li>
      <p>
        Select the desired language and modify the text as necessary. You can use translation editors available on the web,  for example, <a href="https://poedit.net/" target="_blank">poedit</a>, to modify text. The final result should be a binary .mo file.
      </p>
    </li>
  </ol>
  
  <p class="mce-procedure">
    <span>To upload language texts</span>
  </p>
  
  <ol>
    <li>
      <span style="line-height: 16px; background-color: initial;">Select the </span><em style="font-weight: bold; line-height: 16px; background-color: initial;">Languages</em><span style="line-height: 16px; background-color: initial;"> module in the Global section.</span>
    </li>
    <li>
      <span style="line-height: 16px; background-color: initial;"></span>Click +Add UpdateCustom Language to upload the new/modified texts for KMS or your KAF instance (a binary .mo file).<br /><br /><img src="{{site.url}}/assets/3103">
    </li>
    <li>
      Configure the following fields to upload the custom Language and click Save.<br /><table style="width: 630px;" border="1" cellspacing="0" cellpadding="0" align="left">
        <thead>
          <tr>
            <td valign="top" width="31%">
              <p class="TableHeading">
                <strong>Field</strong>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableHeading">
                <strong>Description</strong>
              </p>
            </td>
          </tr>
        </thead>
        
        <tbody>
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                <em>languageAdminName</em>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Enter the name of the language to be presented in the language drop down list (for the admin), in <em>Application</em> module, <em>languageSelection</em> and <em>language</em> fields.
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                <em>languageClientName </em>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Enter the name of the language to be presented in the language drop down list for the users.
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                <em>languageCode</em>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                For KAF only: Select the formal language code to be used to sync the instance language to the hosting application (LMS,CMS, SBS) chosen language.
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                <em>localeFile</em>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Click upload locale. Upload your customized .mo file.In order to convert your customized .po file to an.mp file you can use some available tools on the web.
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                <em>localeIcon</em>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Click upload flag. Upload a custom language flag icon to be presented to the users. The icon should be in *.jpg;*.jpeg;*.bmp;*.png;*.gif;*.tif;*.tiff;*.ico format and the dimensions should be 30px X 26px (The application will resize any given image, however for the best visual result, use these dimensions). You can also choose from this library of icons: <a href="http://freebiesbug.com/psd-freebies/100-flat-flag-psd-icons/">http://freebiesbug.com/psd-freebies/100-flat-flag-psd-icons/</a>
              </p>
            </td>
          </tr>
          
          <tr>
            <td valign="top" width="31%">
              <p class="TableBodyText">
                <em>languageId</em>
              </p>
            </td>
            
            <td valign="top" width="68%">
              <p class="TableBodyText">
                Unique language id for application usage (not for KMS/KAF admin usage).
              </p>
            </td>
          </tr>
        </tbody>
      </table>
    </li>
  </ol>
  
  <p style="text-align: left;">
     
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
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <h3>
    <strong><a name="kaf_specific"></a>KAF Specific Information</strong>
  </h3>
  
  <p>
    When the instance is from a KAF-based LMS Extension (specifically - Sakai, Blackboard, Canvas, Brightspace, Moodle to follow in the future) the following is relevant:
  </p>
  
  <ul>
    <li>
      The Kaltura instance (the Kaltura screens) receive the language settings from the hosting application (Sakai, Blackboard, Canvas, Brightspace) – whether created or added by the application admin or the user.
    </li>
    <li>
      <p>
        Custom languages may be added as described in the <a href="#customizing">Customizing Languages for a KMS or KAF Instance</a> section in this article.
      </p>
    </li>
    
    <li>
      The <em>languageCode</em> field is a for KAF use only. The KAF admin should set it for a custom language. This field is used to sync the instance language to the hosting application chosen language. The <em>languageCode</em> of a custom language takes precedence over the Kaltura default language with the same code.
    </li>
  </ul>