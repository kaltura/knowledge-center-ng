---
layout: page
title: "Legacy Live Streaming via CDN Provisioning"
date: 2011-12-25 14:46:35
---

<p class="mce-heading-1 mce-heading-4">
  For the latest information on Live Streaming, see the additional articles in the Related URLs section.
</p>

<p class="mce-heading-1">
  Live Streaming
</p>

You can broadcast live streams through a Content Delivery Network (CDN) such as Akamai, through the KMC. The encoding software installed (such as FMLE) encodes your real-time camera signal and sends it out through a secure RTMP connection to the CDN. Then, using a Kaltura Player, you can embed the live broadcast in your websites. You can set the live stream entry metadata and specify broadcasting settings in the KMC in the same way VOD content is managed. 

By using a CDN for live streaming, you guarantee a better experience for your viewers world-wide. 

<span class="mce-note-graphic">In the Kaltura SaaS Edition, Live Streaming is an additional service. <br />To add Live Streaming to your account, contact your Account Manager.</span>

In Kaltura Community Edition, Live Streaming requires a Flash Streaming Server software installed such as Adobe FMS, Red5 and Wowza or alternatively, an Akamai CDN account.

 

<span class="mce-procedure">To enable live streaming for your account </span>

<span class="mce-sub-heading">Kaltura SaaS and On Prem Customers</span>

•<span class="Apple-tab-span" style="white-space: pre;"> </span><a href="http://corp.kaltura.com/company/contact-us" target="_blank" title="Contact Us">Contact us</a> or call +1-800-871-5224

Once your account is enabled you can set up Kaltura’s Live Streaming service.

This section describes how to set up the KMC, the encoder, and a device for the live streaming service.

<p class="mce-sub-heading">
  Users of Kaltura CE
</p>

To enable live streaming and webcam recording on Kaltura CE, you must have a Streaming Server (such as Adobe FMS, Red5 and Wowza) or a Live Streaming enabled CDN account.

Then you will need to integrate your Streaming Server or CDN with your Kaltura CE. Read "<span style="background-color: #ffffff;"><a href="http://blog.kaltura.org/rtmp-vod-and-live-streaming-using-red5-and-kaltura-ce-4" target="_blank"><span style="background-color: #ffffff;">How to integrate Kaltura CE 4.0 with Red5</span></a></span>" on our blog if you use Red5 (can be used with other Streaming Servers).

 

<p class="mce-heading-2">
  <a name="workflow_4ls"></a>Workflow for Setting up Live Streaming
</p>

1.  [Set up the Hardware and Software][1].
2.  [Create a Live Streaming Entry in the KMC][2].
3.  [Configure the Live Streaming Parameters in the KMC][3].
4.  [Set up the Broadcasting Computer][4].
5.  [View the Broadcasting Setup (optional)][5]

 [1]: #Setting_Up_HW "Setting Up the Hardware and Software for Live Streaming"
 [2]: #Creating_LS_Entry
 [3]: #Cfg_LS_Parm_in_KMC
 [4]: #Settin_Up_Broadcasting_comp
 [5]: #Viewing_Broadcast_setup

 

<a name="Setting_Up_HW"></a><span class="mce-heading-3">Setting up the Hardware and Software</span>

<p class="mce-procedure">
    To set up the hardware and software for live streaming
</p>

1.  Download the Flash Media Live Encoder (FMLE) from: <a href="http://www.adobe.com/products/flashmediaserver/flashmediaencoder/" target="_blank" title="Flash Media Encoder">http://www.adobe.com/products/flashmediaserver/flashmediaencoder/</a>
2.  Install the FMLE on your local Windows machine. 
3.  Connect your camera to the installed computer.

<p class="mce-note-graphic">
  NOTE: Be certain that your system has the minimum requirements. <br />See <a href="http://www.adobe.com/products/flashmediaserver/flashmediaencoder/systemreqs/" target="_blank">http://www.adobe.com/products/flashmediaserver/flashmediaencoder/systemreqs/</a> for details.
</p>

<a name="Creating_LS_Entry"></a><span class="mce-heading-3">Creating a Live Streaming Entry in the KMC</span>

<p class="mce-procedure">
  To create a live streaming entry in the KMC
</p>

1.  Login into the KMC and go to the Upload tab.
2.  Select Live Stream Entry.  
    <img src="../../assets/98.img">
3.  Then the Add New Stream window appears.  
    <img src="../../assets/102.img">
4.  Fill in the values and click Save. 

 

<p class="mce-sub-heading">
  The following table describes the input fields
</p>

<table class="kaltura-table" style="width: 100%;">
  <thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 50%; text-align: left;">
         Field
      </th>
      
      <th class="kaltura-table-head-item" style="width: 50%; text-align: left;">
         Description
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td style="text-align: left;">
        Name 
      </td>
      
      <td style="text-align: left;">
        The name of the stream that will appear in the KMC entries list. 
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="text-align: left;">
        Description
      </td>
      
      <td style="text-align: left;">
        A description of the stream (optional). 
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="text-align: left;">
        Primary Encoder IP
      </td>
      
      <td style="text-align: left;">
        <p>
          The public address that will be used for streaming (the computer where the client encoder such as Adobe FMLE is installed).
        </p>
        
        <p>
          Note: Your IP address can be retrieved by browsing from the computer where the FMLE is installed to http://www.whatismyip.com/ 
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="text-align: left;">
        Secondary Encoder IP
      </td>
      
      <td style="text-align: left;">
        If you are using two encoders (for redundancy), fill in the secondary encoder IP. If you are using a single encoder, copy the Primary encoder IP to the Secondary encoder IP field.  
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td style="text-align: left;">
        Broadcasting password
      </td>
      
      <td style="text-align: left;">
        This password is required in the client encoder (FMLE) software. If you do not enter a password the system will automatically create one for you and it will be displayed in the Live Stream tab of the entry details window under “Broadcasting credentials”. 
      </td>
    </tr>
  </tbody>
</table>

 

<p class="mce-note-graphic">
  NOTE: When using Kaltura’s SaaS edition, Kaltura will provision your new Live Stream with the CDN (for example, Akamai). The CDN will then populate the information about the new Live Stream to the CDN’s servers. This may incur up to a 20 minute delay, for the stream to become available for broadcasting. You should always provision your Live Stream ahead of time, and be certain that you have at least 20 minutes lead time to going live.
</p>

 

Kaltura's uses Akamai as the default CDN. You can also use a CDN other than Akamai, however, you will have to provision the stream via the CDN portal, or through technical support, and then ask Kaltura Support to create a live stream entry pointing to the provisioned stream.

<p class="mce-heading-2">
  Multiple Bitrate Encoding
</p>

To maintain the best possible viewing experience and video quality, it is often necessary to stream different versions of the encoded video to different clients using different devices and over variable connection speeds.

Multiple Bit Rate (MBR) encoding is designed to adjust to fluctuations in bandwidth while maintaining an acceptable quality. MBR combines several bit rates into a single encoded file. When the file is accessed, the player determines the appropriate bit rate based on the available bandwidth, and then retrieves the encoded file at the optimal bit rate.  If the available bandwidth decreases for any reason, a stream at a lower bit rate can then be served. With a lower bit rate, there is often a decrease in quality.

<p class="mce-heading-3">
  <a name="Cfg_LS_Parm_in_KMC"></a>Configuring the Live Stream Parameters in the KMC
</p>

<p class="mce-procedure">
  To configure the live stream parameters
</p>

1.  Go the Content tab in the KMC.
2.  Click on the Live Stream Entry in the Entries table.
3.  Select the Live Stream tab.
4.  Set the MBR. (Optional)

*   When broadcasting with MBR the player will choose the most appropriate bitrate to stream. Be certain that your client encoder is aligned with the same settings.
*   Determining the right bit rates for your Live Stream is generally dependent on the quality of your video, the size of the player your viewers will use, the bandwidth your client encoder computer has and the bandwidth of your viewers. It is common to have widths of 240, 360, 480, 720 and 1080 with HD content streaming. If you are broadcasting a webcam, it is generally best to use the default KMC settings. To get professional assistance, please contact Kaltura’s support.

<img src="../../assets/103.img">

  
<img src="../../assets/108.img">

 

<p class="mce-heading-3">
  <a name="Settin_Up_Broadcasting_comp"></a>Setting up the Broadcasting Computer
</p>

<p class="mce-procedure">
   <span class="Apple-tab-span" style="white-space: pre;"> </span>To set up the broadcasting computer
</p>

1.  Connect your camera /recording device to the broadcasting computer.
2.  Run the Adobe Flash Media Live Encoder (FMLE).
3.  Select the relevant recording Device from the drop-down menu. Copy the details of the live entry to the Flash Media Live Encoder. You can copy the details manually, or use the “Export XML to FME” option.
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
    Use the Preset dropdown menu in the FMLE to select the MBR.<br />Enter the Bit Rates as configured in the KMC. If you select to Save to File, you must append %i to the 'Stream' field.<br /><span class="mce-note-graphic">The Stream name is formatted for use with the FMLE. If you are using an encoder other then FMLE, such as Wirecast, you will need to replace the "%i" with a "1". For example, remove the % and replace the i with a 1 for the first stream or 2 if it is the second stream and so on.</span>
  </li>
</ol>

4.  Click Connect.
5.  Enter the Broadcasting credentials, (User Name and Password) as configured in the KMC Live Stream tab and click OK. The system will prompt you twice for the Broadcasting credentials. 
6.  Click Start. You are now broadcasting live.
7.  When your broadcast is finished, click Stop.

 

<p class="mce-heading-3">
  <a name="Viewing_Broadcast_setup"></a>Viewing the Broadcasting Setup (Optional)
</p>

<span class="mce-procedure">To view the  broadcasting setup</span>

1.  Return to the KMC and select the Content tab.
2.  In the KMC Entries Table, click the Preview & Embed link for the live stream entry.  
    <img src="../../assets/107.img">
3.  Select the player from the drop-down menu and copy the Embed Code.
4.  Paste the Embed Code within an HTML page.<span class="Apple-tab-span" style="white-space: pre;"> </span>
5.  Browse to the page where the embed code was inserted and press Play on the video player.

 

<p class="mce-heading-4">
  Advanced Configuration Options
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

For further reading on how to set up these parameters in the Flash Media Live Encoder, as well as additional advanced configuration options, refer to the FMLE guide available at: <a href="http://help.adobe.com/en_US/FlashMediaLiveEncoder/3.0/Using/flashmedialiveencoder_3_help.pdf" target="_blank" title="FMLE Guide">http://help.adobe.com/en_US/FlashMediaLiveEncoder/3.0/Using/flashmedialiveencoder_3_help.pdf</a>

For the latest information on Live Streaming see the additional articles in the Related URLs section.