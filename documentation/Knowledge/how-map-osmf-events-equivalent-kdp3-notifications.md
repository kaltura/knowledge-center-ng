---
layout: page
title: "How to Map OSMF Events to Equivalent KDP3 Notifications"
date: 2012-03-27 00:52:46
---

OSMP events may be mapped to notifications withing the KDP 3. Event names may change with new versions of the OSMF, however the names of the KDP notifications will remain the same. Check the [KDP documentation][1] for more information about notifications and their usage.

 [1]: http://www.kaltura.org/demos/kdp3/docs.html "KDP Documentation"

<table border="0" align="left">
  <tbody>
    <tr>
      <td style="text-align: left;">
        <strong>OSMP EVENT NAME</strong>
      </td>
      
      <td style="text-align: left;">
        <strong>NOTIFICATIONS WITHIN THE KDP3</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        <span>DisplayObjectEvent.DISPLAY_OBJECT_CHANGE</span>
      </td>
      
      <td style="text-align: left;">
        MEDIA_VIEWABLE_CHANGE ("mediaViewableChange")
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        <span>DisplayObjectEvent.MEDIA_SIZE_CHANGE </span>
      </td>
      
      <td style="text-align: left;">
        No notification fired
      </td>
    </tr>
    
    <tr>
      <td>
        MediaPlayerStateChangeEvent.MEDIA_PLAYER_STATE_CHANGE
      </td>
      
      <td style="text-align: left;">
        PLAYER_STATE_CHANGE ("playerStateChange"), body of the notification contains the state ("uninitialized", "loading", "ready", "playing", "paused", "stopped", "buffering")
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        TimeEvent.CURRENT_TIME_CHANGE
      </td>
      
      <td style="text-align: left;">
        PLAYER_UPDATE _PLAYHEAD ("playerUpdatePlayhead") body of the notification contains the current time of the player.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        AudioEvent.VOLUME_CHANGE 
      </td>
      
      <td style="text-align: left;">
        VOLUME_CHANGED ("volumeChanged"), body of the notification contains the new volume.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        BufferEvent.BUFFER_TIME_CHANGE 
      </td>
      
      <td style="text-align: left;">
        BUFFER_PROGRESS ("bufferProgress"), body of the notification contains the new buffered time
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        BufferEvent.BUFFERING_CHANGE
      </td>
      
      <td style="text-align: left;">
        BUFFER_CHANGE ("bufferChange"), body of the notification contains the buffering state (true/false)
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        MediaErrorEvent.MEDIA_ERROR
      </td>
      
      <td style="text-align: left;">
        MEDIA_ERROR ("mediaError")
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        LoadEvent.BYTES_TOTAL_CHANGE
      </td>
      
      <td style="text-align: left;">
        BYTES_TOTAL_CHANGE ("bytesTotalChange") , body of the notification contains the new total bytes value.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        LoadEvent.BYTES_LOADED_CHANGE
      </td>
      
      <td style="text-align: left;">
        BYTES_DOWNLOADED_CHANGE ("bytesDownloadedChange"), body of the notification contains the downloaded bytes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        TimeEvent.DURATION_CHANGE
      </td>
      
      <td style="text-align: left;">
        DURATION_CHANGE ("durationChange"), the body of the notification contains the new duration.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        DynamicStreamEvent.SWITCHING_CHANGE
      </td>
      
      <td style="text-align: left;">
        SWITCHING_CHANGE
      </td>
    </tr>
  </tbody>
</table>

 