---
layout: page
title: "How to Add an Audio Description Track to Play on the Kaltura 508 Player"
date: 2013-02-28 23:09:52
---

Audio Description Tracks allow playback of an additional narration track for blind and visually impaired viewers while using the Kaltura Player.

The Kaltura v2 Player is 508 compliant. For more information see the <a href="{{site.url}}/documentation/Knowledge/universal-studio-information-guide.html" target="_blank">Universal Stuido Information Guide.</a>

<h3 class="mce-heading-3">
  508 Compliancy
</h3>

All Universal Studio players are 508 compliant. The player’s features include:

*   Support for captions file in timed text or SRT formats for the video/audio file 
*   Support for an audio description in a standardized format for the video/audio file
*   Hidden text elements for every non-text element (for screen readers)
*   Tooltips
*   Keyboard tabbing and controls

For more information see <a href="{{site.url}}/documentation/Knowledge/508-support-within-kaltura-player-toolkit.html" target="_blank">508 Support within the Kaltura Player Toolkit</a>.

<p class="mce-note-graphic">
  The following information for the 508 compliant V1 player has been deprecated.
</p>

<p class="mce-procedure">
  Adding an Audio Description to an Entry Workflow
</p>

1.  In the Upload tab, <a href="{{site.url}}/documentation/Knowledge/how-use-upload-tab.html" target="_blank">upload an entry</a>.
2.  <a href="{{site.url}}/documentation/Knowledge/how-create-player.html" target="_blank">Create a 508 player</a> and <a href="{{site.url}}/documentation/Knowledge/how-add-content-player.html" target="_blank">add content to the player</a>.
3.  Configure the player’s Subtitles and Transcriptions options and check Audio Description. 
4.  Select an entry and [assign an audio description file to the entry][1].
5.  Hear[ the entry with the audio description.][2]

 [1]: #assign
 [2]: file:///C:/Users/Debbie/Documents/KMC/Hercules/Kaltura_Management_Console_(KMC)_User_Manual_gemini_updates.docx#_Viewing_an_Entry

     <a name="assign"></a><span class="mce-procedure">To assign an audio description file to an entry</span>

1.  Select the Content tab and click on an entry.
2.  Add a custom data field. See  <a href="{{site.url}}/documentation/Knowledge/how-add-fields-custom-metadata-profile.html" target="_blank">Adding Custom Data Fields.</a>
3.  Add a text field named “AudioFile”.  
4.  Select the Metadata tab.
5.  Enter the value of the URL of the audio file.  
    <img src="../../assets/1060">
6.  Click Save.

<p class="mce-procedure">
  To hear the audio file
</p>

1.  Select the entry that you added the audio file to.
2.  Click Preview and Embed.
3.  Select the 508 Player.
4.  Click AD to On.
5.  Press Play.

The following is an example of an entry with the Audio Description turned on.<img src="../../assets/992">

[Here][3] you can find an example that demonstrates the functionality. You can turn the background music on/off by clicking the "AD" button on the player. Please keep in mind that background music is obviously not the typical use case, and is just used for demo purposes.

 [3]: http://projects.kaltura.com/ariel/508/Kaltura_508_player.html

<p class="mce-heading-3">
  How to Use a Kaltura Entry as an Audio Description Track<span></span>
</p>

<p class="mce-note-graphic">
  This is an advanced topic and requires prior knowledge of the Kaltura APIs.
</p>

You will need to provide a URL to an audio file  in a dedicated custom metadata field as described in step 5 of [Assigning an Entry][1]. It is possible to store the audio file as a Kaltura Audio entry and then use the Kaltura APIs to pull the URL to the audio asset in Kaltura.

<p class="mce-procedure">
  To use a Kaltura Entry as an Audio Description Track
</p>

1.  Upload an audio file to Kaltura. You can use any of Kaltura's ingestion methods, such 'Upload From Desktop' in the KMC, bulk upload using an xml file or using the Kaltura APIs.
2.  Make sure the entry is Ready.
3.  Using the Kaltura APIs call the media->Get() service providing the entry id of the newly uploaded audio entry.
4.  <span style="font-size: 10px;">Use the </span><strong style="font-size: 10px;">downloadUrl</strong><span style="font-size: 10px;"> property of the returned </span><strong style="font-size: 10px;">KalturaMediaEntry</strong><span style="font-size: 10px;"> object as the URL in step 5 in the instructions above.</span>

Code example:

<pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;?php
  require_once('lib/KalturaClient.php');
  $config = new KalturaConfiguration($partnerId);
  $config-&gt;serviceUrl = 'http://www.kaltura.com/';
  $client = new KalturaClient($config);
  $entryId = '0_wia6rhpq';
  $version = null;
  $result = $client-&gt;media-&gt;get($entryId, $version);
  $url = $result['downloadUrl']; // this is the url to asset and can be used in step 4 above
?&gt;</pre>

 