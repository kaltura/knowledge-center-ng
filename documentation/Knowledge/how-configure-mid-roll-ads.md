---
layout: page
title: "How to configure mid-roll ads?"
date: 2012-01-11 14:11:14
---

<span style="font-size: small;">Midrolls and overlays are cuepoints that are defined on an entry level in the player configuration section of the Studio Advertising tab.</span>

<p class="mce-procedure">
  <span style="font-size: small;">To add a mid-roll ad</span>
</p>

> 1.  <span style="font-size: small;"><strong></strong><a href="http://knowledge.kaltura.com/faq/how-configure-player-advertising-settings" target="_blank" title="How to configure the player advertising settings">Configure the Player Advertising Settings.</a></span>
> 2.  <span style="font-size: small;"><strong></strong>Select the Content Tab and select an entry.</span>
> 3.  <span style="font-size: small;"><strong></strong>Select the Advertisements tab.</span><img src="{{site.url}}/assets/242">
> 4.  <span style="font-size: small;">Select the method to obtain the midroll add from the File Actions drop down menu.</span>
> 5.  <span style="font-size: small;"><strong></strong>Choose the granularity level for the time-based display. The choices are:</span>
> <ol style="list-style-type: lower-alpha;">
>   <li>
>     <span style="font-size: small;">100%</span>
>   </li>
>   <li>
>     <span style="font-size: small;">5 sec</span>
>   </li>
>   <li>
>     <span style="font-size: small;">1 sec</span>
>   </li>
>   <li>
>     <span style="font-size: small;"><span style="font-size: small;">Frames.<br /></span></span><br /><img src="{{site.url}}/assets/243">
>   </li>
> </ol>
> 
> 6.  <span style="font-size: small;">Identify the exact scene or frame to display the advertisement and insert a cue.</span>  
>     <span style="font-size: small;">This can be done on the timeline:</span>  
>     <img src="{{site.url}}/assets/245">
>     <span style="font-size: small;"></span>
> 7.  <span style="font-size: small;">To edit a cue point, select whether the advertisement will be a video or an overlay.</span>
> <ol style="list-style-type: lower-alpha;">
>   <li>
>     <span style="font-size: small;">For a video - the entry will stop playing, the ad will play, and then the entry will resume.</span>
>   </li>
>   <li>
>     <span style="font-size: small;">For an overlay - while the entry is playing, a banner will appear on the screen. The entry never stops playing.</span>
>   </li>
> </ol>
> 
> 8.  <span style="font-size: small;"><strong></strong>For both video and overlay, there are 2 options in the provider section:  VAST and OTHER. VAST allows a user to insert a VAST ad tag URL. OTHER is for customers who have created a custom plugin that allows for creating cue points Other, does NOT refer to existing ad plugins such as Tremor, Adap.tv, etc.</span>
> 9.  <span style="font-size: small;"><span style="font-size: small;">If you select overlay, the display time will be indicated next to the Overlay option:<br /></span></span>  
>     <img src="{{site.url}}/assets/244">
> 10. <span style="font-size: small;"><strong></strong>To apply the selected cue points to the player, create a new player or edit an existing one under the “Studio” tab. Within the advertisement portion of the player, make sure that the “Request Ads From Entry’s Cuepoints” is set to “Yes”.</span>