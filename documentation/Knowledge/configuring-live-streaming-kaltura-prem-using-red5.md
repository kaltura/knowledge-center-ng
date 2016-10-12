---
layout: page
title: "Configuring Live Streaming on Kaltura On-Prem Using Red5"
date: 2012-11-05 15:44:01
---

To support a non-Akamai live stream from the KMC, this article describes a workaround on how to configure live streaming through the TestMe Console. Red5 through FMS live streaming can be configured using the process described here.

### Prerequisites:

FMLE (Flash Media Live Encoder) – Can be downloaded from here: <a href="http://www.adobe.com/sea/products/flash-media-encoder.html" target="_blank">http://www.adobe.com/sea/products/flash-media-encoder.html</a>

Make sure you have <a href="http://knowledge.kaltura.com/node/461" target="_blank">created and set a valid Kaltura Session</a>.

<p class="mce-procedure">
  To configure live streaming through the TestMe Console:
</p>

1.  LiveStream->add with the following parameters:  
    <ol style="list-style-type: lower-alpha;">
      <li>
        liveStreamEntry:name => whatever you choose
      </li>
      <li>
        liveStreamEntry:mediaType => LIVE_STREAM_FLASH
      </li>
      <li>
        liveStreamEntry:bitrates => relevant if you want to stream more than 1 bitrate. Could be left as-is. Otherwise edit and add the parameters as you would like to stream them.
      </li>
      <li>
        liveStreamEntry:streamName => anything you like. If you need to stream more than 1 bitrate, include “<strong>%i</strong>” in the name which the Adobe FMLE and the Kaltura backend interpret as the token for bitrate index.
      </li>
      <li>
        liveStreamEntry:streamUrl =>onprem-falcon1/oflaDemo
      </li>
      <li>
        liveStreamEntry:encodingIP1 => the IP address of the machine you are streaming from. From your own computer, get the IP address from: <a href="http://www.whatismyip.com/" target="_blank">http://www.whatismyip.com/</a>.
      </li>
      <li>
        liveStreamEntry:encodingIP2 => the IP address of the machine you are streaming from. From your own computer, get the IP address from: <a href="http://www.whatismyip.com/" target="_blank">http://www.whatismyip.com/</a>
      </li>
      <li>
        sourceType => MANUAL_LIVE_STREAM <br /><strong>Configuring the sourceType parameter to MANUAL_LIVE_STREAM is crucial for the live streaming process to succeed. </strong>
      </li>
    </ol>

2.  Save.  
      
    The live stream should appear as “Ready” in your KMC.
3.  In the FMLE, under the tab “encoding options”, enter the following information:  
    <ol style="list-style-type: lower-alpha;">
      <li>
        In the section titled “video”, find the “Bit rate” section and enter the same bitrates' information as in the live stream entry. Enter the bitrate, height and width information identical to what you entered when creating the live stream entry.
      </li>
      <li>
        In the section titled “stream to flash media server”, enter:
      </li>
    </ol>
    
    *   FMS URL => rtmp://onprem-falcon1/oflaDemo
    *   Stream => the stream name as you entered in the Live Stream Entry along with the **%i **token, if required.
4.  Click “Start” at the bottom of the FME application window.
5.  When selecting "Preview & embed", for the entry in the KMC, the stream will be shown as “OnLine” after several seconds and you can select to play.