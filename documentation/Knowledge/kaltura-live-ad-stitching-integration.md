---
layout: page
title: "Kaltura Live Ad Stitching Integration"
date: 2014-11-30 11:12:00
---

<div id="main-header">
  <div id="title-heading">
    <div id="main-header">
      <div id="title-heading">
        <h1 id="title-text">
          Architecture
        </h1>
      </div>
    </div>
  </div>
</div>

<div id="content" class="page view">
  <div id="main-content" class="wiki-content">
    <p>
      When Kaltura ad stitching is enabled, the Kaltura 'play-server' cloud manages all client HLS manifest and segment requests. This enables the swapping of individual segments with respective alternate pieces of content. Ads are configured against the Kaltura Ad cuepoint API, or represented directly on the ingest stream. Ad events include a VAST ad tag URL. After the play server reaches a time that includes an ad, a VAST request is made on the server to retrieve ads for each client that is consuming the stream. Ad tags should be configured with respective substitutionsas described in the <a href="{{site.url}}/documentation/Knowledge/integrating-kaltura-vast-adtag-url.html" target="_blank" class="external-link" rel="nofollow">Integrating Kaltura with VAST adTag URL</a> article.
    </p>
    
    <p>
      <span style="color: #ff0000;"><br /><img src="../../assets/2427.img">
    </p>
    
    <p class="mce-heading-2">
      Configuration
    </p>
    
    <p class="mce-heading-4 mce-heading-3">
      Configuring Ad Stitching Ads via the API  
    </p>
    
    <p>
      To allow Kaltura to push ads, the stream must go through Kaltura. Kaltura requires a valid Live stream entry to monitor when the ads should be stitched.
    </p>
    
    <p>
      Monitoring the ads' timing is done by watching for any new cuePoints that are being associated with the live stream entry in Kaltura. The cuePoint holds within in, all the information that Kaltura requires to stitch the ad.
    </p>
    
    <p>
      To add new cue point's to Kaltura, you should execute a cuePoint->add a call where the type of the cuePoint being added is "KalturaAdCuePoint".
    </p>
    
    <p>
      Mandatory parameters for this call are: 
    </p>
    
    <ul>
      <li>
        <span>entryID - The entry ID associated with the live stream.</span>
      </li>
      <li>
        <span>triggeredAt/<span>startTime - <span>Only one of these fields is required. triggeredAt indicates the absolute time when the ad should be stitched and where, as the startTime is an offset from the beginning of the stream.</span><br /></span></span>
      </li>
      <li>
        <span>sourceUrl - Indicates the ad provider URL.</span>
      </li>
      <li>
        <span>duration - The duration of the ad. <span> (milliseconds).</span></span>
      </li>
      <li>
        <span>adType - Should be set to 'VIDEO'.</span>
      </li>
    </ul>
    
    <p>
      Optional parameters:
    </p>
    
    <ul>
      <li>
        Title - Textual identifier of the cue point inserted.
      </li>
    </ul>
    
    <h3 id="KalturaLiveAdStitchingIntegrationDoc-ConfiguringAdStitching–in-streamadevents" class="mce-heading-4 mce-heading-3">
      <strong>Sample php Integration Code</strong>
    </h3>
    
    <pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;?php
    //Require Mandatory Classes
    error_reporting ( E_ALL );
    echo "pre-require..." . PHP_EOL;
    require_once (dirname ( __FILE__ ) . '/php5/KalturaClient.php');
     
    //Validate Input Count
    if (count($argv) &lt; 6)
    {
        die ("Usage: [Partner_ID] [KS] [Entry_id] [Ad_Triggered_At] [Ad_Source_Url] [Cue_Point_Title] [Ad_Duration]\n");
    }
     
    //Get Input Params From User
    $partnerId = $argv[1];
    $ks = $argv[2];
    $entryId = $argv[3];
    $adTriggeredAt = $argv[4];
    $adSourceUrl = $argv[5];
    $cuePointTitle = $argv[6];
    $adDuration = $argv[7];
     
    //Create new config & client
    $config = new KalturaConfiguration($partnerId);
    $config-&gt;serviceUrl = 'http://www.kaltura.com/';
    $client = new KalturaClient($config);
    $client-&gt;setKs($ks);
     
    //Add The New Ad Cue Point
    echo "Adding Ad Cue Point Using The Following Input:\n EntryID = [$entryId]\n Triggered At = [$adStartTime]\n Ad Source Url = [$adSourceUrl]\n ad Duration = [$adDuration] \n";
    $cuePoint = new KalturaAdCuePoint();
    $cuePoint-&gt;entryId = $entryId;
    $cuePoint-&gt;triggeredAt = $adTriggeredAt;
    $cuePoint-&gt;sourceUrl = $adSourceUrl;
    $cuePoint-&gt;adType = 1; //VIDEO
    $cuePoint-&gt;title = $cuePointTitle;
    $cuePoint-&gt;duration = $adDuration;
    $cuepointPlugin = KalturaCuepointClientPlugin::get($client);
    $result = $cuepointPlugin-&gt;cuePoint-&gt;add($cuePoint);
    echo "Cue Point Created With ID [{$result-&gt;id}]\n";
     
    echo "Done! :) \n"
?&gt;</pre>
    
    <h3 id="KalturaLiveAdStitchingIntegrationDoc-ConfiguringAdStitching–in-streamadevents" class="mce-heading-4 mce-heading-3">
      <span style="font-size: 12pt;">Configuring Ad Stitching Ads via in-stream Ad Events</span>
    </h3>
    
    <p>
      <span>Stream ad events require custom configuration.</span>
    </p>
    
    <h3 id="KalturaLiveAdStitchingIntegrationDoc-ConfiguringUiConfPlayer" class="mce-heading-4 mce-heading-3">
      Configuring UiConf Player
    </h3>
    
    <p>
      Kaltura ad stitching works against the same UiConf player identifiers as the Kaltura Universal Studio players. This enables consolidating ad stitching logic against the same player JSON that drives more feature rich player embeds. The player "VAST" configuration can be configured in the Kaltura Universal studio. You can use different players for web embeds than those used for ad stitching, but note they are managed in the same way with the <a href="{{site.url}}/documentation/Knowledge/universal-studio-information-guide.html">Universal Studio Player.</a>  
    </p>
    
    <p>
      To enable ad tracking by the player and the ad stitching server, you should set trackCuePoints to true in the player JSON configuration. You can do this in one of the following ways:
    </p>
    
    <ul>
      <li>
        Via the KMC:
      </li>
    </ul>
    
    <ol>
      <ol>
        <li>
          Go to the Studio tab.
        </li>
        <li>
          Edit the player you want to track Kaltura stitched ads.
        </li>
        <li>
          Select the Monetization tab and open the VAST configuration.
        </li>
        <li>
          Turn on the "Track cue points" flag.
        </li>
      </ol>
    </ol>
    
    <ul>
      <li>
        Via the API:
      </li>
      <ul>
        <li>
          In the player config, add the the following line ' "trackCuePoints": true '. This should be added under plugins–>vast section.<br />Additionally you must enable the "playServerUrls" plugin. <br />To do so:
        </li>
        <li>
          Go to the Ui vars custom plugins section add "<strong>playServerUrls.plugin</strong>" : <strong>true</strong> and "<strong>playServerUrls.enabledOn</strong>" :  "<strong>all</strong>" uiVars 
        </li>
      </ul>
    </ul>
    
    <h2 id="KalturaLiveAdStitchingIntegrationDoc-ConsumingtheAdStitchingURLS" class="mce-heading-2">
      Consuming the Ad Stitching URLS 
    </h2>
    
    <h3 id="KalturaLiveAdStitchingIntegrationDoc-ViaplayManifestURLs" class="mce-heading-3">
      Via playManifest URLs
    </h3>
    
    <p>
      Play-server URLs work against the standard Kaltura playMainfest URLs with the addition of a UiConf-id for player configuration. Here is an example URL with identification of standard identifiers: 
    </p>
    
    <div id="main-content" class="wiki-content">
      <p>
        <a href="http://dev-hudson9.dev.kaltura.com/p/102/playManifest/format/applehttp/entryId/0_wwsxfta8/uiConfId/11601194/usePlayServer/1/a/playlist.m3u8" target="_blank" class="external-link" rel="nofollow">http://<serviceHost>/p/<partnerIdValue>/playManifest/format/applehttp/entryId/<entryIdValue>/uiConfId/<uiConfIdValue>/usePlayServer/1/a/playlist.m3u8</a>
      </p>
      
      <p class="mce-heading-4">
        Parameters:
      </p>
      
      <p>
        entryId - Entry Id to play
      </p>
      
      <p>
        uiConfId - UI Conf id, if you want to use an Ad stitching server you should turn on the vast.trackCuePoints feature in your UI Conf.
      </p>
      
      <p>
        usePlayServer - Set to 1 if the Ad stitching server should be used.
      </p>
      
      <p class="mce-heading-4">
        <strong>Additional Parameters that can be Passed on Flashvars</strong>:
      </p>
      
      <p>
        sessionId- Optional, identifies the unique session id for the specific user. If the sessionId is not passed it is generated by the play server, see 'SessionId concept and Generation' for more details.
      </p>
      
      <h3 id="KalturaLiveAdStitchingIntegrationDoc-ViadirectplayserverURLs(forRoku)" class="mce-heading-3">
        Via direct play server URLs (for Roku)
      </h3>
      
      <p>
        Play-server URLs can be accessed directly as in the following example:
      </p>
      
      <p>
        <a href="http://dev-hudson9.dev.kaltura.com/p/102/playManifest/format/applehttp/entryId/0_wwsxfta8/uiConfId/11601194/usePlayServer/1/a/playlist.m3u8" class="external-link" rel="nofollow">http://<playServerHost>/p/<partnerIdValue>/master/manifest/entryId/<entryIdValue>/uiConfId/<uiConfIdValue>/sessionId/<sessionIdValue>/?url=<originalLiveStreamUrl>/playlist.m3u8</a>
      </p>
      
      <p class="mce-heading-4">
        <strong>Parameters:</strong>
      </p>
      
      <p>
        entryId - Entry Id to play
      </p>
      
      <p>
        uiConfId - UI Conf id, if you want to use an Ad stitching server you should turn on the vast.trackCuePoints feature in your UI Conf.
      </p>
      
      <p>
        sessionId- Optional, identifies the unique sessionId for the specific user. If the sessionId is not passed, it will be generated by the play server. See  <a href="#concept">Session Id Concept and Ceneration</a> for more details.
      </p>
      
      <p>
        url - Original live stream maseter URL.
      </p>
      
      <h3 id="KalturaLiveAdStitchingIntegrationDoc-SessionIdconceptandgeneration">
        <a name="concept"></a>SessionId Concept and Generation
      </h3>
      
      <p>
        The SessionId identifies the unique user session against the play server and allows the play server to manage ads and beacons per user. It is initialized in the master/manifest request passed to the play server. The sessionId can be either passed as a parameter or generated by the play server.
      </p>
      
      <p>
        If the sessionId is not passed as a parameter the play server will generate a new sessionId every time the new call is performed for the master/manifest request. This is usually done when the player is refreshed. 
      </p>
      
      <p>
        Generation: You will need to generate a random number/string
      </p>
      
      <p>
        Nodejs example: use Math.random()
      </p>
      
      <p>
        PHP example: use <span class="refname">uniqid()</span>
      </p>
      
      <p>
         
      </p>
    </div>
  </div>
</div>