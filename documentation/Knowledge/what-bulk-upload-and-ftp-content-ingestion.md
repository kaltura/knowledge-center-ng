---
layout: page
title: "What is bulk upload and FTP content ingestion?"
date: 2011-12-25 21:21:08
---

You can import multiple files per session via a simple comma separated file (CSV) or an XML file. With these options, you can also ingest files from your own FTP server, or any publicly accessible file’s host. Metadata fields can be populated from CSV/XML.  
  
The CSV Bulk Upload file is a simple format. You can use the CSV format for simple content ingestion based on imported source media files and their related metadata. Each entry is added from a single line in the CSV file. Each line includes a path to a media file that will be uploaded and each uploaded media file creates an entry. We recommend a maximum of 500 lines/uploaded media files included within one csv file.

  
The XML Bulk Upload file is based on Kaltura’s MRSS format schema for content ingestion. The XML format enables bulk ingestion of complex video or audio packages.  
  
Complex packages may include:

*   Multiple bit-rate Transcoding Flavors already transcoded by a local transcoder
*   Multiple thumbnails
*   Related metadata and publishing options

 