---
layout: page
title: "How do I dynamically embed an HTML5 video player"
date: 2012-01-05 20:06:22
---

If you want to embed the player dynamically, the library supports rewriting swfObject or flashembed. In addition, the library supports a native mechanism to embed the iframe:

<div class="mw-geshi" dir="ltr">
  <div class="html5 source-html5">
    <pre class="de1">kalturaIframeEmbed( 'kaltura-video', {
        'wid'&nbsp;: '_243342',
        'uiconf_id'&nbsp;: '5349042',
        'entry_id'&nbsp;: '0_ntovmku5'
    });</pre>
    
    <p>
       Please visit our <a href="http://html5video.org/wiki/Kaltura_SaaS_FAQ">html5 video faq on the html5video.org wiki</a> for the latest HTML5 documentation.
    </p>
  </div>
</div>