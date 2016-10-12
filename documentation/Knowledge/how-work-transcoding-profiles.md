---
layout: page
title: "How to work with transcoding profiles?"
date: 2011-12-20 12:59:42
---

If you want to configure your KMC account to support automated content ingestion workflows, you can optionally add default metadata settings from an existing entry. The default entry metadata setting automatically will populate the new content when using each specific transcoding profile.

For example, you want to target two distinct audiences with your videos, the first is public facing videos and the second is internal company videos.

You can create two transcoding profiles, one for each of your target audiences, even though you might convert them to the same flavors you can use different “default metadata settings” so your public facing videos will have their specific metadata values, while the internal company videos can have different fields or data. All this is done automatically after you prepare one template entry for the process.

<p class="Procedure mce-procedure">
  <span style="font-size: small;">To use metadata settings with transcoding profiles</span>
</p>

> 1.  Create the template entry you want to use:  
>     Create a “Draft” entry, using the Upload Tab. See <a href="http://knowledge.kaltura.com/node/341" target="_blank">How to prepare a metadata-only "Draft" entry for future ingestion of media files</a>.
> 2.  Prepare the metadata.  
>     For example: Template Entry for Transcoding Profile X”:  
>     <img src="../../assets/745">
> 
> 3.  If you use custom metadata, edit the entry metadata fields. For example you can enter data that reflects the template data for your company, such as your “company name” field since your company name is unlikely to change.  
>     If you do not use custom metadata, click <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=metadata_metadata" target="_blank" title="Custom Metadata Intro Page">here</a> to learn more about it.   
>     You next have to set the template entry on the transcoding profile.
> 4.  Go to the Settings tab and select the Transcoding Profiles menu.
> 5.  Select the flavors of your default transcoding profile.
> 6.  Click Switch to Advanced Mode link at the bottom of the page.
> 7.  Edit the transcoding profile you wish to create a template entry for, by clicking on it.
> 8.  In the Edit Transcoding Profile window, enter the Entry ID you want to set as the template entry in the Default Metadata Settings field.