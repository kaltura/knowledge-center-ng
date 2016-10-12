---
layout: page
title: "How to use Kaltura API abstract classes"
date: 2012-01-03 17:34:57
---

Abstract classes cannot be instantiated. Therefore abstract have derived classes, but not objects.

For each abstract class, use one of its sub classes.

Each abstract class has a subset of required properties. The specific properties that are required depend on the service/action pair and object used with the sub class.

<p class="APEdocument APEinternal">
  For example, for the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=syndicationfeed&action=add">syndicationFeed.add</a> API, select one of the sub classes listed for the abstract <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaBaseSyndicationFeed">KalturaBaseSyndicationFeed</a> class, such as <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaGenericSyndicationFeed">KalturaGenericSyndicationFeed</a>.
</p>

<p class="APEdocument APEinternal">
  <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaBaseSyndicationFeed">KalturaBaseSyndicationFeed</a> supports <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaGoogleVideoSyndicationFeed">Google</a>, <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaITunesSyndicationFeed">iTunes</a>, <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaTubeMogulSyndicationFeed">TubeMogul</a>, <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaYahooSyndicationFeed">Yahoo</a>, and <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaGenericXsltSyndicationFeed">KalturaGenericXsltSyndicationFeed</a> (a sub class of <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaGenericSyndicationFeed" class="APEdocument APEinternal">KalturaGenericSyndicationFeed</a>). <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaGenericXsltSyndicationFeed">KalturaGenericXsltSyndicationFeed</a> supports running a custom XSLT on the XML feed that the Kaltura system generates internally.
</p>

<p class="APEdocument APEinternal">
  To call the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=syndicationfeed&action=add">syndicationFeed.add</a> API with the <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaGenericXsltSyndicationFeed">KalturaGenericXsltSyndicationFeed</a> sub class:
</p>{syntaxhighlighter brush: php;fontsize: 100; first-line: 1; }<?php require\_once('lib/KalturaClient.php'); $config = new KalturaConfiguration($partnerId); $config->serviceUrl = 'http://www.kaltura.com/'; $client = new KalturaClient($config); $ks = '213mg23433\_q2fq'; //Add your KS here $client->setKs('$ks'); $syndicationFeed = new KalturaGenericXsltSyndicationFeed(); $syndicationFeed->type = KalturaSyndicationFeedType::KALTURA_XSLT; $results = $client-> syndicationFeed ->add($syndicationFeed);{/syntaxhighlighter}