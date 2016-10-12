---
layout: page
title: "Backend behavior with respect to entitlement and privacy context settings"
date: 2015-05-14 01:59:01
---

This article describes how the Kaltura backend behavior is impacted by the different types of entitlement settings.

*   If the entry is ONLY assigned to categories that have a privacy context, **and** the partner is **checked** with "Default Entitlement Enforcement”:
*   If the KS does not include any entitlements-related privileges:the **entry will not be returned.**
*   If the KS explicitly **disables entitlement: the entry will be returned.**
*   If the KS does not disable entitlements, but defines privacy context (and the right one, of that entry): the **entry will be returned.**

*   if the entry is ONLY assigned to categories that have a privacy context, and the partner is **NOT** checked with "Default Entitlement Enforcement”:
*   If the KS does not include any entitlements-related privileges: the **entry will be returned.**
*   If the KS explicitly disables entitlement:** ethe ntry will be returned.**
*   If the KS does not disable entitlements, but defines a privacy context (and the correct one, for that entry): the **entry will be returned.**

*   If the entry is ONLY assigned to categories that do not have a privacy context
*   If the KS does not disable entitlements, but defines a privacy context (and the correct one for that entry): the **entry will be NOT returned **because it does not belong to the searched privacy context (regardless of  the "Default Entitlement Enforcement”).

*   If the entry belongs to both categories with privacy context and without:
*   If the KS does not include any entitlements-related privileges: the **entry will be returned **(regardless of "Default Entitlement Enforcement”, because it is essentially public.)
*   If the KS explicitly disables entitlement: the **entry will be returned**
*   If the KS does not disable entitlements, but defines a privacy context (and the rcorrect one for that entry): the **entry will be returned.**

You must match the KS to the content that you try to fetch.

--