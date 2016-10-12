---
layout: page
title: "How to use the API to add new flavor params"
date: 2012-01-03 17:44:56
---

<p class="mce-note-graphic">
  Kaltura.com SaaS users - Please contact your Kaltura Account Manager to add new flavor params to your account. Configuration of the transcoding layer requires specialized ecnoding expertise.
</p>

 

To add flavor params, call the [flavorParams.add][1] API action.

 [1]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=flavorparams&action=add

<pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;?php
require_once('lib/KalturaClient.php');
$config = new KalturaConfiguration($partnerId);
$config-&gt;serviceUrl = 'http://www.kaltura.com/';
$client = new KalturaClient($config);
$client-&gt;setKs('AddYourKS');
$flavorParams = new KalturaFlavorParams();
$flavorParams-&gt;name = 'YourflavorParamsName';
$flavorParams-&gt;systemName = 'YourflavorParamssystemName';
$flavorParams-&gt;description = 'YourflavorParamsDescription';
$flavorParams-&gt;tags = 'YourflavorParamsTag1, YourflavorParamsTag2';
$flavorParams-&gt;videoCodec = KalturaVideoCodec::FLV;
$results = $client-&gt;flavorParams-&gt;add($flavorParams);
</pre>