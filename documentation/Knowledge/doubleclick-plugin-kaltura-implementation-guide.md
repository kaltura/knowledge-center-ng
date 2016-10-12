---
layout: page
title: "DoubleClick Plugin for Kaltura Implementation Guide"
date: 2013-06-27 00:25:02
---

Kaltura has partnered with Google and is a DoubleClick approved platform partner. Kaltura offers a rich IMA3 plugin conﬁguration for Flash and HTML5. This includes easy setting of on-page parameters and custom entry metadata for contextual ad delivery. When a Kaltura player is integrated with Google’s IMA3 SDK, publishers can take advantage of advanced features in the DoubleClick for Publishers (DFP) video module. We recommend that you use FireFox for this implementation, so that the browser properly renders the XML responses making them readable.

The following topics are described:

*   [Understanding Linear Ads, Non-Linear Ads, Companion Ads, and AdRules ][1]
*   [Adding the DoubleClick Plugin][2]
*   [Adding Cue Points][3]
*   [DoubleClick Plugin Properties][4]
*   [Accessing/Updating the Player’s Configuration Through the TestMe Console][5] <span style="text-decoration: underline;"></span>

 [1]: #UnderstandingLinear
 [2]: #Adding_the_Plugin
 [3]: file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#_Adding_Cuepoints
 [4]: file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#_DoubleClick_Plugin_Properties
 [5]: file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#_Accessing/Updating_the_Player’s_1

The DoubleClick Plugin can also be viewed and tested at:<a href="http://player.kaltura.com/docs/DoubleClick" target="_blank"> http://player.kaltura.com/docs/DoubleClick</a>.

<div class="WordSection1">
  <h2>
    <a name="UnderstandingLinear"></a>Understanding Linear Ads, Non-Linear Ads, Companion Ads and Adrules
  </h2>
  
  <p>
    The Google Interactive Media Ads (IMA) SDK enables publishers to display linear, non-linear, companion ads in interactive media content such as videos and games:
  </p>
  
  <ul>
    <li>
      <a href="#Linear_ads">Linear Ads</a><span style="text-decoration: underline;"></span>
    </li>
    <li>
      <a href="#Non-Linear_Ads">Non-linear Ads</a><span style="text-decoration: underline;"></span>
    </li>
    <li>
      <a href="file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#_Companion_Ads">Companion Ads</a><span style="text-decoration: underline;"></span>
    </li>
    <li>
      <a href="file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#_AdRules">AdRules</a>  <span style="text-decoration: underline;"></span>
    </li>
  </ul>
  
  <h3>
    <a name="Linear_ads"></a>Linear Ads<span style="text-decoration: underline;"></span>
  </h3>
  
  <p>
    Linear ads appear before, after, or during a break in the video content (otherwise known as pre-roll, post-roll or mid-roll).
  </p>
  
  <h4>
    <a name="Example:_Linear_adTagUrl"></a>Example: Linear adTagUrl:
  </h4>
  
  <pre class="Code">http://pubads.g.doubleclick.net/gampad/ads?sz=400x300&iu=%2F6062%2Fiab_vast_samples&ciu_szs=300x250%2C728x90&impl=s&gdfp_req=1&env=vp&output=xml_vast2&unviewed_position_start=1&url=[referrer_url]&correlator=[timestamp]&cust_params=iab_vast_samples%3Dlinear<span style="text-decoration: underline;"></span></pre>
  
  <h3>
    <a name="Non-Linear_Ads"></a>Non-Linear Ads
  </h3>
  
  <p>
    Non-linear ads appear along with the video content.  Overlays, a common non-linear ad format, cover part of the video as it plays.<span style="text-decoration: underline;"></span>
  </p>
  
  <h4>
    <a name="Example_Non-Linear_adTagUrl"></a>Example Non-Linear adTagUrl
  </h4>
  
  <pre class="Code">http://pubads.g.doubleclick.net/gampad/ads?sz=400x300&iu=%2F6062%2Fiab_vast_samples&ciu_szs=300x250%2C728x90&impl=s&gdfp_req=1&env=vp&output=xml_vast2&unviewed_position_start=1&url=[referrer_url]&correlator=[timestamp]&cust_params=iab_vast_samples%3Dimageoverlay<span style="text-decoration: underline;"></span></pre>
  
  <h3>
    Companion Ads
  </h3>
  
  <p>
    Companion ads are similar to non-linear ads as they are overlays and are displayed within an HTML environment, alongside other Flash content, or within a Flash website.<span style="text-decoration: underline;"></span>
  </p>
  
  <h3>
    AdRules
  </h3>
  
  <p>
    Linear, non-linear, AND companion ads may be configured through the Kaltura Management Console (KMC) and UiConf to play/display through cuepoints, pre-rolls, post-rolls. Using AdRules greatly simplifies the process by supporting ad-breaks without additional code. If you choose to use an AdRule, you should not use other types of ads.   
  </p>
  
  <p>
    Kaltura recommends that you apply an AdRule adTagUrl at the beginning of a cuepoint system or directly to the config as a presequence item.  Mixing other adTagUrls with an AdRule service is discouraged and may lead to unexpected behavior.  For example, we do not recommend that you use an AdRule along with a linear ad postroll and an overlay mid-roll.                                                                       
  </p>
  
  <h4>
    Example  AdRules adTagUrl: 
  </h4>
  
  <pre class="Code">http://pubads.g.doubleclick.net/gampad/ads?sz=640x480&iu=%2F3510761%2FadRulesSampleTags&ciu_szs=160x600%2C300x250%2C728x90&cust_params=adrule%3Dpremidpostpodandbumpers&impl=s&gdfp_req=1&env=vp&ad_rule=1&vid=41117659&cmsid=481&output=xml_vast2&unviewed_position_start=1&url=[referrer_url]&correlator=[timestamp]</pre>
</div>

## <a name="Adding_the_Plugin"></a>Adding the DoubleClick Plugin

You can add the DoubleClick Plugin through the:

*   [KMC][6]
*   [TestMe Console][7]

 [6]: #through_KMC
 [7]: #thru_TestMe

### <a name="through_KMC"></a>Adding the Plugin Through the Kaltura Management Console (KMC)

<p class="Procedure">
       <span class="mce-procedure">To configure the DoubleClick ad plug in</span>
</p>

1.  Go to your DoubleClick account; define ads, scheduling, targeting, etc. on the DoubleClick end.
2.  Go to<a href="%20http://kmc.kaltura.com/index.php/kmc#dashboard|" target="_blank"> http://kmc.kaltura.com/index.php/kmc#dashboard|</a> and logon.
3.  Go to the Studio tab and edit an existing player or create a new one.
4.  Select the Advertising tab.
5.  Enable ads for the selected player.
6.  Select DoubleClick as the Ad Source.  
    <img src="{{site.url}}/assets/1075">
7.  On the left pane, click **Features**.
8.  Click on **Additional parameters and plugins**.
9.  Add the AdTagUrl. See [Add the adTagUrl][8].
10. Under <a name="line_code"></a>**Paste your plug-in here: ** paste  any custom settings (<a href="http://player.kaltura.com/docs/DoubleClick" target="_blank"> listed in the Custommize tab</a> ) as key value pairs. For example you can enter the following line of code:  
    <pre class="CodeList">doubleClick.plugin=true&doubleClick.path=http://kgit.html5video.org/ps/pulls/18/ps/DoubleClick/resources/flash/doubleClickPlugin/bin-release/doubleClickPlugin.swf&doubleClick.width=100%&doubleClick.height=100%&doubleClick.includeInLayout=true&doubleClick.relativeTo=screensLayer&doubleClick.position=after&doubleClick.disableCompanionAds=false&doubleClick.postSequence=0&doubleClick.preSequence=1&doubleClick.trackCuePoints=false&doubleClick.debugMode=true&adsOnReplay=true&debugMode=true</pre>

11. Click **Go.**

 [8]: file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#adtagurl

The** adTagUrl** is not included in the sample line of code.The reason the **adTagUrl** was not added to the code is because ampersands are often included in the adTagUrl and this confuses the KMC.  Therefore, the **adTagUrl **must be added in separately.

The added fields with their values should display.  The first value should be **doubleClick.plugin **with a value of **true **followed by the rest of the properties specified in [step 10][9].  The properties and values can be entered in separately, however, the line of code provided here saves lots of time since multiple properties separated by an ‘&’ are entered at once.

 [9]: #line_code

<p class="Procedure mce-procedure">
       To add the adTagUrl
</p>

1.  Under Paste your plug-in here: type or paste doubleClick.adTagUrl
2.  Click Go.
3.  Right below, in the Key-value table, the first property should be the one just added (doubleClick.adTagUrl).
4.  In it’s value box, enter in your adTagUrl.  
    You can also use one of the samples provided in this document such as the sample linear adTagUrl.  
    <pre class="CodeList"><a href="http://pubads.g.doubleclick.net/gampad/ads?sz=400x300&iu=%2F6062%2Fiab_vast_samples&ciu_szs=300x250%2C728x90&impl=s&gdfp_req=1&env=vp&output=xml_vast2&unviewed_position_start=1&url=%5Breferrer_url%5D&correlator=%5Btimestamp%5D&cust_params=iab_vast_samples%3Dlinear">http://pubads.g.doubleclick.net/gampad/ads?sz=400x300&iu=%2F6062%2Fiab_vast_samples&ciu_szs=300x250%2C728x90&impl=s&gdfp_req=1&env=vp&output=xml_vast2&unviewed_position_start=1&url=[referrer_url]&correlator=[timestamp]&cust_params=iab_vast_samples%3Dlinear</a></pre>

5.  Click Save Changes.

The player should now be updated and can be viewed from the KMC by selecting the Content menu and then selecting the Entries tab and selecting an entry to Preview & embed.

### <a name="thru_TestMe"></a>Adding the Plugin Through the TestMe Console

This section assumes that the configuration code for the player to be modified has already been pasted onto a text document and is ready to be modified as described in [Accessing/Updating the Player’s Configuration Through the TestMe Console][10].

 [10]: file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#_Accessing/Updating_the_Player’s

<p class="Procedure">
     <span class="mce-procedure">  To add the plugin through the TestMe Console</span>
</p>

1.  In the configuration code, paste the following lines of code right before the   **<Screens ….> **node.  
    <pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;Plugin id="doubleClick" 
					path="http://kgit.html5video.org/ps/pulls/18/ps/DoubleClick/resources/flash/doubleClickPlugin/bin-release/doubleClickPlugin.swf" 
					width="100%" 
					height="100%" 
					includeInLayout="true" 
					relativeTo="screensLayer" 
					position="after" 
					adTagUrl=" http://pubads.g.doubleclick.net/gampad/ads?sz=400x300&iu=%2F6062%2Fiab_vast_samples&ciu_szs=300x250%2C728x90&impl=s&gdfp_req=1&env=vp&output=xml_vast2&unviewed_position_start=1&url=[referrer_url]&correlator=[timestamp]&cust_params=iab_vast_samples%3Dlinear" 
					disableCompanionAds="false" 
					postSequence="0" 
					preSequence="1" 
					trackCuePoints="false" 
					adsOnReplay=”true”
					debugMode="true" /&gt;
This code has the plugin setup to run the sample linear ad (provided in Example: Linear adTagUrl:) to run as a pre roll.  See DoubleClick Plugin Properties to modify the properties.</pre>

 

This code has the plugin setup to run the sample linear ad (provided in [Example: Linear adTagUrl:][11]) to run as a pre roll.  See [DoubleClick Plugin Properties][12] to modify the properties.

 [11]: #Example:_Linear_adTagUrl
 [12]: #properties

1.  After the code has been added and modified, see [Accessing/Updating the Player’s Configuration Through the TestMe Console][13] to update the UiConf.

 [13]: #accessing_updating

<div class="WordSection1">
  <h1>
    <a name="adding_cue"></a>Adding Cue Points
  </h1>
  
  <p>
    Kaltura allows publishers to set and manage cue points within each video and to define with great accuracy the exact timing of mid roll ads and overlays.  Cue points are managed through the KMC.
  </p>
  
  <h2>
    Configuring the Player Advertising Settings
  </h2>
  
  <p class="Procedure mce-procedure">
         To configure the player advertising settings
  </p>
  
  <ol>
    <li>
      Go to <a href="http://kmc.kaltura.com/index.php/kmc#dashboard|">http://kmc.kaltura.com/index.php/kmc#dashboard</a> and logon.
    </li>
    <li>
      Select the Studio tab and then select or create a player.
    </li>
    <li>
      Select the Advertisments tab.
    </li>
    <li>
      Toggle on Yes to Request ads for this player.
    </li>
    <li>
      Fill in the fields that define how the player handles advertisements, and click Save Changes.
    </li>
  </ol>
  
  <p class="Procedure">
       <span class="mce-procedure">  To manage cue points through the KMC</span>
  </p>
  
  <ol>
    <li>
      Select the <strong>Content </strong>tab and then select the media that you would like to add cue points to.
    </li>
    <li>
      Select the Advertisements tab.<br />On the bottom half of the window, the video clip’s timeline is displayed.
    </li>
    <li>
      Select the method to obtain the ad from the File Actions drop down menu.
    </li>
    <li>
      Choose the granularity level for the time-based display. The choices are:<br /><ul>
        <li>
          100%
        </li>
        <li>
          5 sec
        </li>
        <li>
          1 sec
        </li>
        <li>
          Frames.
        </li>
      </ul>
    </li>
    
    <li>
      Identify the exact scene or frame to display the advertisement and insert a cue point.  This can be done on the timeline:
    </li>
    <li>
      To edit a cue point, select whether the advertisement will be a video or an overlay.
    </li>
    <li>
      For a video - the entry will stop playing, the ad will play, and then the entry will resume.
    </li>
    <li>
      For an overlay - while the entry is playing, a banner will appear on the screen. The entry never stops playing.For both video and overlay, there are 2 options in the provider section:  VAST and OTHER. VAST allows a user to insert a VAST ad tag URL. OTHER is for customers who have created a custom plugin that allows for creating cue points Other, does NOT refer to existing ad plugins such as Tremor, Adap.tv, etc.
    </li>
    <li>
      If you select overlay, the display time will be indicated next to the Overlay option:  You can modify the amount of time you want the overlay to appear on the video using the up and down arrows.
    </li>
    <li>
      To apply the selected cue points to the player, create a new player or edit an existing one under the “Studio” tab. Within the advertisement portion of the player, make sure that the “Request Ads From Entry’s Cue points” is set to “Yes”.
    </li>
    <li>
      Click on the <strong>“+” icon</strong> to add a cue point. (The trash icon deletes the selected cue point.)
    </li>
    <li>
      Click and drag that cue point to the desired position on the timeline.
    </li>
    <li>
      If the cue point is not already selected, click on it to view that cue point’s settings.
    </li>
    <li>
      Next to <strong>Type, </strong>there is a drop down box with two options: <strong>Video </strong>and <strong>Overlay.  </strong>Select the appropriate option depending on the type of ad.  For this example we will be using the Sample Linear adTagUrl and select the option Video:
    </li>
  </ol>
  
  <p class="CodeList">
    <a href="http://pubads.g.doubleclick.net/gampad/ads?sz=400x300&iu=%2F6062%2Fiab_vast_samples&ciu_szs=300x250%2C728x90&impl=s&gdfp_req=1&env=vp&output=xml_vast2&unviewed_position_start=1&url=%5Breferrer_url%5D&correlator=%5Btimestamp%5D&cust_params=iab_vast_samples%3Dlinear">http://pubads.g.doubleclick.net/gampad/ads?sz=400x300&iu=%2F6062%2Fiab_vast_samples&ciu_szs=300x250%2C728x90&impl=s&gdfp_req=1&env=vp&output=xml_vast2&unviewed_position_start=1&url=[referrer_url]&correlator=[timestamp]&cust_params=iab_vast_samples%3Dlinear</a>
  </p>
  
  <ol>
    <li>
      <strong>13.  </strong>Under <strong>Provider, </strong>there are two options, <strong>VAST </strong>and <strong>Other.  </strong>For our example we will select Other.
    </li>
    <li>
      <strong>14.  </strong>In the box underneath the Provider drop down box, where it says <strong>Enter ad provider, </strong>enter <strong>doubleclick</strong>
    </li>
    <li>
      <strong>15.  </strong>In the box labelled <strong>URL, </strong>paste in the adTagUrl of the ad you want to add to this cue point.  For our example we will add in the <a href="file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#_Example:_Linear_adTagUrl:">Sample Linear adTagUrl.</a>
    </li>
    <li>
      <strong>16.  </strong>In the box labelled <strong>Name, </strong>enter <strong>doubleclick </strong>
    </li>
    <li>
      <strong>17.  </strong>Click <strong>Save</strong>.
    </li>
    <li>
      <strong>18.  </strong>The DoubleClick Plugin Property <strong>trackCuePoints</strong> must be set to <strong>true.   </strong>Edit this property through the <strong>TestMe Console </strong>or the <strong>KMC </strong>as explained in <a href="file:///C:/Users/Debbie/Documents/Doubleclick/DoubleClick%20Plugin%20Documentation.doc#_Adding_the_DoubleClick">Adding the DoubleClick Plugin.</a>
    </li>
  </ol>
</div>

<div class="WordSection2">
  <h1>
    <a name="properties"></a>DoubleClick Plugin Properties
  </h1>
  
  <p>
    The DoubleClick Plugin Properties and values are described in the Customize tab in the <a href="http://player.kaltura.com/modules/DoubleClick/tests/DoubleClickManagedPlayerAdApi.qunit.html#tab-edit-videoTarget_doc">DoubleClick Managed Player site</a>.
  </p>
</div>

# <a name="accessing_updating"></a>Accessing/Updating the Player’s Configuration Through the TestMe Console

<p class="Procedure">
       <span class="mce-procedure">To access the player’s configuration through the TestMe console</span>
</p>

1.  Log on to the KMC.  
    Note the **UI Conf ID** of the player that needs to be modified.

2.  Bring up the Account Information necessary for the TestMe Console.
<ol style="list-style-type: lower-alpha;">
  <li>
    Select Settings then select Integration Settings.
  </li>
  <li>
    <a name="step2b"></a>Leave this window open so that the information is readily available.
  </li>
</ol>

3.  Open another browser window and go to <a href="http://www.kaltura.com/api_v3/testme/" target="_blank">http://www.kaltura.com/api_v3/testme/</a>
4.  Under the drop down box Select service, select session.
5.  Another drop down box should appear called Select action.  Select start.  Below, some other entry boxes should appear.
6.  Under secret (string), cut and paste the Administrator Secret found in the KMC window that was left open in [step 2b][14].
7.  Under type(KalturaSessionType):, select ADMIN from the drop down box.
8.  Under partnerId(int):, cut and paste the Partner ID, from the KMC window.
9.  Click Send.
10. Under the drop down box Select service, select uiConf.
11. Under the drop down box Select action, select get.   
    If all of the information was entered correctly, the KS(string) field (2<sup>nd</sup> field from the top) should now be populated with a series of characters.  This is the session string and the player configuration can now be accessed.
12. Under id (int):, enter the UI Conf ID of the player that needs to be modified.
13. Click Send. <a name="step13"></a>The player’s configuration appears on the right.  
    Leave this window open.  It will save you the time of opening up another session when you are ready to paste in the new modified configuration.
14. Select all the contents of the player’s configuration and copy/paste into a text editor such as Notepad(PC) or TextWrangler(Mac).
15. Save the file as config.xml, or any name with .xml extension, so that the editor will indent the code properly for better readability.  
    The configuration (config.xml) can now be modified through the text editor. Refer to  [Accessing/Updating the Player’s Configuration Through the TestMe Console][5] to update the configuration code with the closed caption code.
<ol style="list-style-type: lower-alpha;">
  <li>
    The actual configuration code (<a name="confFile_string"></a>confFile(string)) begins with  <layout…>  and ends with </layout>
  </li>
  <li>
    The <a name="confFileFeatures"></a>confFileFeatures(string), found after </layout>, begins with <snapshot> and ends with </snapshot>  **sometimes with custom player.  This (confFileFeatures) may not exist and that is fine.
  </li>
</ol>

 [14]: #step2b

After you have changed the player’s configuration in the text editor, the updated configuration can be uploaded to the KMC via the Test Me Console.

<p class="Procedure">
      <span class="mce-procedure"> To update the player’s configuration  to the KMC</span>
</p>

1.  Assuming that the window from [step #13][15] is still open, under the drop down box **Select action, **select **update**
2.  Under **id (int):**, enter the **UI Conf ID **of the player that needs to be modified.
3.  Make sure the checkbox to the right of the drop down box with **KalturaUiConf **is checked; otherwise a MISSING\_MANDATORY\_PARAMETER will pop up.
4.  Click **Send** and the player’s (unmodified) configuration will appear on right just as it did in [step #13][15].
5.  Click the **Edit **button which is above the Sendbutton.  Another pane of entry boxes is displayed.
6.  In the entry box labelled **confFile(string):**, copy and paste the new updated configuration code from your text editor as specified in [step #15a.][16]
7.  In the entry box labelled **confFileFeatures(string):**, copy and paste the confFileFeatures as specified in [step #15b][17].
8.  Click **Send.**

 [15]: #step13
 [16]: #confFile_string
 [17]: #confFileFeatures

The player should now be updated and can be viewed from the KMC by selecting the Content menu and then selecting the Entries tab and selecting an entry to Preview & embed.

After all the updates have been made, you must end your session.

<p class="Procedure mce-procedure">
       To end the session
</p>

1.  In the drop down box labelled **Select service**, select **session.**
2.  In the drop down box labelled **Select actions**, select **end.**
3.  Click **Send.**