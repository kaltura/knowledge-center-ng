---
layout: page
title: "Broadcasting to Kaltura with Adobe Flash Media Live Encoder (FMLE)"
date: 2016-08-10 21:26:47
---

<p>
    Adobe Flash Media Live Encoder (FMLE) is a free encoder that you can use to broadcast directly to Kaltura.
  </p>
  
  <h2 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-Prerequisites:">
    <span>Prerequisites:</span>
  </h2>
  
  <p>
    <span>This article assumes you have already performed the following actions:</span>
  </p>
  
  <ol>
    <li>
      Created a Kaltura account and am certain that Live streaming is enabled. 
    </li>
    <li>
      Tested the available <a href="https://knowledge.kaltura.com/node/1750/#speedtest">network bandwidth between your encoder and Kaltura data centers</a>
    </li>
    <li>
      Created a <a href="https://knowledge.kaltura.com/node/126/">live stream entry in the Kaltura Management Console (KMC)</a>. 
    </li>
  </ol>
  
  <h2 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-AdobeFlashMediaLiveEncoder(FMLE)Installation:">
    <span>Adobe Flash Media Live Encoder (FMLE) Installation</span>
  </h2>
  
  <p class="mce-procedure">
    <span>To download Adobe FMLE</span>
  </p>
  
  <ol>
    <li>
      Download and install FMLE 3 from Adobe <a href="http://www.adobe.com/products/flash-media-encoder.html" class="external-link" rel="nofollow">here</a>.
    </li>
    <li>
      Be certain that your system has the minimum requirements. See the <a href="http://www.adobe.com/products/flashmediaserver/flashmediaencoder/systemreqs/" class="external-link" rel="nofollow">system requirements</a> for details.
    </li>
  </ol>
  
  <h2 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-ExporttheFMLEconfigurationfilefromtheKalturaManagementConsole" class="mce-note-graphic">
    Export the FMLE Configuration File from the Kaltura Management Console
  </h2>
  
  <p class="mce-procedure">
    To export the FMLE XML
  </p>
  
  <ol>
    <li>
      Log in to your Kaltura Management Console in <a href="http://kmc.kaltura.com/" class="external-link" rel="nofollow">http://kmc.kaltura.com</a>
    </li>
    <li>
      In the Content tab, locate your live entry and click on it to edit the entry.
    </li>
    <li>
      Click on "Export XML to FMLE".<br /><img src="{{site.url}}/assets/3373">
    </li>
    <li>
      Save the exported XML to your computer
    </li>
  </ol>
  
  <h2 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-ConfiguringFMLEtoBroadcast">
    Configuring FMLE to Broadcast
  </h2>
  
  <p class="mce-procedure">
    To import the XML file to FMLE
  </p>
  
  <ol>
    <li>
      Launch FMLE on your computer.
    </li>
    <li>
      Go to File→Open Profile.<br /><img src="{{site.url}}/assets/3374">
    </li>
    <li>
      Navigate to where the XML was saved and select Open to automatically configure the broadcasting URLs to Kaltura SaaS.<br /><img src="{{site.url}}/assets/3375">
    </li>
  </ol>
  
  <h3 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-EnableStreamSynchronization">
    Enable Stream Synchronization
  </h3>
  
  <p class="mce-procedure">
    To enable stream synchronization
  </p>
  
  <p>
    This step configures the outgoing streams to be synchronized with UTC timestamps, to provide a better user experience.
  </p>
  
  <ol>
    <li>
      Close the FMLE application.
    </li>
    <li>
      Open the Flash Media Live Encoder <code class="code">config.xml</code> file in a text editor. The default installation location depends on your operating system:<br /><ul class="itemizedlist">
        <li class="listitem">
          <p>
            <span class="bold"><strong>32-bit Windows: </strong></span><code class="code">C:\Program Files &lt;span>(x86)&lt;/span>\Adobe\Flash Media Live Encoder 3.2</code>
          </p>
        </li>
        
        <li class="listitem">
          <p>
            <span class="bold"><strong>64-bit Windows: </strong></span><code class="code">C:\Program Files (x86)\Adobe\Flash Media Live Encoder 3.2</code>
          </p>
        </li>
        
        <li class="listitem">
          <p>
            <span class="bold"><strong>Macintosh:/</strong></span><code class="code">Applications/Adobe/Flash\ Media\ Live \Encoder\ 3.2</code>./conf/
          </p>
        </li>
      </ul>
    </li>
    
    <li>
      In <code class="code">config.xml</code>, set the value of the following <code class="code">&lt;enable&gt;</code> element to <code class="code">true</code>:<br /><pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;mbrconfig&gt;
       &lt;streamsynchronization&gt;
                &lt;!-- "true" to enable this feature, "false" to disable. --&gt;
                &lt;enable&gt;true&lt;/enable&gt;
                &lt;referencetime&gt;
                     &lt;month&gt;0&lt;/month&gt;
                     &lt;year&gt;0&lt;/year&gt;
                &lt;/referencetime&gt;
       &lt;/streamsynchronization&gt;
&lt;/mbrconfig&gt;</pre>
    </li>
    
    <li>
      Start the FMLE application.
    </li>
  </ol>
  
  <h3 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-FMLEEncodingOptions">
    FMLE Encoding Options
  </h3>
  
  <p>
    The following graphic provides an overview of the FMLE encoding options and the recommended values when streaming to Kaltura:
  </p>
  
  <p>
    <span class="confluence-embedded-file-wrapper"><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/158367880/image2016-8-4%2018%3A52%3A20.png?version=1&modificationDate=1470325940571&api=v2" border="0" data-image-src="/wiki/download/attachments/158367880/image2016-8-4%2018%3A52%3A20.png?version=1&modificationDate=1470325940571&api=v2" data-unresolved-comment-count="0" data-linked-resource-id="160792990" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2016-8-4 18:52:20.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-content-type="image/png" data-linked-resource-container-id="158367880" data-linked-resource-container-version="7" /></span>
  </p>
  
  <ol>
    <li>
      Video Device: Select the video device you want to use for live streaming, for example, Camera, Webcam, capture card, etc
    </li>
    <li>
      Video Format: Select H.264 
    </li>
    <li>
      Frame Rate: Based on your capture device capabilities. recommended values are 25 or 30 fps.
    </li>
    <li>
      Input Size : Choose an input size that is equal to your output size. Check the "Maintain Aspect Ratio" checkbox.
    </li>
    <li>
      <a name="Output_size"></a>Output Size and Video Bit Rate: This important parameters defines the resolution and bitrate of the outgoing stream.<br />Please keep in mind the following constraints:<ul>
        <li>
          Encoding at high bitrates will require more CPU resources and bandwidth.
        </li>
        <li>
          The total amount of bandwidth required must not bypass 50% of your available bandwidth to Kaltura servers.
        </li>
      </ul>
    </li>
    
    <li>
      Audio device: Select the<span> audio device you want to use for the stream. This does not need to be the built in mic of your camera. You can select an alternate audio input.</span>
    </li>
    <li>
      <span>Audio format: AAC and MP3 are supported. when possible, AAC is recommended.</span>
    </li>
    <li>
      <span>Channels: Choose stereo or mono. Stereo is recommended.</span>
    </li>
    <li>
      <span>Sample rate: 44100 Hz (44.1 kHz) is a good starting point unless you have audio gear that requires something else.</span>
    </li>
    <li>
      <span>Audio Bit Rate: Based on your audio stream quality. You could start at 96 kbps and go up from there.</span>
    </li>
  </ol>
  
  <h4 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-SendingMulti-BitrateStreaminFMLE">
    Sending Multi-Bit-rate Stream in FMLE
  </h4>
  
  <p>
    If you have sufficient bandwidth and CPU resources, you can broadcast multi-bit-rate stream directly from FMLE, instead of creating the lower-flavors in Kaltura servers.
  </p>
  
  <ol>
    <li>
      In the "<a href="#Output_size">Output Size and Video Bit Rate</a>" section, you can send up to 3 streams to Kaltura. Order your streams with the highest bit rate /output size stream in the first position. You can then place the lower quality stream(s) in descending over in the two other slots.
    </li>
    <li>
      Edit the "Stream" field (under the RTMP URLs) and add an "%i" to the end of the Stream name. This %i tells Kaltura that you will be sending multiple quality streams.
    </li>
  </ol>
  
  <p>
    You can have up to 3 streams at once going to the same channel when streaming with FMLE. It is recommended to add streams one at a time to help make sure you have adequate bandwidth. If you are sending multiple streams, please make sure that the transcoding profile is set to "Pass-through"
  </p>
  
  <h3 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-StartingtheBroadcast">
    Starting the Broadcast
  </h3>
  
  <p>
    Press Start to start streaming to Kaltura. <span> Please allow 2-3 minutes for the stream to initialize and process before it can be played by the video player.</span>
  </p>
  
  <h3 id="BroadcastingtoKalturawithAdobeFlashMediaLiveEncoder(FMLE)-Whilestreaming">
    While streaming
  </h3>
  
  <p>
    During the broadcast, please review the FMLE logs and statistics.
  </p>
  
  <ul>
    <li>
      Make sure that FMLE has connected successfully to Kaltura servers.
    </li>
    <li>
      Any disconnection or failure will appear in the encoding logs.
    </li>
    <li>
      Review the  FMLE encoding and publishing statistics tabs to make sure the stream is properly broadcasted to Kaltura servers (primary and backup). If you experience frame drops, please make sure you have sufficient bandwidth and CPU resources.<br /><img src="{{site.url}}/assets/3376">
    </li>
  </ul>
  
  <p>
    Press Stop to stop broadcasting.
  </p>