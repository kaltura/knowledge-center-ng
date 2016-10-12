---
layout: page
title: "How to configure the AdapTV plugin?"
date: 2012-01-23 10:25:20
---

AdapTV has two different models – the standard model and the marketplace. The standard model allows Kaltura partners to define their own ads. The marketplace provides the customer the ability to connect with all sorts of ad companies to choose the most fitting ads.

<p class="mce-procedure">
  To configure the AdapTV ad plugin
</p>

1.  Go to your AdapTV account, define ads, scheduling, targeting, etc. on the AdapTV end.
2.  Go to the Studio tab and edit an existing player or create a new one.
3.  Select the Advertising tab.
4.  Enable ads for the selected player.
5.  Select AdapTV as the Ad Source.<img src="http://cdnknowledge.kaltura.com//sites/default/files/Ad%20config%20AdapTV.png" border="0" width="600" />
6.  Enter the Custom SWF URL.  
    The Kaltura partner administrator should contact their ad server company to obtain the SWF URL and the proper Key-Value Pairs to insert.
7.  In the key-value section insert key=[your AdapTV key]. In AdapTV, many users utilize the zone to differentiate between different ads. In this case, the customer needs to insert zone=[zone name] in the key-value section as well.
8.  To utilize the latest AdapTV plugin (the current out-of-the-box plugin is utilizing AdapTV’s legacy integration of AS2, the new plugin utilizes AS3 integration): in the Additional Parameters and Plugins section of the player, insert key=customAd.path value= [http://cdnbakmi.kaltura.com/flash/kdp3/v3.5.7.6/plugins/adaptvas3Plugin.swf<img src="{{site.url}}/assets/1093">

 [1]: http://cdnbakmi.kaltura.com/flash/kdp3/v3.5.7.6/plugins/adaptvas3Plugin.swf

 