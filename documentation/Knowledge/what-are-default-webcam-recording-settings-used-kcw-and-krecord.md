---
layout: page
title: "What are the default webcam recording settings used in the KCW and KRecord?"
date: 2013-02-24 21:57:23
---

### For KCW

KCW parameters are controlled using uiconf.

For example, the Webcam recording in KMC uses the following default values when no data is received:

keyFrame interval - 5;

width - 336,

height - 252,

framerate - 25,

bandwidth - 0,

quality -  85

The values you use depend on your network, camera, and other related components.

**Important Note:**  Webcam recordings are expected to be low-quality and the widgets are designed for low-quality and short (minutes) recordings. The better quality you configure and the longer the recording is, the more likely it is that the end-result will have gaps. You can set the bufferTime to a long value to avoid this problem, however the resulting recording will be delayed and not ready as soon as the recording is over (which is what expected in many use-cases).

### For KRecord

The following describes the KRecord parameters:

  

<table style="width: 576px;" border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="115">
        <p>
          <strong>Parameter Name</strong>
        </p>
      </td>
      
      <td valign="top" width="369">
        <p>
          <strong>Explanation</strong>
        </p>
      </td>
      
      <td valign="top" width="91">
        <p>
          <strong>Value used in KRecord</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="115">
        <p style="text-align: left;">
          quality
        </p>
      </td>
      
      <td valign="top" width="369">
        <p style="text-align: left;">
          An integer that specifies the required level of picture quality, as determined by the amount of compression being applied to each video frame. Acceptable values range from 1 (lowest quality, maximum compression) to 100 (highest quality, no compression).
        </p>
      </td>
      
      <td valign="top" width="91">
        <p>
          85
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="115">
        <p style="text-align: left;">
          bw
        </p>
      </td>
      
      <td valign="top" width="369">
        <p style="text-align: left;">
          An integer that specifies the maximum amount of bandwidth that the current outgoing video feed can use, in bytes per second. Used to specify that Flash video can use as much bandwidth as needed to maintain the value of <em>frameQuality</em>, pass 0.
        </p>
      </td>
      
      <td valign="top" width="91">
        <p>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="115">
        <p style="text-align: left;">
          w
        </p>
      </td>
      
      <td valign="top" width="369">
        <p style="text-align: left;">
          Frame width
        </p>
      </td>
      
      <td valign="top" width="91">
        <p>
          336
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="115">
        <p style="text-align: left;">
          h
        </p>
      </td>
      
      <td valign="top" width="369">
        <p style="text-align: left;">
          Frame height
        </p>
      </td>
      
      <td valign="top" width="91">
        <p>
          252
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="115">
        <p style="text-align: left;">
          fps
        </p>
      </td>
      
      <td valign="top" width="369">
        <p style="text-align: left;">
          Frame Per Second
        </p>
      </td>
      
      <td valign="top" width="91">
        <p>
          25
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="115">
        <p style="text-align: left;">
          gop
        </p>
      </td>
      
      <td valign="top" width="369">
        <p style="text-align: left;">
          Group Of Pictures
        </p>
      </td>
      
      <td valign="top" width="91">
        <p>
          25
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="115">
        <p style="text-align: left;">
          bufferTime
        </p>
      </td>
      
      <td valign="top" width="369">
        <p style="text-align: left;">
          Used to compensate for bandwidth instability. When the bandwidth isn’t sufficient for the stream, the stream is stored in the buffer. The higher this parameter is, the more reliability there is that the stream will be passed without losing frames. On the other hand – the higher this parameter is, it may take longer until you are able to play the recording.
        </p>
      </td>
      
      <td valign="top" width="91">
        <p>
          70
        </p>
      </td>
    </tr>
  </tbody>
</table>

  