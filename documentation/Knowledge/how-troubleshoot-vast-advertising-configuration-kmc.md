---
layout: page
title: "How to Troubleshoot VAST Advertising Configuration in the KMC"
date: 2012-01-23 14:32:07
---

<span style="font-size: small;">Here are a few helpful steps to troubleshoot VAST advertising configuration:</span>

<span style="font-size: small;">For VAST ads:</span>

 

1.  <span><span style="font-size: small;">Check that you have a working ad tag URL. Always see that VAST 2.0. 1.0 are also supported for the media file content.</span></span><span style="font-size: small;"><br /></span>
    *   <span style="font-size: small;">An example of a working ad tag URL is at: <a href="http://ox-d.hbr.org/v/1.0/av?auid=35998">http://ox-d.hbr.org/v/1.0/av?auid=35998</a></span>
    *   <span style="font-size: small;">In addition to this, a very helpful site that has working VAST ad tag URLs can be found here: <a href="http://www.iab.net/iab_products_and_industry_services/508676/digitalvideo/vast/vast_xml_samples">http://www.iab.net/iab_products_and_industry_services/508676/digitalvideo/vast/vast_xml_samples</a> .</span>
2.  <span><strong></strong><span style="font-size: small;">Put the ad tag URL in your browser. You should see an XML that clearly shows that it is a VAST XML. Various other criteria will appear in the URL. An important tag to look for is the media file. Take the URL of the media file and make sure it plays properly.<br /></span></span>\<img src="../../assets/276">
3.  <span style="font-size: small;">If the VAST ad tag URL looks valid and the media file plays properly, the next step is to go to Fiddler.(Debugger) The first important thing to look for here is to make sure that the crossdomain is working properly. Here is a working Fiddler response:</span><img src="../../assets/277">
4.  ****<span style="font-size: small;"><span style="font-size: small;"><span style="font-size: small;">If the Crossdomain request/response is red or has some abnormal result like 404, you will need to enable your domain’s crossdomain to allow Kaltura to access it. Here is Kaltura’s crossdomain.xml, which can be provided as an example of a proper crossdomain.xml : <a href="http://www.kaltura.com/crossdomain.xml">http://www.kaltura.com/crossdomain.xml</a>.<br />The next steps are to make sure that the ad is properly being called via Fiddler: </span></span></span><span style="font-size: small;"><img src="../../assets/278">

 