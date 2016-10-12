---
layout: page
title: "Example Encoder Setup using Adobe FMLE to Set Up the Live Video Stream"
date: 2015-11-01 15:35:40
---

<p style="padding-left: 30px;">
    This article walks through the process of setting up a live stream for a webcast event using Adobe FMLE. Verify that you have the following Live Stream details from the Webcast Event page: 
  </p>
  
  <ul>
    <ul>
      <li>
        <strong>Primary URL - </strong><span>the system automatically generates this URL</span>
      </li>
      <li>
        <strong><strong>Backup URL - </strong></strong>the system automatically generates this URL
      </li>
      <li>
        <strong><strong><strong>Stream Name - </strong></strong></strong>the stream name is the stream ID and is generated automatically
      </li>
    </ul>
  </ul>
  
  <p style="padding-left: 30px;">
    You can use various live encoders. Kaltura Webcasting creates an XML file (FMLE format) to seamlessly export the live encoder information.
  </p>
  
  <p style="padding-left: 30px;">
    You can also export an XML file containing all of the Live Stream details that can later be imported to the encoder. If you're unsure about where to find the Live Stream details, review the article for <a href="http://knowledge.kaltura.com/editing-webcasting-event" target="_blank">Editing a Webcasting Event</a>.
  </p>
  
  <p class="Procedure mce-procedure">
    Setting up the hardware and software for Live Streaming
  </p>
  
  <ol>
    <li>
      Download the Flash Media Live Encoder (FMLE) from <a href="http://www.adobe.com/products/flashmediaserver/flashmediaencoder/" class="external-link" rel="nofollow">here</a>.
    </li>
    <li>
      Install the FMLE on your local machine.<br /><span class="mce-note-graphic">Verify that your system has the minimum requirements (see </span><a href="http://www.adobe.com/products/flashmediaserver/flashmediaencoder/systemreqs/" class="external-link mce-note-graphic" rel="nofollow">http://www.adobe.com/products/flashmediaserver/flashmediaencoder/systemreqs/</a><span class="mce-note-graphic"> for details).</span>
    </li>
    <li>
      Verify that your camera is shown in the preview screen.
    </li>
  </ol>
  
  <p class="mce-note-graphic">
    NOTE: You can use many types of live encoders with Kaltura Webcasting. See recommended encoders <a href="http://knowledge.kaltura.com/faq/what-encoders-can-i-use-kaltura-live-streaming" target="_blank">here</a>. 
  </p>
  
  <p>
    <span class="mce-procedure">Setting up the Live Stream</span>
  </p>
  
  <ol style="padding-left: 30px;">
    <li>
      Connect your camera /recording device to the broadcasting computer.
    </li>
    <li>
      Run the Adobe Flash Media Live Encoder (FMLE).
    </li>
    <li>
      To enter the live stream details you have two options: 
    </li>
    <ol style="list-style-type: lower-alpha;">
      <li>
        Select <strong>File  > Open Profile</strong>. Browse to the exported XML file and click <strong>OK</strong>.
      </li>
      <li>
        Enter the Live Stream details manually in the corresponding fields.
      </li>
    </ol>
  </ol>
  
  <p style="padding-left: 30px;">
    <img src="../../assets/2533">
  </p>
  
  <p style="padding-left: 30px;">
    4. Click <strong>Connect</strong> on the right hand side to verify that you're connected to the streaming server.
  </p>
  
  <p style="padding-left: 30px;">
    5. Click <strong>Start</strong> to begin broadcasting. When the event ends, click <strong>Stop</strong> to stop broadcasting. 
  </p>
  
  <p>
    <span class="mce-procedure" style="font-size: 1.17em;">To start the slide broadcast</span>
  </p>
  
  <ol>
    <li>
      Verify that you have created the Webcast event, set up the encoder and have your slides, presenters, moderators and attendees invited to begin broadcasting.
    </li>
    <li>
      Launch the Kaltura Webcasting application.<br />You will see an <strong>On-Air</strong> indication when there's a live broadcast and the first slide will be broadcast automatically. <br /><br /><img src="../../assets/3456">
    </li>
  </ol>
  
  <p style="padding-left: 30px;">
     
  </p>
  
  <p>
    To learn more about the types of encoders you can use, see <a href="http://knowledge.kaltura.com/node/1146" target="_blank">Which Encoders can I use with the Kaltura Live Streaming</a>?
  </p>