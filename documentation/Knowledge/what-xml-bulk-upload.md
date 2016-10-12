---
layout: page
title: "What is XML bulk upload?"
date: 2011-12-25 21:24:51
---

<span style="font-size: small;">XML Bulk Upload supports full CRUD (Create, Read, Update, and Delete) operations, allowing for ingestion of entries, updates to existing entries, and deletion of bulk entries using an XML format. XML Bulk Upload is the recommended bulk upload option.</span>  
  
<span style="font-size: small;">In addition, XML supports a hierarchical structure while CSV does not. You can define a complete content package using the XML Bulk Upload feature that includes the video source file, its metadata, its custom metadata profiles, distribution profiles, set of transcoding flavors ( for cases when you are using your own transcoders), thumbnails and other additional relevant data.</span>  
  
<span style="font-size: small;">The advantages of using XML Bulk Upload are:</span>  
  


*   <span style="font-size: small;">Simplified integration with other systems (for example, migrating media files including their complete metadata from one server to another).</span>
*   <span style="font-size: small;">A streamlined ingestion mechanism, by using XML it is easy to create automated processes to ingest content.</span>
*   <span style="font-size: small;">More comprehensive ingestion models that allow you to manipulate all of the media entry object attributes and their related objects (such as flavors, custom metadata, access control and distribution profiles, etc.).</span>

  
<span style="font-size: small;">The full sets of features supported by the XML Bulk Upload are described in the <a href="http://www.kaltura.com/api_v3/xsdDoc/?type=bulkUploadXml.bulkUploadXML" target="_blank" title="XML schema document">XSD</a> (the XML template).</span>  
  
<span style="font-size: small;">An example XML file can be found <a href="http://www.kaltura.com/api_v3/xsdDoc/?type=bulkUploadXml.bulkUploadXML" target="_blank" title="XML schema document">here</a> (or downloaded from the KMC Upload menu).</span>  
  
<span style="font-size: small;">The bulk upload status is monitored through the bulk upload log under the Uploads control tab, see Tracking Your Uploads. A log file and a copy of the CSV file are made available for troubleshooting or for historical records of uploaded content. </span>  
  
<span style="font-size: small;">Whether you are a medium sized video publisher or if you're a media giant, you should consider the Bulk Upload option.</span>