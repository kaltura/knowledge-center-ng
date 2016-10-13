---
layout: page
title: "Live Streaming Using Kaltura Live Streaming (HDS / HLS / DASH) "
date: 2014-02-03 11:01:08
---

<a name="anchor"></a>[collapsed title="Kaltura Live Streaming Overview"]

<p class="mce-heading-2">
  <a name="Kaltura_Live_Streaming"></a>Kaltura Live Streaming
</p>

The Kaltura live streaming platform enables you to broadcast live events or 24/7 broadcasts to any screen. A Kaltura live stream can be provisioned in the kaltura management console ( KMC ) or directly from applications such as MediaSpace. Kaltura live streaming supports both passthrough and cloud encoding with multi protocol output for HLS, HDS, MPEG-DASH and Smooth Streaming.  Kaltura live streams can be delivered through a Content Delivery Network (CDN) such as Akamai, as well as support internal delivery in diverse network topologies with support for eCDNs and Multicast. Kaltura live streaming also support Live to VOD with a single embed code, instant provisioning and live captions passthrough.  

You can encode a stream with any RTMP encoder. <a href="http://www.adobe.com/products/flashmediaserver/flashmediaencoder/" target="_blank">Adobe Flash Media Live Encoder</a> (Free) <a href="http://www.telestream.net/wire-cast/overview.htm" target="_blank">Telestream Wirecast</a> (Commercial) and others such as <a href="http://www.viewcast.com/products/niagara-systems" target="_blank">ViewCast Niagara</a> and <a href="http://www.newtek.com" target="_blank">NewTek</a> tricaster hardware encoders are supported. The encoder sends you stream out through a secure RTMP connection to the Kaltura Live Streaming service. Then, using a Kaltura Player, you can embed the live broadcast entry your websites. You can set the live stream entry metadata and specify broadcasting settings in the KMC in the same way VOD content is managed. 

In the Kaltura SaaS Edition, Live Streaming is an additional service.   
To add Live Streaming to your account, contact your Account Manager.

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Features Overview</span>

*   **Instant provisioning**  — streams are provisioned instantly without delays both in KMC and via API calls. 
*   [**Cloud Transcoding**][1] — supports single RTMP stream ingest being transcoded in the cloud to a few different flavors for high quality adaptive delivery experience with minimal ingest bandwidth and CPU requirements. RTSP is an additional ingest protocol supported, for encoders such as <a href="http://www.wowza.com/products/gocoder" target="_blank">Wowza GoCoder</a>. 
*   [**Live Recording**][2], and live to VOD — records your live broadcast for instant VOD access once the live event is complete via the same embed code.
*   [**Live Clipping**][3] — enables you to create VOD clips from a live event while the live event is still active. 
*   **[Passthrough and multi protocol support][4] **— stream to multiple protocols and delivery modes; HDS, HLS, MPEG-DASH, Smooth Streaming to delivery to mobile and desktop
*   **Live Captions** — supports live captions passthrough to Kaltura players and compatible devices. 

 [1]: #cloud
 [2]: #enable_recording
 [3]: #clipping
 [4]: #live_transcoding_profile

<p class="mce-heading-4">
  <span class="mce-sub-heading"><span>To enable live streaming for your account </span></span>
</p>

<span class="mce-sub-heading">Kaltura SaaS, MediaSpace and On-Prem Customers</span>

•<span class="Apple-tab-span" style="white-space: pre;"> </span><a href="http://corp.kaltura.com/company/contact-us" target="_blank" title="Contact Us">Contact us</a> or call +1-800-871-5224

After your account is enabled you can set up Kaltura’s Live Streaming service.

This article describes how to set up the KMC, the encoder, and a device for the live streaming service using Kaltura Live Streaming (HDS / HLS / DASH) .

<p class="mce-sub-heading">
  Users of Kaltura CE
</p>

<a href="https://github.com/kaltura/platform-install-packages/blob/Jupiter-10.19.0/doc/install-kaltura-redhat-based.md#note-about-using-wowza-as-media-server" target="_blank">Wowza</a> is the supported media server for Live streaming. For <a href="https://github.com/kaltura/platform-install-packages/blob/Jupiter-10.19.0/doc/install-kaltura-redhat-based.md#configure-red5-server-1" target="_blank">Red5</a>, web recording and playback over RTMP is supported.

[Back][5]

 [5]: #anchor

 [/collapsed]

[collapsed title="Worklow for Setting up Live Streaming"]

<p class="mce-heading-2">
  <a name="workflow_4ls"></a>Workflow for Setting up Live Streaming<a name="workflow"></a>
</p>

1.  <span><a href="#live_servers">Check that you have the Appropriate Bandwidth from your Network to Kaltura Live Servers</a><a href="#live_servers">.</a></span>
2.  [Set up the Hardware and Software][6].
3.  [Create a Live Streaming Entry in the KMC.][7]
4.  [Configure the Live Streaming Parameters in the KMC][8].
5.  [Set up the Broadcasting Computer][9].
6.  [View the Broadcasting Setup (optional)][10]

 [6]: #Setting_Up_HW "Setting Up the Hardware and Software for Live Streaming"
 [7]: #Creating_LS_Entry
 [8]: #Cfg_LS_Parm_in_KMC
 [9]: #Settin_Up_Broadcasting_comp
 [10]: #Viewing_Broadcast_setup

<span class="mce-heading-3"><a name="live_servers"></a>Check that you have the Appropriate Bandwidth from your Network to Kaltura Live Servers</span>

Kaltura provides a testing tool to measure the bandwidth available when streaming to Kaltura live servers. Please use the following links to test the bandwidth that is available for live.

*   <a href="http://ny-publish-speedtest.kaltura.com:1935/" target="_blank">East Coast data center</a>
*   <a href="http://pa-publish-speedtest.kaltura.com:1935/" target="_blank">West Coast data center</a>

<p class="mce-note-graphic">
  <span>Do not stream video to Kaltura in your area while testing. You are connected to the same internet connection that your broadcasting device will be using.</span>
</p>

<a name="Setting_Up_HW" style="background-color: #ffffff;"></a><span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Setting up the Hardware and Software</span>

<p class="mce-procedure">
    To set up the hardware and software for live streaming
</p>

For the purposes of documentation we outline the use of Flash Media Encoder, your setup may differ from this guide if using a different encoder. 

1.  Download the <a href="http://www.adobe.com/products/flashmediaserver/flashmediaencoder/" target="_blank">Flash Media Live Encoder (FMLE)</a>.
2.  Install the FMLE on your local Windows machine. 
3.  Connect your camera to the installed computer.

<p class="mce-note-graphic">
  Be certain that your system has the minimum requirements. <br />See <a href="http://www.adobe.com/products/flashmediaserver/flashmediaencoder/systemreqs/" target="_blank">http://www.adobe.com/products/flashmediaserver/flashmediaencoder/systemreqs/</a> for details.<a name="Creating_LS_Entry" style="background-color: #ffffff;"></a>
</p>

[Back to Workflow][11]

 [11]: #workflow

<span class="mce-heading-3"><a name="Creating_LS_Entry"></a>Creating a Live Streaming Entry in the KMC</span>

<p class="mce-procedure">
  To create a live stream entry in the KMC
</p>

1.  Login into the KMC and go to the Upload tab.  
    <img src="{{site.url}}/assets/1332">
2.  Select Live Stream Entry.  
    The Add New Stream window is displayed.  
    <img src="{{site.url}}/assets/2226">
3.  Select the Live Stream Type. For this particular example, select **Kaltura Live Streaming**.  
    The following Live Stream types are available:
    
    **Kaltura Live Streaming (HDS / HLS / DASH)** – Default - Kaltura live streaming services are provisioned within the Kaltura data center. Supports cloud transcoding, extended DVR window, live to VOD archiving with a single embed code, instant provisioning, and multi protocol delivery.  Depending on your live streaming package simultaneous cloud transcodes will be restricted.
    
    **Manual Live Stream URLs** - Allows you to associate custom live end user URLs with a Kaltura entry. This option is useful if you are using a 3<sup>rd</sup> party to provision and broadcast a live stream.

4.  Enter values for the following fields and check the relevant options.  
    <table style="width: 922px;" border="0" cellspacing="0" cellpadding="0">
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="274">
            <p>
              <strong>Field</strong>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="648">
            <p>
              <strong>Description</strong>
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="274">
            <p>
              Name
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="648">
            <p>
              <strong>Required,</strong> minimum 5 characters. The name of the stream that will appear in the KMC entries list.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="274">
            <p>
              Description
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="648">
            <p>
              A description of the stream (Optional).
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="274">
            <p>
              <a name="live_transcoding_profile"></a>Live Transcoding Profile
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="648">
            <p>
              Select a transcoding profile from the drop down list. The available profiles are Cloud Transcode and Passthrough
            </p>
            
            <p>
              <strong><a name="cloud"></a>Cloud Transocde</strong> – enables cloud transcoding per defined cloud transcoding profile. The default cloud transcoding profile includes the source stream + 3 transcode flavors. Your ingest stream for default cloud transcode profile should be 1-2 mbs for 640P resolution.
            </p>
            
            <p>
              To broadcast multiple cloud transcode streams simultaneously contact your Kaltura account manager. <br /><br /><strong>Passthrough</strong> - takes the stream from the encoder and repackages the stream for desktop and mobile users without re-encoding.
            </p>
            
            <p>
              You can set additional transcoding profiles for live streaming. See<a href="{{site.url}}/documentation/Knowledge/how-set-transcoding-profiles-live-streaming.html" target="_blank"> How to Set Transcoding Profiles for Live Streaming</a> and <a href="{{site.url}}/documentation/Knowledge/how-create-transcoding-profile.html" target="_blank">Adding a Transcoding Profile</a> for more information.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="274">
            <p>
              <a name="enable_dvr"></a>Enable Live DVR (provide the ability to seek within the recorded DVR to up to 2 hours prior to your existing point of the live stream).
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="648">
            <p>
              The DVR window is set to 2 hours by default. The DVR window within your player will dynamically adjust per the duration of your event, up to 2 hours. 
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="274">
            <p>
              <a name="enable_recording"></a>Enable Recording
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="648">
            <p>
              Check this to create a VOD of the live stream. The recordings are limited to 24 hours.  Select one of the following options:
            </p>
            
            <ul>
              <li>
                Append the recorded content to a single entry 
              </li>
            </ul>
            
            <ul>
              <li>
                Create new Entries for each broadcast session.
              </li>
            </ul>
            
            <p>
              We recommend to stop broadcasting for an interval of approximately 5 minutes or so, because otherwise the system assumes it is an accidental disconnect and will continue with appending the recorded content.
            </p>
            
            <p>
              <span><span> </span></span>
            </p>
          </td>
        </tr>
      </tbody>
    </table>
    
     

5.  Fill in the values and click Create Live Stream. 

[Back to Workflow][11]

<p class="mce-heading-3">
  <a name="Cfg_LS_Parm_in_KMC"></a>Configuring the Live Stream Parameters in the KMC
</p>

<p class="mce-procedure">
  To configure the live stream parameters
</p>

1.  Go the Content tab in the KMC.
2.  Click on the Live Stream Entry in the Entries table.
3.  Select the Live Stream tab.<img src="{{site.url}}/assets/1334">
    For the** Kaltura Live Streaming (HDS / HLS / DASH)** type, the primary and Backup URLs are automatically created by Kaltura.

4.  Click Export for FMLE to export the client encoder information to an XML that will be used to enter into encoder.
5.  Save the file.
6.  [Set up the broadcasting computer][9].

[Back to Workflow][11]

<p class="mce-heading-3">
  <a name="Settin_Up_Broadcasting_comp"></a>Setting up the Broadcasting Computer
</p>

<p class="mce-procedure">
   <span class="Apple-tab-span" style="white-space: pre;"> </span>To set up the broadcasting computer
</p>

1.  Connect your camera /recording device to the broadcasting computer.
2.  Run the Adobe Flash Media Live Encoder (FMLE).
3.  Select File > Openfile.
4.  Select the exported saved file and click OK.
5.  Click Connect and then click Start.  
    Wait until you see the broadcasting prompt to start broadcasting.<img src="{{site.url}}/assets/1335">
6.  Select the relevant recording Device from the drop-down menu. Copy the details of the live entry to the Flash Media Live Encoder. You can copy the details manually, or use the “Export XML to FME” option.  
    <ol style="list-style-type: lower-alpha;">
      <li>
        Enter or copy the Primary URL in the FMS URL field, and the Backup URL in the Secondary URL as configured in the KMC.
      </li>
      <li>
        Enter the Stream Name as displayed in the KMC.
      </li>
      <li>
        Enter the MBR settings if you have defined them. See Multiple Bitrate Encoding.
      </li>
      <li>
        Use the Preset dropdown menu in the FMLE to select the MBR.
      </li>
      <li>
        Enter the Bit Rates as configured in the KMC. If you select to Save to File, you must append %i to the 'Stream' field.<br /><span class="mce-note-graphic"><span class="mce-note-graphic">The Stream name is formatted for use with the FMLE. If you are using an encoder other then FMLE, such as Wirecast, you will need to replace the "%i" with a "1". For example, remove the % and replace the i with a 1 for the first stream or 2 if it is the second stream and so on<br /></span></span>Note with Flash Live Media Encoder you can use _%i to automatically map multiple streams, with other encoders you should substitute _1 with the index of each live stream flavor.
      </li>
    </ol>

7.  Click Connect.
8.  Enter the Broadcasting credentials, (User Name and Password) as configured in the KMC Live Stream tab and click OK. The system will prompt you twice for the Broadcasting credentials. 
9.  Click Start. You are now broadcasting live.
10. When your broadcast is finished, click Stop.

[Back to Workflow][11]

<p class="mce-heading-3">
  <a name="Viewing_Broadcast_setup"></a>Viewing the Broadcasting Setup (Optional)
</p>

If you checked [enable recording][2] – a new entry is created with the chunks of VOD recordings. It may take a few minutes until the content is ready.

<span class="mce-procedure">To view the  broadcasting setup</span>

1.  Return to the KMC and select the Content tab.
2.  In the KMC Entries Table, click the Preview & Embed link for the live stream entry.<img src="{{site.url}}/assets/1337">
3.  Select the player from the drop-down menu and copy the Embed Code.
4.  Paste the Embed Code within an HTML page or use the short link URL created for this live stream.<span class="Apple-tab-span" style="white-space: pre;"><br /></span>
5.  Browse to the page where the embed code was inserted and press Play on the video player.

<p class="Procedure mce-procedure">
  To see the DVR
</p>

1.  Inside the live stream entry use the scrubber to go back to the point in the video that you want to view.
2.  If you have [DVR enabled][12], and play a previous section of the stream, the live button on the player is enabled and returns you to the actual current point in the live stream.
3.  Click Stop.
4.  Click Disconnect.

 [12]: #enable_dvr

<p class="mce-heading-4">
  <a name="advanced_config"></a>Advanced Configuration Options
</p>

There are multiple factors that can influence the video quality for live streaming. To receive good results you should optimize the settings based on your specific needs.

The following table can be used as a starting point for optimization and setup. A rough estimate is provided for the different factors, based on the video dimensions.

<table class="kaltura-table" style="width: 100%;">
  <thead>
    <tr class="kaltura-table-header">
      <th style="text-align: left;" align="center" valign="middle">
         Video Dimensions
      </th>
      
      <th style="text-align: left;" align="center" valign="middle">
        Bitrate Required (Mbps) 
      </th>
      
      <th style="text-align: left;" align="center" valign="middle">
         Camera Requirements
      </th>
      
      <th style="text-align: left;" align="center" valign="middle">
         FMLE HW Requirements Broadcaster Uplink
      </th>
      
      <th style="text-align: left;" align="center" valign="middle">
        Viewer Downlink Requirements (Mbps) 
      </th>
      
      <th style="text-align: left;" align="center" valign="middle">
        Throughput example for 1000 concurrent viewers of 1 hour broadcast 
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
         320x240
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        0.3
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        Dual Core 2GB RAM
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        0.4 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        135 GB
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
         640x480
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        1.4 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        Support frame size & bit rate 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        Quad Core Zeon 3GB RAM
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        2 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        630 GB 
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
         1024x720
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        3.5 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        8 Core Xeon 3GB RAM 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        5 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 16%; text-align: left;">
        1600 GB  
      </td>
    </tr>
  </tbody>
</table>

For further reading on how to set up these parameters in the Flash Media Live Encoder, as well as additional advanced configuration options, see the <a href="http://help.adobe.com/en_US/FlashMediaLiveEncoder/3.0/Using/flashmedialiveencoder_3_help.pdf" target="_blank">FMLE guide</a>. 

[Back to Workflow][11]

 [/collapsed]

[collapsed title="Clipping and trimming Media Files"]

<p class="mce-heading-3">
  <a name="clipping"></a>Clipping and Trimming Media Files
</p>

You can create clips from existing videos, set in and out points. Each clip becomes its own media entry encoded to multiple flavors, and can be downloaded, distributed and played back on any device. You can also trim the length of a video directly from within the Kaltura Management Console. The clipping tool enables you to edit your videos visually or by setting the start time and end time of your clip. For additional information see [Server Side Clipping and Trimming][13].

 [13]: http://blog.kaltura.org/server-side-clipping-and-trimming

Clipping creates a new entry from an existing entry and allows you to specify the start and end time for the new entry. For example you can clip an entry that can be used to create a 2 minute intro video to a long lecture, or clip part of an entry, such as homework assignments. You can also clip a long lecture to several shorter clips divided by subjects. The new entry will point to its source entry so that you can always identify the source entry for the clip.

<p class="mce-procedure">
  To clip a media entry
</p>

1.  Select the Content tab and then select an entry from the Entries Table.
2.  In the Metadata tab, click Clip This.  
    <img src="{{site.url}}/assets/2359">
    The Clipping Tool window is displayed.
3.  Click Add New Clip.  
    <img src="{{site.url}}/assets/2360">
4.  Use the arrow to choose the granularity level for the display.  
    The choices are:  
    *   100%
    *   5 sec
    *   1 sec
    *   Frames
5.  Press Play and click Set In as the starting point of the video clip, or alternatively, select the start time.
6.  Select Set Out as the end point of the video clip, or alternatively select the end time.
7.  Provide a New name and Description for the clip (optional).
8.  Click Save.  
    The new clip appears in the Entries Table.

This Clips tab is available after you create a clip. The read-only list of all created clips includes the following information:

*   Name
*   ID
*   Creator
*   Plays
*   Duration

<p class="Procedure mce-procedure">
  To trim a media entry
</p>

1.  Select the Content tab and then select an entry from the Entries Table.
2.  In the Metadata tab, click Trim This.  
    <img src="{{site.url}}/assets/3079">
3.  Use the trimming timeline or enter exact in and out times.
4.  Press Play and click Set In as the starting point of the video clip or alternatively, select the start time.
5.  Select Set Out as the end point of the video clip, or alternatively select the end time.
6.  Provide a New name and Description for the clip (optional)
7.  Click Save.  
    The trimmed video appears in the entries table.

<h3 class="mce-heading-3">
  Troubleshooting Trimming and Clipping
</h3>

The Trim and Clip feature may be disabled if your transcoding profile does not include the flavor for the file you want to trim or clip.

When you upload content, new flavors are created from the Source flavor and transcoded to the flavors you define in your Transcoding Settings.

<p class="Procedure mce-procedure">
  To add the Source flavor to your transcoding profile
</p>

1.  Go to Settings tab and select the Transcoding Settings tab.
2.  At the bottom of the page, click Switch to Advanced mode.
3.  Click on the name of your default transcoding profile.
4.  In the Edit Transcoding profile check the Source flavor and then Save Changes.

 [/collapsed]

For more information see the  [Live Encoding Best Practices Guide][14].

 [14]: http://knowledge.kaltura.com/node/1559