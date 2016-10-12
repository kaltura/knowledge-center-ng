---
layout: page
title: "How To Add Fields To Custom Metadata Profile"
date: 2012-02-26 14:17:53
---

<p class="mce-procedure">
  To add custom data fields
</p>

1.  Select the Settings tab and then select the Custom Data menu.
2.  Add a schema. See <a href="https://knowledge.kaltura.com/node/346" target="_blank">Adding a Schema</a>.
3.  Click Add Field.  
    The New Field window appears.<span style="font-size: small;"><br /><img src="{{site.url}}/assets/293">
4.  Select the Field type. See [What fields can be configured in the Kaltura custom metadata schema][1].
5.  Enter values for the field or list.
6.  (Optional) Add a Description, or Full Description.
7.  Click Save. The Custom Fields List is displayed.
8.  Use the up and down arrows to change the order of the fields.<span style="font-size: small;"><br /></span>The following is an example of entering data as a Text Select list for the field Publish Values.<img src="{{site.url}}/assets/687">

 [1]: http://knowledge.kaltura.com/node/343

 

You can add the following types of fields:

 

*   Text field – Values are free text.
*   Text select list – Similar to the text field, also known as List of Values. Allows the publisher to define a list of fields to use. After you enter the values, a select box element enables you to select a value from the existing list (for example, countries or months.)
*   Date - A date field
*   Entry ID list - A list to a different entry (asset) that can be used to create compound structure. Examples include Related Videos and linking a trailer to a full-length film.

 

The following is an example of a Custom Metadata Schema.

 

<span><img src="{{site.url}}/assets/289">

 

As a best practice, we recommend richly mapping your media assets with metadata. This will make your assets more findable and more usable as business objects.

 

You can fill in the values for the defined schema for each media asset (entry). The UI elements are built per the field type supporting text fields, check boxes for multiple selections (from predefined values list), date selector (for date fields), text list (for multiple value fields), and linked entries (for creating structure).

 

The schemas you customize may be used for viewing and editing, as well as for filtering, search, and syndication rules. Custom data may be used as a condition for distributing content. For example, if you are trying to distribute data and a custom data field has been defined and is expected by the distribution channel — if the custom data is not received, the content will not be distributed.

 

Searching (and creating syndication rules) by a custom field is integrated into the KMC UI and work flows. See [How to perform a search based on metadata fields][2].

 [2]: http://knowledge.kaltura.com/node/350

<span style="font-size: small;"> </span>