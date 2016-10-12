---
layout: page
title: "What types of metadata can be used in the KMC?"
date: 2012-02-15 13:05:09
---

## Types of Metadata

Kaltura supports three types of metadata for its media assets.

1.  Technical metadata (read only) – includes the technical attributes of the media file. For example, the file type, duration, file format.
2.  Basic metadata – includes Name, Description, Tags, and Categories’ fields. In addition, Kaltura allows referencing the media entry using an external identifier which can be stored in the Reference ID field.
3.  Custom metadata – includes custom fields, defined under one or more schemas, which allow enhancing any media object into a custom business object.

Commercial users, please contact your account manager to enable this feature in your account.

Technical metadata, also known as system metadata, is generated automatically during ingestion and encoding of the file. All technical metadata information can be accessed through the Kaltura APIs. 

Basic metadata is the information you input to the KMC through the Metadata tab. The Reference ID field allows storing an external identifier for supporting integrations with systems external to Kaltura or can be is used to match a filename to an entry using the Drop Folder feature.  See <a href="http://knowledge.kaltura.com/node/46" target="_blank">Kaltura Drop Folders Service For Content Ingestion</a>. Tags are comma separated and can be used as filters for searching through your content. Categories allow assigning media objects to taxonomies.

Custom metadata, also referred to as Custom Data is stored in a schema, also known as a metadata profile. You can create multiple schemas and assign them to any Kaltura object. The KMC supports schemas for entries and categories only.  To extend the metadata of an entry, you need to create a custom schema. See <a href="http://knowledge.kaltura.com/node/346" target="_blank">Adding a Schema</a>.

Custom data is stored as an XSD schema that you can use to create, edit, and manipulate data. You can also use the XSD schema to generate you own metadata interface. Custom data XSDs are account specific.