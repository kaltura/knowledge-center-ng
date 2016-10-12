---
layout: page
title: "How to configure Bumper post-rolls"
date: 2012-01-11 14:46:08
---

<p class="mce-procedure">
  This FAQ applies to the legacy KDP Flash player. To configure ads using the Universal player please see <a href="http://knowledge.kaltura.com/universal-studio-information-guide#monetization" target="_blank">here</a>
</p>

<p class="mce-procedure">
  <span style="font-size: small;">To configure Bumper post-rolls</span>
</p>

> 1.  Create a Bumper video. See <a href="http://knowledge.kaltura.com/faq/how-create-bumper-ads" target="_blank" title="How to create Bumper ads">How to create Bumper ads</a>.
> 2.  In the Features tab on the left, select the Additional Parameters and Plugins section.  
>     Enter the following code: 
> 
> <pre class="brush: php;fontsize: 100; first-line: 1; ">bumper.preSequence=0&bumper.postSequence=1  </pre>Whenever both pre-rolls and bumper videos are enabled, pre-rolls will always play before the bumper video. This is because the pre-roll is configured as, preSequence=1, and the bumper video is, preSequence=2. You can change the play order via the uiconf.  Post-roll ads will always play AFTER the bumper post-rolls.