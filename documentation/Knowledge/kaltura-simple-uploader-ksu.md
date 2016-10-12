---
layout: page
title: "Kaltura Simple Uploader (KSU)"
date: 2011-12-29 16:25:14
---

In a simple upload process, the KSU transparent widget plays the role of a service delegator, establishing direct communication between the desktop browser application and Kaltura services.

If you want to enable advanced upload options, such as importing content from external media sources (such as MySpace and Flickr), consider integrating your web application with the Kaltura Contribution Wizard, which is Kaltura’s more sophisticated media uploader/importer widget.

The KSU Widget supports the following functionality for uploading media:

*   Uploading single/multiple media file/s using desktop browser selection
*   JavaScript-enabled configuration of uploaded media type/s, maximum file size, maximum number of uploads, and maximum size of total uploads
*   JavaScript-enabled setting of metadata fields related to the uploaded media

<h2 class="mce-heading-2">
  Generic uiConf for KSU
</h2>

For a set of common media groups and file types, use the generic uiConf:Id = 1103.

You can use the default KSU uiConf to upload the following file formats:

*   Video: .flv, .asf, .qt, .mov, .mpg, .mpeg, .avi, .wmv, .mp4, .m4v, .3gp
*   Image: .jpg, .jpeg, .bmp, .png, .gif, .tif, .tiff
*   Audio: .flv, .asf, .wmv, .qt, .mov, .mpg, .avi, .mp3, .wav, .mp4, .wma, .3gp
*   Media group (video/image/audio): .qt, .mov, .mpg, .avi, .mp3, .wav, .mp4, .wma, .flv, .asf, .qt, .mov, .mpeg, .avi, .wmv, .m4v, .3gp, .jpg, .jpeg, .bmp, .png, .gif, .tif, .tiff
*   Documents: .csv, .doc, .docx, .txt, .xls, .xlsx, .ppt, .pptx, .pdf, .rtf, .tab, .gif, .jpg, .jpeg, .art, .bmp, .tif
*   SWF (flash document): .swf
*   Any (all groups): .swf, .csv, .doc, .docx, .txt, .xls, .xlsx, .ppt, .pptx, .pdf, .rtf, .tab, .mov, .mpg, .avi, .mp3, .wav, .mp4, .wma, .flv, .asf, .qt, .mov, .mpg, .mpeg, .avi, .wmv, .m4v, .3gp, .wav, .mp4, .jpg, .jpeg, .art, .bmp, .png, .gif, .tif, .tiff 

<p class="mce-note-graphic">
  The file format is detected according to the media file extension.
</p>

<p class="mce-note-graphic">
  You can change the supported file types by modifying the <a href="http://knowledge.kaltura.com/kaltura-simple-uploader-ksu-uiconf-and-file-type-filters">uiConf of the KSU widget</a>.
</p>

<h2 class="mce-heading-2">
  GUI Screenshot
</h2>

While the KSU Widget is a GUI-less transparent widget, that triggers a standard desktop browser application for media selection.

  
![Upload Window][1]

 [1]: http://www.kaltura.org/sites/default/files/imagepicker/k/Kalturian/CropperCapture[3].jpg