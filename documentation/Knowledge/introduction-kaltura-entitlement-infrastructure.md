---
layout: page
title: "Introduction to the Kaltura Entitlement Infrastructure"
date: 2012-06-18 02:19:09
---

Kaltura’s core platform provides a built-in infrastructure for controlling and managing end-user entitlements to content. This infrastructure includes the required attributes and permission controls as well as the server utilities for enforcing those controls.

Using Kaltura’s entitlement services, MediaSpace was extended to add the following capabilities:

*   **Groups’ media channels - **Provides the capability to set media channels that limit access and contribution of content to members of a specific group of users.
*   **Granular control over user permissions to content - **Provides the capability to define different privacy and permission levels for accessing and managing content in media galleries and group’s media channels.
*   **Personalized Global Search Engine - **Provides the capability for users to easily search and find relevant content from the <span style="text-decoration: underline;">entire set</span> of media they are entitled to access.
*   **A Built-in entitlement-based protection to media items - **Control of content entitlement rules for content published inside and/or outside of MediaSpace. 

## Kaltura MediaSpace Related Terminology

The following MediaSpace terms are used within this document to demonstrate the utilization of Kaltura’s entitlement services in MediaSpace 4.0:

*   **MediaSpace Galleries** –Represent the structured, centrally curated media galleries that are available from the MediaSpace top menu and side navigation.  The MediaSpace Galleries may be organized around specific topics in either hierarchal or flat navigation layout. When MediaSpace is used as a company/institution-wide media portal - the MediaSpace Galleries are usually shared with the entire organization and may even become available to the public on the web.
*   **MediaSpace Channels –** Represent the media collections that may be created and/or managed by authorized users within the organization for any purpose. The MediaSpace Channels may be created for specific groups within the organization or created by users focusing on specific topics or interest related to the organization activities and projects. 

MediaSpace Channels are available to people in the organization and not open to the public on the web. 3 types of channels are supported in MediaSpace:

*   **Open -** All users are entitled to access the channel and contribute content.
*   **Restricted** – All users are entitled to access the channel, but only specific users are entitled to contribute content.
*   **Private **– Only specific users are entitled to access the channel and contribute content.

A company/Institution-wide shared channel listing is available in MediaSpace for channel searching and content discovery – channels can be searched by tags, topics and social activity criteria.  In addition, each user has direct access to the list of all channels they are granted specific permission to.

In the Kaltura backend - both **MediaSpace Galleries** and **MediaSpace Channels** are based on Kaltura’s **Category** object and its API services.