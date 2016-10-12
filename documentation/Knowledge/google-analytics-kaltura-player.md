---
layout: page
title: "Google Analytics for the Kaltura Player"
date: 2012-09-10 15:59:08
---

[Jump to Implementation][1].

 [1]: #implementation

# Overview

 

Google Analytics (GA) is a web analytics service that uses a combination of cookies and APIs to enter events into a tracking site. Kaltura player includes a plugin to easily translate player events into GA beacons. The collection of beacons can then provide an analysis of player actions. 

To use this plugin, you must first have a Google analytics account (<a href="http://www.google.com/analytics/" target="_blank">http://www.google.com/analytics/</a>)

After signing up, you'll receive an urchin ID, appearing similar to UA-XXXXXXXXX-1.  This ID is the link between your player and the GA servers. 

After you install configure Google Analytics in the player, events may be reported to your Google Analytics account and will be collected under the Content->Events page.

To drill down into events: Go to Content->Events->Pages.

Under each page, the Kaltura Events category is displayed with the relevant events.  Under each event, the label is in the form:

<span style="color: #0000ff;">Clip title | entry Id | widget Id </span>

where each line shows the number of times the event was received, with the exception of progress events (xx\_pct\_watched).

See [Implementation][1]. The following is a screen capture of the Google Analytics Events Page.

<img src="../../assets/680">

## Demo Page

A player with the Google Analytics plugin installed is showcased on the following page: <a href="http://player.kaltura.com/docs/GoogleAnalytics" target="_blank">http://player.kaltura.com/docs/GoogleAnalytics</a>

You can use Fiddler or the onPage tracking tool, to track the events sent to Google.

<img src="../../assets/681">

Contents are broken up as:

<span style="color: #0000ff;">([“Kaltura Video Events”][type of event][“Clip title | entry Id | widget Id”])([value])</span>

## <a name="technical-details"></a>Technical Details

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="642">
        <p>
          Compiled against: KDP 3.5.43
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="642">
        <p>
          Release file size(s): 49kb
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="642">
        <p>
          UIConf path: <a href="http://www.kaltura.com/content/uiconf/google_analytics/kdp3.5.43/plugins/googleAnalyticsPlugin2.swf" target="_blank">/content/uiconf/google_analytics/kdp3.5.43/plugins/googleAnalyticsPlugin2.swf</a>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="642">
        <p>
          Code paths: <a href="https://github.com/kaltura/kdp/tree/master/plugins/googleAnalyticsPlugin" target="_blank">kdp/trunk/plugins/googleAnalyticsPlugin</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

## Google Analytics Infomation

Google documentation can be found at: [http:/code.google.com/apis/analytics/docs/tracking/eventTrackerGuide.html#Anatomy][2]

 [2]: http://code.google.com/apis/analytics/docs/tracking/eventTrackerGuide.html#Anatomy

A Google Analytics event has the following specifications:

*   Category – in our case – “Kaltura Video Events”  (hard coded)
*   Action – the event name
*   Label (optional) – dimension for the action
*   Value (optional) – numerical data

## Event Details

Data is recorded as listed:

*   Label – is always the title of the video, coupled with the entry ID and player ID:   
    video title | entryID | widgetId ( also known as the partner id )  
    The use of the vertical separator “|” is for easy readability.
*   Category – is always “Kaltura Events”
*   Action – the event type (as in the player event name)
*   Value – usually 1, for events where it makes sense to count the aggregate amount of times the event was triggered. 

## Add Google Analytics with the KMC

You can add Goodle Analytics using the FlashStudio as well as the Universal Studio.

<p class="mce-heading-4">
  Flash Studio
</p>

The Google Analytics plugin can be selected from the player studio within the KMC. Select the Sudio tab and then slect the Flash Studio menu.  
  
<img src="../../assets/1028">

The checkbox for google analytics should be set. Then in options the <span style="color: #0000ff;">urchinCode</span> property is required.

 <img src="../../assets/1029">

## Universal Studio

The Google Analytics plugin can be selected from the player studio within the KMC.

1.  Select the Studio tab and then select the Universal Studio menu.
2.  Select the Monitization icon and then Select Goole Analytics. For more information see the <a href="http://knowledge.kaltura.com/universal-studio-information-guide#google" target="_blank">Universal Studio Information Guide</a>.

 

## Plugin Definition 

The following is a sample plugin configuration that can be copied to your player's uiConf.  Change the <span style="color: #0000ff;">blue</span> values to accommodate the events to your own setup.

<Plugin id="googleAnalytics" visualDebug="false” width="0%" height="0%" loadingPolicy="wait" urchinCode="<span style="color: #0000ff;">UA-XXXXXXX-1</span>"/>

This configuration beams the following events: 

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          <strong>Action</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          <strong>Value (integer)</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          <strong>Comments</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          Play
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          Actually viewing the file
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          OpenedFullScreen
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          Indicates more interest
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          CloseFullScreen
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          kdpReady
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          playerEmpty
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          For cases like MediaSpace where the media is loaded after the player by external javascript
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          mediaReady
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          Google time stamp will allow detecting problems (slow load)
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          changeMedia
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          Track “related” and similar video changes.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          doDownload
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          doGigya
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          1
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

 

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          25_pct_watched
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          (current clip time)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          Dispatch after the player reaches the 25% mark of the clip.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          50_pct_watched
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          (current clip time)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          Dispatch after the player reaches the 50% mark of the clip.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          75_pct_watched
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          (current clip time)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          Dispatch after the player reaches the 75% mark of the clip.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          100_pct_watched
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
          (current clip time)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
          Dispatch after the player reaches the 100% mark of the clip.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="162">
        <p>
          doPause
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="155">
        <p>
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="321">
        <p>
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

## Advanced Implementation – Custom Events

<h4 class="Subheading">
  Example 1
</h4>

You can add the ability to listen for additional events that are not listed in the table. You can also specify your own values in the beacon string:

(\[“Kaltura Video Events”\]\[type of event\][“Clip title | entry Id | widget Id”])([value])

where:

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="205">
        <p>
          <span style="color: #0000ff;">[“Kaltura Video Events”]  </span>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p>
          <span style="color: #0000ff;"><strong>Category</strong></span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="205">
        <p>
          <span style="color: #0000ff;">[type of event]</span>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p>
          <span style="color: #0000ff;"><strong>Action</strong></span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="205">
        <p>
          <span style="color: #0000ff;">[“Clip title | entry Id | widget Id”]</span>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p>
          <span style="color: #0000ff;"><strong>Label</strong></span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="205">
        <p>
          <span style="color: #0000ff;">[value]    </span>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="90">
        <p>
          <span style="color: #0000ff;"><strong>Value</strong></span>
        </p>
      </td>
    </tr>
  </tbody>
</table>

To add additional events you will need to identify the event and set each definition. Omitting any of the definitions will result in the plugin's default settings. You can use this capability to listen for events triggered by other plugins, and beam those events to Google Analytics.

<h4 class="Subheading">
  Example 2
</h4>

The following is a configuration example that listens for additional events such as “doPlay”.

<span style="color: #0000ff;"><Plugin id="googleAnalytics" visualDebug="false” path="googleAnalyticsPlugin.swf"</span>

<span style="color: #0000ff;">customEvent=”<strong>doPlay</strong>”</span>

<span style="color: #0000ff;"><strong>doPlayCategory</strong>=”My Custom event”</span>

<span style="color: #0000ff;"><strong>doPlayAction</strong>=”player is playing”</span>

<span style="color: #0000ff;"><strong>doPlayValue</strong>=”1”</span>

<span style="color: #0000ff;">width="0%" height="0%" loadingPolicy="wait" urchinCode="UA-XXXXXXX-1"/></span>

The configuration above sends doPlay events each time a play event occurs. A play event happens after each click of the Play button. Notice the doPlayLabel parameter was left out. Leaving the doPlayLabel parameter out will default to the plugin's own settings and change the other parameters. The following is what each sent beacon will look like after each play event.

<span style="color: #0000ff;">(“My Custom event” “player is playing” [“Clip title | entry Id | widget Id”])(“1”)</span>

<span style="color: #0000ff;">[“Clip title | entry Id | widget Id”]</span> will display the Clip's title, entry Id, and widget Id in the above beacon.

<h4 class="Subheading">
  Example 3
</h4>

Users can omit a Category, Action, Value, and Label and only declare the event in “customEvents” as in the following example.

<span style="color: #0000ff;"><Plugin id="googleAnalytics" visualDebug="false” path="googleAnalyticsPlugin.swf"</span>

<span style="color: #0000ff;">customEvent=”<strong>doPlay</strong>” width="0%" height="0%" loadingPolicy="wait" urchinCode="UA-30149691-1"/></span>

This custom event sends all the plugin's default settings each time the doPlay action is triggered.  Multiple custom events are separated by commas as in the following:

<span style="color: #0000ff;"><Plugin id="googleAnalytics" visualDebug="false” path="googleAnalyticsPlugin.swf"</span>

<span style="color: #0000ff;">customEvent=”<strong>doPlay,playerStateChange,addThis</strong>”</span>

<span style="color: #0000ff;">addThisCategory=”My AddThis Category”</span>

<span style="color: #0000ff;">addThisAction=”My AddThis Action”</span>

<span style="color: #0000ff;">addThisLabel=”My AddThis Label”</span>

<span style="color: #0000ff;">addThisValue=”1”</span>

<span style="color: #0000ff;">width="0%" height="0%" loadingPolicy="wait" urchinCode="UA-30149691-1"/></span>

 

## <a name="GoogleAnalyticsInterface"></a>Using the Google Analytics interface

**Live reports on active viewers**

Google has added support for realtime analytics, enabling you to list the active users on a page. This can be used for real-time estimates of live stream viewers.

1.  Configure Google analytics for your player
2.  Embed your live entry with your GA enabled player.
3.  Navigate to the "real-time" section within your google analytics console
4.  Locate the content page with the live stream.  
    You can now monitor real-time visitors for your live stream video.

<img src="../../assets/1030">

**  
Accessing per content entry reports**

Google Analytics collects details reports on a per entry basis. This enables you to create segment views per content per event. For example if you wanted to see how many users reached the "playerPlayEnd" event ( i.e completed a video view ):**  
**

1.  Configure and embed a player with google analtyics.
2.  Within the google console select "Content"
3.  Select the "Events" pull down
4.  Click on "Top Events" then "Kaltura Video Events" ( for the default kaltura player events )
5.  Click on the "Event Action" your interested in i.e "mediaReady" or "75\_pct\_watched"
6.  Enter the **entryId** your interested in tracking within the search field.
7.  Here we select mediaReady, we then get the number of times the mediaReady event was called for that entry.

<img src="../../assets/1031">

 

**Accessing per live content entry reports**

Google analytics content reports for live entries can be handled very similar to VOD entries. Just be sure to make note of the specific** entryId **that your interested in tracking.**  
**

1.  Configure and embed a player with Google Analytics.
2.  Within the google console select "Content"
3.  Select the "Events" pull down
4.  Click on "Top Events" then "Kaltura Video Events" ( for the default kaltura player events )
5.  Click on the "Event Action" your interested in i.e "mediaReady" or "75\_pct\_watched"
6.  Enter the **live** **entryId** in the search field.
7.  Here we select mediaReady, we then get segments by media labels. This gives details on how many player impressions where rendered to clients. The mediaReady event is fried once the player is displayed on page.

<span style="color: #005c9c; font-family: Arial, Helvetica, Geneva, sans-serif; font-size: 13px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; line-height: normal; orphans: auto; text-align: left; text-indent: 0px; text-transform: none; white-space: normal; widows: auto; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: #f8f8f8; display: inline !important; float: none;"> </span>