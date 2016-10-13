---
layout: page
title: "What ad servers are supported in the KMC?"
date: 2012-01-11 11:55:14
---

All VAST compliant ad servers are supported in the KMC. For more information see [Kaltura’s Generic Ads Player Plugin for VAST][1].<span style="font-size: small;"> </span>

 [1]: http://knowledge.kaltura.com/kaltura%E2%80%99s-generic-ads-player-plugin-vast

The Kaltura Player all VAST compliant ad servers and supports the following ad plugins:

> *   AdapTV - For more information see <a href="http://knowledge.kaltura.com/faq/how-configure-adaptv-plugin" target="_blank">How to configure the AdapTV plugin?</a>
> 
> *   Tremor  - For more information see <a href="http://knowledge.kaltura.com/faq/how-configure-tremor-media-plugin" target="_blank">How to configure the Tremor Media plugin?</a>
> 
> *   DoubleClick - for more information see  the <a href="{{site.url}}/documentation/Knowledge/doubleclick-plugin-kaltura-implementation-guide.html" target="_blank">DoubleClick Plugin for Kaltura Implementation Guide</a>
> 
> *   FreeWheel
>     
>     There are additional ad servers that Kaltura supports, which are a bit more complex than just plugins. For example, Kaltura is now fully integrated with** DoubleClick and Freewheel**. Their integrations are more complex since there is a server-side connector that allows you to define the metadata to submit to the ad server for ad targeting purposes. The Kaltura metadata gets mapped to ad server’s metadata. Then, just like with a distribution module, see <a href="http://knowledge.kaltura.com/kaltura-distribution-module" target="_blank">Kaltura Distribution Module</a>, when a Kaltura partner wants an entry to be included in the ad server, it is marked as such in the KMC. The ad server connector passes all of the metadata to the ad server, where the Kaltura partner can then decide how ads should be targeted based on the metadata.