---
layout: page
title: "Kaltura MediaPrep Ingest"
date: 2016-08-04 05:40:07
---

<p>
    This article outlines the supported ingest capabilities in Kaltura MediaPrep
  </p>
  
  <div id="main-content" class="wiki-content">
    <ul>
      <li>
        <a href="#video_formats">Video Formats</a>
      </li>
      <li>
        <a href="#captions_support">Captions Support</a>
      </li>
      <li>
        <a href="#multi_audio">Multi Audio Support</a>
      </li>
      <li>
        <a href="#encryption">Encryption at Rest</a>
      </li>
      <li>
        <a href="#metadata">Metadata</a>
      </li>
    </ul>
    
    <p>
      <span style="text-decoration: underline;"><strong><span class="confluence-anchor-link conf-macro output-inline" data-hasbody="false" data-macro-name="anchor"><a name="video_formats"></a></span>Video Formats</strong></span>
    </p>
    
    <p>
      Supported video formats are detailed <a href="{{site.url}}/documentation/Knowledge/what-are-supported-transcoding-formats-saas-edition.html" class="external-link" rel="nofollow">here</a>.
    </p>
    
    <p>
      All formats can be uploaded via Drop Folders/Aspera/API/KMC.
    </p>
    
    <p>
      Some restrictions may apply, when using features such as multiple audio and <a href="#encryption">Encryption at Rest</a>.
    </p>
    
    <p>
      <span style="text-decoration: underline;"><strong><span class="confluence-anchor-link conf-macro output-inline" data-hasbody="false" data-macro-name="anchor"><a name="captions_support"></a></span>Captions Support</strong></span>
    </p>
    
    <p>
      Supported caption formats for ingest are:
    </p>
    
    <ul>
      <li>
        srt
      </li>
      <li>
        DFXP (TTML)
      </li>
      <li>
        WebVTT
      </li>
    </ul>
    
    <p>
      As part of Kaltura's on the fly packaging capabilities, Kaltura takes the ingested caption source format and converts it to the appropriate in band caption format for the specific delivery type (based on the device/browser/OS used for playback). The supported player/delivery caption formats can be found <a href="{{site.url}}/documentation/Knowledge/kaltura-player-capabilities-matrix.html" rel="nofollow">here</a>.
    </p>
    
    <p>
      All the specified formats can be uploaded via Drop Folders/Aspera/API/KMC.
    </p>
    
    <p>
      For WebVTT caption format, Kaltura supports CSS embedded in the VTT file itself. Currently, external CSS files are not supported and should be embedded in the .vtt file prior to ingest.
    </p>
    
    <p>
      <span style="text-decoration: underline;"><strong><span class="confluence-anchor-link conf-macro output-inline" data-hasbody="false" data-macro-name="anchor"><a name="multi_audio"></a></span>Multi Audio Support</strong></span>
    </p>
    
    <p>
      Kaltura currently supports multi audio through a single source ingest of a multi channel tracked video file, for example, ingest of an mp4 container (or any H264/AAC codec file convertible to an mp4 container such as .mxf or .mov). Video files are currently assumed to be tagged appropriately with the relevant language tracks. Support for defining audio tracks explicitly through XML/API ingest is currently under development and intended to be released soon.
    </p>
    
    <p>
      <strong><span class="confluence-anchor-link conf-macro output-inline" data-hasbody="false" data-macro-name="anchor"><a name="encryption"></a></span><span style="text-decoration: underline;">Encryption at Rest</span></strong>
    </p>
    
    <p>
      Kaltura supports storing video content securely by applying an AES CBC encryption per flavor upon transcoding. Configuration of the encryption at rest feature is done through the conversionProfile, and can be configured by the Delivery Desk. Content is decrypted before playback by the packager and encryption on delivery such as DRM or AES is applied.
    </p>
    
    <p>
      <strong>Known Limitations</strong>:
    </p>
    
    <ul>
      <li>
        Encryption at Rest is not supported for progressive download playback (mp4 playback).
      </li>
      <li>
        Entries under 10 seconds will not be encrypted.
      </li>
      <li>
        Only mp4 containers (or any H264/AAC supporting containers such as .mxf that can be converted to mp4) are supported on ingest for Encryption at rest.
      </li>
    </ul>
    
    <p>
      <span style="text-decoration: underline;"><strong><span class="confluence-anchor-link conf-macro output-inline" data-hasbody="false" data-macro-name="anchor"><a name="metadata"></a></span>Metadata</strong></span>
    </p>
    
    <p>
      Metadata can be uploaded to Kaltura using API/KMC/Drop Folders/Aspera.
    </p>
    
    <p>
      When using Drop Folders/Aspera, the native XML support is for the <a href="https://www.kaltura.com/api_v3/xsdDoc/?type=dropFolderXmlBulkUpload.dropFolderXml" class="external-link" rel="nofollow">Kaltura MRSS format</a>. For custom client XML formats (such as CableLabs ADI formats mostly used for Media/OTT), an XSLT needs to be created to map between the custom XML format to the Kaltura MRSS. This XSLT is created by Kaltura Professional Services (some XSLTs such as ADI XSLTs may be available from previous projects) and configured on the relevant conversion profile. Contact your Kaltura representative for more information about creating the XSLT.
    </p>
  </div>