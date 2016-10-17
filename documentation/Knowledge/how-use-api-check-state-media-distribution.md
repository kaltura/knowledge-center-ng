---
layout: page
title: "How to use the API to check the state of media distribution"
date: 2012-01-03 17:28:08
---

To check for validation errors after submitting media for distribution, call the [entryDistribution.get][1] API action.

 [1]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=contentdistribution_entrydistribution&action=get{% highlight php %}<?php require_once('lib/KalturaClient.php'); $config = new KalturaConfiguration($partnerId); $config->serviceUrl = 'http://www.kaltura.com/'; $client = new KalturaClient($config); $id = null; $client->setKs(''); $results = $client->entryDistribution->get($id);{% endhighlight %}