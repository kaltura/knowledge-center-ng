---
layout: page
title: "How to overrule the Kaltura flavor generation policy"
date: 2014-05-28 17:00:13
---

<p class="mce-heading-4">
  Component/Application:
</p>

KMC

<p class="mce-heading-4">
  Problem: 
</p>

The Kaltura default transcoding generation policy attempts to apply optimization logic to avoid generation of redundant flavors and to save both storage and CPU. In most cases the transcoding generation policy applies to creation of higher bit rate flavors when the source bitrate is lower than the flavor bitrate.

<p class="mce-heading-4">
  Solution:
</p>

Transcoding flavors are automatically created from the ingested source file. There is no lower bound for the content ingestion source bitrate. The higher the source bitrate is, the more likely a higher bitrate flavor will be created. You can force the system to create any flavor, including the a higher bit rate flavor than the source flavor.

  
<span class="mce-procedure">To overrule the flavor generation policy in the KMC</span>

1.  Go to Settings and select Transcoding Settings.
2.  Click on the Conversion Flavor for which you would like to create a higher bitrate flavor.  
    The default is set to "Use Kaltura's Optimization" which uses Kaltura's standard conversion logic, where file assets are not created for source files that have a bitrate that is lower than that of the flavor. 
3.  Select "Flavor Generation Policy" to bypass the standard logic.  
    <img src="{{site.url}}/assets/1440">
4.  Click Save. 

The above steps ensure that the selected flavor assets are generated.

<span>Note: A source with a higher bitrate always leads to </span><span>greater quality and less playback issues. </span>  
<span><br /></span>