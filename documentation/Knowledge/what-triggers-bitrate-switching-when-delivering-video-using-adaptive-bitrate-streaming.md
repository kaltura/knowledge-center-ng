---
layout: page
title: "What Triggers The Bitrate Switching When Delivering Video Using Adaptive Bitrate Streaming"
date: 2013-03-13 19:48:06
---

<p class="mce-heading-2">
  Background
</p>

The bitrate switching is generally transparent to the player as it is decided by either the CDN or Video Stream Optimization Plugins such as <a href="http://www.akamai.com/" target="_blank">Akamai</a> or <a href="http://www.conviva.com/" target="_blank">Conviva</a>.

Publishers can control <a href="http://html5video.org/kaltura-player/modules/KalturaSupport/tests/FlavorSelector.preferedFlavorBR.qunit.html" target="_blank">the initial bitrate</a>, after that point the respective adaptive algorithm takes over and makes the decisions based on variables such as network utilization/congestion, screen size, geographic location and more.

<p class="mce-heading-2">
  Adaptive Streaming methods used by the Kaltura Players
</p>

With iOS devices Kaltura will leverage HTTP live streaming (aka <a href="http://en.wikipedia.org/wiki/HTTP_Live_Streaming" target="_blank">HLS</a>).

Where Flash is used, the choice will be adobe HTTP dynamic streaming (aka <a href="http://www.adobe.com/products/hds-dynamic-streaming.html" target="_blank">HDS</a>).

Each respective algorithm will dynamically adjust the content stream on a set interval to fit available network bandwidth and device resource constraints.

Setting the initial bitrate will dictate what bitrate is used first.