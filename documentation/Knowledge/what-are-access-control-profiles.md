---
layout: page
title: "What are access control profiles?"
date: 2011-12-27 20:28:19
---

Kaltura supports several publication restrictions allowing limited access to content when business requirements dictate it. These restrictions can be placed on the entry level but can also be streamlined to be set automatically or on demand, on a group of items based on a set of criteria, during upload via a bulk upload CSV file, or during an update transaction using Kaltura’s APIs. See <a href="https://developer.kaltura.com/api-docs/#/KalturaResource" target="_blank" title="Kaltura API documentation">Kaltura API</a> documentation.

An Access Control Profile defines authorized and restricted domains where your content can or cannot be displayed, countries from which it can or cannot be viewed, white and black lists of IP addresses and authorized and unauthorized domains in which your media can be embedded. Use the Access Control menu to view existing profiles and create new ones.

Controlled access provides authentication and authorization capabilities. Developer authentication is done using a combination of the Partner ID and one of two “secrets”, each providing a different set of authorization capabilities. In return, a Kaltura Session token (“KS”) is generated, through which API calls can be made.