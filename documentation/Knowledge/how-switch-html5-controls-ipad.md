---
layout: page
title: "How to switch off HTML5 controls for iPad"
date: 2012-01-05 19:52:48
---

The iPad has two modes of usage for HTML5, HTML controls or native player. There are tradeoffs to both options:

Advantages of HTML controls:

*   On screen overlays ( like ad overlays )
*   Control over the playhead scrubber ( no ad skip)
*   Custom branded player and 'experience' ( watermarks, control bar logo, share option etc. )

Advantages of Native controls:

*   Smooth transition to true fullscreen ( no "new browser window" or address bar )
*   Consistent with iPhone experience ( native player )
*   Analytics and flavor selection work the same for both modes

To switch **off** HTML5 controls for iPad:

<pre class="brush: jscript;fontsize: 100; first-line: 1; ">mw.setConfig('EmbedPlayer.EnableIpadHTMLControls', false );</pre>

<div class="mw-geshi" dir="ltr">
  <div class="html5 source-html5">
    <p>
      Please visit our <a href="http://html5video.org/wiki/Kaltura_HTML5_Configuration#Hybrid_HTML_controls.2C_native_fullscreen_mode_on_iPad">HTML5 video FAQ on the html5video.org wiki</a> for the latest HTML5 documentation.
    </p>
    
    <p>
      <a href="http://html5video.org/kgit/branches/develop/modules/KalturaSupport/tests/iPadHTML_Controls_Native_EnableIpadNativeFullscreen.html">Demo page</a>.
    </p>
  </div>
</div>