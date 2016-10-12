---
layout: page
title: "How to locate the ad tag url?"
date: 2012-01-23 13:18:16
---

<span class="mce-heading-1" style="font-size: small;">DFP</span>

<span class="mce-heading-1" style="font-size: small;"></span><span style="font-size: small;">In DFP there is a “Tag Generator” utility in the dashboard to generate the ad tag url. </span>  
<span style="font-size: small;"> The ad tag url (<a href="http://ad.doubleclick.net/pfadx/mysite.com/">http://ad.doubleclick.net/pfadx/mysite.com/</a>... ) is at the bottom of the widget.</span>  
<img src="../../assets/269">

<span class="mce-heading-1" style="font-size: small;">OpenX</span>

<span style="font-size: small;">In OpenX the adtag URL is linked to an OpenX Zone, in the following format:</span>

<p style="padding-left: 30px;">
  <span style="font-size: x-small; font-family: courier new,courier;">http://[<span style="background-color: #ffff00;">OPENX_INSTALL</span>]/fc.php?script=bannerTypeHtml:vastInlineBannerTypeHtml:vastInlineHtml&source=&format=vast&charset=UTF_8&nz=1&zones=z1=[<span style="background-color: #ffff00;">ZONE_ID</span>]<br /> for openX hosted, the URL is d1.openX.org. , <br /> from within your OpenX account you can retrieve the zone Id.<br /> for example  for zone id 150750 in openX hosted the ad tag url would be:<br /> <a href="http://d1.openx.org/fc.php?script=bannerTypeHtml:vastInlineBannerTypeHtml:vastInlineHtml&source=&format=vast&charset=UTF_8&nz=1&zones=z1=150750">http://d1.openx.org/fc.php?script=bannerTypeHtml:vastInlineBannerTypeHtml:vastInlineHtml&source=&format=vast&charset=UTF_8&nz=1&zones=z1=150750</a></span>
</p>

<p class="mce-heading-1">
  <span style="font-size: small;">AdapTV (via VAST)</span>
</p>

<span style="font-size: small;">Copy the “Specific Ad Tag” from the Ad screen</span>

<span style="font-size: small;"><img src="../../assets/270">