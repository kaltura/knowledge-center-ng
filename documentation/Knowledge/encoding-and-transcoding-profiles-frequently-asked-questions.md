---
layout: page
title: "Encoding and Transcoding Profiles Frequently Asked Questions"
date: 2015-01-16 22:12:26
---

<table border="0">
  <tbody>
    <tr style="background-color: #ffffff;">
      <td>
        <p>
          <span style="font-family: verdana, geneva; color: #000000;">In this document you will learn about frequently asked questions about Encoding and Transcoding. </span>
        </p>
        
        <span style="font-family: verdana, geneva; color: #000000;">For a complete description about Kaltura's Transcoding Services, see </span><a href="{{site.url}}/documentation/Knowledge/kaltura-media-transcoding-services-and-technology.html" target="_blank">Kaltura Media Transcoding Services and Technology</a>.<p>
          <span style="font-family: verdana, geneva; color: #ffffff;"><span style="color: #000000;">In addition to this article,  you can also refer to best practices for Multi-Device Transcoding</span> <span style="color: #0000ff;"><a href="{{site.url}}/documentation/Knowledge/best-practices-multi-device-transcoding.html" target="_blank"><span style="color: #0000ff;">here</span></a>.</span></span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;"><span style="color: #ffffff;"><span style="color: #000000;">If you are unable to find the information that you are looking for here, please use the search bar above to search for the information you seek, or report a missing information: "</span><span style="color: #0000ff;"><a href="{{site.url}}/documentation/Knowledge/couldnt-find-what-youre-looking.html"><span style="color: #0000ff;">Couldn't find what you were looking for</span></a>?</span>” form</span>.</span>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">When a video is uploaded to the KMC, the video is associated with a conversion profile, also known as a Transcoding Profile. A Transcoding profile may be comprised of a single flavor or multiple flavors. For each upload session, you can select the Transcoding Profile. You can also set a default Transcoding Profile. A transcode is made from taking an encoded piece of video and then converting it into one or more newly and more compressed streams that can then be played in a player on a computer or mobile device depending on the settings and methods used. Kaltura flavors are transcoded versions of an entry that are used to specify resolutions and formats. You can select to generate or add multiple flavors to an entry, including flavors geared towards displaying media on mobile devices (low bandwidth, small screens, and/or HTML5 supporting devices).</span>

<span style="font-family: verdana, geneva;">A flavor is a single output file with its specific file type, bit-rate, GOP size, that may be used for playback, download or editing. The Kaltura platform supports ingestion of all forms of rich media (including video, images, audio, PDF, SWF files, etc.), and allows you to define different transcoding profiles, depending on your publishing needs. Additional transcoding flavors can easily be added for publishing across different devices, network bandwidths and screen sizes. Kaltura's transcoding decision layer engine supports more than 60 video and image formats as well as 140 video and audio codecs. When you upload content you determine what type of flavors you want to associate with your output. There are three transcoding profiles that are automatically created for new accounts:    </span>

*   <span style="font-family: verdana, geneva;">Default - the flavors included in the default transcoding profile of the account These flavors appear in the main Transcoding Settings page.    </span>
*   <span style="font-family: verdana, geneva;">Source Only - uploads the source file, but does not transcode it; the source is the original file uploaded as is. Other flavors will not be created.    </span>
*   <span style="font-family: verdana, geneva;">All Flavors - transcodes uploaded files into all of the flavors defined in the main Transcoding Settings page.</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">To display the default flavors for transcoding your content:</span>

1.  <span style="font-family: verdana, geneva;">Select the<strong> </strong>Settings tab and then select Transcoding Settings.</span>  
    <span style="font-family: verdana, geneva;"><img src="../../assets/2021">
2.  <span style="font-family: verdana, geneva;">The Default Transcoding Flavors window is displayed which contains the flavor selection of the Default Transcoding profile.<br /><img src="../../assets/2022">
3.  <span style="font-family: verdana, geneva;">Each file uploaded to the system is transcoded into the flavors that are checked.</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">Follow the steps <a href="{{site.url}}/documentation/Knowledge/how-edit-transcoding-profile.html" target="_blank">here</a> to edit transcoding profile.</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">This guide describes how to create transcoding profiles. <a href="{{site.url}}/documentation/Knowledge/how-create-transcoding-profile.html" target="_blank">Click here</a>.</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">The following options may be edited for each transcoding flavor selected in a Transcoding Profile:</span>

<span style="font-family: verdana, geneva;">Impact on Entry Readiness –Determines the impact of each specific transcoding flavor on entry readiness for publishing. The options are:</span>

*   <span style="font-family: verdana, geneva;">Required</span>
*   <span style="font-family: verdana, geneva;">Optional</span>
*   <span style="font-family: verdana, geneva;">No impact</span>

<span style="font-family: verdana, geneva;"><a href="{{site.url}}/documentation/Knowledge/what-are-editing-options-flavors-transcoding-profile.html" target="_blank">Click here</a> to learn more.</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">A default transcoding profile is included with the KMC. After you create a Transcoding Profile, an ID is created and listed in the Transcoding Profiles page.</span>  
<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">To assign a transcoding profile other than the default profile, to a bulk upload</span>

1.  <span style="font-family: verdana, geneva;">Set the ID from the Transcoding Profiles to the conversionProfileId in your CSV.</span>
2.  <span style="font-family: verdana, geneva;">Set the ID from the Transcoding Profiles List to the conversionProfileId in your XML file.</span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">The challenge of streaming video is to find the right balance between bitrate and resolution as it relates to an end user’s connection speed and system ability. There are far too many variables that could interrupt playback for us to account for them all, at least as of the time of this writing. Here is a short list of potential stream killing variables:</span>

*   <span style="font-family: verdana, geneva;">Device and Screen size</span>
*   <span style="font-family: verdana, geneva;">Internet Service Provider Connection Speed or Cap</span>
*   <span style="font-family: verdana, geneva;">Bandwidth available through the wireless router due to distance or usage</span>
*   <span style="font-family: verdana, geneva;">Network traffic to and from the sever hosting the video</span>
*   <span style="font-family: verdana, geneva;">The CPU and GPU abilities on the playing device</span>
*   <span style="font-family: verdana, geneva;">Browser brand and version</span>
*   <span style="font-family: verdana, geneva;">Available plugins such as Flash and Silverlight</span>
*   <span style="font-family: verdana, geneva;">Other programs running in the background.</span>

<span style="font-family: verdana, geneva;"><a href="{{site.url}}/documentation/Knowledge/best-practices-multi-device-transcoding.html" target="_blank">Learn more</a>.</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span><span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">The Flavors tab in the Edit Entry window allows you to manage the <em>flavors</em> that are available as well as replace media files and their transcoding flavors. <a href="{{site.url}}/documentation/Knowledge/how-use-flavors-tab.html" target="_blank">Learn more</a>.</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<span style="font-family: verdana, geneva;">To upload media files recorded from a webcam</span>

1.  <span style="font-family: verdana, geneva;">Select the Upload tab.</span>
2.  <span style="font-family: verdana, geneva;">Click Record from Webcam.</span>
3.  <span style="font-family: verdana, geneva;">Select the Transcoding Profile and click Next. See <a href="https://portal.kaltura.com/community-team/Shared%20Documents/Knowledge%20Management/Work%20in%20Progress/Kaltura%20Management%20Console%20(KMC)/KMC_UserManual_WIP.docx#_Configuring__Transcoding">Configuring Transcoding Profiles</a>.</span>
4.  <span style="font-family: verdana, geneva;">Select a webcam from the dropdown list and click Allow.</span>
5.  <span style="font-family: verdana, geneva;">Press Record to record your media file.</span>
6.  <span style="font-family: verdana, geneva;">When done, click Next.</span>
7.  <span style="font-family: verdana, geneva;">Enter a Name and all other relevant information for the webcam recording and click Next.</span>

<span style="font-family: verdana, geneva;">The recording is processed and added to the Entries table.</span>

<span style="font-family: verdana, geneva;"> </span> 



\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\_\_\_|\\___|

To learn more about the supported transcoding formats <a href="{{site.url}}/documentation/Knowledge/what-are-supported-transcoding-formats-saas-edition.html" target="_blank">Click here</a>.

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"></span><span style="font-family: verdana, geneva;"></span>

<span style="font-family: verdana, geneva;">_______________________________________________________________________________________</span>

<p class="p1">
  <span class="s1"><em>Transcoding </em></span><span class="s2">usage is defined as the volume in MB of transcoded assets, that are the output of transcoding. </span><span class="s1"><em>Transcoding </em></span><span class="s2">usage is measured and billed one time per transcode,  unlike Storage for example, which is measured and billed repeatedly per the consumed storage even if a new entry was not added. </span>
</p>

<p class="p1">
  <br /><span class="s2"></span>
</p>

<span style="font-family: verdana, geneva;"></span><span style="font-family: verdana, geneva;"></span>

<p class="p2">
  <span class="s1">_______________________________________________________________________________________</span>
</p>

<p class="p1">
  <span class="s1">Failed transcoded</span><span class="s2"> jobs</span><span class="s1"> are not counted, even if the failure was due to a corrupted source file (which may have been uploaded by the user) or due to a Kaltura </span><span class="s3"><em>transcoding </em></span><span class="s1">malfunction.</span>
</p>

<p class="p1">
  <span class="s1">For example:</span>
</p>

<ul class="ul1">
  <li class="li1">
    <span class="s1">A partner is uploading 10GB of source for transcoding.</span>
  </li>
  <li class="li1">
    <span class="s4"></span><span class="s3"><em>Transcoding </em></span><span class="s1">is done on the 10GB and outputs with 7 flavors of total 25GB (including the source).</span>
  </li>
  <li class="li1">
    <span class="s4"></span><span class="s3"><em>Transcoding </em></span><span class="s1">Usage will be 15GB (25GB - 10GB of source files)</span>
  </li>
</ul>

<p class="p1">
  <span class="s1">A more complex example may be as follows:</span>
</p>

<ul class="ul1">
  <li class="li1">
    <span class="s1">A partner is uploading 10GB of source for </span><span class="s3"><em>transcoding </em></span><span class="s1">as well as 2GB of ready-made flavors (not for transcoding).</span>
  </li>
  <li class="li1">
    <span class="s4"></span><span class="s3"><em>Transcoding </em></span><span class="s1">is done on the 10GB and outputs with 7 flavors. The total storage is 27GB.</span>
  </li>
  <li class="li1">
    <span class="s1">The partner then deletes 1GB of flavors.</span>
  </li>
  <li class="li1">
    <span class="s1">The total storage for this partner is 26GB.</span>
  </li>
  <li class="li1">
    <span class="s4"></span><span class="s3"><em>Transcoding </em></span><span class="s1">Usage in this case is 15GB (27GB – 2GB – 10GB).</span>
  </li>
  <li class="li1">
    <span class="s1">All the deleted flavors and the ready-made flavors do not impact the </span><span class="s3"><em>transcoding </em></span><span class="s1">usage.</span>
  </li>
</ul>

<span style="color: #888888;"></span>