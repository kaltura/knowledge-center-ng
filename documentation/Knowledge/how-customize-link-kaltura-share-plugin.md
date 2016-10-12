---
layout: page
title: "How to customize the link for the Kaltura Share plugin"
date: 2012-10-24 16:30:37
---

The Share plugin uses the AddThis platform.

<p class="mce-procedure">
  To add a specific addThis partner id
</p>

*   Add the uivar (this assumes 111111 is your add this partner id)

<p style="padding-left: 30px;">
  Key:
</p>

<p style="padding-left: 30px;">
  kalturaShare.pubid
</p>

<p style="padding-left: 30px;">
  Value:
</p>

<p style="padding-left: 30px;">
  111111
</p>

<p class="mce-procedure">
  To change your Twitter via (like to point who twit this)
</p>

<p style="padding-left: 30px;">
  Key:
</p>

<p style="padding-left: 30px;">
  kalturaShare.via
</p>

<p style="padding-left: 30px;">
  Value:
</p>

<p style="padding-left: 30px;">
  <yourname>
</p>

<p class="mce-procedure">
  To change the link of the landing page
</p>

*   Add the following uivar:

<p style="padding-left: 30px;">
  Key:
</p>

<p style="padding-left: 30px;">
  kalturaShare.dynamicLink
</p>

<p style="padding-left: 30px;">
  Value:
</p>

<p style="padding-left: 30px;">
  http://www.mydomain.com/entryId/{mediaProxy.entry.id}/pakapak
</p>

Changing the landing page link allows you to write whatever you wish, prefix and postfix, to the entry.id.

The expression {mediaProxy.entry.id} will be replaced with the current entry.id.

Keep in mind that the customized site should be able to display the player on the page (synced with the entry.id), and also generate the OpenGraph meta tags in the head of the HTML, so that Facebook will be able to crawl the page and grab the widget. See <a href="http://blog.kaltura.org/tag/open-graph" target="_blank">Facebook Now Requires HTML5 and Fallback in Open Graph</a>.

There is also the ability to hide parts of the plugin's UI. Use the following code to: 

*   hide the networks button area: kalturaShare.showNetworks=false
*   hide the embed UI: kalturaShare.showEmbed=false
*   hide the link UI: kalturaShare.showLink=false
*   hide seperate networks button: 
*   kalturaShare.showTwitter=false
*   kalturaShare.showFacebook=false 
*   kalturaShare.showLinkedIn=false
*   kalturaShare.showWordpress=false