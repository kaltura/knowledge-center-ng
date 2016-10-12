---
layout: page
title: "Kaltura Supported CDN (Content Delivery Networks) and Streaming Servers"
date: 2013-04-01 01:30:02
---

Various Content Delivery Networks and Streaming Servers are supported by Kaltura for delivery of media. This article provides a compatibility matrix of all CDNs and Streaming Servers and the specific delivery features supported for each.

Please note that while the information here outlines supported CDNs and Streaming Servers on all Kaltura editions, configuring the use of a specific CDN or Streaming Server may require customization and setup work.

<p class="mce-heading-2">
  Kaltura Supported CDNs for Origin Pull VOD
</p>

For video files that are stored in Kaltura, Kaltura supports HLS, HDS, Smooth and Dash practically on any CDN.  
Kaltura packages these protocols in our datacenters, and the CDN acts as a simple HTTP proxy.

<div dir="ltr">
  <table>
    <colgroup><col width="90"><col width="95"><col width="43"><col width="44"><col width="40"><col width="54"><col width="67"><col width="79"></colgroup><tbody>
      <tr>
        <td>
          <strong>CDN / Streaming Server</strong>
        </td>
        
        <td>
          <strong>Tokenization</strong>
        </td>
        
        <td>
          <a href="http://en.wikipedia.org/wiki/Progressive_download" target="_blank"><strong>Progressive Download</strong></a>
        </td>
        
        <td>
          <strong><a href="http://www.adobe.com/products/hds-dynamic-streaming.html" target="_blank">HDS</a></strong>
        </td>
        
        <td>
          <strong><a href="http://en.wikipedia.org/wiki/HTTP_Live_Streaming" target="_blank">HLS</a></strong>
        </td>
        
        <td>
          <strong><a href="http://www.adobe.com/devnet/rtmp.html" target="_blank">RTMP</a></strong>
        </td>
        
        <td>
          <strong><a href="http://en.wikipedia.org/wiki/Real_Time_Streaming_Protocol" target="_blank">RTSP</a></strong>
        </td>
        
        <td>
          <strong><a href="http://www.iis.net/downloads/microsoft/smooth-streaming" target="_blank">Smooth Streaming</a></strong>
        </td>
        
        <td>
          <p>
            <strong><a href="http://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP" target="_blank">DASH Streaming</a></strong>
          </p>
        </td>
        
        <td>
          <p>
            <strong>CDN Live Packaging</strong>
          </p>
        </td>
      </tr>
      
      <tr>
        <td>
          <strong><a href="http://www.akamai.com/" target="_blank">Akamai</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;"><span>x</span></span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;"><span>x</span></span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;"><span>x</span></span>
        </td>
      </tr>
      
      <tr>
        <td>
          <a href="http://aws.amazon.com/cloudfront/" target="_blank"><strong>Amazon CF</strong></a>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
        
        <td style="text-align: center;">
           
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
      </tr>
      
      <tr>
        <td>
          <a href="http://cdn.tatacommunications.com/" target="_blank"><strong>Tata CDN</strong></a>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-size: x-small;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
      
      <tr>
        <td>
          <strong><a href="http://www.limelight.com/" target="_blank">Limelight</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"><a href="http://en.wikipedia.org/wiki/Progressive_download" target="_blank">PD Only</a></span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
      
      <tr>
        <td>
          <strong><a href="http://www.level3.com/" target="_blank">Level3</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
      
      <tr>
        <td>
          <strong><a href="http://www.adobe.com/products/adobe-media-server-family.html" target="_blank">FMS 4.5</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
      
      <tr>
        <td>
          <strong><a href="http://www.red5.org/" target="_blank">Red5</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
      
      <tr>
        <td>
          <strong><a href="http://www.edgecast.com/" target="_blank">EdgeCast</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
      </tr>
      
      <tr>
        <td>
          <strong><a href="http://www.mirror-image.com/" target="_blank">MirrorImage</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="font-family: arial, helvetica, sans-serif;">x </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
    </tbody>
  </table>
</div>

<p class="mce-heading-2">
  Kaltura Supported CDNs for Remote Storage VOD
</p>

<div dir="ltr">
  <table>
    <colgroup><col width="90"><col width="95"><col width="43"><col width="44"><col width="40"><col width="54"><col width="67"><col width="79"></colgroup><tbody>
      <tr>
        <td style="text-align: center;">
          <strong>CDN / Streaming Server</strong>
        </td>
        
        <td style="text-align: center;">
          <strong>URL Tokenization</strong>
        </td>
        
        <td style="text-align: center;">
          <a href="http://en.wikipedia.org/wiki/Progressive_download" target="_blank"><strong>Progressive Download</strong></a>
        </td>
        
        <td style="text-align: center;">
          <strong><a href="http://www.adobe.com/products/hds-dynamic-streaming.html" target="_blank">HDS</a></strong>
        </td>
        
        <td style="text-align: center;">
          <strong><a href="http://en.wikipedia.org/wiki/HTTP_Live_Streaming" target="_blank">HLS</a></strong>
        </td>
        
        <td style="text-align: center;">
          <strong><a href="http://www.adobe.com/devnet/rtmp.html" target="_blank">RTMP</a></strong>
        </td>
        
        <td style="text-align: center;">
          <strong><a href="http://en.wikipedia.org/wiki/Real_Time_Streaming_Protocol" target="_blank">RTSP</a></strong>
        </td>
        
        <td style="text-align: center;">
          <strong><a href="http://www.iis.net/downloads/microsoft/smooth-streaming" target="_blank">Smooth Streaming</a></strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <strong><a href="http://www.akamai.com/" target="_blank">Akamai</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;">x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <strong><a href="http://aws.amazon.com/cloudfront/" target="_blank"><strong>Amazon CF</strong></a></strong>
        </td>
        
        <td style="text-align: center;">
          x
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <a href="http://cdn.tatacommunications.com/" target="_blank"><strong>Tata CDN</strong></a>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <strong><a href="http://www.limelight.com/" target="_blank">Limelight</a></strong>
        </td>
        
        <td style="text-align: center;">
          <a href="http://en.wikipedia.org/wiki/Progressive_download" target="_blank"><span style="color: #800000;">PD Only</span></a>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
        
        <td style="text-align: center;">
           
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <strong><a href="http://www.level3.com/" target="_blank">Level3</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
        
        <td style="text-align: center;">
           
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <strong><a href="http://www.adobe.com/products/adobe-media-server-family.html" target="_blank">FMS 4.5</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
        
        <td style="text-align: center;">
           
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <strong><a href="http://www.red5.org/" target="_blank">Red5</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
        
        <td style="text-align: center;">
           
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <strong><a href="http://www.edgecast.com/" target="_blank">EdgeCast</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
        
        <td style="text-align: center;">
           
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;">
          <strong><a href="http://www.mirror-image.com/" target="_blank">MirrorImage</a></strong>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span style="color: #000000;"> </span>
        </td>
        
        <td style="text-align: center;">
          <span>x</span>
        </td>
        
        <td style="text-align: center;">
           
        </td>
        
        <td style="text-align: center;">
           
        </td>
      </tr>
    </tbody>
  </table>
</div>

<p class="mce-heading-2">
  Kaltura Supported CDNs for Live Streaming (Web Broadcast) 
</p>

Kaltura Live provides automatic provisioning of Live Streaming via CDNs and Streaming Servers. Kaltura's datacenters have internal servers that package the content and allow you to configure any CDN to pull the live streaming HTTP segments from our datacenter and serve them to your end users. Supported delivery protocols for live are: HLS, HDS and MPEG-DASH.