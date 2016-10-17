---
layout: page
title: "How to add entitlements to categories"
date: 2012-09-24 16:08:38
---

Entitlement settings may be added to categories integrated in applications to support content entitlement.

From the Integration Settings page you control to which categories in your account, entitlement settings are added and enforced. See <a href="http://knowledge.kaltura.com/node/191" target="_blank">Managing Content Entitlement</a> for more information.

The Entitlement Settings option in the Integration Settings page is available with entitlement account configuration only.

Use the "Privacy Context" to add entitlement to categories.

Privacy Context is a free text label that indicates to which application the entitlement settings apply, for example, “MediaSpace” .The Privacy Context label is used for specific indexing of categories and content associated with it, and should also be configured in the application session (KS) itself.  The Privacy Context configuration for an application guarantees the following:

*   User’s entitlements to content in the application are determined based on the specific categories the application is integrated with. 
*   Categories that are not directly integrated with the application can be used for any content organization and applicative classification purposes. A content item can be shared with such categories with no impact on their visibility to end-users through the application.

In the common case, a single Privacy Context should be set to an entire ‘branch’ within the category-tree, and indicate the application integrated with it. In more complex scenarios, multiple privacy contexts can be set to categories to enable access to content shared between multiple applications within the account, and under the same organizational context.

<p class="Note">
  The Privacy Context is set to categories as part of the MediaSpace installation process. Following this configuration, the MediaSpace categories can be edited to include entitlements settings.
</p>

<p class="Note">
  For any other purposes, entitlements and privacy context can be added to categories from the Integration Settings page in the KMC.
</p>

<p class="mce-procedure">
   To add entitlements to categories
</p>

1.  Select the Settings tab and then select Integration Settings.
2.  In the Entitlement Settings sections click Add Entitlements to Categories.<img src="../../assets/710.img">
3.  Enter the name of the root category integrated with your application/s.
4.  Enter the privacy context label. Multiple labels can be separated by commas. In MediaSpace, the privacy context label is visible through the MediaSpace configuration panel.<img src="../../assets/711.img">
5.  Click Save.  
    Following this action the categories tree is updated in the Kaltura backend, and the privacy context is gradually propagated into all sub categories. This operation may take a few minutes.

<p class="mce-note-graphic">
  If entitlement enforcement is enabled by default in your account, after you complete this step, all content under the category that was set with entitlements (including all sub-categories) will only be accessible through an application that was updated to work with Kaltura’s entitlement services and that is set with the defined privacy context label as part of its session privileges.
</p>