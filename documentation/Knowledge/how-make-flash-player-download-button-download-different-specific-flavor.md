---
layout: page
title: "How to make the flash player download button download a different specific flavor"
date: 2012-05-07 00:02:12
---

<span>Add this additionalParam to the player</span>

<pre><span>key=<span class="highlight"><strong><span>download</span></strong></span>.flavorId</span></pre>

<span>value=FlavorID taken from KMC->Settings->Transcoding Settings->ID (from ID column).</span>

<span>If the flavor does not exist, the flavor will fall back to the default flv.</span>