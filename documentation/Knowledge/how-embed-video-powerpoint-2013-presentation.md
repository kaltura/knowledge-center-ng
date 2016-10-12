---
layout: page
title: "How to Embed a Video in a PowerPoint 2013 Presentation"
date: 2015-07-19 10:30:25
---

<p>
    <span>When PowerPoint 2013 was released, the supported methods of embedding code within a presentation changed. Using the built-in hidden Developer menu in the PowerPoint toolbar allows you to add a Flash player and embed code to your presentation. This method of embedding also applies to previous releases of PowerPoint, such as 2010 and 2007. </span>This article is divided into two parts. The first part covers two methods of generating the correct embed code to be used when embedding a video. The second part explains how to enable the Developer menu in PowerPoint, adding a Shockwave Object and changing its attribute to our embed code.
  </p>
  
  <p class="mce-procedure">
    To generate the embed code using Kaltura Management Console
  </p>
  
  <ol>
    <li>
      Access the Kaltura Management Console and navigate to <strong>Content.</strong>
    </li>
    <li>
      Select the entry you want to embed. <br /><img src="../../assets/2382">
    </li>
    <li>
      After the entry screen is loaded, click <strong>Preview & Embed.</strong><br /><img src="../../assets/2383">
    </li>
    <li>
      Select a <strong>KDP Player</strong> (Flash player) and choose <strong>Legacy Flash Embed </strong>as the Embed Type. <br />** This adds the Legacy embed method to drop-down menu.<br /><br /><img src="../../assets/2384">
    </li>
    <li>
       Only a small part of the embed code is needed, search for the <strong>data</strong> attribute and copy the value.<br /><br /><img src="../../assets/2385">
    </li>
  </ol>
  
  <p class="mce-procedure">
    To generate the embed code without the  Kaltura Management Console 
  </p>
  
  <ol>
    <li>
      Use the following pattern and replace the content of the curly braces <strong>and the curly braces</strong> with your information:<br />http://cdnapi.kaltura.com/index.php/kwidget/wid/_<strong>{PartnerID}</strong>/uiconf_id/<strong>{UiConfID}</strong>/entry_id/<strong>{EntryID}<br /><br /></strong>**The UiConfID refers to the player ID, you must choose a Flashplayer.<br />After replacing your own values, the URL should be similar to:<br />http://cdnapi.kaltura.com/index.php/kwidget/wid/_1763321/uiconf_id/26354192/entry_id/1_2iju5utg
    </li>
    <li>
      Save the embed code either in a text document or in the clipboard.
    </li>
  </ol>
  
  <p class="mce-heading-3">
    Embedding the Media in a PowerPoint Presentation
  </p>
  
  <p>
    To add a Shockwave Object to display media, the Developer Toolbar needs to be added to the PowerPoint ribbon.
  </p>
  
  <p>
    <a name="developer_toolbar"></a><span class="mce-procedure">To enable the Developer Toolbar</span>
  </p>
  
  <ol>
    <li>
      Open <strong>PowerPoint</strong> and <strong>right click</strong> anywhere in the <strong>Ribbon </strong>and Select <strong>Customize the Ribbon.<br /><img src="../../assets/2386">
    </li>
    <li>
      In the right side list, check the <strong>Developer</strong> box and click <strong>OK.<br /><img src="../../assets/2387">
    </li>
  </ol>
  
  <p class="mce-heading-3">
    Adding the Shockwave Object and Player
  </p>
  
  <p class="mce-procedure">
    To add the Shockwave Object and Player
  </p>
  
  <ol>
    <li>
      Navigate to newly added <strong><a href="#developer_toolbar">Developer</a> </strong>toolbar and click the <strong>Tools</strong> icon.<br /><img src="../../assets/2388">
    </li>
    <li>
      Scroll through the list and select <strong>Shockwave Flash Object</strong> and click <strong>OK</strong>.<br /><img src="../../assets/2389">
    </li>
    <li>
      Click and drag to insert the Shockwave Flash Object.<br /><img src="../../assets/2390">
    </li>
    <li>
      <strong>Right click</strong> the <strong>Shockwave Flash Object</strong> and select<strong> Property Sheet</strong> from the menu.<br /><img src="../../assets/2391">
    </li>
    <li>
      In the Properties window, insert the embed code collected in previous steps in the Movie row.<br /><img src="../../assets/2392">
    </li>
    <li>
      Close the Properties menu, play the presentation to see changes. <br /><img src="../../assets/2393">
    </li>
  </ol>