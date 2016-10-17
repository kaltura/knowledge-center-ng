---
layout: page
title: "How to use the API to create a new flavor asset for an existing entry"
date: 2012-02-09 08:40:51
---

To create a new flavor asset for an existing entry, call the [flavorAsset.convert][1] API action.

 [1]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=flavorasset&action=convert{% highlight php %}<?php require\_once('lib/KalturaClient.php'); $config = new KalturaConfiguration($partnerId); $config->serviceUrl = 'http://www.kaltura.com/'; $client = new KalturaClient($config); $client->setKs('AddYourKS'); $entryId = '1\_entryIdString'; $flavorParamsId = 11111; $results = $client->flavorAsset->convert($entryId, $flavorParamsId); {% endhighlight %}