---
layout: page
title: "Best Practices For Multi-Device Transcoding"
date: 2011-12-29 03:25:07
---

<p class="mce-heading-2">
  Introduction
</p>

Today video is everywhere. Every site. Every device. Everywhere you turn video is streaming. Consumer eyes are better trained than ever, expecting higher and higher quality with faster and faster service.

Content is king and no one wants their content interrupted because of video buffering, skipped frames or the dreaded crashed player.

The following document details the current Best Practices for Multi-Device Transcoding. Each section will detail the recommended encoding settings and resolutions for the current array of devices along with use cases and background information. 

<p style="text-align: center;">
   <span class="mce-sub-heading" style="text-align: center;">IT'S ALL ABOUT BALANCE</span>
</p>

The challenge of streaming video is to find the right balance between bitrate and resolution as it relates to an end user’s connection speed and system ability. There are far too many variable sthat could interrupt playback for us to account for them all, at least as of the time of this writing. Here is a short list of potential stream killing variables:

*   Device and Screen size
*   Internet Service Provider Connection Speed or Cap
*   Bandwidth available through the wireless router due to distance or usage
*   Network traffic to and from the sever hosting the video
*   The CPU and GPU abilities on the playing device
*   Browser brand and version
*   Available plugins such as Flash and Silverlight
*   Other programs running in the background

These are just the more obvious variables to consider and though we can not control them all we can take steps to avoid or account of most of them.

 

<p class="mce-heading-2">
  Streaming Content
</p>

Content flows to an end users system in a stream of data much like a river might flow from a mountain reservoir to a small town. All content that is viewed on the internet inside an application is considered streaming content. This document focuses on streaming video.

<p class="mce-heading-3">
  Goals Of Streaming Video
</p>

*   Immediate Playback Start
*   Uninterrupted Playback (no “buffering”)
*   Smooth Playback (no frame drops)
*   Highest quality possible

 

<p class="mce-heading-3">
  Adaptive Streaming
</p>

Adaptive streaming is a technique of detecting a users bandwidth capabilities in real time and then adjusting the quality of the video stream accordingly. This results in less buffering, fast start times and overall better experience for both high-speed and low-speed connections. Adaptive streaming works by having multiple bit rates available that the player or server (or CDN) can pull based on the users connection speed and ability. To exemplify this let's pretend we're streaming a movie called "The Big Movie". Though the end user would see a smoothly playing video, unknown to them multiple streams are actually available and may be seamlessly switched to if their connection drops lower or improves. The key here is "seamless". When adaptive is done correctly there should be no interruption of playback.

So for The Big Movie a player might be serving up the following all at once:

*   The Big Movie @ 2612 kbps
*   The Big Movie @ 1600 kbps
*   The Big Movie @ 1200 kbps
*   The Big Movie @ 800 kbps

 

<p class="mce-sub-heading">
  USE CASE:
</p>

If a user's connection dropped from over 2.5 Mbps to say 1600 kbps the video player would switch, again seamlessly, from the 2612 bit rate down to the 1600. Often the player is designed to start on the lowest possible bit rate so that playback starts immediately. So for this example the 800 kbps stream might be served up first and then as the player realizes that the user can handle a higher bitrate it would then switch up.

<p class="mce-heading-3">
  Adaptive Set
</p>

An Adaptive Set is a package of transcodes for the same video that span multiple bit rates and are meant to find a balance between connection speed and resolution.

In order for Adaptive Streaming to provide the optimal viewing experience, all the streams in the Adaptive Set must be in some alignment. Typically, for Desktop and Set Box applications, this means that the frame rates, key frame intervals (GOP size), audio sample rates, and so on should be the same within a set. This is so that as the player switches between bit rates a smooth, seamless switch is achieved without any buffering, stuttering or noticeable audio pops. 

This is not followed, however, when looking at adaptive sets for mobile. When users are viewing content on a mobile device they may be moving in between wireless or cell zones and their signal strength may fluctuate widely. Though we will get into this in more detail in the mobile section generally because of this variable you want your bit rates to not only span possible mobile connections but also be optimized for maintaining the stream – this may mean hard shifts down in bit rates so that the end user does not have their mobile player crash and disengage them from your content and business. Because of this as bit rates go lower the resolution also decreases, as does the frame rate. Frame rates for mobile may go as low as 8 fps. Again, we will get into this in more detail in the Mobile Section. 

Every device has different requirements currently for what they ideally want in an Adaptive Set. This can become overwhelming to video producers, editors and managers as it does, in reality, mean you need many versions of your video files for one video to be playable across multiple devices. This list could go as high as 40 different transcodes that need to take place however do not panic, you do not need to use all 40 if your budget, storage considerations and time do not permit it. You can compromise, but understand that those variables we discussed in the first section of this document may become a factor and cause poor playback. In a later section we will discuss specific device groups and the settings and use cases applicable to each.

* * *

<p class="mce-heading-2">
  General Settings And Concepts
</p>

Before we can dive into the specific device groups and their intended settings it is important to understand the essentials of transcoding. This section will detail the most commonly used settings in this process ranging from GOP size (or I-Frame interval) to resolutions and frame rates and so on.

<p class="mce-heading-3">
  Transcoding
</p>

Let's start with that word "transcoding".  A correctly formatted video master will NOT stream on the internet and must be converted, or transcoded, in order to be viewed. A transcode is made from taking an encoded piece of video and then converting it into one or more newly and more compressed streams that can then be played in a player on a computer or mobile device depending on the settings and methods used.

<p class="mce-sub-heading">
  USE CASE:
</p>

A user wishes to take a piece of video shot in 1920 x 1080 and make it playable in an adaptive player on the internet. In order to do this the Master Video, which is of a high quality at 1080 in resolution, must be converted to at least 3 or more different bitrates that may even scale down in resolution.

<img src="{{site.url}}/assets/198">

Note that the 1920 x 1080 master video which was created at 80 mbps is converted to four different and more compressed bit rates. Though the first on the list is a 1920x1080 resolution the bit rate is only 4000 kbps, much lower than the 80,000 kbps (or 80 Mbps) stream. The next three bitrates that are produced scale down from the 1080 resolution to 720 and then 480 – making this video playable for a wide range of users and connections.

<p class="mce-heading-3">
  Transcoding Methods
</p>

Different methods can be used to transcode video that trade quality for time. An Encoder can choose between at least 3 different encoding methods that effect bit rate and picture quality:

*   CBR - Constant Bit Rate (CBR)
*   VBR - Variable Bit Rate (VBR)
*   2-PASS VBR - 2-Pass Variable Bit Rate

<p class="mce-heading-4">
  CBR
</p>

As the name suggests this method will encode each frame of video with the same bitrate, no matter what his happening in the frame or what is changing from frame to frame. Encodes done in this method often have lower visual quality but also lower file sizes. This method is also the fastest in terms of transcode time. 

<p class="mce-sub-heading">
  USE CASE: 
</p>

A news organization may choose to encode CBR so that the video is outputted quickly enough to make a news deadline. Time for them is more important than video quality. If they choose CBR (or even 1-Pass VBR) they may make the decision to encode it at a medium resolution (say 480) at a mid-level bit rate (say 1200 kbps) so that they can maintain some level of visual quality.

<p class="mce-heading-4">
  VBR
</p>

Unlike Constant, Variable Bit Rate adjusts the amount of bits assigned to a frame depending on what the encoder believes is happening in the frame. This means the bit rate fluctuates over time, going over the average when a complex frame is encountered. How far above the average bit rate is determined by setting the Max Bit rate appropriately. (discussed in a later section)

<p class="mce-heading-4">
  2-PASS VBR
</p>

This is the most recommended method for transcoding when picture quality is important. Like VBR, 2-Pass allows the bit rate to increase for complex scenes (say a rainy scene where every frame is different). Unlike straight VBR 2- Pass does a little more work. It does a first pass at the encode that creates a log file. This file is then used on a second pass to improve quality on difficult scenes. This results in a higher picture quality (fairly significant compared to 1-Pass) and a more consistent stream with fewer data/bit rate spikes.

<p class="mce-heading-3">
  Bandwidth
</p>

Bandwidth refers to the amount of data that a user may be able to receive and/or transmit. Often this is thought in terms of kilobits per second and is separated into both upload and download ability. Internet Service Providers tend to cap these data rates depending on the plan that the user has purchased which presents a challenge to content creators as they try to meet the needs of a broad range of users who have a varied range of bandwidths.

<p class="mce-note-graphic">
  NOTE: According to Cisco's report Mobile connections in the U.S. currently are at 1,059 kbps and by 2014 should be, per their forecast, 2902 kbps.
</p>

A U.S. customer may only have a connection as low as around 3 Mbps or, if they could afford a better plan, up to 50 Mbps – that's an incredibly wide range of possible connections for which to account and presents a challenge. On one hand a content creator wants their guests to experience the highest level of quality, but on the other hand that guest may simply not be capable of handling that quality. So a balance, yet again, must be considered.

<p class="mce-heading-3">
  Bit Rate
</p>

A Bitrate is a measurement of data speed across a network, often in Kilobits per second or kbps (1000 bits per second). This number correlates with potential bandwidth levels that a user may experience and should be in balance to the resolution of the stream. 

<p class="mce-sub-heading">
  USE CASE:
</p>

A household who's data plan is limited to 3 Mbps can not handle a bit rate that peaks to over 2500 kbps. You may think that because their data plan says they can handle up to 3000 kbps (that's 3 Mbps in kilobits) that they would be able to use all of that bandwidth for streaming. There a couple of reasons why this isn't the case. First – an average data rate of around 2500 kbps may spike to at least 30% and at times up to and even over 50% of the average at various points in the video stream if the content creator has transcoded using variable bit rate, which is a common method. Secondly – the user may have a CPU that cannot take advantage of the entire 3 Mbps, especially if other programs are active in the background. This could be because they have an older system and have yet to be able to upgrade.

<p style="text-align: left;">
  <em>Example: AT&T's ISP Connections By Data Plan (<a href="http://www.att.com/shop/internet/?gnLinkId=s2004#fbid=o2ZQRgwaUXE" target="_blank">Source</a>):</em>
</p>

<img src="{{site.url}}/assets/199">

If you are using Akamai  HD HTTP Streaming bit rate spikes are less of an issue as it uses client side caching allowing for a higher threshold – however  if network conditions worsen those spikes may still present a problem. 

<p class="mce-sub-heading">
  USE CASE: A Modern Family -
</p>

A household of four shares the same wireless internet connection but has many devices using that network all at the same time. It is entirely possible that this one household of four could have a father using the internet on his laptop, a mother using an iPhone streaming Pandora, one chid on an Xbox and another streaming a movie in the living room on their HD television using a set top box – all on the same wireless connection! Let's hope that the kid watching the movie in the living room is using adaptive streaming with a wide range of bit rates!

Again it is always about a balance between performance and visual quality. 

<p class="mce-heading-3">
  Average vs. Max Bit Rate
</p>

The Video Bit rate has two main components: The Average and the Max.

 

<p class="mce-heading-3">
  Average Bit Rate
</p>

The average bit rate for video should coincide with the target bandwidth of the end user and should be in balance with the resolution)

Just changing a bit rate alone is not sufficient for dealing with bandwidth limitations and is not recommended. It is advised that low bitrates also scale down in resolution so that the end user has a good balance between image and playback quality.

<p class="mce-sub-heading">
  USE CASE: 
</p>

It is not advisable to send a mobile smart phone user a 1080 resolution at a low bitrate of 500kbps not only because the image quality will be unwatchable but also because the end user, though able to handle 500 kbps, does not possess a system that can comfortably handle 1080 lines of resolution. Potentially such a user would have their player crash or at the least a very poor playback experience if they tried to watch that 1080p video on a smart phone. Additionally low bitrates at high resolutions show larger digital artefacts/errors which make the image look undesirable. At such low bitrates it is better to reduce the resolution so that the resulting video is compressed enough to have a small file size, and then you can rely on the end user's GPU to scale-up.

 

<p class="mce-heading-3">
  Max Bit Rate
</p>

A Max Bit Rate governs the ceiling that a variable bit rate may reach and should be within balance of the average and the target connection/device. Max Bit rates do not effect Progressive Download and some services like Akamai have some built in functionality that limit the impact of bit rate spikes. That being said, not everyone uses Akamai and Progressive download is not often ideal for streaming. (A high max bit rates essentially make the video bitrate unreliable complicating streaming applications.)

Potential Performance Issues Due to a High Max Bit Rate:

*   Frequent or Unwanted Bit Rate Switching
*   Playback Stuttering
*   Frequent Buffering
*   Player Crashing

Industry standards say you should calculate the Max bit rate by taking the Average and adding 50%. It is recommended to reduce this even to 30% in order to create a truly consistent stream but still taking advantage of a variable bit rate. 

<p class="mce-sub-heading">
  USE CASE:
</p>

If a transcoded stream has an Average of say 1400 kbps but spikes at 2600 kbps that user may experience one of the above performance issues.  This is especially true if their bandwidth can only support between 1000 kbps and 2000 kbps, which is highly likely for many users who's ISP's cap their data plans. This would mean that when the stream spiked to 2600 it is outside the threshold that the user can handle and they will have a poor playback experience. Also – remember the earlier example of that family of four all using their devices on the same wireless network!

 

<p class="mce-heading-3">
  Adaptive Bit Rate Requirements
</p>

Bit rates should be at least 400 kbps apart in an adaptive set for the mid range to high range encodes. The lower encodes can be closer together and should scale down in resolution. The two settings, bit rate and resolution, should always be in alignment per industry practice. 

There is no need to create a low bit rate for 720 and higher resolutions for two primary reasons – first image quality would be very poor as the loss of detail would become too great for a good viewing experience and secondly because a lower bitrate may be being consumed by a mobile device that can not handle a high resolution. For example - a 3GS iPhone can not stream 720 or higher resolution video without taxing the devices system and causing poor performance. Content creators want to reach the largest possible audience – it is always important to consider backwards compatibility when designing adaptive sets. More recent devices may have more latitude, especially newer 4G and Tablets such as the iPad 2. Later in this document we will detail potential adaptive sets for various devices.

<p class="mce-note-graphic">
  NOTE: Lower bitrates are NOT meant to look perfect. They are only meant to keep the signal from being interrupted and to minimize the risk of the player crashing. The hope is that these lower bitrates only appear briefly while the users bandwidth fluctuates. See the mobile section for use cases where this is exemplified.
</p>

 

 

<p class="mce-heading-3">
  Resolutions
</p>

The resolution of a video is measured in the height in pixels. A content creator could use any resolution she wanted however there are industry standards to consider. 

Though larger and newer formats are emerging currently the preferred resolutions for streaming are: 

*   480p – (SD) Standard Definition
*   720p – (hd) mini-high definition
*   1080p – (HD) True High Definition

<p class="mce-heading-4">
  HD – 1080p
</p>

True High Definition, HD, is defined as 1080 lines of horizontal progressive resolution.  Think of your television as a series of very small lines – these lines make up the image of one frame and are scanned onto the screen in order, one line progressing after the other. Another way to imagine it is to take a painting and cut it into 1080 thin strips that are 1 pixel tall (very small) and then reassemble those strips one at a time in the order they would appear going from the top of the frame to the bottom. This form of High Definition is referred to as 1080p – where the ‘p' stands for progressive and is identified by the HD acronym. The highest resolution possible for Internet streaming is 1920 x 1080, or 1080p.

<p class="mce-note-graphic">
  NOTE: 1080i video also exists and uses an interlaced method similar to standard definition broadcast and along with 720p is the more common, modern broadcast format. 1080i is not used for internet streaming.
</p>

<p class="mce-heading-4">
  hd – 720
</p>

In addition to 1080p and 1080i there is also a 720p resolution. This resolution is used for broadcast television and sometimes, independent filmmaking and home video. It is of a lower resolution than it's big brother 1080 which makes it easier to transmit and store. 

This smaller version of High Definition can sometimes be referred to with the lower case acronym, hd. This is, by the way, not true high definition. High definition must be at least twice the resolution of Standard Definition Video, which is comprised of 525 lines of resolution. 

<p class="mce-sub-heading">
  HISTORY:
</p>

The precursor to the High Definition Television needed to carry a signal over a frequency wave – transmitted through the air from antennae to antennae. This method required bundling all the video and audio information into this signal so that when it reached a television set it was decoded properly. Standard Definition television's used an interlace method to deliver this signal – meaning odd lines where scanned onto the television screen followed then by the even lines. This was accomplished by having one frame of video comprised of two fields – field A would contain the odd scan lines and field B the even – combined, or interlaced, they presented a completed image. Each frame of video contained 525 lines of horizontal resolution. This standard also is referred to as NTSC which is the North American broadcast standard that set the television frame rate, at the time, to 29.97 frames per second. This is in contrast to the European, or PAL, method, which uses 625 lines of resolution at 25 frames per second. 

It is important to understand this history when dealing with modern digital delivery as many users, especially at the Studio Level, may need to handle old footage that was created for analogue standard definition signals and will need to be converted it so that it can be streamed.

<p class="mce-heading-4">
  SD – 480p
</p>

Standard Definition is still used for Internet streaming as it's smaller file sizes and simpler resolution often meets the right balance for end users to have a positive playback experience. Standard Definition for streaming is not the same as broadcast standard definition – though qualitatively they may look similar. For Internet Streaming a common standard definition resolution is 480 progressive lines of resolution, or 480p.

 

<p class="mce-heading-3">
  Resolution Considerations (MOD-16)
</p>

When determining what resolution and/or frame size to use it is important to keep those dimensions divisible by 16. This is because encoders divide the image into 16 x 16 pixel macro blocks. If for some reason 16 is not a possible divisor for you it is also okay to use 8 though some loss in quality may occur. 

 

<p class="mce-heading-4">
  Resolution vs. Dimension
</p>

It is easy to get resolution and dimension confused – primarily because they often refer to the same thing. However Resolution refers to the amount of detail the image has and Dimension only refers to the Aspect Ratio of that image. Both are measured in Width and Height. 

Resolutions should scale according to the desired device and bitrate. It is advisable to not try to scale video up but rather present it in the original resolution of the master.  Scaling up will result in noticeable degradation in picture quality. Likewise is it unadvisable to try to fit a larger dimension (a.k.a. frame size) onto a device that has a smaller resolution. (i.e. trying to fit a 1080 HD image onto an iPhone that can only handle 480 and below)

An Aspect Ratio is indicated by notating the relationship between the width and height in a numerical value such as 133 – now 133 is shorthand and means that for ever 1 unit of height there is 1.33 units of width. The correct way of notating 133 would be 1.33:1 or 1.33x1.

Here are some common Theatrical and Broadcast Aspect Ratios:

<table class="kaltura-table" style="width: 400px;" align="left">
  <caption class="mce-sub-heading">Common Aspect Ratios</caption><tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%;">
        1.33
      </td>
      
      <td style="text-align: left;" align="left">
        Sometimes referred to as Academy Aspect Ratio and is 4x3 content
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%;">
        1.78
      </td>
      
      <td style="text-align: left;" align="left">
        16x9 Television and the most common Film Aspect Ratio
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%;">
        1.66
      </td>
      
      <td style="text-align: left;" align="left">
        An older aspect ratio popular with some filmmakers and animators
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%;">
        1.85
      </td>
      
      <td style="text-align: left;" align="left">
        A very common aspect ratio used a great deal fo 1980-1990's features
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%;">
        2.35
      </td>
      
      <td style="text-align: left;" align="left">
        The next most used aspect ratio for theatrical films after 1.78 
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%;">
        2.40
      </td>
      
      <td style="text-align: left;" align="left">
         A varation on 2.35
      </td>
    </tr>
  </tbody>
</table>

 

 

 

 

 

 

 

 

 

 

 

 

 

 

<p class="mce-note-graphic">
  NOTE: An Aspect Ratio is calculated by dividing the width by the height. 178 is actually 1.78 to 1 as a ratio of that width to height. A Resolution of 848x480 using this formula, for example, comes to 1.766 or rounded up, 1.78 – tradition drops the decimal and so this is simply called 178. As you calculated your resolutions keep this formula and the need to have the resolutions be divisible by 16 in mind (as previously discussed).
</p>

<p class="mce-heading-3">
  Group Of Pictures And I-Frame Intervals
</p>

The key to video encoding is the use of compression – taking a large resolution image as it might appear on 35mm film or HD video and making it viewable by a home user. Though bit rates and resolutions do much of the work to create a balanced viewing experience there are other factors that also contribute to this compression. The most vital of these is the I-Frame Interval, sometimes referred to as the Key Frame Interval or the Instantaneous Decoder Refresh (IDR). All refer to essentially the same thing – the need for a reference frame from which guesses can be made about the subsequent frames. Every frame of video of a master once transcoded is not fully represented. 

<img src="{{site.url}}/assets/201">

Every encoder has the ability to call out how far apart key frames are created – this is referred to as the Key Frame Interval also known as the i-Frame interval.  The frames in between Key frames are called P-Frames (predictive coded picture) and B-Frames (bi-directionally predictive) . P frames make a guess as to what the picture looks like based on those Kay Frames. B frames are additional reference frames that help improve the quality of P-Frames and the overall look of the stream. 

Ideal Key Frame intervals should be between 2 and 4 seconds. Meaning, for a 29.97 fps piece of video, the key frames should be between 60 frames and 120 frames. 

B-Frame usage should be limited to 1 to 2 reference frames – going over 3 reference frames may cause poor playback on some players (Quicktime for example). However, if you are confident that your users will be using players that support B-Frame decoding you can increase these B-Frames to increase picture quality. Understand though that you will be increasing file size which may slow down load times and cause some buffering. 

<p class="mce-sub-heading">
  IMPORTANT CONSIDERATIONS:
</p>

Key Frames are used for a variety of purposes and not just for the compression of the video. They are also Adaptive Switch and Seek Points – an adaptive player will switch bitrates when needed at Key Frames and when seeking on a player's timeline – those seek point are tied to i-Frames. If the Key Frame Interval is too short bit rate switching may happen too frequently and if too long a user's player may crash if a switch is required because the users' bandwidth has dropped. Also if a Key Frame Interval is too close together file sizes increase and the work needed to decode the picture increases causing a poor playback experience, especially for users with mid to low range bandwidths. For seeking considerations an interval that is very long means that a user will not be able to seek within the video between those points – causing a poor experience.

<p class="mce-heading-4">
  Buffer
</p>

The player loads information from a video payload (your encoded video asset) ahead of your real time playback. This buffer should be in balance between the bit rate and connection speed. To calculate the Bitrate Buffer Size all you need to do is take the Average bit rate and add at least 50% so that the buffer would be 150% of Average.

<p class="mce-heading-4">
  Profiles
</p>

There are three primary encoding methods used – these Profiles allow different levels of complexity in the video stream and are useful, if not required, to find that balance between connection and stream. The three levels are:

*   **Baseline –** This is the simplest method used and the most limiting. One would use this setting for mid to low end delivery on a mobile device or for videoconferencing. The image quality will be limited as neither VBR nor B-Frames are allowed.
*   **Main –** Used primarily for standard definition broadcast and streaming. (Level 3.1)
*   **High –** Used for high definition video streams and is the profile used for Blu-Ray authoring.

 

<p class="mce-heading-4">
  Video And Playback Artifacts
</p>

If the above settings are not followed a variety of playback artifacts or errors may appear. These artifacts may include:

*   **Buffering** – If there are huge bit rate spikes or if file sizes are large for various bit rates a player may stop playback and pause – loading the video and waiting for system resources to free up. This also may be because the buffer is set too low during transcoding.
*   **Frame Skips/Drops** – Frames of video may drop if signal strength is not sufficient or if the wrong frame rate was used during transcoding. Resolution may also be a culprit of frame skips. If a user is using an average laptop over a wireless connection in their home, 720 and 1080 resolutions will most likely skip frames, creating a choppy playback experience. 
*   **Stutter** – Like frame skips, frames are dropping, but the perceived experience is that the video is stuttering. This may appear as if a frame is pausing for a split second before catching up to audio which normally does not stutter or skip. (audio typically plays back fine even if video artifacts are present as the two, though bundled in the same container, are treated separately)
*   **Macro-Blocking (or just Blocking)** – The image may appear as a mosaic of blocks – this is often referred to as pixilation.  This especially happens on fast motion scenes or scenes with heavy detail like rain. 
*   **Aliasing** – Lower resolutions do not handle diagonal lines well – these may appear as steps and be jagged rather than smooth diagonals. 
*   **Banding** – Though on a video master an image may appear to have a consistent color, often after transcoding to mid to low bit rates/resolutions that same color appears as a gradient or a series of bands. This is referred to as banding. An encoder, especially if 1-Pass or CBR was used, may not be able to tell the difference between subtle color changes and instead presents them as big changes, rather than subtle shifts. This is most often in sky shots and in animation; the latter is most problematic and challenging to transcode – especially modern CG based animation. Many transcoders have built in algorithms to deal with banding and over time this issue should dissipate. 
*   **Ghosting/Gibbs Effect/Ringing/Mosquito Noise** – The image may seem doubled with the edges of an object seeming to flutter at a high rate. You would see a faint outline around an object or subject in the video that appears to fluctuate from frame to frame.

 

<p class="mce-heading-4">
  Audio
</p>

Audio tends to be simpler to transmit and is significantly lower than a Video bit rate. Audio Bit Rates range from 20kbps up to only 384 kbps (for 5.1 Audio Only) and typically use 44.1 khz per second or 22 khz for a sample rate.

* * *

<p class="mce-heading-2">
  The Best Practices Charts
</p>

Below you will find a series of charts detailing the best practice settings. These are meant as guidelines. You can move from these settings but always remember you are trying to achieve a balance and there are potential consequences for varying from recommendations.

The charts assume 23.98 fps which is fast becoming the standard for media content. If your content is 29.97 (or 30) fps the key frame interval would be all that would need adjustment from what is presented here. For example: The Key Frame interval for the SD-High_2612 at 23.98 fps is 96 (or roughly 4 seconds) if it was instead 29.97 fps the interval, for four seconds, would be 119.

Also, all these charts only reference 16x9, 178 material. Resolutions/Dimensions should be adjusted according to your source. 

<span class="mce-heading-3">Video Masters</span> 

<p style="text-align: center;">
  <em><span class="mce-sub-heading">A transcode is only as good as the Master it was made from.</span></em>
</p>

Transcoding always starts with a Video Master. **The transcode can never be of a better quality than the Master.**

A master file intended for transcoding is often referred to as a Mezzanine file – as it's an intermediary step in the postproduction process. A true 4k uncompressed piece of video is far too large to even play back on most computers and certainly too big  to transcode from as it would take a substantial amount of time to even move the files so that an encoder can pick it up and complete the transcode. 

Ideally the video master should be at the native resolution of active picture – in other words – if the video has an aspect ratio of 178 than the master should be 178, if the video, however, was 235 the master should also be 235 with no burned in matting.

<img src="{{site.url}}/assets/202">

The above is an example of a 1.78 master that contains 2.40 active pictures - meaning that if you looked at this video master on a monitor you would see black mattes recorded, or burned, into the master. If this master was transcoded as 1.78 those black mattes would remain and take away from the image quality by consuming more bits. Mattes should be removed to maximize picture quality and the active picture should be reflected in the final output dimensions.

Here is a chart detailing possible Master settings: 

<table class="kaltura-table" style="width: 300px;">
  <caption class="mce-sub-heading">Assumptions: <br />H.264/MPEG-4 AVC or ProRes 422</caption><thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
         
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;" colspan="2">
        Resolution
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <th class="mce-sub-heading" align="center" valign="middle">
        <p style="text-align: center;">
          Bit Rate
        </p>
      </th>
      
      <th class="mce-sub-heading" style="text-align: center;" align="center" valign="middle">
        Width
      </th>
      
      <th class="mce-sub-heading" style="text-align: center;" align="center" valign="middle">
        Height 
      </th>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%;">
        80 Mbps
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1920
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1080
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%;">
        50 Mbps
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1920
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1080
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%;">
        25 Mbps
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1920
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1080
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%;">
        15 Mbps
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1920
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1080
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%;">
        80 Mbps
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1280
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        720
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%;">
        50 Mbps
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1280
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        720
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%;">
        25 Mbps
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1280
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        720
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%;">
        15 Mbps
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        1280
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%;">
        720
      </td>
    </tr>
  </tbody>
</table>

You may wish to create a sub-master that is easier to transmit to partners and can be used to transcode lesser quality streams. This chart details what a sub-master transcode could look like:

<table class="kaltura-table" style="width: 100%;">
  <caption class="mce-sub-heading">Intermediary Master aka Sub-Master Settings</caption><thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
         Kaltura Flavor Name
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        A/V Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Video Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Audio Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Width 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Height 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Type 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Key Frame Interval 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Frames Per Second 
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
         HD-Master
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        8128 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        8000 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1080 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98 
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        hs-Master
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        8128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        8000 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        720 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98 
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        SD-Master
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        8128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        8000 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98 
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Desktop Settings
</p>

Settings for Desktop applications differ greatly from those used on other devices primarily because a desktop may be able to handle a more complex set of transcodes albeit with a wider variety of potential stream killers. Though desktop can serve up even High Definition most users still do not have home desktop systems nor ISP connections that can stream HD in a manner that is acceptable. Currently HD streams cause skip frames and stuttering and may even crash the video player causing a poor user experience. As bandwidths and devices improve these problems will dissipate but it is important to understand this when designing your desktop bit rates as you must account for what consumers can actually handle, not what you wish they could handle.

The following chart details the Best Practices for Desktop:

<p style="text-align: center;">
   
</p>

<table class="kaltura-table" style="width: 100%;">
  <caption><span class="mce-sub-heading">Desktop Best Practices</span> </caption><thead>
    <tr class="kaltura-table-header">
      <th style="text-align: center;">
        Kaltura Flavor Name
      </th>
      
      <th style="text-align: center;">
        A/V Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Video Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Audio Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Width 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Height 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Type 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Key Frame Interval 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Frames Per Second 
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        HD-High_6128
      </td>
      
      <td style="width: 8%;">
        6128 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        6000
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1080
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        HD-High_5128
      </td>
      
      <td style="width: 8%;">
        5128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        5000
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        720
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        hs-High_4628
      </td>
      
      <td style="width: 8%;">
        3628
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        4500
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        720
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        hd-High_3628
      </td>
      
      <td style="width: 8%;">
        3628
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        3500
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        720
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-High_2612
      </td>
      
      <td style="width: 8%;">
        2612
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        2482
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-High_1616
      </td>
      
      <td style="width: 8%;">
        1616
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1488
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-Med_1028
      </td>
      
      <td style="width: 8%;">
        1028
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        900
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-Med_816
      </td>
      
      <td style="width: 8%;">
        816
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        688
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-Low_552
      </td>
      
      <td style="width: 8%;">
        552
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        488
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        352
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-Low_448
      </td>
      
      <td style="width: 8%;">
        448
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        384
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        352
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Mobile Settings
</p>

Mobile requirements are separated into two device platform sets – iOS for Apple devices and Android/Other for non-Apple mobile devices.

<p class="mce-sub-heading">
  IMPORTANT CONSIDERATIONS:
</p>

Though it may be tempting to try to fit your streaming video to the maximum resolution/dimension of the target device it is not recommended. Each device requires a small buffer to allow processing. This buffer is achieved partially by feeding video at a slightly smaller resolution/dimension than the max allowed for that device. This is improving and even recently Apple has begun adding full resolution to their recommendations – though some playback problems may still occur. This is primarily true for older non-iOS devices.

<p class="mce-heading-4">
  iOS Best Practices (Mobile)
</p>

Apple has strict requirements for how video should stream. The following is based upon their recommendation.

<table class="kaltura-table" style="width: 100%;">
  <caption class="mce-sub-heading">iOS Best Practices</caption><thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Kaltura Flavor Name
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        A/V Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Video Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Audio Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Width 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Height 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Type 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Key Frame Interval 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Frames Per Second 
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        iOS_WIFI_hd_4540
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        4540
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        4500
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        40
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1024 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        576
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        72
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        iOS_WIFI_hd_2540
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        2540
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        2500
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        40
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1024
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        576
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        72
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        iOS_WIFI_SD_1840
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1800
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1800
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        40
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        960
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        544
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        72
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        iOS_WIFI_SD_1240
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1240
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1200
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        40
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        640
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        352
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        72
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        iOS_WIFI_SD_640
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        640
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        600
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        40
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        640
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        352
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        72
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        iOS_CELL_SD_440
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        440
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        400
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        40
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        416
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        234
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        72
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        iOS_CELL_SD_240
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        240
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        200
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        40
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        416
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        234
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        36
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        12
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        iOS_CELL_SD_110
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        150
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        110
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        40
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        416
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        234
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        24
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        8
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-note-graphic">
  NOTE: Apple also recommends creating an audio only bit rate at 64 Kbps. This is so that if the user's connection drops very low between cell zones the stream will not be interrupted and will continue playing, keeping the user engaged, until the signal improves. This audio only bitrate would contain, ideally, a still image that appeared while the audio played back. 
</p>

<p class="mce-sub-heading">
  iOS USE CASE #1: 
</p>

A Media Company has decided to only offer 3 mobile bit rates: 

*   320 x 240 @ 128 kbps
*   480 x 320 @ 414 kbps
*   480 x 320 @ 564 kbps

This Media Company is trying to achieve a lot with just three bitrates. The 320x240 bit rate is an iPod dimension and they feel comfortable with this bitrate showing up on an iPhone or iPad with black bars on all sides. They also have two other bitrates at 320 resolution within 100 kbps of each other which are a bit too close together to create any benefit.

These bitrates will work but will result in potentially a poor user experience as the player may have a difficult time staying on one of the two upper bit rates - the 414 and 564 – and may switch between them. Also if the end user is viewing these on an iPAD 2 with a 4G connection these bitrates would not be using the full potential of that device – that is why it is recommended to have bit rates over 500 for those higher end uses. 

 

<p class="mce-sub-heading">
  iOS USE CASE #2: 
</p>

Consider a real world scenario with a slightly different set of variants:

A single mother is driving from Los Angeles to San Diego with her daughter. Her daughter, age 7, is watching an iPAD 2 during the journey but she is watching a stream that only has 3 bit rates – 1240 kbps, 640 and 440. The content creator likes the look of these on an iPad but doesn't want to go below 440 because of the image quality loss. The daughter is enjoying her film but because they are traveling down a highway they are moving from one zone to another and her signal fluctuates wildly. Because the content creator is not offering a bit rate below 440 the player crashes forcing the mother to either tell her daughter to do something else or she must decide to pull over and reload her child's iPAD and re-launch the player.

 

<p class="mce-note-graphic">
  NOTE: The way iOS works is that each of the above bit rates would be segmented into small chunks (10 seconds to maybe a minute) that are then called by the player one at t time in a progressive manner. This allows the amount of data flowing to a mobile device to be in small enough packets to allow smooth playback, limiting the drag on system resources. 
</p>

<p class="mce-heading-4">
  Android/Other Best Practices (Mobile)
</p>

<table class="kaltura-table" style="width: 100%;">
  <caption class="mce-sub-heading">Android/Other Best Practices<br />*Dimensions/Resolutions reflect Horizontal View Only </caption><thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Kaltura Flavor Name
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        A/V Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Video Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Audio Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Width 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Height 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Type 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Key Frame Interval 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Frames Per Second 
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Low_Edge_80
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        80
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        56
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        24
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        72
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Low_Edge_150
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        150
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        102
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        72
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Low_Edge_250
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        250
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        202
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        256
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        144
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Low_Edge_400
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        400
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        352
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        256
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        144
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Low_3G4G_600
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        600
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        552
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        512
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        288
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Low_3G4G_800
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        800
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        736
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        512
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        288
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Med_4GWiFi_1000
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1000
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        936
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        512
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        288
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Med_4GWiFi_1300
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1300
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1236
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        512
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        288
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Med_4GWiFi_1600
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1600
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1536
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        512
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        288
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        High_4GWiFi_1900
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1900
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1836
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        512
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        288
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        High_4GWiFi_2200
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        2200
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        2136
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        512
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        288
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        High_4GWiFi_2500
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        2500
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        2436
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        512
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        288
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Base
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Adv_4GWiFi_1200
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1200
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1136
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        768
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        432
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Adv_4GWiFi_1600
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1600
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1536
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        768
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        432
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 11%;">
        Adv_4GWiFi_1900
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1900
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1836
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        768
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        432
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        48
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
  </tbody>
</table>

The above bit rates may appear at first to be daunting but remember – you can always pair down a set of bitrates as long as you include a wide enough range. The downside of having too few bit rates spanning several bandwidth levels is that the shift in quality becomes more obvious as the player switches between them. One reason for a larger number is simply to give the end user the smoothest experience. Also for non-iOS devices there is a wider range of possible devices to account for – thus the long list of potential encodes. The above is based on Adobe's recommendation, combining their Variant 8 and 9 charts.

<p class="mce-heading-4">
  Connected Devices Best Practices (Roku, Boxee, TV, etc.)
</p>

<table class="kaltura-table" style="width: 100%;">
  <caption class="mce-sub-heading">Connected Devices Best Practices (Roku, Boxee, TV, etc.)</caption><thead>
    <tr class="kaltura-table-header">
      <th style="text-align: center;">
        Kaltura Flavor Name
      </th>
      
      <th style="text-align: center;">
        A/V Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Video Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Audio Bit Rate 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Width 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Height 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Type 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Key Frame Interval 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 11%; text-align: center;">
        Frames Per Second 
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        HD-High_5128
      </td>
      
      <td style="width: 8%;">
        5128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        5000
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1080
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        hd-High_3628
      </td>
      
      <td style="width: 8%;">
        3628
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        3500
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        720
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        High
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-High_2612
      </td>
      
      <td style="width: 8%;">
        2612
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        2484
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-Med_1616
      </td>
      
      <td style="width: 8%;">
        1616
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        1488
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-Med_1028
      </td>
      
      <td style="width: 8%;">
        1028
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        900
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-Low_816
      </td>
      
      <td style="width: 8%;">
        816
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        688
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        128
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="width: 14%;">
        SD-Low_552
      </td>
      
      <td style="width: 8%;">
        552
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        488
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        64
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Auto
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        Main
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        96
      </td>
      
      <td class="kaltura-table-row-item" style="width: 11%;">
        23.98
      </td>
    </tr>
  </tbody>
</table>

* The above dimensions and bit rates are based on the requirements for the Roku player.

<p class="mce-heading-3">
  Kaltura Transcoding Flavors Best Practices Master Chart
</p>

<a href="http://knowledge.kaltura.com/sites/default/files/Best%20Practices%20Master%20Chart.pdf" target="_blank" title="Kaltura Transcoding Flavors Best Practices Master Chart"><strong>Download the above charts combined as PDF.</strong></a>

<p class="mce-heading-3">
  HTML5 Video Formats Browser Compatibility
</p>

<img src="{{site.url}}/assets/204">

* Denotes Manual Install - meaning user will have to manually install a plugin or application.  
** Possible on some systems if the HTML5 extension for Windows Media Player Firefox plug-in is installed [28] - Note taken from Wikipedia.  
\***| Support for H.264 may be removed shortly as they are trying to strictly use VP8.

Above chart references: 

1.  [http://html5video.org/wiki/Kaltura\_Video\_Library\_Compatibility\_Chart][1] 
2.  <http://en.wikipedia.org/wiki/HTML5_video#Table>
3.  [http://en.wikipedia.org/wiki/Comparison\_of\_container_formats][2]
4.  <http://kb2.adobe.com/cps/141/tn_14159.html>

 [1]: http://html5video.org/wiki/Kaltura_Video_Library_Compatibility_Chart
 [2]: http://en.wikipedia.org/wiki/Comparison_of_container_formats

<img src="{{site.url}}/assets/205">

 * Will not function properly on older smart phones - for those older phones, 3GP is recommended.

 

 