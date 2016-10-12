---
layout: page
title: "Kaltura Facebook Distribution Connector 1.0 Release Notes"
date: 2016-01-28 18:39:51
---

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
      <tr>
        <td valign="bottom">
          <p style="text-align: left;">
            In this document you will find the release notes pertaining to the <strong>Kaltura Facebook Distribution Connector</strong>.
          </p>
          
          <p style="text-align: left;">
            If you are unable to find the information that you are looking for here, please use the search bar above to search for the information you seek, or report a missing information: "<a href="http://knowledge.kaltura.com/node/86">Couldn't find what you were looking for</a>?” form.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
     
  </p>
  
  <p>
    [collapsed title="Menu to navigate by release dates and version numbers"] <a name="top" style="background-color: #ffffff;"></a>
  </p>
  
  <table border="0">
    <thead>
      <tr>
        <td style="border: 1px solid #000000; border-image: none; text-align: left;">
          <strong>Version</strong>
        </td>
        
        <td style="border: 1px solid #000000; border-image: none; text-align: left;">
          <strong>Date Released</strong>
        </td>
        
        <td style="border: 1px solid #000000; border-image: none; text-align: left;">
          <strong>Details</strong>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="border: 1px solid #000000; border-image: none; text-align: left;">
          1.00.06
        </td>
        
        <td style="border: 1px solid #000000; border-image: none; text-align: left;">
          January 31, 2016
        </td>
        
        <td style="border: 1px solid #000000; border-image: none; text-align: left;">
          <a href="#version1_0">Details</a><a href="#v5_33_03"></a>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
     
  </p>
  
  <p class="mce-heading-2">
    <a name="version1_0"></a>Version 1.0
  </p>
  
  <p>
    These release notes pertain to Kaltura Facebook Distribution Connector 1.0, released January 31, 2016. 
  </p>
  
  <p class="mce-heading-3">
    <span style="color: #828a8c; font-size: 14pt; font-weight: bold;">What's New in This Release</span>
  </p>
  
  <div>
    The <strong>Facebook Distribution Connector</strong> enables publishers to distribute video from Kaltura to Facebook in an automated, controlled manner, which allows publishers to enjoy the benefits of Facebook’s promotion of Native Video (in-feed Mobile playback, auto-play, Call to Action buttons, wider distribution in Facebook, targeting and advertising) while retaining the control of the distribution in Kaltura.
  </div>
  
  <p>
    The Kaltura Facebook Distribution Connector uses the Facebook Graph API (<span>which is the primary way for apps to read and write to the Facebook social graph)</span> to distribute Video, Thumbnails and Captions to the partner's Facebook Page. Content can contain metadata to further enrich the distributed content - including metadata to support calls to action, feed targeting, page tagging, and places.
  </p>
  
  <p>
    The Facebook Distribution Connector is an API-based connector that relies on the Facebook Video API for video upload and management.
  </p>
  
  <p class="mce-heading-3">
    Using the Facebook Distribution Connector
  </p>
  
  <p>
    Distribution to Facebook is managed using a single Kaltura-managed Facebook application. To distribute content to Facebook, the partner must provide specific permissions to the Kaltura Facebook application, including:
  </p>
  
  <ul>
    <li>
      manage_pages
    </li>
    <li>
      publish_actions
    </li>
  </ul>
  
  <p class="mce-heading-3">
    Facebook Authentication
  </p>
  
  <p>
    Authentifcation with Facebook is done via the standard Facebook oAuth athentication using the permissions listed above.
  </p>
  
  <p>
    The Facebook token used is a long lived access token.
  </p>
  
  <p class="mce-heading-3">
    Video Distribution
  </p>
  
  <p>
    Video distribution is performed through the <a href="https://developers.facebook.com/docs/graph-api/video-uploads" target="_blank">resumable</a> upload functionality available from Graph API v2.3 .
  </p>
  
  <p class="mce-heading-3">
    Video Upload
  </p>
  
  <ul>
    <li>
      The current video upload limitations are:
    </li>
    <ul>
      <li>
        1.75GB
      </li>
      <li>
        45 min
      </li>
    </ul>
    
    <li>
      The supported file formats include: 3g2, 3gp, 3gpp, asf, avi, dat, divx, dv, f4v, flv, m2ts, m4v, mkv, mod, mov, mp4, mpe, mpeg, mpeg4, mpg, mts, nsv, ogm, ogv, qt, tod, ts, vob, wmv.
    </li>
    <li>
      Video ratio must be between 9x16 to 16x9.
    </li>
  </ul>
  
  <p class="mce-heading-3">
    Thumbnails
  </p>
  
  <p>
    Thumbnails can be uploaded as part of the video creation API but not updated.
  </p>
  
  <p class="mce-heading-3">
    Supported Fields
  </p>
  
  <table style="width: 638px;" border="0" cellspacing="0" cellpadding="0" align="left">
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="168">
          <p style="text-align: center;" align="center">
            <strong>Facebook field name</strong>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="89">
          <p align="center">
            <strong>Kaltura element</strong>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="217">
          <p align="center">
            <strong>Description</strong>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="78">
          <p align="center">
            <strong>Updatable</strong>
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="168">
          Name
        </td>
        
        <td valign="top" width="89">
          Title
        </td>
        
        <td valign="top" width="217">
          Title of video
        </td>
        
        <td valign="top" width="78">
          Y
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="168">
          Description
        </td>
        
        <td valign="top" width="89">
          Description
        </td>
        
        <td valign="top" width="217">
          Description of video
        </td>
        
        <td valign="top" width="78">
          Y
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="168">
          scheduled publishing time
        </td>
        
        <td valign="top" width="89">
          Sunrise
        </td>
        
        <td valign="top" width="217">
          Time when video should be published. UNIX timestamp between 10 minutes to 6 months.
        </td>
        
        <td valign="top" width="78">
          N
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="168">
          Call To Action type
        </td>
        
        <td valign="top" width="89">
          Custom Metadata
        </td>
        
        <td valign="top" width="217">
          Facebook supports the following call to action parameters:-          SHOP_NOW-          BOOK_TRAVEL-          LEARN_MORE-          SIGN_UP-          DOWNLOAD-          WATCH_MORE Specifying a call to action will add an action on the video to the Call To Action URL specified below.
        </td>
        
        <td valign="top" width="78">
          Y
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="168">
          Call To Action Value
        </td>
        
        <td valign="top" width="89">
          Custom metadata
        </td>
        
        <td valign="top" width="217">
          URL to call on call_to_action click.
        </td>
        
        <td valign="top" width="78">
          Y
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="168">
          Place
        </td>
        
        <td valign="top" width="89">
          Custom metadata
        </td>
        
        <td valign="top" width="217">
          ID of location to tag in video.
        </td>
        
        <td valign="top" width="78">
          Y
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="168">
          Tags
        </td>
        
        <td valign="top" width="89">
          Custom metadata
        </td>
        
        <td valign="top" width="217">
          IDs (comma separated) of persons to tag in video.
        </td>
        
        <td valign="top" width="78">
          Y
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="168">
          Targeting
        </td>
        
        <td valign="top" width="89">
          Custom metadata
        </td>
        
        <td valign="top" width="217">
          Key IDs for ad targeting objects used to limit the audience of the video. See all relevant fields <a href="https://developers.facebook.com/docs/graph-api/reference/video" target="_blank">here</a>.
        </td>
        
        <td valign="top" width="78">
          N
        </td>
      </tr>
      
      <tr>
        <td style="text-align: center;" valign="top" width="168">
          Feed Targeting
        </td>
        
        <td style="text-align: center;" valign="top" width="89">
          Custom metadata
        </td>
        
        <td style="text-align: center;" valign="top" width="217">
          Key IDs for ad targeting objects used to promote the video in specific audience feeds. See all relevant fields <a href="https://developers.facebook.com/docs/graph-api/reference/video" target="_blank">here</a>.
        </td>
        
        <td valign="top" width="78">
          N
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
    <span style="font-size: 14pt; color: #828a8c; font-weight: bold;"> </span>
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
    <span style="font-weight: bold;"></span><span class="mce-heading-3">Limitations & Known Issues</span>
  </p>
  
  <table border="0">
    <tbody>
      <tr>
        <td style="text-align: left;">
          Facebook Distribution Connector does not block you from using both video ratios (9x16 to 16x9) when uploading videos. In this case, Facebook determines the optimal video ratio
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          If you enter a name that is over the allowed number of characters according to Facebook, the video distribution will fail.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          Captions are not updatable due to Facebook limitations.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          When adding captions to a video, Facebook will only allow you to add one set of captions, and will save only the last version uploaded.
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
     
  </p>
  
  <p>
     
  </p>