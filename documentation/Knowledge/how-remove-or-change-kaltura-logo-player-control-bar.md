---
layout: page
title: "How to remove or change the Kaltura logo from the Player control bar?"
date: 2012-01-06 03:52:08
---

<p class="mce-heading-2">
  Setting UIVars
</p>

To learn about UIVars and how to set the variables in your player, follow the [How to Use ][1]*[Additional Parameters and Plugins][1] article*. 

 [1]: http://knowledge.kaltura.com/faq/how-use-kaltura-player-studios-additional-parameters-and-plugins-uivars

<p class="mce-heading-2">
  Removing the default logo
</p>

How does one remove the small Kaltura Sun Icon from the player control bar?

1.  Copy the following UIVars string to the ”Paste your plug-in line here” box and then click the “go” button.  
    *kalturaLogo.visible=false&kalturaLogo.includeInLayout=false* 
2.  Save and preview your player.

<p class="mce-heading-2">
  Changing the default logo
</p>

How does one change the small Kaltura Sun Icon to a custom icon?

The following instructions will guide users on how to replcae the Kaltura player logo.

1.  Copy the following UIVars string to the ”Paste your plug-in line here” box and then click the “go” button.  
    *kalturaLogo.visible=false&kalturaLogo.includeInLayout=false&mylogo.plugin=true&mylogo.className=Watermark&mylogo.width=30&mylogo.height=30&mylogo.watermarkPath=YOURLOGO&mylogo.watermarkClickPath=YOURURL&mylogo.position=after&mylogo.relativeTo=kalturaLogo* 
2.  Scroll the variables list and find the ***mylogo.watermarkPath*** variable. Change the value of this variable (*YOURLOGO*) to the URL of your desired icon (swf, png or jpg file).
3.  Scroll down and find the ***mylogo.watermarkClickPath*** variable. Change the value of this variable (*YOURURL*) to the URL to which the user will be taken, when clicking on the icon.
4.  Save and preview your player.

 <span class="mce-heading-2">Dynamically setting player logo</span>

Occasionaly, publishers will choose to set a logo based on an entry’s custom metadata field to allow for a dynamically branding the player based on the video being played.

<p class="mce-procedure">
  To create a custom data driven logo follow these steps:
</p>

1.  Make sure that your account have custom data enabled (contact your project manager for more information).
2.  Add a new custom data field: *dynamicLogo**URL* of type text. - This field will point to the URL of the image that will be used as the logo.  
    Make sure the metadata field's system name (appears in the custom metadata fields table left column) has the right spelling and capitalization. 
3.  Add a new custom data field: *dynamicLogoClick**URL* of type text. - This field will point to the URL to which the user will be taken when clicking on the logo.  
    Make sure the metadata field's system name (appears in the custom metadata fields table left column) has the right spelling and capitalization. 
4.  Copy the following UIVars string to the ”Paste your plug-in line here” box and then click the “go” button:  
    * kalturaLogo.visible=false&kalturaLogo.includeInLayout=false&mylogo.plugin=true&mylogo.className=Watermark&mylogo.width=30&mylogo.height=30&mylogo.watermarkPath={mediaProxy.entryMetadata.dynamicLogoURL}&mylogo.watermarkClickPath={mediaProxy.entryMetadata.dynamicLogoClickURL}&mylogo.position=after&mylogo.relativeTo=kalturaLogo&requiredMetadataFields=true*
5.  Save and preview your player.

 

<p class="mce-heading-2">
  Dynamically setting player watermark and click path
</p>

Occasionally, publishers will choose to set a watermark and click path based on a video’s custom metadata field to allow for a dynamically branding the player based on the video being played.

<p class="mce-procedure">
  To create a custom data driven logo follow these steps:
</p>

1.  Make sure that your account have custom data enabled (contact your project manager for more information).
2.  Add a new custom data field: *WatermarkUrl* of type text. - This field will point to the URL of the image that will be used as the watermark.   
    Make sure the metadata field's system name (appears in the custom metadata fields table left column) has the right spelling and capitalization.
3.  Add a new custom data field: *WatermarkClickUrl* of type text. - This field will point to the URL to which the user will be taken when clicking on the watermark.   
    Make sure the metadata field's system name (appears in the custom metadata fields table left column) has the right spelling and capitalization.
4.  Copy the following UIVars string to the ”Paste your plug-in line here” box and then click the “go” button:  
    *watermark.watermarkPath={mediaProxy.entryMetadata.WatermarkUrl}&watermark.watermarkCustomPath={mediaProxy.entryMetadata.WatermarkClickUrl}&requiredMetadataFields=true*
5.  Make sure the metadata fields of the video you are loading in the player contain correct and valid links.
6.  Save and preview your player with the desired video.

 

<p class="mce-note-graphic">
  Be certain that the root of your domain has a valid allowing crossdomain.xml file. <br />Such as <a href="http://www.kaltura.com/crossdomain.xml" target="_blank"><span>http://www.kaltura.com/crossdomain.xm</span><span>l</span></a>. Otherwise, Flash cannot load assets from your domain.<br />To learn more about crossdomain.xml files <a href="http://www.adobe.com/devnet/articles/crossdomain_policy_file_spec.html" target="_blank" title="Cross-domain policy file specification">read this article</a>. 
</p>