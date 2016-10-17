---
layout: page
title: "How to enforce delivery type for each player using UI Variables?"
date: 2015-10-18 20:55:00
---

<div class="columnLayout single" data-layout="single">
    <div class="cell normal" data-type="normal">
      <div class="innerCell">
        <div class="conf-macro output-block" data-hasbody="true" data-macro-name="div">
          <p>
            Kaltura supports many delivery types, such as Akamai HDS, HTTP Progressive and others.<br />In many cases you may want to enforce the use of a specific delivery method. This article describes how to enforce a specific delivery type using UI Variables in the KMC.
          </p>
        </div>
      </div>
    </div>
  </div>
  
  <div class="columnLayout single" data-layout="single">
    <div class="cell normal" data-type="normal">
      <div class="innerCell" style="padding-left: 30px;">
        <span class="mce-procedure">To enforce a specific delivery method using a v2 player</span><br /><br />**In case you are using the v1 player, skip to <a href="#v1">How to enforce delivery method in V1 player</a>? <ol>
          <li>
            Log in to your Kaltura Management Console (KMC), select the <strong>Studio</strong>, then <strong>Universal Studio.<br /><img src="../../assets/2487.img">
          </li>
          <li>
            Click on the player you would like to edit (be certain that the player is<a href="http://knowledge.kaltura.com/faq/universal-studio-faq"> v2 player</a>), then click the <strong>plugins</strong> icon(shaped like a plug).<br /><img src="../../assets/2488.img">
          </li>
          <li>
            Add the different Ui variables, depending on the delivery method you have chosen.<br /><strong>Kaltura Auto</strong><br />This is the default delivery method. There is no need to add Ui variables to enforce this method.<br /><br /><strong>HTTP Progressive Download</strong><br />Key: streamerType<br />Value:  http<strong><br /><br />HTTP Streaming(Akamai):<br /></strong>Key: loadingPolicy<br />Value:  preInitialize<br /><br />Key:  asyncInit<br />Value: true<br /><br />Key:  streamerType<br />Value: hdnetwork <br /><br /><span><strong>HTTP Streaming(HDS):</strong></span><br />Key: loadingPolicy<br />Value:  preInitialize<br /><br />Key:  asyncInit<br />Value: true<br /><br />Key:  streamerType<br />Value: hdnetworkmanifest<br /><br />Key:  twoPhaseManifest<br />Value: true <br /><br /><span><strong>RTMP Streaming:</strong></span><br />Key:  streamerType<br />Value: rtmp<br /><br />Key: mediaProtocol<br />Value: rtmp <br /><img src="../../assets/2489.img">
          </li>
          <li>
            Click the <strong>Save Player Settings</strong> button to apply the changes.<br /><img src="../../assets/2490.img">
          </li>
        </ol>
      </div>
      
      <div class="innerCell" style="padding-left: 30px;">
        <h3 id="HowtoenforcedeliverytypeforeachplayerusingUiVariables?-HowtoenforcedeliverymethodinV1player?">
          <a name="v1"></a>How to enforce delivery method in V1 player? 
        </h3>
        
        <p>
          This section describes how to enforce delivery method for V1 players,using the Flash Studio  in the KMC.
        </p>
        
        <ol>
          <li>
            Log in to your Kaltura Managment Console, choose <strong>Studio</strong> from top navigation bar, then select the <strong>Flash Studio</strong>.<br /><img src="../../assets/2491.img">
          </li>
          <li>
            Select the player you would like to edit, click <strong>Select Action</strong> and from the drop-down menu, select <strong>Edit</strong>.<br /><img src="../../assets/2493.img">
          </li>
          <li>
            In the Features page, Expand the<strong> Additional parameters and plugins</strong> section.<br /><img src="../../assets/2494.img">
          </li>
          <li>
            Add the different Ui variables, depending on the delivery method you chose.<br /><img src="../../assets/2495.img">
              <strong><span>HTTP Progressive Download:</span><br /></strong>This is the default delivery method, no need to add Ui variables to enforce this method.<strong><br /><br /><span>HTTP Streaming(Akamai):</span><br /></strong>loadingPolicy=preInitialize&asyncInit=true&streamerType=hdnetwork <br /><br /><span><strong>HTTP Streaming(HDS):</strong></span><br />loadingPolicy=preInitialize&asyncInit=true&streamerType=hdnetworkmanifest&twoPhaseManifest=true <br /><br /><span><strong>RTMP Streaming:</strong></span><br />streamerType=rtmp&mediaProtocol=rtmp 
            </p>
            
            <p>
              The Edit Player page should look like this:
            </p>
            
            <p>
              <img src="../../assets/2496.img">
            </p>
          </li>
          
          <li>
            Click the<strong> Save Changes</strong> button to apply the changes.<br /><img src="../../assets/2497.img">
          </li>
        </ol>
        
        <p>
          The player should now enforce the delivery method you have chosen.
        </p>
      </div>
    </div>
  </div>