---
layout: page
title: "Best Practices For Uploading Content Created Using Screencast Tools"
date: 2012-11-21 13:01:09
---

Best practices or Uploading Content to Kaltura are provided for the following screencast tools:

*   [Webex][1]
*   [Camtasia][2]
*   [GotToWebinar][3]

 [1]: #webex
 [2]: file:///C:/Users/Debbie/AppData/Local/Microsoft/Windows/Temporary%20Internet%20Files/Content.Outlook/5XXSIHB0/screencast%20source%20video_dzNov20.docx#_Camtasia
 [3]: file:///C:/Users/Debbie/AppData/Local/Microsoft/Windows/Temporary%20Internet%20Files/Content.Outlook/5XXSIHB0/screencast%20source%20video_dzNov20.docx#_GoToWebinar

## <a name="webex" href="http://www.webex.com/" target="_blank"></a><a href="http://www.webex.com" target="_blank">Webex</a>

Recorded sessions with Webex produce a proprietary* **ARF or WRF ***file formats that Kaltura cannot transcode. You can use the <a href="http://www.webex.com/play-webex-recording.html" target="_blank">Network Recording Player</a>, a desktop utility converter offered by Webex, to convert the ***arf ***format to one of the following formats:

*   MP4
*   WMV
*   SWF

After you convert content using Network Recording Player, and you upload the content to Kaltura, using the default transcoding profile, the video quality may not be optimal. The file is transcoded into flavors that are at a low bitrate, and then played on large frame size that does not display the content satisfactorily.

<p class="mce-procedure">
  To produce the best possible quality for a Webex screencast source video
</p>

1.  Record your screencast using the large screen option.
2.  Use the <a href="http://www.webex.com/play-webex-recording.html" target="_blank">Network Recording Player</a> and convert the file to MP4.
3.  [Upload Content to Kaltura.][4]

 [4]: file:///C:/Users/Debbie/AppData/Local/Microsoft/Windows/Temporary%20Internet%20Files/Content.Outlook/5XXSIHB0/screencast%20source%20video_dzNov20.docx#_Upload_the_Content

## <a name="camtasia" href="http://www.techsmith.com/camtasia.html" target="_blank"></a>[Camtasia][5]

 [5]: http://www.techsmith.com/camtasia.html

Camtasia offers 2 default formats:

*   **camrec** – does not transcode content properly since it is a Camtasia proprietary format.
*   **AVI** – does not transcode content properly since it uses tsc2 format which is not supported by Kaltura. tscc format is supported.

You can use the  “Produce and share” option offered by Camtasia and convert content to one of the following formats:  

*   MP4
*   WMV
*   MOV
*   M4V

After you convert content to one of the formats using the Camtasia tool, and you upload the content to Kaltura using the default transcoding profile, the video quality may not be optimal. The file is transcoded into flavors that are at a low bitrate, and then played on large frame size that does not display the content satisfactorily.

<p class="Procedure mce-procedure">
  To produce the best possible quality for a Camtasia screencast source video
</p>

*   Use the <a href="http://exchange.kaltura.com/content/camtasia-relay-publishing-plug" target="_blank">Camtasia Relay Publishing Plug-in for Kaltura<br /><br /></a>or:

1.  Record your screencast using the large screen option.
2.  Use the “Produce and share” option offered by Camtasia and convert your content to MP4.
3.  [Upload Content to Kaltura.][6]

 [6]: #upload

## <a name="webinar" href="http://www.gotomeeting.com/fec/webinar" target="_blank"></a><a href="http://www.gotomeeting.com/fec/webinar" target="_blank">GoToWebinar</a>

GoToWebinar offers 2 file formats:

*   **WMV** - source creates good transcoded videos.
*   **g2m4** - does not transcode content properly. The g2m4 source format requires an intermediate-source conversion to convert g2m4 into a format that ffmpeg can process. The resulting intermediate source is WMV format. When using a Mac,  g2m4 creates a mov file which produces good quality display on Kaltura.

<p class="Procedure">
       To produce the best possible quality for a GoToWebinar  screencast source video
</p>

1.  Record your screencast using the large screen option.
2.  Save the file in MP4 format.
3.  [Upload Content to Kaltura.][6]

After converting the g2m4 source format into the intermediate-source work-flow, the results produce a reasonable quality video, though this format is not optionally recommended.

## <a name="upload"></a>Upload Content to Kaltura

After you upload your content to Kaltura you must be certain that the entry is transcoded to the HD flavor (1080).

<p class="Procedure mce-procedure">
  To transcode content to HD in the Kaltura Management Console
</p>

1.  Select the Content tab
2.  Click on an entry and then select the Flavors tab.
3.  You can manually select the option to transcode the content to HD flavor (1080). Select Reconvert in the entry’s Action pull down menu.<img src="{{site.url}}/assets/867">
      
    or  
      
    You can create a 'Screencast Transcoding Profile' and check the Source and HD flavors only.<img src="{{site.url}}/assets/868">
      
    You can then set this profile as the default profile for future screencast uploads. See <a href="http://www.kaltura.com/content/docs/falconHelp/NetHelp/default.htm#!Documents/addingatranscodingpr.htm" target="_blank">Adding a Transcoding Profile</a> for more information.

<div>
  <br /><div>
     
  </div>
</div>