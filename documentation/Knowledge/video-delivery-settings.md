---
layout: page
title: "Video Delivery Settings"
date: 2013-06-16 21:27:25
---

You can choose between the following types of video delivery settings:

[Kaltura Auto][1] -  The default delivery type. Kaltura server chooses between HTTP Progressive Download and Akamai’s HTTP Adaptive Streaming, based on entry duration and available flavors. Auto gives you the best video delivery and playback quality for your entry.

 [1]: #auto

[HTTP Progressive Download Delivery][2]– Allows you to pause the video playback and wait for the content to download. Typically used where viewers have very limited bandwidth.and might experience more buffering than adaptive bitrate.

 [2]: #progressive

[HTTP Streaming (HDS)][3] - HTTP streaming based on Adobe technology. Allows adaptive bitrate so the player can adjust the video quality on the fly based on network and CPU conditions.

 [3]: #hds

[HTTP Streaming Based on Akamai's Technology][4]– HTTP streaming based on Akamai’s technology. Allows adaptive bitrate so the player can adjust the video quality on the fly based on network and CPU conditions, formally called Akamai HD.

 [4]: #akamai

[RTMP Streaming][5] – RTMP streaming based on Adobe technology. Allows adaptive bitrate so the player can adjust the video quality on the fly based on network and CPU conditions.

 [5]: #rtmp

[Secure Transport (RTMPE)][6] - RTMP encrypted using Adobe's security mechanism which wraps the RTMP session in a lighter-weight encryption layer.

 [6]: #rtmpe

For more information see <a href="http://knowledge.kaltura.com/node/217" target="_blank">Best Practices for Multi-Device Transcoding</a>.

For Kaltura SaaS users, the default delivery format is Kaltura Auto.

For users using MP4 (new flavor set), Akamai HTTP Streaming is the default delivery format. For users using VP6, (old flavor set) Progressive download is the default delivery format.

### <a name="auto"></a>Kaltura Auto

The Kaltura server internal logic chooses between two formats:

*   HTTP Progressive Download
*   Akamai’s HTTP Streaming. 

Based on entry’s characteristics, before playback, the server decides which format is  best for your video delivery and playback quality.

For a video length  <5 minutes (short form) – delivery format will be Progressive Download.

For a video length  >5 minutes (long form) – delivery format will be Akamai HTTP Streaming.

If you have defined an <a href="http://knowledge.kaltura.com/node/447" target="_blank">Access Control Profile</a>, the delivery format will be HDS .

### <a name="progressive"></a>HTTP Progressive Download Delivery

With HTTP Progressive download, the digital media begins downloading and after a specified amount of data becomes available to the video player, the media begins to play while the rest of the data continues to buffer.

[][7]

 [7]: http://www.kaltura.com/content/docs/falconHelp/NetHelp/Documents/akamaihdnetworkallow.htm

### <a name="akamai"></a>HTTP Streaming (Based on Akamai’s Technology)

Akamai's advanced adaptive bitrate streaming technology intelligently adjusts the bit rate of a video stream to ensure the optimum playback quality based on changing bandwidth conditions. It also allows for flavor switching without the loss of content. You can send streaming video over HTTP from an ordinary web server for playback on iPhone and iPad, or other devices, such as desktop computers, without the limitations of Progressive Downloads. An optional feature with this selected delivery setting is that the implementation also provides for media encryption and user authentication over HTTPS, allowing publishers to protect their work.The Akamai HD Network is designed and optimized for large-scale broadcasters and film distributors to increase audience engagement and expand revenues by complementing traditional mediums such as TV and DVD with the Internet.

### <a name="hds"></a>HTTP Dynamic Streaming (HDS) Based on Adobe

HTTP Dynamic Streaming (HDS) enables adaptive bitrate video delivery over regular HTTP connections.

### <a name="rtmp"></a>RTMP Streaming (Legacy)

Adaptive Bit Rate (ABR) streaming is a technique of detecting a viewer's bandwidth capabilities in real time, and then adjusting the quality of the video stream accordingly, always delivering the best possible picture quality. ABR streaming results in less buffering, fast start time and an overall better experience for both high-speed and low-speed connections.

ABR dynamically shifts bandwidth to higher and lower levels based on availability. For Adaptive Bitrate Streaming to work, a video is first encoded at different bitrates to accommodate varying bandwidth connections. Each bitrate version is sliced up into tiny fragments — typically 2 to 10 seconds. The Kaltura player pulls fragments from the different encodings and inserts them into the stream as bandwidth dictates resulting in faster video start times and a continuous, uninterrupted video experience.

For example, a movie called The “Big Movie” is streaming. The end user would view a smoothly playing video. Unknown to the user, multiple streams are actually available and may be seamlessly switched to, if their connection drops lower or improves.  The key here is “seamless”. When adaptive bit streaming is done correctly, there should be no interruption of playback.

For The Big Movie, a player might be serving up the following all at once:

The Big Movie @ 2612 kbps

The Big Movie @ 1600 kbps

The Big Movie @ 1200 kbps

The Big Movie @ 800 kbps

<p class="Sub-Heading">
  USE CASE
</p>

If a user’s connection dropped from over 2.5 Mbps to 1600kbps, the Kaltura player would switch, again seamlessly, from the 2612 bit rate down to the 1600. Often the Kaltura player is designed to begin playing using the lowest possible bit rate so that playback starts immediately. For this example, the 800 kbps stream might be served up first and then as the Kaltura player realizes that the user can handle a higher bitrate, the streaming rate would then be switched up higher.

### <a name="rtmpe"></a>Secure Transport RTMPE (Legacy)

Kaltura supports various methods of securing delivery of video streams (for example,  Progressive download over HTTPS, Akamai HD Network or SWF verification) RTMPE is one of them.

RTMP Encrypted uses Adobe's security mechanism which wraps the RTMP session in a lighter-weight encryption layer.