---
layout: page
title: "Determining an Encoder's Capabilities"
date: 2015-10-28 14:28:58
---

<p>
    It is important to understand the capabilities of the software and hardware used to encode live streams and how streams are sent to Kaltura.
  </p>
  
  <p>
    Depending on what Kaltura live entry configuration you have chosen, your encoder will either be encoding and outputting single or multiple RTMP streams. This process involves ingesting a feed from production, and encoding this feed into H.264 before outputting over IP to Kaltura.
  </p>
  
  <ul>
    <li>
      Single bitrate streams are less resource intensive on your encoder, since only one stream is being encoded to H.264
    </li>
    <li>
      Multi-bitrate streams are more resource intensive on your encoder, since multiple streams needs to be concurrently encoded to H.264
    </li>
    <li>
      HD streams (720p, 1080p) are more resource intensive on your encoder than smaller definition streams (360p, 540p)
    </li>
  </ul>
  
  <h2 id="DetermininganEncoder'sCapabilities-MonitoringyourEncoder">
    Monitoring your Encoder
  </h2>
  
  <p>
    Most encoders in the market today provide some kind of real-time status information on live stream output:
  </p>
  
  <ul>
    <li>
      <strong>CPU Usage</strong><br />Whatever your configuration - single or multi-bitrate output - your CPU usage should not exceed 80% - 85%.
    </li>
    <li>
      <strong>GPU Usage</strong><br />If you are using an encoder that harnesses both CPU and GPU, your usage on both should not exceed 80% - 85%.
    </li>
    <li>
      <strong>FPS</strong> (frame per second or frame-rate)<br />Your fps should consistently be close to the rate configured on your encoder. For example, if you configured your encoder to output 24fps then the realtime log should show output at approximately 22fps - 25fps. If the fps drops significantly lower than this, check your D<em>ropped Frames</em> log. 
    </li>
    <li>
      <strong>Buffer Usage</strong><br />Many encoders let you configure a buffer, often from 0 - 2000ms. The encoder buffer helps to send out streams without compromise on slower internet lines. If you are dropping frames and are using a slower internet line, try increasing your buffer. A fast internet line (50%+ faster than your combined output bitrate) would use a buffer of approximate 300ms whereas a slower internet line (10% - 20% faster than your combined output bitrate, or a line that is not dedicated).
    </li>
    <li>
      <strong>Dropped Frames </strong><br />If you are consistently dropping frames, either your encoder CPU/GPU usage is too high and therefore your encoder cannot handle the output that has been configured or your internet line is too slow. Dropping frames will cause your live picture to appear jerky. 
    </li>
    <li>
      <strong>Bitrate</strong><br />If you have configured your encoder to stream using CBR (constant bitrate that does not fluctuate), your output bitrate should match your configuration. When using CBR, if the bitrate is dropping, your internet line may not be fast enough. If you have configured your encoder to stream using VBR (variable bitrate that fluctuates according to picture detail), your bitrate will fluctuate somewhat.
    </li>
    <li>
      <span><strong>Flash Queue</strong><br />Certain encoders, such as Wirecast, display a Flash queue which shows how much data is currently buffered on your machine waiting to be transferred to the server. Your Flash queue should be low or empty. If your Flash queue is close to full or completely full, your output bitrate is too high for your internet line or the CPU.</span>
    </li>
  </ul>
  
  <p>
    <span> <img src="../../assets/2504">
  </p>
  
  <p>
    <span><em>Wirecast Real Time Logs</em></span>
  </p>
  
  <p>
    <span><em> <img src="../../assets/2505">
  </p>
  
  <p>
    <span><em>FMLE Real Time Logs</em></span>
  </p>