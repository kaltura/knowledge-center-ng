---
layout: page
title: "WebVTT and HLS Captions Support"
date: 2013-10-11 17:50:56
---

#### **What is WebVTT?**

The <dfn id="dfn-webvtt">WebVTT</dfn> (Web Video Text Tracks) format is intended for marking up external text track resources. The main use for WebVTT files is captioning video content. You can learn more about [WebVTT standard][1] on the w3c site. If you have an Apple developer id, you can also learn about WebVTT with <a href="https://developer.apple.com/videos/wwdc/2012/?id=512" target="_blank" title="apple webVTT">Apples WebVTT media presentation</a>.. 

 [1]: http://dev.w3.org/html5/webvtt/ "WebVTT"

#### **Why would I need to use WebVTT?**

Kaltura players support a few captions formats including [SRT][2] and <a href="http://player.kaltura.com/docs/CaptionsCustomVarsTTML" target="_blank" title="Kaltura Player Captions support">TTML / DFXP</a> which are rendered with the HTML5 or flash player library.  Some devices and platform such as the iPhone and some smartTVs do not support HTML controls and instead use the native player controls when playing content from webviews.

 [2]: http://player.kaltura.com/docs/CaptionsKalturaApi "Captions API"

To deliver captions to these devices the captions must either be part of the video file itself or referenced in streaming file. Apple supports referencing WebVTT in the streaming mainfest or m3u8 file.

#### **What Devices Support HLS and WebVTT?**

The wikimedia article on HLS, provides a good overview of <a href="https://en.wikipedia.org/wiki/HTTP_Live_Streaming#Clients" target="_blank" title="Wikimedia HLS">clients that support HLS</a>. Kaltura is working to evolve our listed of officially supported devices, today we primarily test WebVTT HLS on iOS devices ( iPad and iPhone). Some other devies support HLS, while not the latest features like WebVTT. Watch this space for updates on OTT device targets.     

#### **How does Kaltura support WebVTT?**     

Kaltura supports ingestion of WebVTT format files as well as automatic conversion of WebVTT on the fly from SRT or TTML source. Kaltura recommends srt or TTML source files for maximizing compatibility across platforms and automatically converting to WebVTT.  Kaltura then generates an m3u8 that includes the captions as WebVTT.

#### **How Do I enable WebVTT HLS on my Kaltura Account?**

To enable this feature contact your Customer Success Manager/Account Manager. The CSM/AM will then enable "<span>Captions - Auto generate WebVTT captions"</span>

#### **Sample m3u8 stream with subtitles enabled from Kaltura:**

This is how the m3u8 appears to the iOS device. You can view this [sample m3u8 url with captions here][3].

 [3]: http://cdnbakmi.kaltura.com/p/243342/sp/24334200/playManifest/entryId/0_uka1msg4/flavorIds/1_vqhfu6uy,1_80sohj7p/format/applehttp/protocol/http/a.m3u8

#EXTM3U  
#EXT-X-MEDIA:TYPE=SUBTITLES,GROUP-ID="subs",NAME="English",DEFAULT=YES,AUTOSELECT=YES,FORCED=NO,LANGUAGE="eng",URI="http://cdnbakmi.kaltura.com/api\_v3/index.php/service/caption\_captionasset/action/serveWebVTT/captionAssetId/0_ucxlurda/a.m3u8"  
#EXT-X-MEDIA:TYPE=SUBTITLES,GROUP-ID="subs",NAME="French",DEFAULT=NO,AUTOSELECT=YES,FORCED=NO,LANGUAGE="fra",URI="http://cdnbakmi.kaltura.com/api\_v3/index.php/service/caption\_captionasset/action/serveWebVTT/captionAssetId/0_s8saifol/a.m3u8"  
#EXT-X-MEDIA:TYPE=SUBTITLES,GROUP-ID="subs",NAME="German",DEFAULT=NO,AUTOSELECT=YES,FORCED=NO,LANGUAGE="deu",URI="http://cdnbakmi.kaltura.com/api\_v3/index.php/service/caption\_captionasset/action/serveWebVTT/captionAssetId/0_k74wquon/a.m3u8"  
#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=450560,RESOLUTION=480x352,SUBTITLES="subs"  
http://kalturavod-vh.akamaihd.net/i/p/243342/sp/24334200/serveFlavor/entryId/0\_uka1msg4/flavorId/1\_vqhfu6uy/index\_0\_av.m3u8  
#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=855040,RESOLUTION=480x352,SUBTITLES="subs"  
http://kalturavod-vh.akamaihd.net/i/p/243342/sp/24334200/serveFlavor/entryId/0\_uka1msg4/flavorId/1\_80sohj7p/index\_0\_av.m3u8

#### **How will Captions Appear on the iPhone?**

<img src="../../assets/1299.img">