---
layout: page
title: "Enabling the Silverlight Plugin (NPAPI Plugins) in Chrome"
date: 2015-04-26 02:01:54
---

<span style="color: rgb(130, 138, 140); font-size: 14pt; font-weight: bold;">Chrome 42 _ support for NPAPI Plugins</span>

As of April 2015, starting with Chrome Version 42, Google has added an additional step to configuring NPAPI based plugins to run. As of the latest version of Chrome (42), released last week, Google has decided to block NPAPI based plugins by default, as described here: <a href="http://go.kaltura.com/m000cf40p0W81PnkDKY0SM0" data-mce-href="http://go.kaltura.com/m000cf40p0W81PnkDKY0SM0">https://java.com/en/download/faq/chrome.xml</a>. As a result, some Kaltura products that use instances of Chrome that have recently been installed or which have auto-updated to the latest version will not work. 

<span>Products affected by Chrome 42 NPAPI disablement include:</span>

*   <a data-mce-href="http://knowledge.kaltura.com/kaltura-screen-record-ksr-integration-guide#kaltura+screen+recorder" href="http://knowledge.kaltura.com/kaltura-screen-record-ksr-integration-guide#kaltura+screen+recorder" target="_blank"><strong>Kaltura Screen Recorder</strong></a>
*   <a data-mce-href="http://knowledge.kaltura.com/kaltura%E2%80%99s-digital-rights-management-drm-service-widevine-setup-and-workflow-guide#drm" href="http://knowledge.kaltura.com/kaltura%E2%80%99s-digital-rights-management-drm-service-widevine-setup-and-workflow-guide#drm" target="_blank"><strong>DRM</strong></a>
*   <a data-mce-href="http://knowledge.kaltura.com/node/1185/attachment/field_media#ecdn" href="http://knowledge.kaltura.com/node/1185/attachment/field_media#ecdn" target="_blank"><strong>Silverlight Multicast </strong></a>

All of Kaltura's products continue to function properly in all other major browsers.

<p class="mce-procedure">
  To ensure that the Kaltura products work properly in Chrome (42)
</p>

1.  <span>Open Chrome and browse to </span><a href="chrome://flags/#enable-npapi" target="_blank" data-mce-href="chrome://flags/#enable-npapi">chrome://flags/#enable-npapi</a>
2.  Click Enable. <img class="media-image" src="http://knowledge.kaltura.com/sites/default/files/styles/large/public/ksr_chrome.png" border="0" alt="" width="446" height="131" data-mce-src="http://knowledge.kaltura.com/sites/default/files/styles/large/public/ksr_chrome.png" />
3.  <span>Click "Relaunch Now" at the bottom of your Chrome window.<br /><img class="media-image" src="http://knowledge.kaltura.com/sites/default/files/styles/large/public/ksr_chrome2_0.png" border="0" alt="" width="396" height="49" data-mce-src="http://knowledge.kaltura.com/sites/default/files/styles/large/public/ksr_chrome2_0.png" /><br />Closing and reopening Chrome is not sufficient, you must click the "Relaunch Now" button.</span>
4.  <span><span>After Chrome relaunches, verify that Silverlight is installed by browsing to <a href="http://www.microsoft.com/getsilverlight/Get-Started/Install/Default.aspx" target="_blank" data-mce-href="http://www.microsoft.com/getsilverlight/Get-Started/Install/Default.aspx">http://www.microsoft.com/getsilverlight/Get-Started/Install/Default.aspx</a></span></span>
5.  <span><span><a href="http://www.microsoft.com/getsilverlight/Get-Started/Install/Default.aspx" target="_blank" data-mce-href="http://www.microsoft.com/getsilverlight/Get-Started/Install/Default.aspx"></a></span></span>If you see the following message, continue as normal.<div>
      <img class="media-image attr__typeof__foaf:Image img__fid__2231 img__view_mode__media_large attr__format__media_large" src="http://knowledge.kaltura.com/sites/default/files/styles/large/public/chrome_silverlight_0.png?itok=ET2LD5wY" border="0" alt="" width="300" height="175" data-mce-src="http://knowledge.kaltura.com/sites/default/files/styles/large/public/chrome_silverlight_0.png?itok=ET2LD5wY" />
    </div>

6.  If you see the following message, <span>Silverlight is not currently installed. Click Click to Install" to install Silverlight.<br /><img class="media-image attr__typeof__foaf:Image img__fid__2232 img__view_mode__media_large attr__format__media_large" src="http://knowledge.kaltura.com/sites/default/files/styles/large/public/chrome_silverlight2_0.png?itok=26y2GQDf" border="0" alt="" width="271" height="248" data-mce-src="http://knowledge.kaltura.com/sites/default/files/styles/large/public/chrome_silverlight2_0.png?itok=26y2GQDf" /><br /></span>