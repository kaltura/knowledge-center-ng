---
layout: page
title: "Configuring Live Streaming on a KMC Account Using a BitGravity Account"
date: 2014-03-25 22:33:59
---

 The following topics are described:

*   [Creating a Live Streaming Entry in the KMC (non DVR)][1]
*   [Adjusting the Live Stream for HDS and RTMP Support][2]
*   [Creating a DVR Enabled Live Streaming Entry Using the APIs][3]

 [1]: #non_dvr
 [2]: #adjusting
 [3]: #dvr

Currently, live streaming provisioning using your BitGravity account can be done upon request and with the BitGravity CDN support team’s assistance that will be provisioning live feeds. Each live feed represents a single bit rate live stream:

<span style="font-size: 12px;"><img src="{{site.url}}/assets/1397">

After live feeds are provisioned you can manage them (edit some of the settings), playback and publish URLs:

<img src="{{site.url}}/assets/1404">

For example, for the live feed **/kaltura/live/cdg/live01** the playback URLs will be as following:

<table class="LightList-Accent11" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="152">
        <p class="TableHeading">
          <strong>Delivery Protocol</strong>
        </p>
      </td>
      
      <td valign="top" width="647">
        <p class="TableHeading">
          <strong>URL Generated</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="152">
        <p class="TableBodyText">
          <strong>RTMP</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="647">
        <p class="TableBodyText">
          Server: rtmp://kaltura.live-s.cdn.bitgravity.com/cdn-live
        </p>
        
        <p class="TableBodyText">
          Stream: /kaltura/live/cdg/live01
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="152">
        <p class="TableBodyText">
          <strong>Adobe HDS</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="647">
        <p class="TableBodyText">
          http://kaltura.live-s.cdn.bitgravity.com/cdn-live/_definst_/kaltura/live/cdg/live01/manifest.f4m
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="152">
        <p class="TableBodyText">
          <strong>Apple HLS</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="647">
        <p class="TableBodyText">
          http://kaltura.live-s.cdn.bitgravity.com/cdn-live/_definst_/kaltura/live/cdg/live01/playlist.m3u8
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <a name="non_dvr"></a>Creating a Live Streaming Entry in the KMC (<span>non DVR)</span>
</p>

<p class="Procedure mce-procedure">
  To create a live stream entry in the KMC
</p>

1.  Login into the KMC and go to the Upload tab.  
      
    <img src="{{site.url}}/assets/1405">
2.  Select Live Stream Entry.  
    The Add New Stream window is displayed.  
    <img src="{{site.url}}/assets/1406">
3.  Select Manual Live Stream URLs.  
    **Manual Live Stream URLs** - Allow you to associate custom live end user URLs with a Kaltura entry. This option is useful if you are using a 3<sup>rd</sup> party to provision and broadcast a live stream.
4.  Enter values for the following fields:  
      
    <table border="0" cellspacing="0" cellpadding="0">
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="229">
            <p>
              <strong>Field</strong>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="539">
            <p>
              <strong>Description</strong>
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="229">
            <p>
              Name
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="539">
            <p>
              <strong>Required,</strong> minimum 5 characters. The name of the stream that will appear in the KMC entries list.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="229">
            <p class="TableBodyText">
              Description
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="539">
            <p class="TableBodyText">
              A description of the stream (Optional).
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="229">
            <p class="TableBodyText">
              Live Flash HDS stream URL
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="539">
            <p class="TableBodyText">
              <strong>Required</strong>, type URL
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="229">
            <p class="TableBodyText">
              Live Mobile HLS stream URL
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="539">
            <p class="TableBodyText">
              <strong>Optional</strong> type URL. 
            </p>
          </td>
        </tr>
      </tbody>
    </table>

5.  Fill in the values and click Create Live Stream.

<p class="mce-heading-4">
  <a name="adjusting"></a>Adjusting the Live Stream for HDS and RTMP Support
</p>

<p class="Procedure mce-procedure">
      To modify the live stream entry in the KMC
</p>

1.  Login into the KMC and go to the Settings tab.
2.  Select Integration Settings to obtain the “Administrator Secret”.
3.  Go to the TestMe Console <a href="http://www.kaltura.com/api_v3/testme/" target="_blank">http://www.kaltura.com/api_v3/testme/</a>
4.  Create a Kaltura Session (KS):
<ol style="list-style-type: lower-alpha;">
  <li>
    Select service “session”, and select action “Start”
  </li>
  <li>
    Fill in the secret (using “Administrator Secret” obtained in <a href="file:///C:/Users/debbie.zioni/Documents/BitGravity/BitGravity_Live_Streaming_Information_Guide_june8dz.docx#admin_secret">step 2</a>)
  </li>
  <li>
    Enter the “userId”
  </li>
  <li>
    Set “type” to “ADMIN”
  </li>
  <li>
    Fill in the “partnerId”.
  </li>
  <li>
    Click Send.<br />The result should be a Kaltura session that is automatically copied to the “KS” field.<br /><img src="{{site.url}}/assets/1451">
  </li>
</ol>

5.  Copy the newly created live stream entry ID from the KMC.  
    <img src="{{site.url}}/assets/1452">
6.  In the <a href="http://www.kaltura.com/api_v3/testme/" target="_blank" style="font-size: 10px;">TestMe Console</a>, Select service “liveStream”, and Select action “update”.
7.  Copy/paste the entry id to the “entryId” field.
8.  Click on the “Edit” button near “liveStreamEntry”.
9.  Click Send.  
    <img src="{{site.url}}/assets/1453">

    <span class="mce-procedure">To adjust the livestream for HDS support</span>

1.  Under “liveStreamConfigurations array” click “Add” to add an item for live stream configuration (if you don’t see it then scroll down):  
    <img src="{{site.url}}/assets/1454">
2.  Edit the item (item0)

<ol style="list-style-type: lower-alpha;">
  <li>
    Set the “protocol” to “HDS”.
  </li>
  <li>
    Fill the “URL” for HDS playback taken from the BitGravity dashboard (The same one that was used to create the manual live stream entry in the KMC).
  </li>
</ol>

    <span class="mce-procedure">To add RTMP support to the livestream</span>

1.  Enter the “streamName” with the name of the stream, taken from the BitGravity dashboard. For example: /customerid/live/feed01
2.  Enter the “streamUrl” with the base URL of the stream, taken from the BitGravity dashboard. For example: rtmp://customerid.live-s.cdn.bitgravity.com/cdn-live

<p style="padding-left: 30px;">
  <img src="{{site.url}}/assets/1455">
</p>

 

<span class="mce-heading-3"><a name="dvr"></a>Creating a DVR Enabled Live Streaming Entry Using the APIs</span>

The Digital Video Recorder (DVR) feature provides the ability to seek within the recorded video up to 24 hours prior to your existing point of the live stream. DVR controls allow you to scrub back in time, while the live stream is still in progress, to replay a highlight or check out a clip that may have missed.

<p class="mce-procedure">
  To create a DVR enabled live streaming entry using the APIs
</p>

1.  Obtain an  “Administrator Secret” from the KMC > Settings > Integration Settings.
2.  Go to the Kaltura TestMe console <http://www.kaltura.com/api_v3/testme/>
3.  [Create a Kaltura Session (KS)][4]:

 [4]: #create_ks

<p class="Procedure mce-procedure">
  <a name="create_ks"></a>To create a Kaltura Session (KS)
</p>

1.  In the KalturaTestme Console, select service “session”, Action “start”.
2.  Enter the secret (using “Administrator Secret” obtained in step 1)
3.  Enter the “userId”
4.  Set “type” to “ADMIN”
5.  Fill in the your “partnerId”.
6.  Click Send.  
    <img src="{{site.url}}/assets/1408">

The result is a Kaltura Session that is automatically copied to the “ks” field.

<p class="Procedure mce-procedure">
      To setup a liveStream service that is DVR enabled
</p>

1.  In the Kaltura Testme Console, select service “liveStream”, Action “add”.
2.  Set “sourceType” to “MANUAL\_LIVE\_STREAM”.
3.  Click “Edit” near the “liveStreamEntry” object.
4.  Enter a “name”.
5.  Set “dvrStatus” to “ENABLED”.  
      
    <img src="{{site.url}}/assets/1409">
6.  Set “dvrWindow” to the amount of minutes for the recording.
7.  <span style="font-size: 12px;">Set “mediaType” to “LIVE_STREAM_FLASH”.</span>
8.  <span style="font-size: 12px;"></span><span style="font-size: 12px;"><span style="font-size: 12px;">Under “liveStrConfigurations” click on “Add” twice, this adds 2 items (Scroll down if they are not visible on your screen):<img src="{{site.url}}/assets/1410">
    
    <ol style="list-style-type: lower-alpha;">
      <li>
        <span>Edit the first item (item0).</span>
      </li>
      <li>
        <span></span><span>Set the “protocol” to “HLS”.</span>
      </li>
      <li>
        <span>Enter the “url” for HLS playback taken from the BitGravity dashboard.</span>
      </li>
      <li>
        <span></span>Edit the second item (item1)
      </li>
      <li>
        Set “protocol” to “HDS”
      </li>
      <li>
        Enter the “url” for HDS playback taken from the BitGravity dashboard.
      </li>
    </ol>

9.  <span style="font-size: 12px;"></span><span style="font-size: 12px;">Click Send.</span>

<span class="mce-heading-3"></span><span style="font-size: 12px;"><br /></span>

<span style="font-size: 12px;"><span> </span></span>