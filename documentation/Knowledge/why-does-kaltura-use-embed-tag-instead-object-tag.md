---
layout: page
title: "Why does Kaltura use the Embed tag Instead of the Object Tag?"
date: 2012-03-26 23:53:03
---

<h2 style="margin-top: 0; padding-top: 0;">
  Background
</h2>

This document aims to outline common and rare situations where the use of the <object> or <embed> tags interrupt with various deployments, browsers or addons. The <object> tag offers significant advantages over the <embed> tag if you prefer to create standards-compliant code or accessible, search-engine–friendly content. [<a href="http://www.alistapart.com/articles/flashembedcagematch/" target="_blank">more</a>]

## Old browsers and the <embed> tag

Being the W3C recommendation, we should use the <object> tag for embedding browser plugins. Although web standards are created to avoid compatibility issues, the <embed> tag has become to "de facto" standard, that can't be ignored due to old browser versions that don't support the W3C <object> standard.

### The various methods

#### Clean <object> tag based syntax

According to <a href="http://allinthehead.com/" target="_blank">Drew McLellan</a>, on <a href="http://www.alistapart.com/articles/flashsatay/" target="_blank">A List Apart</a> embedding article, one can merge attributes from both methods to create a leaner <object> syntax. Using the "The Satay Method" explained by Drew McLellan on the above article, the <object> based code is cleaner, leaner and validates as standard-compliant. However, even though the above method seems to work on most deployments, it seems that rare cases such as when the <a href="http://adblock.mozdev.org/" target="_blank">adblock firefox plugin</a>is installed (or even when disabled?!) - <object> tag based syntax cause firefox not to render the flash movie.

#### Adobe’s Solution: The twice-cooked method

So to support the rare cases, the code should include the <embed> tag in addition to the <object> tag. As stated in <a href="http://kb2.adobe.com/cps/415/tn_4150.html" target="_blank">Adobe tech note tn_4150</a>:

<div style="background: transparent url('/./sites/all/modules/privatemsg/../../../default/themes/kdotorg/images/quoleft.png') no-repeat scroll left top; margin: 10px -5px 0; padding: 15px 0; width: 100%;">
  <strong>Adobe tech note tn_4150</strong><br /><blockquote style="background: transparent url('/./sites/all/modules/privatemsg/../../../default/themes/kdotorg/images/quoright.png') no-repeat scroll right bottom; color: #666666; padding: 15px 0 15px 10px;">
    The <embed> tag is for Netscape Navigator 2.0 or later, or browsers that support the use of the Netscape-compatible plugin version of Flash Player.
  </blockquote>
</div>

The twice-cooked method will makes your web pages non-standard-compliant, and can’t include a mechanism for inserting alternative content (useful for search-engines and users that don't have flash installed).

#### The most compatible solution: Nested <object> tags + IE conditional comments

According to the browser's <a href="http://www.bobbyvandersluis.com/flashembed/testsuite/" target="_blank">Flash embed test suite</a> by <a href="http://www.bobbyvandersluis.com/about/index.html" target="_blank">Bobby van der Sluis</a>, the most compatible syntax, as well as the most standard-compliant is using IE conditional comments and a nested object tag. In this method, one <object> tags is placed inside the other, thus requiring a double object definition (the outer object targeting Internet Explorer and the inner object targeting all other browsers), so you need to define your object attributes and nested param elements twice. This method, however being more complex, according to Bobby's <a href="http://www.bobbyvandersluis.com/flashembed/testsuite/" target="_blank">Flash embed test suite</a>has proven support for all of deployments.

## Media and RSS readers, Facebook, MySpace and other sites - FAQ

### My media player doesn't show inside Google Reader

According to the <a href="http://www.google.com/support/reader/bin/answer.py?hl=en&answer=70664" target="_blank">Google Reader FAQ</a>, Google Reader is only capable of recognizing the \[html\]\[/html\] syntax. In that case, please make sure your RSS include the full \[html\]\[/html\] code for the media player.

### Facebook or MySpace throws exceptions when clicking on the logo or other buttons

Facebook and MySpace prevents direct script access from Flash by adding [html]allowScriptAccess=none[/html]. In order to perform javascript calls from Flash inside Facebook, use the following <a href="http://wiki.developers.facebook.com/index.php/Fb:swf#notes" target="_blank">Facebook Fb:swf guide</a>.

## Summary

To get the most standard-compliant and cross-browser compatible solution, we recommend using <a href="http://code.google.com/p/swfobject/" target="_blank">SWFObject 2</a>. SWFObject is using two methods; a static method using two nested <object> tags, and a javascript based method to dynamically embed flash movies. The [url=http://code.google.com/p/swfobject/wiki/generator]SWFObject Generator[/url] can be used to easily generate the right <object> syntax. The mentioned Adblock firefox plugin issue will **not** be solved by using SWFObject 2, due to Adblock's functionality of blocking the object tag. Since the development of Adblock was discontinued and Adblock is no longer offered for download- in the case of Adblock compatibility, one of the following are advised:\[list\]\[*\] <a href="http://code.google.com/p/swfobject/wiki/faq#14._Why_can%27t_I_see_Flash_content_in_Firefox_3?" target="_blank">SWFObject 2 recommendation</a>: Disable the Adblock extension or upgrade to <a href="https://addons.mozilla.org/nl/firefox/addon/1865" target="_blank">Adblock Plus</a> [*] Use the non-compliant method passing on alternative content: The twice-cooked method[/list] Adobe has recently decided to use SWFObject as the default template for the html wrappers created by Flash builder: "<a href="http://help.adobe.com/en_US/Flex/4.0/UsingSDK/WS2db454920e96a9e51e63e3d11c0bf69084-7b86.html" target="_blank">...The default template included with Flex SDK and Flash Builder embeds the SWFObject 2 functionality...</a>"