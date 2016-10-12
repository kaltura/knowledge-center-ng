---
layout: page
title: "What Are The Differences Between Flavors Set V1 and Flavors Set V2"
date: 2013-03-13 19:41:45
---

In the Falcon version, Kaltura introduced a new transcoding flavors (entry transcoding renditions) set dubbed V2. This FAQ describes the differences between the first version and the new version introduced in Falcon (dubbed V2).

<p class="mce-heading-2">
  Comparison of the flavors sets
</p>

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="471">
        <strong>Flavors Set V2 (Introduced in Falcon)</strong>
      </td>
      
      <td valign="top" width="448">
        <strong>Flavors Set V1 (Pre-Falcon)</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="471">
        Main codec utilized: <a href="http://en.wikipedia.org/wiki/H.264/MPEG-4_AVC" target="_blank">H.264</a>
      </td>
      
      <td style="text-align: left;" valign="top" width="448">
        <div>
          Main codec utilized: <a href="http://en.wikipedia.org/wiki/VP6" target="_blank">VP6</a>
        </div>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="471">
        <div>
          Consolidated single flavors set that is optimized for both desktop and mobile.
        </div>
        
        <div>
          V2 is a set of 6 flavors that is used for Web (Progressive Download, HDS and RTMP) and mobile (Progressive Download and HLS).
        </div>
      </td>
      
      <td style="text-align: left;" valign="top" width="448">
        <div>
          Two seperate sets: desktop and mobile specific flavors.
        </div>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="471">
        <div>
          Optimized ffmpeg settings
        </div>
      </td>
      
      <td style="text-align: left;" valign="top" width="448">
        <div>
          -
        </div>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="471">
        <div>
          Inclusion of the WEBM flavor
        </div>
      </td>
      
      <td style="text-align: left;" valign="top" width="448">
        <div>
          -
        </div>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="471">
        <div>
          Removal of the 'Edit' flavor (As part of the move to deprecate the Flash based editors)
        </div>
      </td>
      
      <td style="text-align: left;" valign="top" width="448">
        <div>
          Redundent 'Edit' flavor (A low-res densed key-frame flavor for Flash app editing)
        </div>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="471">
        <div>
          The default playback mode is HDS (Requires server/CDN support on self hosted editions)
        </div>
      </td>
      
      <td style="text-align: left;" valign="top" width="448">
        <div>
          The default playback mode was Progressive Download
        </div>
      </td>
    </tr>
  </tbody>
</table>

 

<p class="mce-heading-2">
  V1 to V2 constraints and complications
</p>

<p class="mce-sub-heading">
  V1 and V2 assets are not compliant.
</p>

As flavors define the playback sets (assets that will be used by the media player during playback), accounts should not include assets from both V1 and V2 sets.   
Having assets from both sets available per entry -

*   May cause faulty adaptive bitrate playback behaviors.
*   Does not comply with the Akamai requirements and may cause incosistent adaptive playback behaviours.
*   Does not comply with the Apple requirements and will render such entries to be incompatible with the AppStore.

Therefore, the following guidelines should be applied when considering an upgrade:

*   Publishers should have either V1 or V2 sets configured in their account (Admin Console > Configure Action > check either "V1 flavor set" or "V2 flavor set"), **but never both together**.
*   Video Entries should never contain assets from both sets. An existing entry (with V1 set) might be transcoded to V2 assets after the switch to V2, therefor:
*   A switch to V2 should be followed by:
*   Disable of the V1 set.
*   Re-convertion of all the account entries to a V2 set
*   Publishers should understand and approve the consequences of the switch from V1 to V2 as it may affect entries availability during transcoding.