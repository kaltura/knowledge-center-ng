---
layout: page
title: "How to restrict views with a Kaltura session?"
date: 2011-12-27 21:24:02
---

Often, the user authentication/entitlement mechanism that decides whether a user is entitled to access a specific media entry or not, will reside outside of Kaltura. When the authentication mechanism resides outside Kaltura, we recommend that you use an Advanced Kaltura Session (KS) based Access Control mechanism, that permits access to the media only when a valid Kaltura Session is provided. .The external entitlement mechanism will then generate the valid Kaltura Session when users should be permitted to view the content.

The session is created using a secret. The external entitlement mechanism will then generate the valid KS when users should be permitted to view the content.

Common examples include:

When implementing paid content where the payment gateway is not Kaltura,the server processing the payment will be the mechanism deciding on entitlement. After the payment is processed, the payment server creates a valid Kaltura Session by calling the Kaltura API and passes that KS to the Kaltura player.

When implementing a single-sign-on and permissions mechanism using LDAP or other authentication mechanism outside of Kaltura, the server responsible for user authentication contains the entitlement logic. The authentication server will call the Kaltura API and generate a valid KS when appropriate.

A Kaltura Player marked with tokenized access requires a “session token” to be created and provided during every playback. A session token can only be created by a developer possessing valid credentials and expires after a limited amount of time. Thus, even if an attempt to grab the item’s direct URL is successful, the playback session will soon expire and without possession of the valid credentials, regeneration of a new token will not be possible.

This option is useful to prevent scraping of content from your website or re-sharing of content on other sites that are not yours and provides an additional amount of security to content display.