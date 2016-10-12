---
layout: page
title: "Recommendations for Submitting an Application to Apple's App Store"
date: 2012-03-11 21:06:13
---

<p class="mce-heading-2">
  <a name="ios"></a>iOS App Publishing Requirements and Recommendations
</p>

Before publishing your application, we recommend that you to take the following steps:

*   Deliver all content using HTTP Live Streaming (HLS)
*   Make sure all content intended to be displayed on Apple devices is encoded properly with the correct flavors
*   Make sure you have a 64Kbps audio stream for all content – Should be – stream with bitrate  lower than 64kbps
*   Verify that you are implementing the correct URL format when calling playlists
*   Download Apple verification tools and make sure you don’t receive any warnings or errors that may cause Apple to reject your application.
*   View your content on all supported display types (Smartphones / Tablets / Apple TV) and try both Wi-Fi and cellular networks (where possible) and confirm good viewing quality. If not, make sure you have enough flavors to support fallbacks and large screen high quality bitrate. If you don’t have access to all types of devices, we may be able to do provide assistance. Please contact Kaltura for further assistance.
*   Once your app is submitted, be patient as it may take up to few weeks for Apple to reply with an answer.

<span class="mce-heading-2">Display Types</span>

Before deciding on sets of flavors suitable for your app, select the display types you want your app to support. When picking up flavors for your app, look at the column describing which display types the flavor is recommended for, and make sure you have your supported display types covered.

<table style="width: 753px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="219">
        <p style="text-align: left;">
          <strong> </strong><strong>Display Type</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="219">
        <p style="text-align: left;">
          <strong>Devices</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="105">
        <p>
          <strong>DPI</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="210">
        <p>
          <strong>Resolution</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="219">
        <p style="text-align: left;">
           Smartphone – Standard Display
        </p>
      </td>
      
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPhone 3GS
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          163
        </p>
      </td>
      
      <td valign="bottom" width="210">
        <p>
          320x480
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="219">
        <p style="text-align: left;">
           Smartphone – Retina Display
        </p>
      </td>
      
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPhone 4
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          326
        </p>
      </td>
      
      <td valign="bottom" width="210">
        <p>
          640x960
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="219">
        <p style="text-align: left;">
           Tablet – Standard Display
        </p>
      </td>
      
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPad 1<sup>st</sup>  and 2<sup>nd</sup> Generation
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          132
        </p>
      </td>
      
      <td valign="bottom" width="210">
        <p>
          1024x768
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="219">
        <p style="text-align: left;">
           Tablet – Retina Display
        </p>
      </td>
      
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPad 3<sup>rd</sup>  Generation
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          260
        </p>
      </td>
      
      <td valign="bottom" width="210">
        <p>
          2048x1536
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="219">
        <p style="text-align: left;">
           TV Screen
        </p>
      </td>
      
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          Apple TV
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          Varies
        </p>
      </td>
      
      <td valign="bottom" width="210">
        <p>
          Varies
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span class="mce-heading-2"><span>Cellular Network Support</span></span>

If you would like to make your content available in a non Wi-Fi environment such as 3G networks, Apple requires you to enable a lower than 64Kbps, audio only, fallback flavor to support low connectivity scenarios.

<div>
  <h2 class="mce-heading-2">
    Long Form Video Content Requirements
  </h2>
  
  <p>
    Apple requires that HTTP live Streaming is used for video content longer than 10 minutes or 5MB for every 10 minutes of data. For consistency and to avoid application rejection from Apple, Kaltura recommends you encode all relevant content for your app using HLS compatible flavors as described in this article.
  </p>
</div>

<div class="mce-heading-2">
  Flavors & Display Types
</div>

The following table lists the recommended flavors per display type. Please use these flavors accordingly for the display types you intend to support:

<table style="width: 765px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="bottom" nowrap="nowrap" width="159">
        <p>
          <strong>Flavor Name</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="71">
        <p>
          <strong>Format</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="87">
        <p>
          <strong>Video Codec</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="63">
        <p>
          <strong>Video Bitrate</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="57">
        <p>
          <strong>Width</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="67">
        <p>
          <strong>Height</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="93">
        <p>
          <strong>Audio Codec</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="64">
        <p>
          <strong>Audio Bitrate</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="105">
        <p>
          <strong>Display type</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          V2-WEB-MBL/Audio-only/55
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          -
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          -
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          -
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          -
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p style="text-align: center;" align="right">
          55
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          Smartphone (required)
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          V2-WEB-MBL/Basic-Small/110
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264b
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>110</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          480
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
           (auto)
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p style="text-align: center;" align="right">
          40
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          Smartphone
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          V2-WEB-MBL/Basic-Small/200
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264b
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>200</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          480
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          (auto)s
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p style="text-align: center;" align="right">
          40
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          Smartphone
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          V2-WEB-MBL/Basic-Small
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264b
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>400</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          480
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          auto
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p style="text-align: center;" align="right">
          64
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          Smartphone, Tablet
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          V2-WEB-MBL/Basic-Small/2
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264m
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>600</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          auto
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          360
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p style="text-align: center;" align="right">
          96
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          Smartphone, Tablet
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          V2-WEB-MBL/Std-Small
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264m
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>900</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          auto
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          360
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p align="right">
          96
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          Tablet
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          V2-WEB-MBL/Std-Large
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264m
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>1500</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          1024
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          auto
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p align="right">
          128
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          Tablet, TV
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          V2-WEB/High-Large
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264h
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>2500</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          (auto)
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          720
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p align="right">
          128
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          TV
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          HD1
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264h
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>4000</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          (auto)
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          1080
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p align="right">
          128
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          TV
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          HD2
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264h
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>6000</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          (auto)
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          1080
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p align="right">
          128
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          TV
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="159">
        <p style="text-align: left;">
          HD3
        </p>
      </td>
      
      <td valign="bottom" width="71">
        <p>
          mp4
        </p>
      </td>
      
      <td valign="bottom" width="87">
        <p>
          h264h
        </p>
      </td>
      
      <td valign="bottom" width="63">
        <p align="right">
          <strong>8000</strong>
        </p>
      </td>
      
      <td valign="bottom" width="57">
        <p align="right">
          (auto)
        </p>
      </td>
      
      <td valign="bottom" width="67">
        <p align="right">
          1080
        </p>
      </td>
      
      <td valign="bottom" width="93">
        <p>
          aac
        </p>
      </td>
      
      <td valign="bottom" width="64">
        <p align="right">
          128
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
          TV
        </p>
      </td>
    </tr>
  </tbody>
</table>

<div class="mce-heading-2">
  URL Format
</div>

When retrieving asset of flavors available for an entry, it is strongly recommended to use the following format: 

http://cdnapi.kaltura.com/p/{partnerId}/sp/{partnerId}00/playManifest/entryId/{entryId}/format/applehttp/protocol/http/a.m3u8.

[][1]By using this format, Kaltura will automatically generate an m3u8 file containing all available flavors for a specific entry that are compliant with the requesting device’s playback capabilities.

 [1]: http://cdnapi.kaltura.com/p/{partnerId}/sp/{partnerId}00/playManifest/entryId/{entryId}/format/applehttp/protocol/http/a.m3u8%20

<div>
  <h2>
    Apple OS Supported Versions
  </h2>
  
  <p>
    Kaltura is officially supporting video playback for the following Apple devices and operating system versions:
  </p>
</div>

<table style="width: 534px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="bottom" nowrap="nowrap" width="219">
        <p style="text-align: left;">
          <strong>Device</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="105">
        <p style="text-align: left;">
          <strong>OS</strong>
        </p>
      </td>
      
      <td valign="bottom" nowrap="nowrap" width="210">
        <p style="text-align: left;">
          <strong>Notes</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPhone 3GS
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p style="text-align: left;">
          iOS 4.x, iOS 5.x
        </p>
      </td>
      
      <td valign="bottom" width="210">
         
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPhone 4
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p style="text-align: left;">
          iOS 4.x, iOS 5.x
        </p>
      </td>
      
      <td valign="bottom" width="210">
         
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPad 1<sup>st</sup> Generation
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p style="text-align: left;">
          iOS 4.x, iOS 5.x
        </p>
      </td>
      
      <td valign="bottom" width="210">
         
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPad 2<sup>nd</sup> Generation
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p style="text-align: left;">
          iOS 4.x, iOS 5.x
        </p>
      </td>
      
      <td valign="bottom" width="210">
         
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          iPad 3<sup>rd</sup> Generation
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p style="text-align: left;">
          iOS 4.x, iOS 5.x
        </p>
      </td>
      
      <td valign="bottom" width="210">
         
      </td>
    </tr>
    
    <tr>
      <td valign="bottom" width="219">
        <p style="text-align: left;">
          Apple TV
        </p>
      </td>
      
      <td valign="bottom" width="105">
        <p>
           
        </p>
      </td>
      
      <td valign="bottom" width="210">
        <p style="text-align: left;">
          Using Airplay
        </p>
      </td>
    </tr>
  </tbody>
</table>

<div>
  <h2>
    Transcoding Existing Content
  </h2>
</div>

If you are managing content with Kaltura that was not encoded for native application use, Kaltura has a process to automatically re-transcode your existing content library. Please contact support for further assistance.

<div>
  <h2>
    Verification Tools
  </h2>
  
  <p>
    Before submitting your application for approval, it is important that you test your content with verification tools Apple providings. Please visit the following URL for downloads and further information from Apple: <a href="https://developer.apple.com/library/ios/#documentation/networkinginternet/conceptual/streamingmediaguide/UsingHTTPLiveStreaming/UsingHTTPLiveStreaming.html" target="_blank">https://developer.apple.com/library/ios/#documentation/networkinginternet/conceptual/streamingmediaguide/UsingHTTPLiveStreaming/UsingHTTPLiveStreaming.html</a>
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
</div>

<span class="mce-heading-2"><span><br /></span></span>