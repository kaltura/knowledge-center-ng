---
layout: page
title: "KRecord Website Integration Guide"
date: 2013-06-25 18:04:47
---

<div class="mce-heading-3">
  Widget version:
</div>

This information pertains to KRecord v1.6.2 or higher. Previous versions may not support all mentioned flashvars or events.

<div>
   
</div>

<div class="mce-heading-3">
  Sample integration script:
</div>

[Download PHP integration sample script][1]. This script shows an embed of the KRecord widget, implementation of the various event handlers in JavaScript and playback of the recorded Entry when the Save button was clicked.

 [1]: http://cdnknowledge.kaltura.com//sites/default/files/krecord-and-playback-sample-script_1.zip

 

<h1 class="mce-heading-2">
  Load Methods
</h1>

KRecord can be loaded using  the follwoing methods.

*   [Self Hosted Files][2]
*   [Kaltura Uiconf][3]

 [2]: #self-hosted
 [3]: #Kaltura_uiconf

## <a name="self-hosted"></a><span class="mce-heading-3">Self-hosted Files</span>

<p class="mce-procedure">
  To load KRecord using self-hosted files
</p>

1.  Host the entire package on your own server (KRecord.swf, locale.xml, skin.swf).
2.  Use any standard embedding method to create the object on page (swfembed, swfobject, etc).

## <a name="Kaltura_uiconf"></a><span class="mce-heading-3">Kaltura Uiconf</span>

<p class="mce-procedure">
  <span>To load KRecord using Uiconf</span>
</p>

1.  Create a uiconf object in Kaltura of type KRECORD (7).
2.  Set the swfUrl to “/flash/krecord/<required version>/KRecord.swf”.
3.  Use any standard embedding method to create the object on page using the following url:

<p style="padding-left: 30px;">
  “http://www.kaltura.com/krecord/ui_conf_id/<created uiconf id>/”
</p>

Using the uiconf method allows for easier update of versions, support and other maintenance issues.

<h1 class="mce-heading-2">
  Initialization - Existing flashvars
</h1>

KRecord is initialized using flashvars. Flashvars are case-insensitive.

<p class="mce-heading-4">
  <strong>Required Flashvars:</strong>
</p>

*   pid – partner id
*   ks – Kaltura session key. Entry creator and owner are taken from KS.

<p class="mce-heading-4">
  <strong>Optional Flashvars:</strong>
</p>

*   debugMode, traces debug messages. Default: false, if any value given set to true.
*   host, services host. default: www.kaltura.com. No “http”!
*   rtmpHost, media server. default: "rtmp://www.kaltura.com"
*   httpProtocol, http protocol used for API calls. If not specified, the same protocol that was used to load KRecord.swf is used. values of format "https" (no slashes)

*   themeURL, default: locale.xml
*   localeURL, default: skin.swf

*   detectionDelay, delay before initial camera test (allowing hardware to activate), the delay after a failed test is double. default: 0
*   timePerMic, number of miliseconds to wait while looking for mic activity before moving to the next microphone, default: 20000.

See the detailed description of the following flashvars under[ JS functions section > setQuality()][4].

 [4]: #setQuality

*   [quality:int][5],
*   [bw:int][6],
*   [width:int][7],
*   [height:int][8],
*   [fps:Number][9],
*   [gop:int=25][10],
*   [bufferTime:Number=70][11]

 [5]: #quality:int
 [6]: #parambw
 [7]: #paramw
 [8]: #paramh
 [9]: #paramfps:
 [10]: #paramgop
 [11]: #bufferTime

*   isH264, encode video in h264 codec. default: false, if ("1" || "true") set to true
*   h264profile, profile to use (values enumerated in http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/3/flash/media/H264Profile.html)
*   h264level, level to use (values enumerated in http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/3/flash/media/H264Level.html)

*   showUI, shows KRecord UI. If false, a chromeless recorder is shown (can be controlled using JS). default: "false"
*   showErrorMessage, default: false, if ("true" || "1") set to true,
*   autoPreview, default: "1"/ "true". any other value will set to false.
*   showPreviewTimer, default: false, if ("true" || "1") set to true
*   removePlayer, hides the UI controls of the preview player. default: false, if ("1" || "true") set to true
*   limitRecord, automatically stop recording after limitRecord seconds. default: no limit (0), value given in seconds
*   fmsApp, name of the application on the media server. Default: "oflaDemo"
*   messagex, x position of messages. Default: 0.
*   messagey, y position of messages Default: 0.

*   entryName, name of the created entry. Default: recorded\_entry\_pid\_<partner\_id><random number>
*   entryTags, tags for the created entry
*   entryDescription, description of the created entry
*   creditsscreenname, for anonymous user applications - the screen name of the user that contributed the entry (KalturaMediaEntry.creditUserName)
*   creditssiteurl, for anonymous user applications - the website url of the user that contributed the entry (KalturaMediaEntry.creditUrl).
*   categories, comma separated string of categories full names. **DO NOT use if entitlements are enabled for the account!**
*   admintags, admin tags for the created entry (KalturaBaseEntry.adminTags).
*   licensetype, the content license type to use, values enumerated in KalturaLicenseType (this is arbitrary to be set by the partner).
*   groupid, used to group multiple entries in a group (KalturaBaseEntry.groupId).
*   partnerdata, specific data for partners to store (KalturaBaseEntry.partnerData).
*   conversionQuality, conversion profile to be used with entry. if null, partner default profile is used

*   delegate, JS object that is used to delegate methods, this object should have methods corresponding to the KRecord "events".

*   disableglobalclick, default: false, if ("1" || "true") set to true, and then **you will not be able to start recording** via flash UI!

**Deprecated / Unused Flashvars**

The following flashvars are no longer supported, do not use them.

*   subpid
*   uid
*   kshowid
*   credit

<h1 class="mce-heading-3">
  Notifications Mechanism – KRecord Events
</h1>

KRecord notifies its hosting page about certain events. KRecord has 2 notification mechanisms; you can use whichever is more suitable for you.

**On-page Delegator:** Define an object named “delegator” on the page. This object should declare all relevant event handlers (methods). KRecord automatically looks for an object with this name on the page, and tries to invoke its methods.

**Delegate object:** Create a custom JS object with relevant event handlers (methods) and pass it in the “delegate” flashvar. KRecord will try to trigger methods on this object. When you are working on a large-scale project, this method will allow you to keep your code in order.

<pre class="brush: jscript;fontsize: 100; first-line: 1; ">var myDelegate = {

      function swfReady() {

            console.log("KRecord ready for interaction");

      }
       
      function previewEnd() {

            console.log("preview of recorded content is complete");

      }

      ...

}</pre>

Then, in KRecord flashvars:

...&host=www.kaltura.com&pid=*<partner_id>***&delegate=myDelegate**&…

If you don’t define a delegate object, KRecord tries to invoke the methods directly on the window object, so another (slightly less-ordered) option is to define “event handlers“ directly on the page where the swf is embedded.

<p class="mce-note-graphic">
  KRecord tries triggering both delegation methods for any event. Assuming you will only implement one of them, you might see errors saying something is not defined. If you have this event covered by the method you implemented, you shouldn’t worry.
</p>

<h1 class="mce-heading-3">
  Existing events
</h1>

KRecord triggers the following “events”:

*   swfReady – triggered when ExternalInterface callbacks are registered.

<p class="mce-sub-heading">
  Device Detection Events
</p>

*   detectedMicrophone – an active microphone was found.
*   errorMicrophone – no active microphone was found.
*   detectedCamera – an active camera was found.
*   errorCamera - no active camera was found.
*   cameraDenied – there are active cameras installed, but access to them was not granted.
*   microphoneDenied – user selected to deny access to microphone&camera (in settings popup).
*   microphoneAllowed - user selected to allow access to microphone&camera (in settings popup).
*   noCamerasFound – no active cameras were found.
*   workingMicFound – an active microphone was found.
*   noMicsFound – no active microphones detected.
*   micDenied – legacy call, use “microphoneDenied”.
*   micAllowed – legacy call, use “microphoneAllowed”.
*   deviceDetected – triggered when both an active microphone and an active camera are found.

<p class="mce-sub-heading">
  Save Events
</p>

*   beforeAddEntry – triggered when KRecord is about to save a new entry
*   addEntryFailed – triggered when the API call made to add an entry failed. The additional argument describes the error as received from the server: {errorCode, errorMsg}
*   addEntryComplete – triggered when a new entry was created with the recorded video. The additional argument is the entry object.

<p class="mce-sub-heading">
  Connection Events
</p>

*   netconnectionConnectFailed – connection to media server failed
*   netconnectionConnectInvalidapp – connection to media server failed
*   netconnectionConnectClosed – connection to media server failed
*   netconnectionConnectRejected – connection to media server failed
*   connected – connection to media server established successfully
*   connecting – trying to access media server
*   connectingFinish – stopped trying to access media server (either success or failure)

<p class="mce-sub-heading">
  Other Events:
</p>

*   streamIdChange – ID of recorded stream has changed
*   updateRecordedTime – total time of recorded stream has changed
*   flushComplete – record buffer is flushed
*   recordStart – recording started
*   recordComplete – recording ended
*   previewStarted – preview started
*   previewEnd – preview ended
*   previewStopped – preview stopped (click on stop button or JS call)
*   previewPaused – preview paused (click on pause button or JS call)
*   previewResumed - preview resumed (click on pause button or JS call)
*   autoStopRecord – recording reached time limit and stopped

# <a name="JS_functions"></a><span class="mce-heading-3">JS Functions</span>

KRecord’s main functions can be triggered via JS. This allows you, for example, to hide the built-in UI and supply alternative buttons for recording/previewing content.

The following functions exist:

*   <a name="setQuality"></a>setQuality (quality:int, bw:int, w:int, h:int, fps:Number, gop:int, bufferTime:Number) - Sets camera recording quality. This function is triggered internally when KRecord starts, using values taken from flashvars, or the default values.

<p style="padding-left: 60px;">
  <a name="quality:int"></a>@param quality: An integer that specifies the required level of picture quality, as determined by the amount of compression being applied to each video frame. Acceptable values range from 1 (lowest quality, maximum compression) to 100 (highest quality, no compression). To specify that picture quality can vary as needed to avoid exceeding bandwidth, pass 0 for quality.
</p>

<p style="padding-left: 60px;">
  <a name="parambw"></a>@param bw: Specifies the maximum amount of bandwidth that the current outgoing video feed can use, in bytes per second. To specify that Flash Player video can use as much bandwidth as needed to maintain the value of quality, pass 0 for bandwidth.
</p>

<p style="padding-left: 60px;">
  <a name="paramw"></a>@param w: the width of the frame.
</p>

<p style="padding-left: 60px;">
  <a name="paramh"></a>@param h: the height of the frame.
</p>

<p style="padding-left: 60px;">
  @<a name="paramfps:"></a>param fps: frame per second to use.
</p>

<p style="padding-left: 60px;">
  @<a name="paramgop"></a>param gop: Specifies which video frames are transmitted in full (called keyframes) instead of being interpolated by the video compression algorithm. default value: 25
</p>

<p style="padding-left: 60px;">
  @<a name="bufferTime"></a>bufferTime: bufferTime specifies how long the outgoing buffer can grow before the application starts dropping frames. On a high-speed connection, buffer time is not a concern; data is sent almost as quickly as the application can buffer it. On a slow connection, however, there can be a significant difference between how fast the application buffers the data and how fast it is sent to the client. default value: 70.
</p>

*   startRecording()
*   stopRecording()
*   previewRecording()
*   stopPreviewRecording()
*   pausePreview()
*   resumePreview()
*   addEntry(entry\_name, entry\_tags, entry\_description, credits\_screen\_name, credits\_site\_url, categories, admin\_tags, license\_type, credit, group\_id, partner_data, conversionQuality) - Add the last recording as a new Kaltura entry in the Kaltura Network. This is the function that is triggered when user clicks “save”, with values taken from flashvars.

<p style="padding-left: 60px;">
  @param entry_name: name for the new entry.
</p>

<p style="padding-left: 60px;">
  @param entry_tags: tags for the new entry.
</p>

<p style="padding-left: 60px;">
  @param entry_description: description of the new entry.
</p>

<p style="padding-left: 60px;">
  @param credits_screen_name: for anonymous user applications - the screen name of the user that contributed the entry.
</p>

<p style="padding-left: 60px;">
  @param credits_site_url: for anonymous user applications - the website url of the user that contributed the entry.
</p>

<p style="padding-left: 60px;">
  @param categories: comma separated string of categories full names. <strong>DO NOT use if entitlements are enabled for the account!</strong>
</p>

<p style="padding-left: 60px;">
  @param admin_tags: admin tags for the new entry.
</p>

<p style="padding-left: 60px;">
  @param license_type: the content license type to use.
</p>

<p style="padding-left: 60px;">
  @param credit: unused value. Legacy.
</p>

<p style="padding-left: 60px;">
  @param group_id: used to group multiple entries
</p>

<p style="padding-left: 60px;">
  @param partner_data: specific data for partners to store.
</p>

<p style="padding-left: 60px;">
  @param conversionQuality: conversion profile to be used with entry. if null, partner default profile is used.
</p>

*   getRecordedTime() - Returns duration of the recording in milliseconds.
*   getMicrophones() - Returns the list of installed microphones.
*   getMicrophoneActivityLevel() - Returns the amount of sound the active microphone is detecting. Values range from 0 (no sound is detected) to 100 (very loud sound is detected)
*   getMicrophoneGain() - Returns the amount by which the microphone boosts the signal.
*   setMicrophoneGain(value:Number) - Sets the amount by which the microphone boosts the signal. Valid values are 0 to 100.
*   getCameras() - Returns the list of available cameras.
*   setActiveCamera(cameraName) - Set the specific camera device to use.
*   setActiveMicrophone(microphoneName) - Set the specific microphone device to use.
*   getMostRecentEntryId() - Returns the id of the last entry created.