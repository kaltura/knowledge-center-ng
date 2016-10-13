---
layout: page
title: "Live Encoding Best Practices Guide"
date: 2015-11-11 12:17:44
---

<p>
    <span><a name="top"></a>This article describes the following topics:</span>
  </p>
  
  <ul>
    <li>
      <a href="#overview">Overview of Live Encoding</a>
    </li>
    <li>
      <a href="#connectivity">Connectivity and Basic Hardware</a>
    </li>
    <li>
      <a href="#select_encoder">Selecting an Encoder</a>
    </li>
    <li>
      <a href="#determine">Determining an Encoder's Capabilities</a>
    </li>
    <li>
      <a href="#cfg_encoder">Configuring an Encoder</a>
    </li>
    <li>
      <a href="#validating">Validating Available Broadcast Bandwidth</a>
    </li>
    <li>
      <a href="#ABR">Live Adaptive Bitrate Available Broadcast</a>
    </li>
    <li>
      <a href="#setup_entries">Setting up Live Entries in the KMC</a>
    </li>
  </ul>
  
  <h2>
    <span><a name="overview"></a>Overview of Live Encoding</span>
  </h2>
  
  <p>
    Live content needs to be thought about a little differently from on-demand content.
  </p>
  
  <ul>
    <li>
      The production and management workflows are different
    </li>
    <li>
      The objective is to deliver content that has time relevancy, for example sport, news, weather, executive announcements, etc. Due to the nature of relevancy, the margin for error on live content is extremely low
    </li>
    <li>
      Live content needs to consistently hold attention, therefore much thought needs to be put into how content is packaged to make it interesting and relevant to watch. There is a cost associated with this approach.
    </li>
    <li>
      Live content can be pulled from different areas - for example content may be licensed or content may be created by your production team.
    </li>
  </ul>
  
  <p>
    The following diagram illustrates a typical live workflow that spans production through to delivery.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/2549">
  </p>
  
  <h2>
    Live Production Management Checklist
  </h2>
  
  <p>
    Executing a live production successfully requires focus and resources in several areas. The following is a basic checklist for you to get started:
  </p>
  
  <ul>
    <li>
      <strong>Clean content ingestion from production<br /></strong>Make sure to get your content feed from your production team - which includes video in the correct dimensions, frame rate and with properly mixed audio (the correct levels).
    </li>
  </ul>
  
  <ul>
    <li>
      <strong>IT support<br /></strong>Make sure to have the correct speed internet line for outbound streams, and bandwidth that is dedicated to this task.
    </li>
  </ul>
  
  <ul>
    <li>
      <strong>Use appropriate encoders<br /></strong>Make sure to use encoders that support the number of bitrates you have chosen to output, and that off reliability which aligns with the profile of your event.
    </li>
  </ul>
  
  <ul>
    <li>
      <strong>Security and authentication<br /></strong>For sensitive content that is broadcast to a closed audience, be sure to send your content to a player that is embedded in a secure environment - for example a closed MediaSpace or SharePoint instance.
    </li>
  </ul>
  
  <ul>
    <li>
      <strong>Audience development, marketing and management</strong><br /> How will your audience find your live content? Make sure to put the necessary marketing in place to draw viewers to your event. How will your audience get support? Make sure you are prepared to provide technical and account support to viewers.<br /><br />
    </li>
    <li>
      <strong>Compliance and Live Captions<br /></strong>For viewers that require viewing assistance or would like to view content in a different language, be sure to integrate live closed captions into your content.
    </li>
  </ul>
  
  <p class="Sub-Heading">
    <a href="#top">Back to Top</a>
  </p>
  
  <h2>
    <span><a name="connectivity"></a>Connectivity and Basic Hardware</span>
  </h2>
  
  <p>
    Kaltura delivers to many devices and platforms. While streaming protocols are supported on many viewing devices, Kaltura live features with the Kaltura player are tested on all Kaltura player supported platforms. For more information, see <a href="http://knowledge.kaltura.com/browsers-and-mobile-devices-tested-kaltura-players">Browsers and Mobile Devices Tested With Kaltura Players</a>.
  </p>
  
  <h2>
    System Requirements
  </h2>
  
  <p>
    The following specification outlines the basic system requirements for viewers watching live content.
  </p>
  
  <ul>
    <li>
      A wide number of devices are supported -across Mac, PC, mobile devices, TVs, gaming consoles and more
    </li>
    <li>
      Adobe Flash Player 10.0.32 or above (devices supporting Flash only)
    </li>
    <li>
      Internet Explorer 8.0 or above, Firefox 2.0 or above, Safari 3.0 or above, Chrome 4.0 or above  
    </li>
    <li>
      Microsoft Windows XP SP2, Microsoft Windows Vista, Macintosh OS X v10.4 or above, or Linux 
    </li>
    <li>
      256 megabytes (MB) of RAM - 512 MB recommended
    </li>
    <li>
      JavaScript and Cookies must be enabled.
    </li>
    <li>
      Super VGA (800 x 600) or higher resolution
    </li>
    <li>
      16-bit sound card
    </li>
    <li>
      Speakers/headphones
    </li>
  </ul>
  
  <h3>
    <strong>Internet Connection Speed</strong>
  </h3>
  
  <p>
    Viewers require the following internet connections to successfully view live video:
  </p>
  
  <ul>
    <li>
      For a reliable viewing experience, viewers should have access to download speeds approximately 50% faster than the bitrate they are trying to view. For example, a viewer trying to watch a 700kbps live stream, should have access to a 1.4Mbit/sec (down) internet line. Bear in mind that consumer internet connections are typically not dedicated and speeds fluctuate according to shared usage. 
    </li>
    <li>
      By referencing the above example, you should be able to estimate what internet speeds your viewers required based on the live bitrates you send out from your encoder.
    </li>
    <li>
      Viewers can test connection speed at:<p>
        <a href="http://pa-publish-speedtest.kaltura.com:1935/" target="_blank" title="http://pa-publish-speedtest.kaltura.com:1935/
Cmd+Click or tap to follow the link">http://pa-publish-speedtest.kaltura.com:1935/</a>
      </p>
      
      <p>
        <a href="http://pa-publish-speedtest.kaltura.com:1935/" target="_blank" title="http://pa-publish-speedtest.kaltura.com:1935/
Cmd+Click or tap to follow the link">http://ny-publish-speedtest.kaltura.com:1935/</a>
      </p>We recommend testing several times as bandwidth can fluctuate.
    </li>
  </ul>
  
  <h2>
    Broadcasting to Kaltura
  </h2>
  
  <p>
    The following are the minimum recommended encoder hardware and internet line specs for broadcasting live video to Kaltura. Hardware specs are most relevant to software encoders that are installed on a PC or Mac. If you are using a dedicated hardware encoder, the below hardware specs are less relevant - refer to your encoder output specs that came with your device.
  </p>
  
  <h3>
    Minimum System Requirements for Broadcasting
  </h3>
  
  <ul>
    <li>
      Intel Core 2 Duo 2Ghz or Higher
    </li>
    <li>
      4GB RAM
    </li>
    <li>
      1Mbit/sec upload bandwidth
    </li>
    <li>
      Dedicated video card, 256MB VRAM
    </li>
    <li>
      Windows XP / Vista or Mac OS X 10.5 or higher (v20.0.89)
    </li>
  </ul>
  
  <h3>
    Recommended System Specifications for Broadcasting
  </h3>
  
  <ul>
    <li>
      Quad Core CPU
    </li>
    <li>
      4GB RAM
    </li>
    <li>
      2Mbit/sec upload bandwidth
    </li>
    <li>
      Dedicated video card, 512MB VRAM
    </li>
    <li>
      Windows Vista / Windows 7 or Mac OS X 10.5 or higher (v20.0.89)
    </li>
  </ul>
  
  <h3>
    Optimal (for HD Multi-Bitrate Streaming)
  </h3>
  
  <ul>
    <li>
      Quad Core i7-2600 series CPU or better
    </li>
    <li>
      8GB RAM
    </li>
    <li>
      5Mbit/sec or better upload bandwidth
    </li>
    <li>
      Dedicated video card, 512MB VRAM
    </li>
    <li>
      Windows Vista / Windows 7 or Mac OS X 10.6 or higher
    </li>
  </ul>
  
  <p>
    It is a best practice to broadcast from your encoder over wired Ethernet connection. However, if you do need to broadcast over wireless, try to make sure that your wireless hub is not shared with other users that may be concurrently utilizing bandwidth. If you need to broadcast over a cellular connection, it is recommended that you use a bonded solution that combines cellular connections from multiple carriers into a single high-speed output. For an example of a bonded solution -<a href="http://teradek.com/pages/bond">http://teradek.com/pages/bond</a>.
  </p>
  
  <p>
    <span><a href="#top">Back to Top</a></span>
  </p>
  
  <h2>
    <span><a name="select_encoder"></a>Selecting an Encoder</span>
  </h2>
  
  <p>
    What kind of encoders you choose should depend on the nature of your broadcast. Here are a few key questions to consider before making a decision:
  </p>
  
  <p>
    <strong>What type of event are you running?</strong>
  </p>
  
  <ol>
    <li>
      High-end event with large visibility.
    </li>
    <li>
      Lower-end event with small visibility.
    </li>
  </ol>
  
  <p>
    <strong>Mission criticality</strong>
  </p>
  
  <p>
    If the broadcast fails, how serious of an issue is it? 
  </p>
  
  <ol>
    <li>
      Very serious.
    </li>
    <li>
      Manageable.
    </li>
  </ol>
  
  <p>
    <strong>Duration of event</strong>
  </p>
  
  <p>
    How long is your event? 
  </p>
  
  <ol>
    <li>
      Full-day / multi-day .
    </li>
    <li>
      A few hours.
    </li>
  </ol>
  
  <p>
    <strong>Production value?</strong>
  </p>
  
  <ol>
    <li>
      Professionally produced or premium content.
    </li>
    <li>
      Informal or unprofessional content.
    </li>
  </ol>
  
  <p>
    <strong>Multi-bitrate vs single-bitrate</strong>
  </p>
  
  <ol>
    <li>
      Multi-bitrate output required.
    </li>
    <li>
      Single-bitrate output required.
    </li>
  </ol>
  
  <p>
    <strong>Static vs mobile</strong>
  </p>
  
  <ol>
    <li>
      The encoder will be static or rack mounted.
    </li>
    <li>
      The encoder needs to be mobile or used in the field.
    </li>
  </ol>
  
  <p>
    <strong>How will content be ingested?</strong>
  </p>
  
  <ol>
    <li>
      Via an uncompressed broadcast feed - HD-SDI, IP or Fiber
    </li>
    <li>
      Via a prosumer-type feed - HDMI, component, composite, etc
    </li>
  </ol>
  
  <p>
    <strong>Require remote management?</strong>
  </p>
  
  <ol>
    <li>
      The encoder needs to be remotely managed over a local network or from off-sit.e
    </li>
    <li>
      The encoder will be managed in-person.
    </li>
  </ol>
  
  <p>
    <strong>Redundancy required?</strong>
  </p>
  
  <ol>
    <li>
      The encoder needs redundant power supply, CPUs and GPUs to guarantee uninterrupted broadcast should any hardware fail.
    </li>
    <li>
      No redundancy is required.
    </li>
  </ol>
  
  <p>
    If your answers to these questions are mostly #1's, an enterprise-grade encoder is likely a good fit for your use-case. If your answers are mostly #2's, a lower-end encoder is likely a good fit for your use-case.
  </p>
  
  <table style="width: 792px;" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td style="text-align: left;" valign="top" width="248">
          <p class="TableHeading">
            <strong>Enterprise-Grade</strong>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="543">
          <p class="TableHeading">
            <strong>Prosumer-Grade</strong>
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="248">
          <p class="TableBodyText">
            Digital Rapids (Imagine Communications) StreamZ Live
          </p>
        </td>
        
        <td style="text-align: left;" width="543">
          <p class="TableBodyText">
            Telestream WireCast
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="248">
          <p class="TableBodyText">
            Elemental Live
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="543">
          <p class="TableBodyText">
            Flash Media Live Encoder
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="248">
          <p class="TableBodyText">
            Envivio Muse Live
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="543">
          <p class="TableBodyText">
            Teradek Cube / Vidu
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" width="248">
          <p class="TableBodyText">
            Haivision Kulabyte
          </p>
        </td>
        
        <td style="text-align: left;" width="543">
          <p class="TableBodyText">
             
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    For additional information about Akamai Encoders, see the article: <a href="https://kaltura.atlassian.net/wiki/download/attachments/64949126/AkamaiHD_EncoderGuidelines.pdf?version=1&modificationDate=1436811002318&api=v2">AkamaiHD Encoder Guidelines.pdf</a>.
  </p>
  
  <p>
    For additional information about the supported encoders for Kaltura Live streaming,<strong> s</strong>ee the article: <a href="http://cdnknowledge.kaltura.com/node/1146">What encoders can I use with the Kaltura Live streaming?</a>
  </p>
  
  <p>
    <span><a href="#top">Back to Top</a></span>
  </p>
  
  <h2>
    <span><a name="determine"></a>Determining an Encoder's Capabilities</span>
  </h2>
  
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
      <strong>Flash Queue</strong><br />Certain encoders, such as Wirecast, display a Flash queue which shows how much data is currently buffered on your machine waiting to be transferred to the server. Your Flash queue should be low or empty. If your Flash queue is close to full or completely full, your output bitrate is too high for your internet line or the CPU.
    </li>
  </ul>
  
  <p style="padding-left: 30px;">
     <img src="{{site.url}}/assets/2504">
  </p>
  
  <p style="padding-left: 30px;">
    <em>Wirecast Real Time Logs</em>
  </p>
  
  <p style="padding-left: 30px;">
    <em> <img src="{{site.url}}/assets/2505">
  </p>
  
  <p style="padding-left: 30px;">
    <em>FMLE Real Time Logs</em>
  </p>
  
  <p>
    <span><a href="#top">Back to Top</a></span>
  </p>
  
  <div class="WordSection1">
    <h2>
      <a name="cfg_encoder"></a>Configuring an Encoder
    </h2>
    
    <p>
      There are two core areas of your encoder that need to be configured:
    </p>
    
    <ul>
      <li>
        <a href="#stream_settings">Stream Settings</a>
      </li>
      <li>
        <a href="#encoder_settings">Encoder Settings</a>
      </li>
    </ul>
    
    <h2>
      <a name="stream_settings"></a>Stream Settings
    </h2>
    
    <p>
      After you have created a live entry in Kaltura, you can navigate the Edit Entry window and grab your live stream details to input into your encoder.
    </p>
    
    <ul>
      <li>
        Primary RTMP URL
      </li>
      <li>
        Backup RTMP URL
      </li>
      <li>
        Stream Name
      </li>
      <li>
        Username (Universal Streaming only)
      </li>
      <li>
        Password (Universal Streaming only)
      </li>
    </ul>
    
    <p class="Figure">
      You need to copy these details, configure a single or multi-bitrate RTMP stream in your encoder, and paste the details into the fields provided.
    </p>
    
    <p>
      For single-bitrate output, your Stream Name will need to either have a '%i' variable or a '1' at the end. Which option is used depends on your encoder.
    </p>
    
    <p>
      For multi-bitrate output, your Stream Name will need to either have a '%i' variable or sequential numbers for each stream at the end. For example, stream #1 would have the stream name sdflhsdf_1 and stream #2 would have the stream name sdflhsdf_2.
    </p>
    
    <h2>
      <a name="encoder_settings"></a>Encoder Settings
    </h2>
    
    <p>
      You also need to configure the encoder settings to use for each output stream:
    </p>
    
    <ul>
      <li>
        <a href="file:///C:/Users/debbie.zioni/Documents/Live%20Encoding/Live_Encoding_Best_Practices_Guide.docx#_Basic_Settings">Basic Settings</a>
      </li>
      <li>
        <a href="file:///C:/Users/debbie.zioni/Documents/Live%20Encoding/Live_Encoding_Best_Practices_Guide.docx#_Advanced_Settings">Advanced Settings</a>
      </li>
    </ul>
    
    <h3>
      Basic Settings
    </h3>
    
    <ul>
      <li>
        <strong>Video Bitrates - </strong>Video bitrate equates to quality. The higher the bitrate, the better the quality. However, bitrates need to be downloaded by viewers in order to view content, therefore it is important to pick bitrates that will reach the widest audience possible, at quality levels that are acceptable.
      </li>
    </ul>
    
    <table style="width: 493px; padding-left: 30px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td colspan="2" valign="top" width="493">
            <p class="TableBodyText">
              <strong>Bitrate Recommendations per Dimension</strong>
            </p>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td valign="top" width="103">
            <p class="TableBodyText">
              <strong>Dimension</strong>
            </p>
          </td>
          
          <td valign="top" width="390">
            <p class="TableBodyText">
              <strong>Bitrate Range</strong>
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="103">
            <p class="TableBodyText">
              640 X 360
            </p>
          </td>
          
          <td valign="top" width="390">
            <p class="TableBodyText">
              400kbps - 800kbps
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="103">
            <p class="TableBodyText">
              960 x 540
            </p>
          </td>
          
          <td valign="top" width="390">
            <p class="TableBodyText">
              600kbps - 1200kbps
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="103">
            <p class="TableBodyText">
              1280 x 720
            </p>
          </td>
          
          <td valign="top" width="390">
            <p class="TableBodyText">
              900kbps - 2000kbps
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="103">
            <p class="TableBodyText">
              1920 x 1080
            </p>
          </td>
          
          <td valign="top" width="390">
            <p class="TableBodyText">
              1500kbps - 3000kbps
            </p>
          </td>
        </tr>
      </tbody>
    </table>
    
    <ul>
      <li>
        <strong>Video Dimensions</strong> -Each stream that is sent out requires a dimension. As a rule of thumb, never stream a higher dimension than what is being ingested into your encoder. For example, if you receive 720p from production you shouldn't stream at 1080p. For standard 16:9 dimensions and associated bitrates, please see the table above.
      </li>
      <li>
        <strong>FPS (frame per second)</strong> - As a rule of thumb, you will want to stream content matching the fps that is used on ingest into the encoder. For example, if you receive 30fps from production, you should stream at 30fps. Typical frame rates include 23.98, 24, 25, 29.97, 30, 50 and 60 fps. Higher frame rates are best suited to high motion video like sports.
      </li>
      <li>
        <strong>Audio Bitrates</strong> - equates to quality. As a rule of thumb, try to pick either 96kbps, 128kbps or 192 kbps for audio output, with the higher bitrate being the better quality.
      </li>
      <li>
        <strong>Audio Sample Rates</strong> -Audio sample rates should be matched with what is ingested into your encoder from production. Typical sample rates include 41KHz and 48KHz.
      </li>
    </ul>
    
    <h3>
      Advanced Settings
    </h3>
    
    <ul>
      <li>
        <strong>Buffer Size</strong> - The buffer value helps to ensure full fps and bitrate output on internet lines that may need be very fast. Buffer values typically range from 0ms - 2000ms. A fast internet line (50%+ above the total output bitrate) would use a buffer of approximately 300ms while a slower internet line (10% - 20% above the total output bitrate) would use a buffer closer to 1500 - 2000ms.
      </li>
      <li>
        <strong>CBR vs VBR</strong> - The Constant BitRate (CBR) option maintains a steady streaming bitrate and does not fluctuate according to picture complexity, while the Variable BitRate option fluctuates the output bitrate depending on picture complexity and typically has a threshold, for example 150% above the target bitrate. Using VBR with a high threshold can cause more flavor changes during adaptive streaming, so it is a best practice to bring this threshold down to between 110% - 120%. CBR on the other hand does not cause quite as many flavor changes, but can sometimes produce a lower quality picture during segments of high motion or picture complexity.
      </li>
      <li>
        <strong>Keyframe Interval</strong> - Keyframes are individual frames of video that have a full set of image data, they do not reference any other frames. Video playback always needs to start on a keyframe, therefore it is important to set a consistent keyframe interval on your outgoing streams.<strong> The keyframe interval for Kaltura live streams must be </strong><strong><em>2</em></strong><em><strong> seconds</strong></em><strong>.</strong>
      </li>
      <li>
        <strong>Compression profile</strong> - The H.264 codec supports 3 different output profiles - Baseline, Main and High. Each successive profile adds a few extra features and an increase in quality, at the cost of slightly less device support. So for the widest device support, Baseline is the preferred profile. For the best quality, especially in HD, the High profile is better but may not be supported on older devices.
      </li>
    </ul>
  </div>
  
  <p>
    <span><a href="#top">Back to Top</a></span>
  </p>
  
  <div class="WordSection2">
    <h2>
      <a name="validating"></a>Validating Available Broadcast Bandwidth
    </h2>
    
    <p>
      To decide what are the appropriate output settings for your live stream, it is important to determine the available uplink bandwidth on site.
    </p>
    
    <p>
      To determine the bandwidth available visit:
    </p>
    
    <p>
      <a href="http://pa-publish-speedtest.kaltura.com:1935/" target="_blank" title="http://pa-publish-speedtest.kaltura.com:1935/
Cmd+Click or tap to follow the link">http://pa-publish-speedtest.kaltura.com:1935/</a>
    </p>
    
    <p>
      <a href="http://pa-publish-speedtest.kaltura.com:1935/" target="_blank" title="http://pa-publish-speedtest.kaltura.com:1935/
Cmd+Click or tap to follow the link">http://ny-publish-speedtest.kaltura.com:1935/</a>
    </p>
    
    <p>
      When testing for usage with Kaltura Live and Live+, be sure to test by pointing to a server in NY (primary server is located <a href="http://ny-publish-speedtest.kaltura.com:1935/" target="_blank">here</a>) and Palo Alto (backup server is located <a href="http://pa-publish-speedtest.kaltura.com:1935/" target="_blank">here</a>).
    </p>
    
    <p>
      Since the input feed will be streamed to Kaltura over RTMP instead of HTTP, the actual bandwidth available for RTMP connections will be less. 
    </p>
    
    <h3>
      Your Checklist
    </h3>
    
    <ul>
      <li>
        Use Ethernet where possible, as opposed to wifi or cellular connections
      </li>
      <li>
        Use a dedicated line where possible, as opposed to a shared line
      </li>
      <li>
        Best practice is to utilize a line that has uplink speed at 50%+ your combined bitrate output.
      </li>
      <li>
        For example, when sending a 1500kbps, 1000kbps and 500kbps feed (totaling 3000kbps), utilizing a line that can upload 4500kbps and up.
      </li>
    </ul>
  </div>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <div class="WordSection3">
    <h2>
      <a name="ABR"></a>Live Adaptive Bitrate Available Broadcast
    </h2>
    
    <p>
      Adaptive bitrate is the process by which the player pushes the correct flavor (bitrate) to the viewer according to the viewer's internet connection speed. In order for live video to take advantage of adaptive bitrate, multiple flavors of a live video need to be concurrently pushed to the player.
    </p>
    
    <h3>
      How is this achieved?
    </h3>
    
    <ul>
      <li>
        Using Kaltura Live (Passthrough), the encoder sends multiple RTMP streams at various bitrates to the same URL
      </li>
      <li>
        Using Kaltura Live+ (Cloud Transcode), the encoder sends a single high-bitrate RTMP stream to the URL, and Kaltura's servers create live flavors in the cloud
      </li>
      <li>
        Using Kaltura Universal Streaming (Passthrough), the encoder sends multiple RTMP streams at various bitrates to the same URL
      </li>
      <li>
        Using adaptive bitrate is a best practice, as it allows live video to be viewed by a wider audience using varying internet connections. While the player will automatically push the best suited live flavor to the viewer, the viewer can also force a specific live flavor using the <em>Flavor Selection</em> button on the player when it is enabled in the KMC Studio.
      </li>
    </ul>
    
    <a href="#top">Back to Top</a>
  </div>
  
  <h2>
    <a name="setup_entries"></a>Setting up Live Entries in the KMC
  </h2>
  
  <h3>
    <strong>Configure Your Transcoding Profile</strong>
  </h3>
  
  <p>
    Kaltura Live Streaming includes Kaltura Live (Passthrough) and Live+ (Cloud Transcode)
  </p>
  
  <p>
    Before creating new live entries in the KMC, you will need to make sure that your live transcoding profile settings are configured to align with your particular use-case. See <a href="{{site.url}}/documentation/Knowledge/how-set-transcoding-profiles-live-streaming.html" target="_blank">How to Set Transcoding Profiles for Live Streaming</a>.
  </p>
  
  <ul>
    <li>
      In the KMC, navigate to: Settings > Transcoding Settings > Switch to Advanced Mode (bottom left) > Switch to Live Profiles Mode (bottom left)<br />You should see all your live transcoding profiles. Out the box, two profiles should exist in this area:
    </li>
  </ul>
  
  <ol start="1">
    <li>
      Cloud Transcode for Kaltura Live+
    </li>
    <li>
      Passthrough for Kaltura Live
    </li>
  </ol>
  
  <p>
    <strong style="font-size: 1em;">Configuring the Cloud Transcode Profile</strong>
  </p>
  
  <p class="Procedure mce-procedure">
    To configure the Cloud Transcode profile
  </p>
  
  <ol>
    <li>
      Click on the Cloud Transcode profile.<br />You will see checkmarks next to all the flavors that will be created by Kaltura's servers when receiving a single stream from your encoder, plus the Source flavor (the flavor sent by the encoder)
    </li>
    <li>
      Configure what flavors you would like to create by checking and unchecking the relevant boxes<br />If you do not see a flavor that you would like to use, please reach out to support or your CSM to have a custom flavor added to your Partner ID<br />You will see 2 Ingest flavors in this window, which allow you to leverage a hybrid configuration whereby Kaltura creates live flavors from your source bitrate, but also ingests and passes through 2 additional flavors to the player. In this case, you would be sending through 3 flavors from your live encoder.
    </li>
    <li>
      Click Save.<br />You are now ready to create live entries.
    </li>
  </ol>
  
  <h4>
    <strong>Configuring the Passthrough Transcode Profile</strong>
  </h4>
  
  <p class="Procedure mce-procedure">
    To configure the Passthrough Transcode profile
  </p>
  
  <ol>
    <li>
      Click on the Passthrough Transcode profile.<br />You will see checkmarks next to the Source flavor as well as a number of Ingest flavors that will pass through Kaltura's servers and be sent directly to the player.
    </li>
    <li>
      Configure what flavors you would like to ingest by checking and unchecking the relevant boxes. For example, if you plan to send 3 live flavors from your encoder, you will need to check boxes next to the Source, Ingest 2 and Ingest 3 flavors.<br />If you do not see a flavor that you would like to use, please reach out to support or your CSM to have a custom flavor added to your Partner ID.
    </li>
    <li>
      Click Save. <br />You are now ready to create live entries.
    </li>
  </ol>
  
  <h3>
    Creating a Live Stream Entry 
  </h3>
  
  <p class="mce-procedure">
    To create a live stream entry
  </p>
  
  <ol>
    <li>
      See the  <a href="http://knowledge.kaltura.com/node/1047#workflow_4LS">Workflow for Setting up Live Streaming.</a>
    </li>
    <li>
      <a href="http://knowledge.kaltura.com/node/1047#workflow_4LS"></a>Pick the live stream type from the drop down.
    </li>
  </ol>
  
  <ul>
    <li>
      Kaltura Live Streaming includes Kaltura Live (Passthrough) and Live+ (Cloud Transcode)
    </li>
    <li>
      Kaltura Universal Streaming bypasses Kaltura, and sends streams directly to the Akamai CDN. This option is follows a passthrough-type workflow.
    </li>
    <li>
      Manual Live Stream URLs allow feeds to be pulled directly from the CDN into the player that are being broadcast by a 3rd party.
    </li>
  </ul>
  
  <p class="mce-note-graphic">
    Kaltura Live and Live+ both offer Live-to-VOD and a 2hr DVR window, Universal Streaming <span>does not</span> offer Live-to-VOD and offers only a 30min DVR window.
  </p>
  
  <ul>
    <li>
      After you select the stream type:<br /><br /><ul>
        <li>
          <strong>Kaltura Live and Live+</strong><ul>
            <li>
              Give your stream a name.
            </li>
            <li>
              Choose between Cloud Transcode and Passthrough workflows.
            </li>
            <li>
              Enable or disable DVR.
            </li>
            <li>
              Enable or disable recording (Live-to-VOD).<ul>
                <li>
                  Recording comes with 2 additional options - <em>Append to Single Entry</em> and <em>Create New Entry. </em>Append to single entry will always add recordings to the end of the original VOD entry each time you start and stop broadcasting from your encoder. Create new entry will always create a new unique VOD entry each time you start and stop broadcasting from your encoder.
                </li>
              </ul>
            </li>
            
            <li>
              Select <em>Create Live Stream.<br /> </em>
            </li>
          </ul>
        </li>
        
        <li>
          <strong>Universal Streaming</strong><br /><ul>
            <li>
              Give your stream a name.
            </li>
            <li>
              In each IP field, enter a pingable IP address that is close to the location that your encoder will broadcast from. This allows Akamai to provision an endpoint that is geographically close to the streaming location to accept the output streams from the encoder.
            </li>
            <li>
              Optionally, enter a broadcast password.
            </li>
            <li>
              Enable or disable DVR.
            </li>
            <li>
              Select <em>Create Live Stream.<br /><br /></em>
            </li>
          </ul>
        </li>
        
        <li>
          <strong>Manual Live URLs</strong><ul>
            <li>
              Give your stream a name
            </li>
            <li>
              Enter both your HDS and HLS URLs that have been provided by the 3rd party streaming to the CDN.
            </li>
            <li>
              If the Akamai protocol is used on your HDS stream, check this box.<br /><br />
            </li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
  
  <h3>
    <span style="font-size: 1.17em;">Addtional Options</span>
  </h3>
  
  <ul>
    <li>
      After you created your entry, you can access the entry via the entries table. 
    </li>
    <li>
      Clicking on the entry opens the <em>Edit Entry</em> window
    </li>
    <li>
      Navigating to the <em>Live Stream</em> tab will show the details needed to enter into your encoder (Kaltura Live, Live+ and Universal Streaming only).
    </li>
  </ul>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>