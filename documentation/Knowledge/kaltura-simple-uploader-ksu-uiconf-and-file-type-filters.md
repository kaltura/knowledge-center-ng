---
layout: page
title: "Kaltura Simple Uploader (KSU) - uiConf and File Type Filters"
date: 2012-03-27 00:39:02
---

The file types that may be uploaded by the Kaltura Simple Uploader (KSU) are defined in a uiConf xml file that is located on the Kaltura servers and is retrieved by the KUploader using the uiConfId specified in flashVars.

### The following xml shows an example of a uiConf file that enables uploading various  file types:

<div class="geshifilter">
  <div class="xml geshifilter-xml">
    {syntaxhighlighter brush: xml;fontsize: 100; first-line: 1; }<fileFilters default="image"> <fileFilter id="image" description="images" extensions="*.jpg;*.jpeg;*.bmp;*.png;*.gif;*.tif;*.tiff"entryType="1" mediaType="2" /> <fileFilter id="video" description="videos"extensions="*.flv;*.asf;*.qt;*.mov;*.mpg;*.mpeg;*.avi;*.wmv;*.mp4; *.m4v;*.3gp" type="1" entryType="1"mediaType="1" /> <fileFilter id="audio" description="audio"extensions="*.flv;*.asf;*.wmv;*.qt;*.mov;*.mpg;*.avi;*.mp3;*.wav;*. mp4;*.wma;*.3gp" entryType="1"mediaType="5" /> <fileFilter id="media" description="images/videos/audio"extensions="*.qt;*.mov;*.mpg;*.avi;*.mp3;*.wav;*.mp4;*.wma;*.flv;*.asf;*.qt;*.mov;*.mpeg;*.avi;*.wmv;*.m4v;*.3gp;*.jpg;*.jpeg;*.bmp; *.png;*.gif;*.tif;*.tiff" entryType="1" mediaType="‐1" /> <fileFilter id="documents" description="documents" extensions="*.*" entryType="10" mediaType="‐1" /> <fileFilter id="any" description="documents/images/videos/audio" extensions="*.*" entryType="‐1"mediaType="‐1" /> </fileFilters>{/syntaxhighlighter}
  </div>
</div>

The above example enables uploading the following file types:

<ul class="bb-list">
  <li>
    Image files - .jpg, .jpeg, .bmp, .png, .gif, .tif, .tiff 
  </li>
  <li>
    Video files - .flv, .asf, .qt, .mov, .mpg, .mpeg, .avi, .wmv, .mp4, .m4v, .3gp 
  </li>
  <li>
    Audio files - .flv, .asf, .wmv, .qt, .mov, .mpg, .avi, .mp3, .wav, . mp4, .wma, .3gp 
  </li>
  <li>
    Media files (all groups) - .qt, .mov, .mpg, .avi, .mp3, .wav, .mp4, .wma, .flv, .asf, .qt, .mov, .mpeg, .avi, .wmv, .m4v, .3gp, .jpg, .jpeg, .bmp; .png, .gif, .tif, .tiff 
  </li>
  <li>
    Documents - No restriction (any file type can be submitted). The created entry is marked as a document.
  </li>
  <li>
    Any (no group) - No restriction (any file type can be submitted). The created entry will only be hosted on the Kaltura Server - no processing will be performed. (This is useful for using the Kaltura Server just for hosting files).
  </li>
</ul>

<p class="mce-note-graphic">
  Document type entries can be used later by the presentation synch widget and other services, and are converted to swf files after the upload process.
</p>

Use the setMediaType API of the KUploader to select the media type group that the user will be prompted to use when opening the browse window. In the setMediaType API, pass the ID of the desired fileFilter in the uiConf xml.

To create your own uiConf, use the uiconf.add API.