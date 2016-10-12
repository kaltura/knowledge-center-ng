---
layout: page
title: "How to use the API to add a new conversion profile"
date: 2012-01-03 17:41:00
---

To add a conversion profile, call the [conversionProfile.add][1] API action.

 [1]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=conversionprofile&action=add{syntaxhighlighter brush: php;fontsize: 100; first-line: 1; }<?php require\_once('lib/KalturaClient.php'); $config = new KalturaConfiguration($partnerId); $config->serviceUrl = 'http://www.kaltura.com/'; $client = new KalturaClient($config); $client->setKs('AddYourKS'); $conversionProfile = new KalturaConversionProfile(); $conversionProfile->status = KalturaConversionProfileStatus::ENABLED; $conversionProfile->name = 'YourConversionProfileName'; $conversionProfile->isDefault = KalturaNullableBoolean::TRUE\_VALUE; $results = $client-> conversionProfile ->add($conversionProfile);{/syntaxhighlighter}