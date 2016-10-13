---
layout: page
title: "Interactive Video Quiz Canvas Gradebook Integration  Deployment Guide"
date: 2016-02-08 23:48:53
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
        <a href="#audience"></a><a href="#prereq">Prerequisites</a>
      </li>
      <li>
        <a href="#instructions">Interactive Video Quizzes Canvas Gradebook Integration Instructions</a>
      </li>
    </ul>
  </div>
  
  <div class="WordSection2">
    <h3>
      <span style="font-size: 1.5em;"><a name="about"></a>About this Guide</span>
    </h3>
    
    <p>
      This guide describes how to deploy the Interactive Video Quiz Canvas Gradebook Integration.
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
      This guide is for Canvas and Kaltura administrators that intend to integrate the Interactive Video Quiz (IVQ)  feature with the Canvas Gradebook.
    </p>
  </div>
  
  <div class="WordSection3">
    <h2>
      <a name="prereq"></a>Prerequisites
    </h2>
    
    <ul>
      <li>
        Kaltura Video App for Canvas should be installed on your Canvas environment
      </li>
      <li>
        If you haven’t already, re-install the Media Gallery and BSE (Browse, Search and Embed tool) with the latest content item message based integration. The new xml can be generated using your KAF instance.<br />http://123456.kaf.kaltura.com/canvas/config/create-xml-for-instance. <br />For additional information please review the <a href="{{site.url}}/documentation/Knowledge/kaltura-video-app-canvas-deployment-guide-0.html" target="_blank">Kaltura Video App for Canvas Deployment Guide</a>
      </li>
    </ul>
    
    <p>
      <a href="#top">Back to top</a>
    </p>
  </div>
  
  <h1>
    <a name="instructions"></a>Interactive Video Quiz Canvas Gradebook Integration Deployment Instructions
  </h1>
  
  <p class="Procedure mce-procedure">
    To deploy the Interactive Video Quiz Canvas Gradebook Integration
  </p>
  
  <ol>
    <li>
      In your Canvas environment, go to <strong>Settings</strong> and click <strong>Apps</strong>:<br /><img src="../../assets/2761">
    </li>
    <li>
      Click <strong>View App Configurations</strong> to open the list of external apps:<br /><img src="../../assets/2763">
    </li>
    <li>
      Click Add New App to open the Add App dialog.
    </li>
    <li>
      Select Paste XML from the <strong>Configuration Type</strong> drop down menu.<br />Enter the following information: <br /><div align="center">
        <table style="width: 730px;" border="1" cellspacing="0" cellpadding="0" align="left">
          <tbody>
            <tr>
              <td style="text-align: left;" width="120">
                <p class="TableHeading">
                  <strong>Field</strong>
                </p>
              </td>
              
              <td style="text-align: left;" width="375">
                <p class="TableHeading">
                  <strong>Value</strong>
                </p>
              </td>
              
              <td style="text-align: left;" width="194">
                <p class="TableHeading">
                  <strong>Example</strong>
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" width="120">
                <p class="TableBodyText">
                  Name
                </p>
              </td>
              
              <td style="text-align: left;" width="375">
                <p class="TableBodyText">
                  Name (only affects the list of installed tools)
                </p>
              </td>
              
              <td style="text-align: left;" width="194">
                <p class="TableBodyText">
                  “Kaltura Video Quiz”
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" width="120">
                <p class="TableBodyText">
                  Consumer Key
                </p>
              </td>
              
              <td style="text-align: left;" width="375">
                <p class="TableBodyText">
                  You Kaltura account Partner Id
                </p>
              </td>
              
              <td style="text-align: left;" width="194">
                <p class="TableBodyText">
                  123456789
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" width="120">
                <p class="TableBodyText">
                  Shared Secret
                </p>
              </td>
              
              <td style="text-align: left;" width="375">
                <p class="TableBodyText">
                  Your account administrator secret
                </p>
              </td>
              
              <td style="text-align: left;" width="194">
                <p class="TableBodyText">
                  6TS618TVBE48JAPE4H9CJQKEJSMEYXUD'
                </p>
              </td>
            </tr>
            
            <tr>
              <td style="text-align: left;" width="120">
                <p class="TableBodyText">
                  XML Configuration
                </p>
              </td>
              
              <td style="text-align: left;" width="375">
                <p class="TableBodyText">
                  Paste the content of the Video Quiz xml
                </p>
              </td>
              
              <td style="text-align: left;" width="194">
                <p class="TableBodyText">
                  http://123456.kaf.kaltura.com/canvas/config/create-xml-for-instance
                </p>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      
      <br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
    </li>
    <li>
      Click <strong>Submit</strong>. 
    </li>
    <li>
      In your KAF admin go to module: Ltigrading and enable, then click save.<br /><br /><a href="#top">Back to top</a>
    </li>
  </ol>