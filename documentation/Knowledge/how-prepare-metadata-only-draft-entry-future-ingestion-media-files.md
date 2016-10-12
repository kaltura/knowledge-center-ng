---
layout: page
title: "How to prepare a metadata-only "Draft" entry for future ingestion of media files"
date: 2013-08-29 16:06:07
---

Draft entries are entries created without actual content, and are used as a container for adding content.

<p class="mce-note-graphic">
  <span>You can add or attach content at a later time, by using the </span><a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?service=baseentry&action=addcontent" target="_blank">BaseEntry->addContent</a><span>  action and use one of the KalturaResource </span><a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaResource">resources</a><span>. See </span><a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaResource" target="_blank">Kaltura API</a><span> documentation.</span>
</p>

<p class="mce-procedure">
  To create a Draft Entry
</p>

1.  Select the Upload tab.
2.  Select **Video Entry** or **Audio Entry**.
3.  In the New Entry Window provide:  
    *   Name (required).
    *   Description
    *   Tags
    *   Categories – use the pencil icon to select a category from the existing category list.
4.  If you have Custom Data for entries, you can edit the Custom Data fields for the entry. For multiple schemas, use the drop down Jump To menu to select the schema for the entry. See <a href="http://knowledge.kaltura.com/node/345" target="_blank">Managing Schemas</a> for more information.
5.  Click Save and Close.

The ingestion status for a Draft entry is No Media. The following is an example of a Draft entry in the KMC.

<img src="../../assets/1142">

 

 

<span style="font-size: small;"> </span>