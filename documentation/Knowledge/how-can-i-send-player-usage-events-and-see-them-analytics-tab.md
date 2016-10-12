---
layout: page
title: "How can I send player usage events and see them on the Analytics tab"
date: 2012-01-12 15:55:06
---

<p class="mce-heading-1 mce-heading-2">
  Sending Events from a Player to Kaltura Analytics
</p>

You can send events from a player to Kaltura Analytics by passing a URL to **stats.kaltura.com** using the GET method with the following parameters.

<p class="mce-heading-2 mce-heading-3">
  Mandatory Parameters
</p>

*   uiConfID = "event:uiconfId"; numeric must
*   PartnerID = "event:partnerId"
*   entryID = "event:entryId"
*   sessionID = "event:sessionId"; unique generated id
*   duration = "event:duration" - entry duration
*   queryStringReferrer = "event:referrer" - embedded url
*   eventTimestamp = "event:eventTimestamp"

<p class="mce-heading-2 mce-heading-3">
  Event Types
</p>

The following is a list of all event types you can send to the Kaltura Analytics server, arranged by "event\_type\_id" and "event\_type\_name".

<table border="0">
  <tbody>
    <tr>
      <td>
        event_type_id
      </td>
      
      <td>
        event_type_name
      </td>
    </tr>
    
    <tr>
      <td>
        1
      </td>
      
      <td>
        <span>Widget Loaded</span>
      </td>
    </tr>
    
    <tr>
      <td>
        2
      </td>
      
      <td>
        <span>Media Loaded (view)</span>
      </td>
    </tr>
    
    <tr>
      <td>
        3
      </td>
      
      <td>
        <span>Play</span>
      </td>
    </tr>
    
    <tr>
      <td>
        4
      </td>
      
      <td>
        <span>Play reached 25%</span>
      </td>
    </tr>
    
    <tr>
      <td>
        5
      </td>
      
      <td>
        <span>Play reached 50%</span>
      </td>
    </tr>
    
    <tr>
      <td>
        6
      </td>
      
      <td>
        <span>Play reached 75%</span>
      </td>
    </tr>
    
    <tr>
      <td>
        7
      </td>
      
      <td>
        <span>Play reached 100%</span>
      </td>
    </tr>
    
    <tr>
      <td>
        8
      </td>
      
      <td>
        <span>Open Edit</span>
      </td>
    </tr>
    
    <tr>
      <td>
        9
      </td>
      
      <td>
        <span>Open Viral</span>
      </td>
    </tr>
    
    <tr>
      <td>
        10
      </td>
      
      <td>
        <span>Open Download</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        11
      </td>
      
      <td>
        <span>Open Report</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        12
      </td>
      
      <td>
        <span>Buffer Start</span>
      </td>
    </tr>
    
    <tr>
      <td>
        13
      </td>
      
      <td>
        <span>Buffer End</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        14
      </td>
      
      <td>
        <span>Open Full Screen</span>
      </td>
    </tr>
    
    <tr>
      <td>
        15
      </td>
      
      <td>
        <span>Close Full Screen</span>
      </td>
    </tr>
    
    <tr>
      <td>
        16
      </td>
      
      <td>
        <span>Replay</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        17
      </td>
      
      <td>
        <span>Seek</span><span> </span><span> </span><span> </span> 
      </td>
    </tr>
    
    <tr>
      <td>
        18
      </td>
      
      <td>
        <span>Open Upload</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        19
      </td>
      
      <td>
        <span>Save & Publish</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        20
      </td>
      
      <td>
        <span>Close Edtior</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        21
      </td>
      
      <td>
        <span>Pre Bumper Played</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        22
      </td>
      
      <td>
        <span>Post Bumper Played</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        23
      </td>
      
      <td>
        <span>Bumper Clicked</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        24
      </td>
      
      <td>
        <span>Preroll Started</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        25
      </td>
      
      <td>
        <span>Midroll Started</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        26
      </td>
      
      <td>
        <span>Postroll Started</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        27
      </td>
      
      <td>
        <span>Overlay Started</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        28
      </td>
      
      <td>
        <span>Preroll Clicked</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        29
      </td>
      
      <td>
        <span>Midroll Clicked</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        30
      </td>
      
      <td>
        <span>Postroll Clicked</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        31
      </td>
      
      <td>
        <span>Overlay Clicked</span> 
      </td>
    </tr>
    
    <tr>
      <td>
        32
      </td>
      
      <td>
        <span>Preroll 25</span>
      </td>
    </tr>
    
    <tr>
      <td>
        33
      </td>
      
      <td>
        <span>Preroll 50</span>
      </td>
    </tr>
    
    <tr>
      <td>
        34
      </td>
      
      <td>
        <span>Preroll 75</span>
      </td>
    </tr>
    
    <tr>
      <td>
        35
      </td>
      
      <td>
        <span>Midroll 25</span>
      </td>
    </tr>
    
    <tr>
      <td>
        36
      </td>
      
      <td>
        <span>Midroll 50</span>
      </td>
    </tr>
    
    <tr>
      <td>
        37
      </td>
      
      <td>
        <span>Midroll 75</span>
      </td>
    </tr>
    
    <tr>
      <td>
        38
      </td>
      
      <td>
        <span>Postroll 25</span>
      </td>
    </tr>
    
    <tr>
      <td>
        39
      </td>
      
      <td>
        <span>Postroll 50</span>
      </td>
    </tr>
    
    <tr>
      <td>
        40
      </td>
      
      <td>
        <p>
          Postroll 75
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2 mce-heading-3">
  Optional/Unknown:
</p>

*   uid = "event:userId"
*   clientVersion = "event:clientVer"; client version
*   widgetID = "event:widgetId";
*   uv = "event:uniqueViewer";
*   currentPoint = "event:currentPoint";
*   processDuration = "event:processDuration"
*   controlID = "event:controlId"
*   seekStringIndcator = "event:seek" 1 - true, 0 - false
*   newPoint = "event:newPoint"

<p class="mce-note-graphic">
  Every key in must start with "event:" as the prefix, for example: event:partnerId=100.
</p>

<p class="mce-heading-3">
  <span class="mce-heading-2 mce-heading-3">Example URL:</span>
</p>

[http://stats.kaltura.com//api_v3/index.php?service=stats&action=collect&event%3AsessionId=BE9F3DA9%2D4CAD%2D09AA%2D69B2%2DD9627E509311&event%3AeventType=3&event%3AisFirstInSession=false&event%3ApartnerId=524241&event%3AentryId=1%5Ftly1gkdh&ignoreNull=1&event%3Areferrer=http%253A%2F%2Fwww%2Ekaltura%2Ecom%2Fdev%2F&event%3Aseek=false&event%3Aduration=75&event%3AuiconfId=48503&event%3AcurrentPoint=0&event%3AeventTimestamp=1317907399783&event%3AobjectType=KalturaStatsEvent&clientTag=kdp%3Av3%2E5%2E21%2Ccache%5Fst%3A20000000&event%3AclientVer=3%2E0%3Av3%2E5%2E21&ks=MjhmMDQ1OWZjODE3YWZlZGFjMTU4ODE1MjJhNTFmMjdjNTU2ZTFiMXw1MjQyNDE7NTI0MjQxOzEzMTc5OTMyODg7MDsxMzE3OTA2ODg4LjY1NDE7MDt2aWV3Oio7Ow%3D%3][1][D][1]

 [1]: http://www.kaltura.com/api_v3/index.php?service=stats&action=collect&event%3AsessionId=BE9F3DA9%2D4CAD%2D09AA%2D69B2%2DD9627E509311&event%3AeventType=3&event%3AisFirstInSession=false&event%3ApartnerId=524241&event%3AentryId=1%5Ftly1gkdh&ignoreNull=1&event%3Areferrer=http%253A%2F%2Fwww%2Ekaltura%2Ecom%2Fdev%2F&event%3Aseek=false&event%3Aduration=75&event%3AuiconfId=48503&event%3AcurrentPoint=0&event%3AeventTimestamp=1317907399783&event%3AobjectType=KalturaStatsEvent&clientTag=kdp%3Av3%2E5%2E21%2Ccache%5Fst%3A20000000&event%3AclientVer=3%2E0%3Av3%2E5%2E21&ks=MjhmMDQ1OWZjODE3YWZlZGFjMTU4ODE1MjJhNTFmMjdjNTU2ZTFiMXw1MjQyNDE7NTI0MjQxOzEzMTc5OTMyODg7MDsxMzE3OTA2ODg4LjY1NDE7MDt2aWV3Oio7Ow%3D%3D

*'%3' represents ':'*