---
layout: page
title: "Can KAF be configured differently to make use of another SSO attribute as the category name?"
date: 2015-11-19 22:47:23
---

<p>
    In KAF-based integrations, when looking in the KMC category tree, the categories that represents KAF channels in the external system (e.g. Moodle course, SharePoint site) are named using numbered IDs or GUIDs which sometimes may not even make sense to KMC user, and may complicate ability to locate the gallery within the KMC.
  </p>
  
  <p>
    In KAF-based applications, the integration between the 2 systems is very loosely coupled and relies mostly on the SSO part that identifies the external user and the context for KAF.
  </p>
  
  <p>
    Kaltura uses a context ID from the external system (e.g. Moodle course ID from the Moodle database, SharePoint site GUID) that is both <a href="#unique">unique</a> and <a href="#static">static</a>.
  </p>
  
  <p>
    <strong><a name="unique"></a>Unique: </strong>so that Kaltura will not come across a case that two different contexts will have the same identifier.
  </p>
  
  <p>
    In Kaltura, categories in the same level (i.e. siblings in the tree) cannot have the same name. A unique value is required because the KAF channels are all siblings under the "Channels" category.
  </p>
  
  <p>
    <strong><a name="static"></a>Static: </strong>a value that never changes.
  </p>
  
  <p>
    Due to the fact the integration is loosely coupled, the KAF-based solutions are not aware of events,  for example "course name changed".
  </p>
  
  <p>
    For example, If a value that is not static is used  (can be changed by the system, or by the user) , when the KAF gallery is loaded in the same context after the name was changed - all previously assigned content is lost.
  </p>
  
  <p>
    KAF cannot be configured to use other SSO attributes as category names. In all Kaltura's KAF-based applications, this "configuration" is statically set in the code.
  </p>