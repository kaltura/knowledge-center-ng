---
layout: page
title: "How to add an audio description track to the Kaltura V2 Player."
date: 2014-11-17 15:40:02
---

<p id="HowtoAddanAudioDescriptionTracktoPlayontheKalturaV2Player.-EnablingAudioDescriptionbyeditingtheJSONconfigoftheplayer:" class="mce-procedure">
  To enable the Audio Description Track 
</p>

<p style="padding-left: 30px;">
  You can enable the audio description track by editing the JSON config of the player.
</p>

1.  Open the <a href="http://player.kaltura.com/kWidget/tests/PlayerVersionUtility.html" target="_blank" class="external-link" rel="nofollow">player version utility webpage</a>, Click Login to Kaltura.  
    <img src="{{site.url}}/assets/2335">
      
    
2.  Log in using your Kaltura username and password and click Login.  
      
    <img src="{{site.url}}/assets/2334">
      
    
3.  Select Allow access then click Save and Close.  
      
    <img src="{{site.url}}/assets/2332">
      
    
4.   After you are logged in, paste the ID of the player you want to edit and select Edit Player.  
    <img src="{{site.url}}/assets/2331">
      
    
5.   Click the Edit JSON config button.  
      
    <img src="{{site.url}}/assets/2330">
      
    
6.  A new window is displayed. You will need to add a new line after "plugins":{   
      
    <img src="{{site.url}}/assets/2329">
      
    
7.  Insert the following lines of code describing the Audio Description plugin:  
      
    <img src="{{site.url}}/assets/2328">
      
    "audioDescription": {  
    "plugin": true,  
    "width": "0%",  
    "height": "0%",  
    "includeInLayout": false,  
    "volume": 1,  
    "file": "{mediaProxy.entryMetadata.AudioFile}"  
    },

8.  Click Save Changes to apply these new settings.  
      
    <img src="{{site.url}}/assets/2325">
      
    

<p id="HowtoAddanAudioDescriptionTracktoPlayontheKalturaV2Player.-AddingCustomMetadatafield" class="mce-procedure">
  To Add Custom Metadata Fields
</p>

After enabling the Audio Description plugin, you will need to add a Custom Metadata field that is used to instruct the player which audio file to play.

1.  Create a new text custom metadata field, name it "AudioFile". See the instructions on [How to Add Fields to Custom Metadata Profile.][1]
2.  [][1]After creating the custom metadata field, select the entry you want to add the Audio Description to , and insert the direct URL for the audio file in the AudioFile field.  
    <img src="{{site.url}}/assets/2324">
3.  Click the Save & Close button.

 [1]: http://knowledge.kaltura.com/node/347