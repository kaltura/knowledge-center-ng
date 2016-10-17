---
layout: page
title: "How to use the API to validate entry distribution before submission"
date: 2012-01-03 17:26:39
---

To validate an entry distribution by ID before submission, call the [entryDistribution.validate][1] API action.

 [1]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=contentdistribution_entrydistribution&action=validate{% highlight php %}<?php require_once('lib/KalturaClient.php'); $config = new KalturaConfiguration($partnerId); $config->serviceUrl = 'http://www.kaltura.com/'; $client = new KalturaClient($config); $id = null; $client->setKs(''); $results = $client->entryDistribution->validate($id);{% endhighlight %}