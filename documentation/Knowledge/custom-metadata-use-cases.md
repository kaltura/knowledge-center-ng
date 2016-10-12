---
layout: page
title: "Custom Metadata Use Cases"
date: 2012-05-28 14:58:39
---

Kaltura supports multiple types of metadata fields, including text, date, list-of-values (controlled lists), all supporting either a single value or multiple values. Kaltura also supports a special type of field called Linked Entries (Entry-id List), which allows assigning a video to a group of related videos.

Textual custom metadata fields are indexed in Kaltura’s search engine, while list-of-values can be used as custom filters in playlists and in media queries.

Custom fields can easily be added through the KMC and more than one schema can be created. More advanced custom metadata capabilities are available via the Kaltura APIs.  
Accessing and entering custom metadata field values can be done via the Custom data tab in the KMC.

Kaltura’s MediaSpace application automatically supports custom metadata fields. Fields that are added or modified through the KMC or via APIs automatically appear in MediaSpace.

Using Kaltura’s APIs it is possible to enhance your own applications with video custom metadata, supporting your interface guidelines and business workflows.

<span class="mce-note-graphic">Custom fields are not provided with added functionality. For example, for the Searchable On custom field: Google Enterprise Search does not automatically make the entry available on Google Enterprise Search. The example reflects a method of creating custom fields to support this functionality.</span>

### Examples of Custom Data Use Cases

The following screenshot displays potential use cases for Kaltura custom metadata:

<img src="{{site.url}}/assets/503">

###  Enriching Information Describing the Video

1.  **Authors**- The video entry supports assigning Authors through a custom metadata field (multi-value text).
2.  **Related Links** - The video entry supports setting Related Links that can be displayed along with the video form (multi-value text)
3.  **Language** - The video entry supports setting Language spoken in the video (single-value controlled list).

### Support for Business Workflows

Using a single value controlled-list field, the video entry supports setting an Approval Status, allowing you to implement tracking of how a video progresses through an approval workflow, and filtering videos based on approval status, so that only relevant stakeholder roles have access to videos in respective statuses.  
  
The KMC and MediaSpace support entering and displaying these workflow statuses. Additional user experience enhancements such as role-based filtering described above can be implemented either as MediaSpace plugins, or using the Kaltura APIs in your application. For solutions focused on role-based gated workflows for media, Kaltura recommends its <a href="http://videos.kaltura.com/media/Add+Media+Flow+in+All+in+One+Video+for+WordPress/1_3pm71e6x#.T8T0vLBzWnk" target="_blank">MediaFlow</a> product.

### Support for Content Management Workflows

Using a single value controlled-list field, the video entry supports setting an Available [Yes|No] attribute, allowing a content manager to decide if a video is available to end-users based purely on editorial decisions, not technical availability.   
  
The KMC and MediaSpace support entering and displaying these fields and values. Creating rule-based playlists based on these fields and values in the KMC, and displaying these playlists in MediaSpace, allows for a simple way to enhance the MediaSpace experience without additional development. Actual filtering of content based on these values can be implemented either as MediaSpace plugins, or using the Kaltura APIs in your application.

### Implementing Search and Indexing Policies

Using two controlled-list fields, one allowing a single value and one allowing multiple values, the video entry supports setting whether it is Searchable or not and if so, on which search engines it will be indexed. While these policies are not relevant in the KMC or in MediaSpace contexts, which only support editing and displaying of these values, respective customer systems, running media queries using the Kaltura APIs, can now adhere to these new policies.

### Normalizing user-entered information

1.  The use of dropdowns and controlled lists instead of free text fields allows you to normalize additional information stored with the video entry, as entered by users. For example, there are only specific languages the user can select through the Language dropdown, making it easier for a content manager to filter content by a specific language, as well as use the Kaltura APIs to run statistics such as ‘which is the most commonly spoken language in our videos?’, ‘how many videos were recorded in Chinese?
2.  Custom lists-of-values can also be used in Kaltura rule-based playlists, allowing you to create dynamic lists of videos, where content is filtered by specific criteria, defined through custom metadata. For example, using the listed fields described in this article, it is possible to create a playlist for ‘All videos in French which are Pending Review’, for displaying  to French content reviewers.
3.  Another rule-based playlist can be created for ‘All videos which are Available and are Searchable On our Portal Federated Search’, and have it used by the enterprise federated search engine performing periodic media queries.

### Making Content More Findable

Custom metadata fields and custom metadata-powered playlists can be displayed in Kaltura’s MediaSpace, allowing users to experience more related content and have more search results returned. Based on the example provided in this article, users can search MediaSpace for all videos authored by John Drake or Betty Cage. Same searches can be performed using the Kaltura APIs, when implemented in customer applications.

### Additional Technical Use Cases

1.  Creating multiple dimensions using multiple schemas. For example, for videos serving several markets, each with their own native language, the same metadata schema can be multiplied per number of spoken languages allowing you to store multiple language-specific values in the same logical field. This allows you to display for the same video, beyond language-specific captions, metadata forms in their market-specific native language.  
    While multi-dimensional schemas can be displayed in the KMC, MediaSpace supports display of only one schema by default. MediaSpace can be extended to display the additional schemas by implementing a MediaSpace plugin.
2.  Custom metadata schemas are stored in Kaltura as XSD definitions.  Kaltura’s APIs can be used to dynamically build metadata forms using XSD, as fields can be automatically generated solely based on the stored definitions. This method is used both by the KMC and MediaSpace and can also drastically reduce customer development cycles.