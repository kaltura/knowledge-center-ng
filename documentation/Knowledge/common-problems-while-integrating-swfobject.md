---
layout: page
title: "Common problems while integrating with SWFObject"
date: 2011-12-29 19:50:33
---

If you are experiencing problems while embedding Kaltura widgets using SWFObject, please look for more information in the [SWFObject documentation page][1], in addition you may pay attention to the following points:

 [1]: http://code.google.com/p/swfobject/wiki/documentation

In addition you may pay attention to the following points:

*   Make sure you are using SWFObject version 2
*   If you are using Google AJAX Libraries API, for including the SWFObject script, make sure your script definition is directing to the relevant URL. Please look for more information in the [Google AJAX Library API documentation page][2].
*   If you are using a local download of the SWFObject, make sure you downloaded all of SWFObject scripts to a location that is accessible to your web application scripts, and that your include statement within your scripts includes the exact path of this location.
*   Make sure you include a dedicated DIV tag for SWFObject alternative content in your web page. The ID of this DIV should be the same as the ID of your embedded object. Please read more about this topic in the [SWFObject documentation page][1].

 [2]: http://code.google.com/apis/ajaxlibs/documentation/