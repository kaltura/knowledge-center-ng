---
layout: page
title: "KMS Cache Refresh  FAQ"
date: 2015-12-31 01:34:08
---

<p>
    <span>[collapsed title="What is the default KMS cache refresh cycle?"]</span>
  </p>
  
  <p>
    Q: What is the default KMS cache refresh cycle?
  </p>
  
  <p>
    A: The default KMS cache cycle depends on the cached object.
  </p>
  
  <ul>
    <li>
      entries (single, gallery list, etc.) - 10 minutes.
    </li>
    <li>
      categories and other app-related cached objects - 30 minutes
    </li>
    <li>
      users' display name - 24 hours<br />The cache logic is only "TTL" - i.e. when it expires, KMS will recalculate (or re-fetch from API).<br />KMS actively deletes/invalidates items in the cache when needed (when they, or their related items are changed.)
    </li>
  </ul>
  
  <p>
    <span>[/collapsed]</span>
  </p>
  
  <p>
    <span>[collapsed title="Is there a programmatic way to control the cache refresh setting or clear the KMS cache?"]</span>
  </p>
  
  <p>
    Q: Is there a programmatic way to control the cache refresh setting or clear the KMS cache?
  </p>
  
  <p>
    A: You can clear the entire KMS cache using a button in the KMS configuration page (top header). As part of module development , the developer can choose to what length an item would be stored in cache, and will also be responsible for invalidating that length when required.
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Which actions are cached?"]
  </p>
  
  <p>
    Q: Which actions are cached? I’ve had different experienecs between different API calls. For example, when adding/removing a user from a channel it took a cache refresh to see the changes on the Channels list of the user, but after removing a user from a channel the access to the channel itself and its videos was denied immediately.
  </p>
  
  <p>
    A: Almost all API calls are cached, otherwise the application would be extremely slow. The only calls that are not cached may be related to entitlements' checks (i.e. whether the user is a member of a category). If you suspect there's a bug where an action should be reflected immediately - raise it to your Kaltura representative. It may be a bug, but there may be another cause for the problem . For example - some API calls are cached per-user, because their response changes per-user. For example, if you do action A as user X, and expect to see the change in action B with user Y - you may not see the response immediately).
  </p>
  
  <p>
    [/collapsed]
  </p>