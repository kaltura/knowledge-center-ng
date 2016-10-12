---
layout: page
title: "Using MediaSpace without Entitlement Features"
date: 2012-09-06 15:04:48
---

You can use MediaSpace without using entitlement features. In the KMC, verify that your MediaSpace category tree does not have Privacy Context. To verify that entitlement is not enabled, confirm that in the KMC under Content>Categories, the Entitlements tab of your root category's Edit Category window is not displayed.

<p class="mce-heading-2">
  <a name="RestrictingCategories"></a>Restricting Categories
</p>

If you do not want to create channels and restrict users using entitlement features, you can restrict categories to specific roles in the MediaSpace Configuration Panel's Categories tab. Only users with the specified role can view media in the restricted category. Only users with adminRole or unmoderatedAdminRole can add media to the restricted category.

For example, *Category1=PrivateUploads|PublicUploads, Category2=PublicUploads*.

<p class="mce-note-graphic">
  NOTE: Use the category name that is displayed in MediaSpace, omitting the number prefix used for setting the category order in the KMC. For example, use <em>Sneak Peek</em>, not <em>4_Sneak Peak</em>. 
</p>

To display only unrestricted categories to MediaSpace users who do not log in, use restricted categories together with the “Allow anonymous=true” option.

<p class="mce-note-graphic">
  NOTE: Known issue: If your site contains a Related playlist that is displayed next to the media player, the Related playlist includes restricted content.  
</p>