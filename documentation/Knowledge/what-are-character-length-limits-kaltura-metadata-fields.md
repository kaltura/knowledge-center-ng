---
layout: page
title: "What are the character length limits on Kaltura metadata fields"
date: 2015-09-24 10:38:11
---

<p>
    <span style="color: #484848; font-size: 18pt; font-weight: bold;">Basic Metadata Fields</span>
  </p>
  
  <p>
    The Kaltura backend enforces the following character limits on basic metadata fields:
  </p>
  
  <p class="mce-sub-heading">
     
  </p>
  
  <p class="mce-sub-heading">
    Entry Object:
  </p>
  
  <ul>
    <li>
      Entry Title (Name): 256 characters
    </li>
    <li>
      Entry Description: ~16000 characters
    </li>
    <li>
      Entry Keywords (Tags): ~16000 characters 
    </li>
  </ul>
  
  <p class="mce-sub-heading">
    Category Object:
  </p>
  
  <ul>
    <li>
      Category Title (Name): 200 characters
    </li>
    <li>
      Category Description: ~16000 characters
    </li>
    <li>
      Category Keywords (Tags): ~16000 characters
    </li>
  </ul>
  
  <p>
    It is not possible to use the characters < > , in category names. They will be replaced by _ (underscore).
  </p>
  
  <p>
    <span class="mce-heading-2">Custom-Metadata Fields</span>
  </p>
  
  <p>
    For custom metadata fields, no matter if they are related to an entry, category, or user, the character length is not limited on stored values.
  </p>
  
  <p>
    However, if the length is greater than 128 characters, the  text field will not be indexed for searching. (The rest of the searchable fields on that entry, and that field on other entries will be searchable as long as they are under 128 chars in value length).
  </p>
  
  <p>
    This limitation is applied per custom metadata field value. In case of a multi-value custom metadata field, if one value is less than 128 chars, and another larger than 128 chars, only the value that exceeds the limit will not be indexed and searchable.
  </p>