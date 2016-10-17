---
layout: page
title: "Kaltura Players and Internet Explorer 10"
date: 2012-10-21 15:35:48
---

Microsoft announced that Internet Explorer 10 will be available to those running Windows 7 machines sometime in November 2012 and that IE10 will be pre-loaded on machines running Windows 8, which debuts on Oct. 26<sup>th</sup>. See <a href="http://msdn.microsoft.com/en-us/library/ie/jj193557(v=vs.85).aspx" target="_blank">Developer guidance for websites with content for Adobe Flash Player in Windows 8.</a>

Windows 8 has 2 UI versions – the Metro UI and the Desktop UI. Internet Explorer 10 will have matching versions for the 2 UI options. 

On the Desktop UI of Windows 8, IE 10 will continue to support 3<sup>rd</sup> party plug-ins and provide full Flash support, as in previous versions of Windows Internet Explorer that relied on the Flash Player plug-in from Adobe. However, **on the Metro UI, IE 10 will not support 3<sup>rd</sup> party plug-ins on Metro UI, including the Flash Player plug-in from Adobe. Sites will only be allowed to serve Flash in this case, if they are whitelisted by Microsoft.**

<p class="mce-note-graphic">
  Windows 7, which has a Desktop UI only, will run Internet explorer 10 in a mode that fully supports Flash, as in previous versions of Windows Internet Explorer that relied on the Flash Player plug-in from Adobe. 
</p>

<h2 class="mce-heading-3">
  What does this mean to me as a Kaltura customer?
</h2>

This design change by Microsoft may cause the Kaltura player not to load on your webpage, and prevent video playback. To restore functionality, please follow the actions described here. 

<h2 class="mce-heading-4">
  What should you do?
</h2>

**<span style="text-decoration: underline;">Recommended Approach: Support Metro UI Through Flash Version of the Kaltura Player</span>**

1.  Contact Microsoft and request that they “whitelist” your site in the Flash section of the IE10 <a href="http://iecvlist.microsoft.com/ie10/201208/iecompatviewlist.xml" target="_blank">Compatibility View (CV) list</a>. This will permit the Flash Player to run in IE10 on your site.
2.  When your whitelist request is approved, edit your player to force Flash on IE10 Metro UI. You may accomplish this in one of two ways:
*   Editing the player itself, via the Studio tab in your Kaltura Management Console.  Add a uiVar as follows:  
    <**var** key="Kaltura.ForceFlashOnIE10" value="True">  
      
    or

*   By adding the following line of Javascript to each web page using the Kaltura player:  
    mw.setConfig( ‘Kaltura.ForceFlashOnIE10’, true );

You can skip step 2 **only** if you do not support, and do not plan to support mobile playback using the Kaltura HTML5 library.   
If you do support, or plan to support, mobile playback using the Kaltura HTML5 library, and you skip step 2, the Metro UI will use the Kaltura HTML5 player instead of the Flash player, despite being whitelisted by Microsoft.

**<span style="text-decoration: underline;">Second Best Option: Prompt Users to Switch to a Desktop UI</span>**

This is the best option to use if Microsoft does not add your site to their Compatibility View list.

Add a META-tag or HTTP header to the site HTML in order to prompt the user to switch to the Desktop UI.  After the user switches to the IE10 Desktop UI, the Flash player should display as normal. See <a href="http://msdn.microsoft.com/en-us/library/ie/jj193557(v=vs.85).aspx" target="_blank">instructions </a>by Microsoft and instructions to [Add a META-tag or HTTP Header][1].

 [1]: #add_meta

**<span style="text-decoration: underline;">Last Choice Option: Support Metro UI through the HTML5 Version of the Kaltura Player</span>**

This option is only relevant if you support mobile playback using the Kaltura HTML5 library. To check if you are currently configured to support mobile playback using the Kaltura HTML5 library, go the “Preview and Embed” window of an entry and see if the checkbox “Support mobile devices by fall-forward to HTML5” is checked. If checked, the Metro UI will use the Kaltura HTML5 player.

<img src="../../assets/861.img">
You will need to verify that the embed code supports HTML5 on **all** pages and entries on your site, verify encoding flavors, and verify correct plugins' functions (including advertising and analytics).

Also note that this option does not support adaptive streaming. For adaptive streaming formats in IE10 Metro UI you must use a Flash player as recommended above. HTTP Live Streaming (also known as HLS), is not supported by Microsoft and the adaptive streaming offered by Microsoft is <a href="http://www.microsoft.com/silverlight/iis-smooth-streaming/demo/#/on-demand" target="_blank">Smooth Streaming</a>, which is also not supported on IE10 Metro UI.

## <span class="mce-heading-3">Getting Listed in the Microsoft Compatibility View List</span>

Getting listed on Microsoft’s Compatibility View List entails emailing Microsoft with the details of your site and details of how it conforms to<a href="http://msdn.microsoft.com/en-us/library/ie/jj193557(v=vs.85).aspx" target="_blank"> Microsoft's Flash Content Guidelines</a>. It is not sufficient for the SWF origin to be on an included domain. Even though *.Kaltura.com is whitelisted, unless the containing site is also whitelisted, Flash will not be loaded.

<p class="mce-procedure">
  To submit your site for consideration to the CV list
</p>

*   Email <a href="mailto:iepo@microsoft.com" target="_blank">iepo@microsoft.com</a> and include the following details:

<ol start="1">
  <li>
    Your name, company, title, and contact information.
  </li>
  <li>
    <a name="step_2"></a>The domain you want considered (http://contoso.com/) and the specific pages containing Flash content (http://contoso.com/video,http://contoso.com/media).
  </li>
  <li>
    The approximate unique users per month that visit the domain.
  </li>
  <li>
    The capabilities your Flash content requires. For more info see <a href="http://msdn.microsoft.com/en-us/library/ie/jj193557(v=vs.85).aspx#Guidelines">Guidelines for Flash Content in Internet Explorer 10</a>.
  </li>
  <li>
    The name and version of the SWF your site is using, including the version number for the third party .SWF files if appropriate. (For example, kdp3.swf v3.6.5. The version number may be found by right-clicking on Kaltura’s player.)
  </li>
  <li>
    A list of any other plugs-ins (not Flash) that your domain depends on and the specific pages containing those controls. Be aware that if your site depends on other plug-ins, users will be directed to open your site in Internet Explorer 10 for the Desktop.
  </li>
  <li>
    The results of your testing from the pages listed in <a href="#step_2">step 2.</a> For more info see <a href="http://msdn.microsoft.com/en-us/library/ie/jj193557(v=vs.85).aspx#Test_Guidance" target="_blank">Test Guidance</a> and <a href="http://msdn.microsoft.com/en-us/library/ie/jj193557(v=vs.85).aspx#Test_cases">Test Cases</a>.
  </li>
</ol>

## <a name="add_meta"></a>Add a META-tag or HTTP Header

The following META tag or HTTP header will cause IE10 to provide a one-touch option to switch to Internet Explorer for the Desktop. After the user switches to the IE10 Desktop UI, the Flash player should display as normal.

<p style="padding-left: 30px;">
  HTTP header - X-UA-Compatible: requiresActiveX=true
</p>

<p style="padding-left: 30px;">
  META tag - <meta http-equiv="X-UA-Compatible" content="requiresActiveX=true" />
</p>

For more information, contact <a href="mailto:partnersupport@kaltura.com" target="_blank">Kaltura’s support</a>.