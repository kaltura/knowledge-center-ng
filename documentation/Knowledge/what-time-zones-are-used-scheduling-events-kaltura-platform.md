---
layout: page
title: "What time zones are used for scheduling events in the Kaltura Platform"
date: 2014-12-14 23:55:27
---

<p class="mce-heading-4">
  Scheduling the time zone through API or Drop Folders
</p>

1.  The API always uses the Unix timestamp. 
    Note that Unix time is indicatedd in UTC.

2.  Bulk upload uses GMT with the format: YYYY-MM-DDThh:mm:ss (T is just the letter T)
3.  The KMC translates the timestamps to the time zone of the client's computer (for example: GMT-5).