---
layout: page
title: "Creating a Live Stream Entry in Kaltura Using the KMC"
date: 2011-12-25 21:59:12
---

<p class="mce-procedure">
  <span style="font-size: small;">To create a Live Stream entry in the KMC</span>
</p>

1.  Login into the KMC and click on the Upload tab, then click on "Live Stream Entry".  
    <img src="{{site.url}}/assets/3370">
    The Add New Stream window is displayed.  
    <img src="{{site.url}}/assets/3371">
2.  Configure the live stream attributes according to your preferences.  
    <table class="relative-table confluenceTable tablesorter tablesorter-default stickyTableHeaders">
      <colgroup><col /><col /></colgroup><thead class="tableFloatingHeaderOriginal">
        <tr class="tablesorter-headerRow">
          <th class="confluenceTh tablesorter-header sortableHeader tablesorter-headerUnSorted" scope="col" data-column="0">
            <div class="tablesorter-header-inner">
              Attribute
            </div>
          </th>
          
          <th class="confluenceTh tablesorter-header sortableHeader tablesorter-headerUnSorted" scope="col" data-column="1">
            <div class="tablesorter-header-inner">
              Description
            </div>
          </th>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td class="confluenceTd" style="text-align: left;">
            <strong>Live Stream Type</strong>
          </td>
          
          <td class="confluenceTd" style="text-align: left;">
            <p>
              <strong>Kaltura Live Streaming (HDS / HLS / DASH)</strong> – This is the default and recommended live streaming type. Kaltura Live Streaming services are provisioned within the Kaltura data centers. Cloud transcoding, extended DVR window, live to VOD recording with a single embed code, instant provisioning, and multi-protocol delivery are supported.  Depending on your live streaming package, simultaneous cloud transcoding may be restricted.
            </p>
            
            <p>
              <strong>Manual Live Stream URLs</strong> - This mode allows you to associate custom live external URLs with a Kaltura live entry. This option is useful if you are using a 3<sup>rd</sup> party to provision and broadcast a live stream.
            </p>
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd" style="text-align: left;">
            <strong>Name</strong>
          </td>
          
          <td class="confluenceTd" style="text-align: left;">
            The name of the stream that will appear in the KMC entries list. This attribute is <strong>required, </strong>minimum is 5 characters.
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd" style="text-align: left;" colspan="1">
            <strong>Description</strong>
          </td>
          
          <td class="confluenceTd" style="text-align: left;" colspan="1">
            <p>
              A description of the stream/channel (Optional).
            </p>
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd" style="text-align: left;">
            <p>
              <strong>Live Transcoding Profile</strong>
            </p>
          </td>
          
          <td class="confluenceTd" style="text-align: left;">
            <p>
              Select a transcoding profile from the drop down list. The available options are Cloud Transcode and Pass-through
            </p>
            
            <p>
              <strong>Cloud Transcode</strong> – This option enables cloud transcoding for this live entry. A single bitrate coming from your encoder will be transcoded in the Kaltura cloud into multi-bitrate flavors. The default cloud transcoding profile includes the source stream + 3 transcoded flavors. You can set additional transcoding profiles for live streaming. <br />To customize transcoding profiles or broadcast multiple cloud-transcode streams simultaneously, please contact your Kaltura account manager.
            </p>
            
            <p>
              <strong>Pass-through</strong> - This option enables pass-through mode for this live entry. Kaltura will deliver the stream(s) from your encoder without re-encoding.
            </p>
            
            <p>
              For more information about the differences between pass-through and cloud-transcode and which one is better for you, please refer to TBD
            </p>
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd" style="text-align: left;" colspan="1">
            <strong>Enable Live DVR</strong>
          </td>
          
          <td class="confluenceTd" style="text-align: left;" colspan="1">
            Check this to enable Live DVR. Live DVR provides the ability to seek back within the live stream up to 2 hours prior to the current live point. The DVR duration can be extended up to 24 hours. To extend the time, please contact your Kaltura account manager.
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd" style="text-align: left;" colspan="1">
            <p>
              <strong>Enable Recording</strong>
            </p>
          </td>
          
          <td class="confluenceTd" style="text-align: left;" colspan="1">
            <p>
              Check this to enable recording of the live stream into a VOD available for later viewing.  Select one of the following options:
            </p>
            
            <ul>
              <li>
                Append the recorded content to a single entry - This option appends any live stream recording into the same VOD. Choose it if want to append several live events into one recording.
              </li>
            </ul>
            
            <ul>
              <li>
                Create new Entries for each broadcast session - This option creates a new VOD for each broadcast session. In this mode each live event is recorded in a different VOD.<ul>
                  <li>
                    To split recordings between broadcast sessions, we recommend to stop broadcasting for at least 5 minutes before starting a new event. Otherwise the system assumes an accidental disconnect and will continue appending the recorded content.
                  </li>
                </ul>
              </li>
            </ul>
            
            <p>
              <strong>Notes: Recordings are limited to 24 hours. After 24 hours, recording will stop.</strong>
            </p>
          </td>
        </tr>
      </tbody>
    </table>

3.  Click "Create Live Stream" to create the live entry ID.

<a href="https://knowledge.kaltura.com/node/1750" target="_blank">Back</a>

<span style="font-size: small;"> </span>