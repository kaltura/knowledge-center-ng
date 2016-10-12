---
layout: page
title: "Integrating Kaltura with VAST adTag URL"
date: 2014-09-21 16:18:33
---

The Kaltura player has a flexible string substitution system for evaluating ad tag URLs prior to requesting the ads from the ad server. This enables ad requests to include content metadata for better ad targeting. Both the ad stitching and client side "VAST" plugin work and evaluate URLs in the same way. 

For example your VAST plugin config may look like the following: 

<pre class="brush: as3;fontsize: 100; first-line: 1; ">vast: {
    ...
    'prerollUrl' : 'http://adserver.com/videoId={mediaProxy.entry.id}&cache_break={utility.random}'
    ...
}</pre>

This configuration would then be evaluated substituting the entry.id with the current content unique identifier and utility.random with a random number when the ad request is made. 

Arbitrary player state properties can be used in evaluations. These are detailed in the [player api][1] page.  Not all evaluations are available  for server side ad stitching. The properties available are detailed as follows: 

 [1]: http://player.kaltura.com/docs/api#evaluate "player api"

<table border="0" cellspacing="0" cellpadding="0" align="left">
  <tbody>
    <tr>
      <td valign="bottom">
        <p>
          <strong>Property</strong>
        </p>
      </td>
      
      <td valign="bottom">
        <p>
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="bottom">
        <p>
          <strong>Supported in server side evaluations</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          configProxy
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The player configuration object. Allows access to all UI vars and plugin properties
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          duration
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Current video duration in seconds
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          isHTML5
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          A flag specifying if the current player is an HTML5 player (Universal player)
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          mediaProxy.entry
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Returns all entry properties for the currently active entry.
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          mediaProxy.entryCuePoints
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Array of cue points if defined for the current media
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          mediaProxy.entryMetadata
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Metadata object for the current entry
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          mediaProxy.isLive
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Returns true, if the current entries live broadcast is active.
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          mediaProxy.isOffline
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Returns true if the current entries live broadcast is offline.
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          mediaProxy.kalturaMediaFlavorArray
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          An array holding all available flavors for the current media
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          playerStatusProxy.kdpStatus
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The player status. Can be "empty" or "ready"
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          playerStatusProxy.loadTime
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The time it took to load the player on the page
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          playlistAPI.dataProvider
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The data provider of a play list holding all the entries for this list
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          sequenceProxy.activePluginMetadata
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Metadata object of the plugin currently playing the ads sequence
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          sequenceProxy.duration
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The total duration of the current ad set.
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          sequenceProxy.isInSequence
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          A flag specifying if the player is currently playing ads
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          sequenceProxy.skipOffsetRemaining
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          During ad playback, the time remaining until the Skip button appears
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          sequenceProxy.timeRemaining
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Time remaining until the end of the current ads sequence
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          utility.nativeAdId
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The native device identifier, <a href="https://developer.apple.com/library/ios/documentation/AdSupport/Reference/ASIdentifierManager_Ref/#//apple_ref/occ/instp/ASIdentifierManager/advertisingIdentifier" title="advertisingIdentifier">AdvertisingIdentifier</a> for Apple and <a href="http://developer.android.com/reference/com/google/android/gms/ads/identifier/AdvertisingIdClient.Info.html" title="AdvertisingIdClientInfo">AdvertisingIdClient</a> for Android
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Only supported in <a href="http://player.kaltura.com/modules/KalturaSupport/tests/nativeCallout.html">native player SDK</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          utility.random
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Utility for generating a random number
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          utility.referrer_host
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Retrieve the referrer host
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          utility.referrer_url
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Retrieve the referrer URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          utility.timestamp
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Utility for generating the current time stamp
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           yes
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          video.player.currentTime
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The current video time in seconds
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          video.volume
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The volume of the currently playing video (0-1)
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           no
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          mediaSession.userIPaddress
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          The client ip address originating the request
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Server only
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="bottom">
        <p>
          mediaSession.userAgent
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
           The client software originating the request
        </p>
      </td>
      
      <td style="text-align: left;" valign="bottom">
        <p>
          Server only
        </p>
      </td>
    </tr>
  </tbody>
</table>