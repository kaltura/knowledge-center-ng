---
layout: page
title: "What Mobile OS, Devices, and Browsers are Supported by the Kaltura Players?"
date: 2013-01-29 17:58:58
---

<p class="p1">
  <span class="s1"><span class="mce-heading-2">Mobile OS & Devices Video Player Compatibility</span> </span>
</p>

<p class="p1">
  <span class="s1">Native SDKs are available for <a href="http://www.apple.com/ios/" target="_blank">Apple iOS</a> and <a href="http://www.android.com/" target="_blank">Google Android</a> at: <span class="s2"><a href="http://www.kaltura.com/api_v3/testme/client-libs.php" target="_blank">http://www.kaltura.com/api_v3/testme/client-libs.php</a>.</span></span>
</p>

<p class="p2">
  Browser based video playback is compatible for <a href="http://caniuse.com/#feat=video" target="_blank">all devices that support the HTML5 Video element</a>:
</p>

<p class="p2 mce-note-graphic">
  Note, the list below present all browser versions that support the HTML5 video element, and known to be compatible with the Kaltura HTML5 Player, however not all browsers are tested consistently. For a a list of all devices and browsers that were tested on Kaltura, visit: <a href="{{site.url}}/documentation/Knowledge/browsers-and-mobile-devices-tested-kaltura-players.html">Browsers and Mobile Devices Tested With Kaltura Players</a>.
</p>

<p class="p2">
</p>

<p class="p2">
   
</p>

<p class="p1">
  <span class="s1">For Android versions fragmentation compatibility, refer to: <a href="{{site.url}}/documentation/Knowledge/android-platform-fragmentation-and-kaltura-video.html">Android Platform Fragmentation and Kaltura Video</a>.</span>
</p>

<p class="p1">
  <span class="s1">Windows 8 and Internet Explorer 10 are also supported and tested by Kaltura, for more information please refer to: <a href="{{site.url}}/documentation/Knowledge/kaltura-players-and-internet-explorer-10.html">Kaltura Players and Internet Explorer 10</a>.</span>
</p>

<p class="p1">
  <span class="s1">For legacy devices that don't have support for HTML5 Video, Kaltura provides two alternatives:</span>
</p>

1.  For devices that support Mobile Flash 10 and above, Kaltura's Flash Player is supported.
2.  For devices with native video player (but no HTML5 support), Kaltura generates a thumbnail and links to the video which launches the device's native media player.

 

<p class="mce-heading-2">
  Transcoding for Mobile devices and Cross-platform Playback
</p>

Cross-platform video playback support depends on the availability of the video flavors (codec, formats and dimensions) required by the target device's video capabilities.

Due to the fragmentation and variety of codecs, formats, and screen sizes, when planning for cross-platform compatability or mobile reach strategy, publishers are advised to create a list of all major devices to target, and then confirm that their Kaltura account has all the required video flavors configured to support these devices.

To learn more about transcoding profiles and cross-platform video playback, refer to: <a href="{{site.url}}/documentation/Knowledge/best-practices-multi-device-transcoding.html" target="_blank">Best Practices For Multi-Device Transcoding</a>.