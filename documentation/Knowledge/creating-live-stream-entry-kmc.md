---
layout: page
title: "Creating a live stream entry in the KMC"
date: 2013-02-12 15:37:10
---

## Creating a Live Streaming Entry in the KMC

<p class="mce-procedure">
  To create a live stream entry in the KMC
</p>

1.  Login into the KMC and go to the Upload tab.
    
    <img src="../../assets/990">

2.  Select Live Stream Entry.  
    The Add New Stream window appears.<span style="font-size: 10px;"><br /><img src="../../assets/983">
3.  <span style="font-size: 10px;"></span>Select the Live Stream Type.  
    The following Live Stream types are available:<span style="font-size: 10px;"><span style="font-size: 10px;"><br /></span></span>
    *   **Desktop and Mobile (HDS/HLS) Akamai Universal Streaming** - Supports both flash HDS (Adobe HTTP Dynamic Streaming) and HLS (Apple HTTP Live Streaming) from a single ingested stream. Akamai universal live streaming also supports DVR functionality that allows you to seek back in time within the live stream window. The default DVR window is 30 minutes. Contact  Kaltura for more information.
    *   **Legacy Flash Streaming (RTMP)**  - Delivers live content as an RTMP stream. RTMP is limited to only desktop Flash and does not support DVR. We recommend migrating live streams to “Universal Streaming”.
    *   **Manual Live Stream URLs** -  Allows you to associate custom live end user URLs with a Kaltura entry. This option is useful if you are using a 3<sup>rd</sup> party to provision and broadcast a live stream.
4.  Fill in the required values and click Save.  The required fields depend on the Live Stream Type you select. An indication is displayed when required fields are not populated. The following are the Required / Optional fields for Desktop Flash and Mobile ( HDS / HLS ) and Legacy Flash Streaming only (RTMP)<table border="0" cellspacing="0" cellpadding="0">
      <tbody>
        <tr>
          <td valign="top" width="187">
            <p style="text-align: left;">
              <strong>Field</strong>
            </p>
          </td>
          
          <td valign="top" width="446">
            <p style="text-align: left;">
              <strong>Description</strong>
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="187">
            <p style="text-align: left;">
              Name
            </p>
          </td>
          
          <td valign="top" width="446">
            <p style="text-align: left;">
              <strong>Required,</strong> minimum 5 characters. The name of the stream that will appear in the KMC entries list.
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="187">
            <p style="text-align: left;">
              Description
            </p>
          </td>
          
          <td valign="top" width="446">
            <p style="text-align: left;">
              A description of the stream (Optional).
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="187">
            <p style="text-align: left;">
              Primary encoder IP
            </p>
          </td>
          
          <td valign="top" width="446">
            <p style="text-align: left;">
              <strong>Required</strong>, must match “ip” format ( can be IP6 ) The public address that will be used for streaming (the computer where the client encoder, for example Adobe FMLE is installed).
            </p>
            
            <p style="text-align: left;">
              Note: your IP address can be retrieved by browsing from the computer where the FMLE is installed to <a href="http://www.whatismyip.com/">http://www.whatismyip.com/</a>  0.0.0.0 cannot be used as your IP address.
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="187">
            <p style="text-align: left;">
              Secondary encoder IP
            </p>
          </td>
          
          <td valign="top" width="446">
            <p style="text-align: left;">
              <strong>Required</strong> ( can be the same as primary ). If you are using two encoders (for redundancy), fill in the secondary encoder IP. If you are using a single encoder, copy the Primary encoder IP to the Secondary encoder IP field.
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="187">
            <p style="text-align: left;">
              Broadcasting password
            </p>
          </td>
          
          <td valign="top" width="446">
            <p style="text-align: left;">
              (Optional) This password is required in the client encoder (FMLE) software. If you do not enter a password the system will automatically create one for you and it will be displayed in the Live Stream tab of the entry details window under “Broadcasting credentials”.
            </p>
          </td>
        </tr>
      </tbody>
    </table>
    
    <span style="font-size: 10px;"><span style="font-size: 10px;"></span></span>When using Kaltura’s SaaS edition, Kaltura will provision your new Live Stream with the CDN (for example, Akamai). The CDN will then populate the information about the new Live Stream to the CDN’s servers. This may incur up to a 20 minute delay, for the stream to become available for broadcasting. You should always provision your Live Stream ahead of time, and be certain that you have at least 20 minutes lead time to going live.
    Kaltura's uses Akamai as the default CDN. When using Kaltura’s SaaS edition, Kaltura will provision your new Live Stream with the CDN (for example, Akamai). The CDN  populates the information about the new Live Stream to the CDN’s servers which may incur up to a 20 minute delay for the stream to become available for broadcasting. You should always provision your Live Stream ahead of time, and be certain that you have at least 20 minutes lead time to going live. You can also use a CDN other than Akamai, however, you will have to provision the stream via the CDN portal, or through technical support, and then ask Kaltura Support to create a live stream entry pointing to the provisioned stream.   
    
    The following are the Required / Optional fields for the **Manual Live Stream URLs** stream type.
    
    <span style="font-size: 10px;"><span style="font-size: 10px;"></span></span><table border="0" cellspacing="0" cellpadding="0">
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="187">
            <p>
              <strong>Field</strong>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="446">
            <p>
              <strong>Description</strong>
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="187">
            <p>
              Name
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="446">
            <p>
              <strong>Required,</strong> minimum 5 characters. The name of the stream that will appear in the KMC entries list.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="187">
            <p>
              Description
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="446">
            <p>
              A description of the stream (Optional).
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="187">
            <p>
              Live Flash HDS stream URL
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="446">
            <p>
              <strong>Required</strong>, type URL
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="187">
            <p>
              Live Mobile HLS stream URL
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="446">
            <p>
              <strong>Optional</strong> type URL.
            </p>
          </td>
        </tr>
      </tbody>
    </table>

5.  <span style="font-size: 10px;"></span>Click Create Live Stream.

6.  [Configure the live stream parameters in the KMC.][1]

 [1]: #cfg_ls_parms

### Multiple Bitrate Encoding

To maintain the best possible viewing experience and video quality, it is often necessary to stream different versions of the encoded video to different clients using different devices and over variable connection speeds.

Multiple Bit Rate (MBR) encoding is designed to adjust to fluctuations in bandwidth while maintaining an acceptable quality. MBR combines several bit rates into a single encoded file. When the file is accessed, the player determines the appropriate bit rate based on the available bandwidth, and then retrieves the encoded file at the optimal bit rate.  If the available bandwidth decreases for any reason, a stream at a lower bit rate can then be served. With a lower bit rate, there is often a decrease in quality. 

### <a name="cfg_ls_parms"></a>Configuring the Live Stream Parameters in the KMC

<p class="Procedure mce-procedure">
  To configure the live stream parameters
</p>

1.  Go the Content tab in the KMC.
2.  Click on the Live Stream Entry in the Entries table.
3.  Select the Live Stream tab.<span style="font-size: 10px;"><span style="font-size: 10px;"></span></span>
    For the **Legacy Flash** **Streaming** **only (RTMP)** option:
    
    *   Enter the bitrate configuraiton as instructed
    *   Click Save. 
    
    <span>For the </span>**Universal Streaming**<span> option: in the Live Stream Configuration section enter the following:</span>
    
    <span style="font-size: 10px;"><span style="font-size: 10px;"></span></span>
    *   HLS Stream URL—Enter the hlsStreamUrl
    *   Akamai Stream ID – Enter the externalStreamId
    *   DVR Status -- dvrStatus on/off Default is off.
    *   DVR Window –  listed in npt format hh:mm:ss of DVR window
    <span style="font-size: 10px;"><span style="font-size: 10px;"></span></span>
    For the **Manual Live Stream URL **option, the live stream tab within the KMC lists the live stream URLs that were provided .
    
    <span style="font-size: 10px;"><span style="font-size: 10px;"></span></span>
    *   HDS stream url – {value}
    *   HLS stream Url – {value}
4.  Set the MBR. (Optional)  
    When broadcasting with MBR the player will choose the most appropriate bitrate to stream. Be certain that your client encoder is aligned with the same settings.  
    Determining the right bit rates for your Live Stream is generally dependent on the quality of your video, the size of the player your viewers will use, the bandwidth your client encoder computer has and the bandwidth of your viewers. It is common to have widths of 240, 360, 480, 720 and 1080 with HD content streaming. If you are broadcasting a webcam, it is generally best to use the default KMC settings. To get professional assistance, please contact Kaltura’s support.
5.  Click Save.