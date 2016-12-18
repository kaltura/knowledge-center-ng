---
layout: page
title: "How To Search Kaltura Entries By Values Of Custom Metadata Fields Using The API"
date: 2012-01-10 16:26:10
---

<p class="mce-note-graphic">
  To use the KMC to search for entries using custom metadata fields, refer to the <a href="http://knowledge.kaltura.com/sites/default/files/Kaltura_Management_Console_%28KMC%29_User_Manual_2.pdf">Kaltura Management Console (KMC) User Manual</a>, Performing a Search Based on Metadata Fields.
</p>

<p class="mce-procedure">
  To use the API to search for entries using custom metadata fields:
</p>

1.  Start a Kaltura session (KS).
2.  <span>Call the <a href="https://developer.kaltura.com/api-docs/#/media.list">media.list</a> API action.</span>
3.  In the *KalturaMediaEntryFilter* parameter, set the *advancedSearch* field to type *KalturaMetadataSearchItem*.
4.  In *KalturaMetadataSearchItem*: 
<ol style="list-style-type: lower-alpha;">
  <li>
    In the <em>advancedSearch</em> field, select one of the advanced search types: <br />- SEARCH_AND<br />- SEARCH_OR
  </li>
  <li>
    In the <em>metadataProfileId</em> field, enter the metadata profile ID.
  </li>
</ol>

5.  In the *KalturaMediaEntryFilter* parameter, set the *advancedSearch* field to type *KalturaSearchCondition*.
6.  Add one or more *KalturaSearchCondition* items. For each item:
<ol style="list-style-type: lower-alpha;">
  <li>
    Set <em>field</em> to the xPath (in the metadata XML) of the field you want to search for. <br />For example, for <em>objectType</em> use:<br /><pre class="brush: as3;fontsize: 100; first-line: 1; ">/*[local-name()='metadata']/*[local-name()='ObjectType']</pre>
  </li>
  
  <li>
    Set <em>value</em> to the value that you want to search for.
  </li>
</ol>

<pre class="brush: php;fontsize: 100; first-line: 1; ">//Include the client library, instantiate a KalturaClient object and create a valid Kaltura Session.

$filter = new KalturaMediaEntryFilter();

$filterAdvancedSearch = new KalturaMetadataSearchItem();
$filterAdvancedSearch-&gt;type = KalturaSearchOperatorType::SEARCH_OR;
$filterAdvancedSearch-&gt;metadataProfileId = 31; // Obtained by calling metadataProfile service and getting the profile ID

$filterAdvancedSearchItems = new KalturaSearchCondition();
$filterAdvancedSearchItems-&gt;field = "/*[local-name()='metadata']/*[local-name()='FieldName']"; // Replace FieldName with the name obtained by calling metadataProfile service and showing defined fields
$filterAdvancedSearchItems-&gt;value = 'FieldValueToSearch';

$filterAdvancedSearch-&gt;items = array($filterAdvancedSearchItems);
$filter-&gt;advancedSearch = $filterAdvancedSearch;

$results = $client-&gt; media -&gt;listAction($filter);</pre>

<p class="mce-note-graphic">
  To obtain the field name (XPath) of custom metadata fields, such as /*[local-name()='metadata']/*[local-name()='WhatEver'], use the MetadataProfile service and listFields <span>action with the metadata profile ID.</span>
</p>

 

<p class="mce-heading-2">
  Searching across multiple metadata profiles
</p>

For more complex queries where search is across multiple metadata profiles, set the advacedSearch attribute to KalturaSearchOperator and chain as many KalturaMetadataSearchItem as needed.

<pre class="brush: php;fontsize: 100; first-line: 1; ">$filter = new KalturaMediaEntryFilter();
$filterAdvancedSearch = new KalturaSearchOperator();
$filterAdvancedSearch-&gt;type = KalturaSearchOperatorType::SEARCH_AND;
$filterAdvancedSearchItems = array();

//first search item: profile 69182, field DepartmentDivision
$filterAdvancedSearchItems1 = new KalturaMetadataSearchItem();
$filterAdvancedSearchItems1-&gt;metadataProfileId = 69182;
$filterAdvancedSearchItems1Items = array();
$filterAdvancedSearchItems1Items1 = new KalturaSearchCondition();
$filterAdvancedSearchItems1Items1-&gt;field = '/*[local-name()=\'metadata\']/*[local-name()=\'DepartmentDivision\']';
$filterAdvancedSearchItems1Items1-&gt;value = 'Marketing';
$filterAdvancedSearchItems1Items[0] = $filterAdvancedSearchItems1Items1;
$filterAdvancedSearchItems1-&gt;items = $filterAdvancedSearchItems1Items;
$filterAdvancedSearchItems[0] = $filterAdvancedSearchItems1;

//second search item: profile 269161, field Country
$filterAdvancedSearchItems2 = new KalturaMetadataSearchItem();
$filterAdvancedSearchItems2-&gt;metadataProfileId = 269161;
$filterAdvancedSearchItems2Items = array();
$filterAdvancedSearchItems2Items0 = new KalturaSearchCondition();
$filterAdvancedSearchItems2Items0-&gt;field = '/*[local-name()=\'metadata\']/*[local-name()=\'Country\']';
$filterAdvancedSearchItems2Items0-&gt;value = 'Canada';
$filterAdvancedSearchItems2Items[0] = $filterAdvancedSearchItems2Items0;
$filterAdvancedSearchItems2-&gt;items = $filterAdvancedSearchItems2Items;
$filterAdvancedSearchItems[1] = $filterAdvancedSearchItems2;

// call the list API
$filterAdvancedSearch-&gt;items = $filterAdvancedSearchItems;
$filter-&gt;advancedSearch = $filterAdvancedSearch;
$results = $client-&gt;media-&gt;listAction($filter, $pager);</pre>

<p class="p1">
   
</p>

<p class="p1 mce-heading-2">
  Sorting (ordering) the results according to a custom metadata field
</p>

<p class="p1">
  In your list filter, set the orderBy attribute of the KalturaMetadataSearchItem to the xPath of the desired ordering field, prefixed by either a plus sign (indicating Ascending order) or minus sign (indicating Descending order).
</p>

<pre class="brush: php;fontsize: 100; first-line: 1; ">$filter = new KalturaMetadataSearchItem();
$filter-&gt;orderBy = '+/*[local-name()='metadata']/*[local-name()='FieldName']'; //replace FieldName with the system name of the field to order by.
// Prefix with '+' for ascending and '-' for descending.</pre>

<p class="p2">
   
</p>