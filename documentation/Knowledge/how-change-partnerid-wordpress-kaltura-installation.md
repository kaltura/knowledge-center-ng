---
layout: page
title: "How to Change the PartnerID in a WordPress Kaltura Installation"
date: 2012-03-27 17:22:40
---

You may want to install the Kaltura Wordpress plugin to use with an existing Kaltura partner that has already been registered. In the installation process, the plugin prompts you to use an existing Kaltura partner instead of automatically registering one. Howeverm in case you missed did not enter an existing Kaltura partner, and you would like to change the PartnerID, you can do so after the installation. The change is a bit tricky, so following carefully.

### <span style="font-weight: bold;">Prerequisites</span>

<ul class="bb-list">
  <li>
    Kaltura all in one plugin for WordPress installation.
  </li>
  <li>
    An additional Partner ID
  </li>
</ul>

<p class="mce-procedure">
  <span style="font-weight: bold;">To Change the PartnerID in a WordPress Kaltura Installation</span>
</p>

1.  Login to your your WordPress website admin panel.
2.  Go to the Settings page and select All in One Video. The URL should resemble a URL of the following sort: 'http://www.yoursite.com/wp-admin/options-general.php?page=interactive_video'
3.  Add '<span style="font-weight: bold;">&force_registration=true</span>' to the URL which will result in a URL like this: 'http://www.yoursite.com/wp-admin/options-general.php?page=interactive\_video&force\_registration=true . This URL should redirect you back to the partner registration process.
4.  Register for a new partner, or use an existing partner by selecting 'Click here if you already have a Partner ID' at the top of the page (Don't miss it this time!).
5.  Enter your partner ID, CMS email and CMS password to complete the process.

That's it - your Kaltura wordpress plugin will now use a different Kaltura partner.