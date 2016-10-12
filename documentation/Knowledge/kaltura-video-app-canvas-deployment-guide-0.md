---
layout: page
title: "Kaltura Video App for Canvas Deployment Guide"
date: 2015-12-31 12:39:58
---

<div class="WordSection1">
    <p>
      <a name="top"></a>The following topics are described:
    </p>
    
    <ul>
      <li>
        <a href="#about">About this Guide</a>
      </li>
      <li>
        <a href="#audience">Audience</a>
      </li>
      <li>
        <a href="#overview">Kaltura Video App for Canvas Installation Overview and Requirements</a>
      </li>
      <ul>
        <li>
          <a href="#prereq">Prerequisites</a>
        </li>
      </ul>
      
      <li>
        <a href="#instructions">Kaltura Video App for Canvas Deployment Instructions</a>
      </li>
      <ul>
        <li>
          <a href="#deploying_mymedia">Deploying My Media</a>
        </li>
        <li>
          <a href="#deploying_mymedia"></a><a href="#text-editor">Deploying the Media Gallery and the Embed Kaltura Video Text-Editor Button</a>
        </li>
      </ul>
      
      <li>
        <a href="#samples">Kaltura Video App for Canvas Sample Configuration Files (XMLs)</a>
      </li>
      <ul>
        <li>
          <a href="#MyMedia.xml">MyMedia.xml</a>
        </li>
        <li>
          <a href="#MediaGalleryAndBSE.xml">MediaGalleryAndBSE.xml</a>
        </li>
      </ul>
    </ul>
  </div>
  
  <div class="WordSection2">
    <h3>
      <span style="font-size: 1.5em;"><a name="about"></a>About this Guide</span>
    </h3>
    
    <p>
      This guide describes how to add the Kaltura Video App for Canvas to your Instructure Canvas environment.
    </p>
    
    <p class="Note mce-note-graphic">
      Please refer to the official and latest product release notes for last-minute updates. Technical support may be obtained directly from: <a href="mailto:customercare@kaltura.com">Kaltura Customer Care</a>. 
    </p>
    
    <p>
      <strong>Contact Us</strong>: Please send your documentation-related comments and feedback or report mistakes to <a href="mailto:knowledge@kaltura.com">knowledge@kaltura.com</a>. We are committed to improving our documentation and your feedback is important to us.
    </p>
    
    <h2>
      <a name="audience"></a>Audience
    </h2>
    
    <p>
      This guide is intended for Canvas and Kaltura administrators.
    </p>
  </div>
  
  <div class="WordSection3">
    <h1>
      <a name="overview"></a>Kaltura Video App for Canvas Installation Overview and Requirements
    </h1>
    
    <p>
      The Kaltura Video App for Canvas is implemented as a Canvas External Tool and is added manually by a Canvas administrator. Please refer to the <a href="http://guides.instructure.com/s/2204/m/4152/l/57103-how-do-i-manually-configure-an-external-app-for-a-course">Canvas Instructor Guide</a> on how to manually configure an external tool on your Canvas environment.
    </p>
    
    <h2>
      <a name="prereq"></a>Prerequisites
    </h2>
    
    <ul>
      <li>
        <strong>A Kaltura account</strong>:<ul>
          <li>
            Partner id (PID) and Admin Secret for your Kaltura account. Alternatively, you can find this information in KMC under <em>Settings </em><em>à</em><em> Integration Settings</em>.
          </li>
          <li>
            A Kaltura Application Framework instance URL, for example, 12345678.kaf.kaltura.com
          </li>
          <li>
            <strong>App configuration files (xmls)</strong>: The deployment process requires the following two configuration files for your Kaltura Video App for Canvas:
          </li>
          <li>
            MyMedia.xml
          </li>
          <li>
            MediaGalleryAndBSE.xml
          </li>
        </ul>
      </li>
    </ul>
    
    <p>
      This configuration files are used to connect your Canvas environment to your Kaltura account and Kaltura Application Framework (KAF) instance. To create these xml files go to the following URL with your KAF instance: http://123456.kaf.kaltura.com/canvas/config/create-xml-for-instance.
    </p>
    
    <p>
      <a href="#top">Back to top</a>
    </p>
  </div>
  
  <p class="WordSection4">
     
  </p>
  
  <h1>
    <a name="instructions"></a>Kaltura Video App for Canvas Deployment Instructions
  </h1>
  
  <p>
    This section describes how to deploy the Kaltura Video App for Canvas.
  </p>
  
  <h2>
    <a name="deploying_mymedia"></a>Deploying My Media
  </h2>
  
  <p class="Procedure mce-procedure">
    To deploy My Media
  </p>
  
  <ol>
    <li>
      In your Canvas environment, go to <strong>Settings</strong> and click <strong>Apps</strong>:<br /><img src="{{site.url}}/assets/2761">
    </li>
    <li>
      Click <strong>View App Configurations</strong> to open the list of external apps:<br /><img src="{{site.url}}/assets/2763">
    </li>
    <li>
      Click Add New App to open the Edit External Tool Dialog.
    </li>
    <li>
      In the Edit External Tool Dialog, under <strong>Configuration Type</strong> Select “Paste XML”.
    </li>
    <li>
      Enter the following information:<br /><table border="1" cellspacing="0" cellpadding="0">
        <tbody>
          <tr>
            <td width="54">
              <p class="TableHeading">
                #
              </p>
            </td>
            
            <td width="120">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td width="375">
              <p class="TableHeading">
                Value
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                1
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Name
              </p>
            </td>
            
            <td width="375">
              <p class="TableBodyText">
                Name (only affects the list of installed tools)
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                2
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Consumer Key
              </p>
            </td>
            
            <td width="375">
              <p class="TableBodyText">
                You Kaltura account Partner Id
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                3
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Shared Secret
              </p>
            </td>
            
            <td width="375">
              <p class="TableBodyText">
                Your account administrator secret
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                4
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Paste XML Here
              </p>
            </td>
            
            <td width="375">
              <p class="TableBodyText">
                Paste the content of MyMedia.xml provided to you by your Kaltura representative.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <br /><div align="center">
         
      </div>
    </li>
    
    <li>
      Click <strong>Submit</strong>. The My Media tool will be listed in the list of external tools and a new navigation menu item will be added to the course menu.<br /><img src="{{site.url}}/assets/2764">
    </li>
  </ol>
  
  <p style="padding-left: 60px;">
    <img src="{{site.url}}/assets/2765">
  </p>
  
  <p align="center">
     
  </p>
  
  <h2>
    <a name="text-editor"></a>Deploying the Media Gallery and the Embed Kaltura Video Text-Editor Button
  </h2>
  
  <p class="Procedure mce-procedure">
    To deploy the Media Gallery – There are two options:
  </p>
  
  <p>
    <strong><span style="font-size: 10px;">Option 1:</span></strong>
  </p>
  
  <ol>
    <li>
      In your Canvas environment, go to <strong>Settings</strong> and click <strong>Apps</strong>:<br /><img src="{{site.url}}/assets/2766">
    </li>
    <li>
      Click <strong>View App Configurations</strong> to open the list of external apps:<br /><img src="{{site.url}}/assets/2763">
    </li>
    <li>
      Click Add New App to open the Edit External Tool Dialog.
    </li>
    <li>
      In the Edit External Tool Dialog, under <strong>Configuration Type</strong> Select “Paste XML”
    </li>
    <li>
      Enter the following information:<br /><table border="1" cellspacing="0" cellpadding="0">
        <tbody>
          <tr>
            <td width="54">
              <p class="TableHeading">
                #
              </p>
            </td>
            
            <td width="120">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td width="268">
              <p class="TableHeading">
                Value
              </p>
            </td>
            
            <td width="239">
              <p class="TableHeading">
                Example
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                1
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Name
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Name
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                “Media Gallery + BSE”
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                2
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Consumer Key
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Your Kaltura account Partner ID
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                123456789
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                3
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Shared Secret
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Your account administrator secret
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                6TS618TVBE48JAPE4H9CJQKEJSMEYXUD'
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                4
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Paste XML Here
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Paste the content of MediaGalleryAndBSE.xml provided to you by your Kaltura representative.
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                See <a href="https://kaltura.sharepoint.com/community-team/Shared%20Documents/Knowledge%20Management/Final%20Documents%20-%20Ready%20for%20Publishing/Kaltura%20Video%20App%20for%20Canvas/Deployment%20Guide/Kaltura_Video_App_for_Canvas_Deployment_Guide.docx#_MediaGalleryAndBSE.xml">MediaGalleryAndBSE.xml</a>.
              </p>
            </td>
          </tr>
        </tbody>
      </table>
    </li>
    
    <li>
      Click Submit. The Media Gallery tool will be listed in the list of external tools and a new navigation menu item will be added to the course menu.<br /><img src="{{site.url}}/assets/2768">
    </li>
  </ol>
  
  <p style="padding-left: 60px;">
    <img src="{{site.url}}/assets/2769">
  </p>
  
  <p>
    <strong>Option 2:</strong>
  </p>
  
  <ol>
    <li>
      In your Canvas environment, go to <strong>Settings</strong> and click <strong>Apps</strong>:<br /><img src="{{site.url}}/assets/2770">
    </li>
    <li>
      <span style="font-size: 1em;">Search for the </span><strong style="font-size: 1em;">Kaltura</strong><span style="font-size: 1em;"> app.<br /><img src="{{site.url}}/assets/2771">
    </li>
    <li>
      <span style="font-size: 1em;"></span>Select “Add App” and enter the following information:<br /><table border="1" cellspacing="0" cellpadding="0">
        <tbody>
          <tr>
            <td width="54">
              <p class="TableHeading">
                #
              </p>
            </td>
            
            <td width="120">
              <p class="TableHeading">
                Field
              </p>
            </td>
            
            <td width="268">
              <p class="TableHeading">
                Value
              </p>
            </td>
            
            <td width="239">
              <p class="TableHeading">
                Example
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                1
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Name
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Name
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                Kaltura Video App
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                2
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Consumer Key
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Your Kaltura account Partner ID
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                123456789
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                3
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Shared Secret
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Your account administrator secret
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                6TS618TVBE48JAPE4H9CJQKEJSMEYXUD'
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                4
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                KAF Host Name
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Your Kaltura Application Framework URL
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                123456.kaf.kaltura.com
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                5
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Course Menu Label
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                The name that will appear in the course navigation
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                Media Gallery
              </p>
            </td>
          </tr>
          
          <tr>
            <td width="54">
              <p class="TableBodyText">
                6
              </p>
            </td>
            
            <td width="120">
              <p class="TableBodyText">
                Add Kaltura to Rich-Text Editor
              </p>
            </td>
            
            <td width="268">
              <p class="TableBodyText">
                Check if you want to add Kaltura to the rich-text editor
              </p>
            </td>
            
            <td width="239">
              <p class="TableBodyText">
                Checked
              </p>
            </td>
          </tr>
        </tbody>
      </table>
      
      <p>
         
      </p>
      
      <p>
        <a href="#top">Back to top</a>
      </p>
    </li>
  </ol>
  
  <div class="WordSection5">
    <h1>
      <a name="samples"></a>Kaltura Video App for Canvas Sample Configuration Files (XMLs)
    </h1>
    
    <p>
      This section provides sample XML configuration files for My Media and for MediaGalleryAndBSE.
    </p>
    
    <p class="mce-note-graphic">
      <span>The actual xml files you receive from your Kaltura representative may slightly differ from the files presented in this section.</span> 
    </p>
    
    <h2>
      <a name="MyMedia.xml"></a>MyMedia.xml
    </h2>
    
    <pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;xml version="1.0" encoding="UTF-8”?&gt;
&lt;cartridge_basiclti_link xmlns="http://www.imsglobal.org/xsd/imslticc_v1p0"
    xmlns:blti = "http://www.imsglobal.org/xsd/imsbasiclti_v1p0"
    xmlns:lticm ="http://www.imsglobal.org/xsd/imslticm_v1p0"
    xmlns:lticp ="http://www.imsglobal.org/xsd/imslticp_v1p0"
    xmlns:xsi = "http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation = "http://www.imsglobal.org/xsd/imslticc_v1p0 http://www.imsglobal.org/xsd/lti/ltiv1p0/imslticc_v1p0.xsd
    http://www.imsglobal.org/xsd/imsbasiclti_v1p0 http://www.imsglobal.org/xsd/lti/ltiv1p0/imsbasiclti_v1p0.xsd
    http://www.imsglobal.org/xsd/imslticm_v1p0 http://www.imsglobal.org/xsd/lti/ltiv1p0/imslticm_v1p0.xsd
    http://www.imsglobal.org/xsd/imslticp_v1p0 http://www.imsglobal.org/xsd/lti/ltiv1p0/imslticp_v1p0.xsd"&gt;
    &lt;blti:title&gt;My Media Sample&lt;/blti:title&gt;
    &lt;blti:description&gt;My Media Sample&lt;/blti:description&gt;
    &lt;blti:icon&gt;http://hostname/canvaslti/kaltura%20sun.png&lt;/blti:icon&gt;
    &lt;blti:launch_url&gt;https://canvas.kaltura.com/hosted/index/my-media&lt;/blti:launch_url&gt;
    &lt;blti:extensions platform="canvas.instructure.com"&gt;
      &lt;lticm:property name="tool_id"&gt;0000000&lt;/lticm:property&gt;
      &lt;lticm:property name="privacy_level"&gt;public&lt;/lticm:property&gt;
      &lt;lticm:property name="domain"&gt;kaltura.com&lt;/lticm:property&gt;
      &lt;lticm:options name="course_navigation"&gt;
        &lt;lticm:property name="url"&gt;https://123456789.kaf.kaltura.com/canvas/index/launch/target/my-media&lt;/lticm:property&gt;
        &lt;lticm:property name="icon_url"&gt; http://hostname/canvaslti/kaltura%20sun.png&lt;/lticm:property&gt;
        &lt;lticm:property name="text"&gt;My Media - Sample&lt;/lticm:property&gt;
        &lt;lticm:property name="enabled"&gt;true&lt;/lticm:property&gt;
      &lt;/lticm:options&gt;
    &lt;/blti:extensions&gt;
    &lt;cartridge_bundle identifierref="BLTI001_Bundle"/&gt;
    &lt;cartridge_icon identifierref="BLTI001_Icon"/&gt;
&lt;/cartridge_basiclti_link&gt; </pre>
  </div>
  
  <h2>
    <a name="MediaGalleryAndBSE.xml"></a>MediaGalleryAndBSE.xml
  </h2>
  
  <pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;xml version="1.0" encoding="UTF-8”?&gt;
&lt;cartridge_basiclti_link xmlns="http://www.imsglobal.org/xsd/imslticc_v1p0"
    xmlns:blti = "http://www.imsglobal.org/xsd/imsbasiclti_v1p0"
    xmlns:lticm ="http://www.imsglobal.org/xsd/imslticm_v1p0"
    xmlns:lticp ="http://www.imsglobal.org/xsd/imslticp_v1p0"
    xmlns:xsi = "http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation = "http://www.imsglobal.org/xsd/imslticc_v1p0 http://www.imsglobal.org/xsd/lti/ltiv1p0/imslticc_v1p0.xsd
    http://www.imsglobal.org/xsd/imsbasiclti_v1p0 http://www.imsglobal.org/xsd/lti/ltiv1p0/imsbasiclti_v1p0.xsd
    http://www.imsglobal.org/xsd/imslticm_v1p0 http://www.imsglobal.org/xsd/lti/ltiv1p0/imslticm_v1p0.xsd
    http://www.imsglobal.org/xsd/imslticp_v1p0 http://www.imsglobal.org/xsd/lti/ltiv1p0/imslticp_v1p0.xsd"&gt;
    &lt;blti:title&gt;Course Gallery and BSE Sample XML&lt;/blti:title&gt;
    &lt;blti:description&gt;Course Gallery Sample XML&lt;/blti:description&gt;
    &lt;blti:icon&gt; http://hostname/canvaslti/kaltura%20sun.png&lt;/blti:icon&gt;
    &lt;blti:launch_url&gt; https://123456789.kaf.kaltura.com/canvas/index/launch/target/course-gallery &lt;/blti:launch_url&gt;
    &lt;blti:extensions platform="canvas.instructure.com"&gt;
      &lt;lticm:property name="tool_id"&gt;00000000&lt;/lticm:property&gt;
      &lt;lticm:property name="privacy_level"&gt;public&lt;/lticm:property&gt;
      &lt;lticm:property name="domain"&gt;kaltura.com&lt;/lticm:property&gt;
      &lt;lticm:options name="editor_button"&gt;
        &lt;lticm:property name="url"&gt;https://123456789.kaf.kaltura.com/browseandembed/index/browseandembed&lt;/lticm:property&gt;
        &lt;lticm:property name="icon_url"&gt; http://hostname/canvaslti/kaltura%20sun.png &lt;/lticm:property&gt;
        &lt;lticm:property name="text"&gt;Embed Kaltura Media&lt;/lticm:property&gt;
        &lt;lticm:property name="selection_width"&gt;1100&lt;/lticm:property&gt;
        &lt;lticm:property name="selection_height"&gt;600&lt;/lticm:property&gt;
        &lt;lticm:property name="enabled"&gt;true&lt;/lticm:property&gt;
      &lt;/lticm:options&gt;
      &lt;lticm:options name="course_navigation"&gt;
        &lt;lticm:property name="url"&gt;https://123456789.kaf.kaltura.com/canvas/index/launch/target/course-gallery&lt;/lticm:property&gt;
        &lt;lticm:property name="icon_url"&gt; http://hostname/canvaslti/kaltura%20sun.png&lt;/lticm:property&gt;
        &lt;lticm:property name="text"&gt;Course Gallery - Sample&lt;/lticm:property&gt;
        &lt;lticm:property name="enabled"&gt;true&lt;/lticm:property&gt;
      &lt;/lticm:options&gt;
    &lt;/blti:extensions&gt;
    &lt;cartridge_bundle identifierref="BLTI001_Bundle"/&gt;
    &lt;cartridge_icon identifierref="BLTI001_Icon"/&gt;
&lt;/cartridge_basiclti_link&gt;  </pre>
  
  <p>
    <a href="#top">Back to top</a>
  </p>