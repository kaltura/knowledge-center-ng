---
layout: page
title: "Encoders Settings for Kaltura, Akamai Universal Live Streaming"
date: 2013-06-06 02:08:20
---

Kaltura works with Akamai universal streaming to deliver worldwide scalable live video broadcasting for events and live-linear 24/7 broadcasts. Akamai Universal Streaming takes an RTMP stream and then re-packages it for mobile ( HLS ) and flash ( HDS ) delivery. This re-packing process transmuxes the stream and creates respective protocol specific manifest files. Akamai Universal Streaming does not transcode the content. This is an important to note, as the live stream set that you send to Akamai will be the live stream that is delivered to your live viewers. For this reason it’s important that your encoder settings are carefully aligned with the devices you aim to support. It’s also important to test your live stream both on desktop as well as iOS device. In some cases you may need to tweak the settings.

**Important Settings:**

Depending on your content type and production values different encoding settings may apply. But there are a few key settings to keep in mind if you want your content to play well with both HDS and HLS.

**Codec: H.264**

**                **Generally encoders let you select H.264 or vp6, you will want to select H.264 since that is the only thing that will be compatible with HLS devices.

**Codec Profile: ‘main’**

                H.264 comes in a few different profiles. You will want to select  ‘main’. Some encoders such as wirecast appear to work better with "baseline" profile. If you experince some artifacts on mobile you can try setting this to the baseline profile to maximize compatibly.

**KeyFrames: 2 to 4 seconds**

**                **Shorter Keyframe intervals seem to be more compatible with re-packaging live content.

**Audio Codec: AAC**

**                **AAC has in general proved to be more compatible then mp3 audio for transmuxed audio streams.

**Other Settings:**

**                **The other settings are largely dependent on your delivery targets, i.e HD television is very different from a small event where you have limited upstream bandwidth. Often an encoder package will include presents, that are a good starting point for configuring your live stream. Akamai Universal Streaming supports ingest of multiple encodes. This enables adaptive live streaming broadcasts so that viewers with different bandwidth or device constraints can still view the content. Its recommended that you send multiple streams if your point of encode supports it.

**Workflow considerations:**

**                **If you have enabled DVR functionality so that users can seek back in the live stream, its recommended that you do only a single continues broadcast for the duration of the event instead of starting and stopping the broadcast a few times. This can improve your experience and reduce some DVR oddities in rewind windows that appear when you don’t have a continues broadcast timeline.

                Pre-provision more than one stream. It does not hurt to pre-provision a few extra entries, so if you need to, you can switch the broadcast or otherwise use the secondary broadcast point as a backup.             

**Sample working Flash Media Encoder ScreenShot:**

** <img src="{{site.url}}/assets/1061">

**Sample working WireCast encoder ScreenShot: **

 <img src="{{site.url}}/assets/1062">

** **