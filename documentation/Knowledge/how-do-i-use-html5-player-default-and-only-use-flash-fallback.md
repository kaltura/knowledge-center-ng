---
layout: page
title: "How do I use the HTML5 player by default and only use Flash for fallback"
date: 2012-01-05 19:58:17
---

As of version 1.6.1 we now support leading with HTML5. A Kaltura player by default uses flash. With this property you can have the script use html5 first on browsers that support it, while falling back to flash on browsers such as IE8 that do not support the video tag.

<div class="mw-geshi" dir="ltr">
  <div class="html5 source-html5">
    <pre class="de1">mw.setConfig( 'KalturaSupport.LeadWithHTML5', true );</pre>
  </div>
</div>

*   Note if you want fine grain control over which browsers use HTML5 or not, see the <a href="http://html5video.org/w/index.php?title=KalturaPlugin:UserAgentPlayerRules" title="KalturaPlugin:UserAgentPlayerRules (page does not exist)" class="new">KalturaPlugin:UserAgentPlayerRules</a>
*   Note this property is different form the "forceMobileHTML5" flag that will force the HTML5 player regardless of native browser support.

Please visit our [html5 video faq on the html5video.org wiki][1] for the most current html5 documentation.

 [1]: http://html5video.org/wiki/Kaltura_SaaS_FAQ