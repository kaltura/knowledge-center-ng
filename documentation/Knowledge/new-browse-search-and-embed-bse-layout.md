---
layout: page
title: "New Browse Search and Embed (BSE) Layout"
date: 2014-11-16 17:32:51
---

<p class="mce-heading-1 mce-heading-2">
  General
</p>

A new layout for the Browse Search and Embed (BSE) module is available. The existing BSE, is not being depricated at this stage, and the embeded content will stay in place. All new customers and accounts from this point on will receive the new layout unless configured otherwise by their admin.

<p class="mce-note-graphic">
  The new BSE layout is available in the following BSE supported integrations:
</p>

*   Kaltura Building Block for Blackboard Learn
*   Kaltura Video App for Canvas
*   Kaltura Video Package for Moodle
*   Kaltura Video PLugin for Jive
*   Kaltura Video Extension for IBM Connections
*   Kaltura Video Extension for SharePoint 2013

<p class="mce-heading-1 mce-heading-2">
  <span style="font-size: 18pt;">For the End-User</span>
</p>

The same concept of the BSE module is retained. A user can browse and search media to embed, from 'My Media' or from any other source configured, then embed it into a content type of the hosting application.

Instead of the following two screens in the previous layout:

1.  Select Media
2.  Configure Embed (size, metadata)

only a single screen is available - Select Media. The size is chosen from a drop-down menu.

Clicking the select (no drop down), will embed a 'meduim' size player by default.

<img src="../../assets/1675.img">

<span> In the Kaltura Building Block for Blackboard and SharePoint 2013, the drop down for sizes is not available since the hosting application does not allow you to define the size.</span>

Metadata configuration is mandatory and may be displayed  through an info-button on the player.

<img src="../../assets/1673.img">

Metedata currently includes:

*   >Title - can be presented on the player itself (The Title should be enabled in the KMC studio - 'Title Label'.)
*   Description, upload time, number of views (These parameters should be enabled through the  'Info Screen' plugin in the KMC Studio.)

<img src="../../assets/1672.img">

The embeded screen is a video player only (not a video page as in the previous layout).

<span style="color: #484848; font-size: 18pt; font-weight: bold;">For the KAF Admin</span>

<span style="color: #484848; font-size: x-small;">In the existing Browsandembed module you need to set enableNewBSEUI = yes.</span>

<span style="color: #484848; font-size: 18pt;"><img src="../../assets/1674.img">

<span style="font-size: x-small;"><span style="color: #484848;">The new layout uses a new player ID . After</span><span style="color: #484848;"> you enable the feature, the </span><span style="color: #484848;">BSEPlayerId field has to be filled. You can use the existing player ID, or, if not a </span><span style="color: #484848;">player ID is created on-the-fly by clicking: "CLICK ME to create a new player for the new BSE UI and functionality".</span></span>

<span style="color: #484848; font-size: x-small;">embedSkins fields should disappear as they are not relevant (configurable) in the new layout.</span>