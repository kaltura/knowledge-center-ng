---
layout: page
title: "How to build the KDP3 in Flash Builder?"
date: 2012-03-27 17:02:58
---

Building the KDP in a Flash builder involves a standard Flash Builder project import.

<p class="mce-procedure">
  To build the KDP in a Flash builder
</p>

1.  Get <a href="http://www.adobe.com/products/flashbuilder/" target="_blank">Adobe Flash Builder 4</a>.
2.  Checkout the [KDP 3 project trunk][1] using your svn client of choice. or download the project bundle from the [project page][2].
3.  You should import the two projects inside the trunk into Flash Builder:
<ol style="list-style-type: lower-alpha;">
  <li>
    Right click the navigation panel.
  </li>
  <li>
    Import...
  </li>
  <li>
    Choose the project to import (KDP_3 or kdp3Lib) and click Finish.
  </li>
  <li>
    Do the same for both projects.
  </li>
</ol>

4.  Make sure you have Flex 3.4 SDK version installed, if not, you should <a href="http://opensource.adobe.com/wiki/display/flexsdk/Download+Flex+3" target="_blank">download</a> and <a href="http://opensource.adobe.com/wiki/display/flexsdk/Targeting+Flash+Player+10" target="_blank">install it for Flash Player 10</a>.
5.  Right click the KDP_3 project, and click Build Project.

 [1]: http://www.kaltura.org/kalorg/kdp/trunk/
 [2]: http://www.kaltura.org/project/kdp

That's it, you're all set and ready to write KPD 3 plugins.