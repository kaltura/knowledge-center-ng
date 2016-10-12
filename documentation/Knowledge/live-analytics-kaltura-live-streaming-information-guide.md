---
layout: page
title: "Live Analytics for Kaltura Live Streaming Information Guide"
date: 2015-01-08 14:28:31
---

<p class="mce-heading-2">
  <span style="color: #484848; font-size: 18pt; font-weight: bold; font-family: verdana, geneva;"><a name="top"></a>Introduction to Live Analytics</span>
</p>

Live Streaming Analytics is a management tool that provides powerful information about live streams in a user-friendly KMC interface – informing real-time decision-making through interactive dashboards that visualize trends and track quality metrics for both current and past live events.

*   Includes **Status-at-a-Glance**: See and share Kaltura Live session utilization and status (what's popular, trending, and going viral, etc.)
*   Assists in **Resource Planning**: Monitor utilization and plan for the future (increase video engagement, monetization, etc.)
*   Simplifies **Troubleshooting**: Quickly identify problems / root causes related to live streaming errors (and find solutions)
*   Deployment-wide service intelligence for customer’s Kaltura administrators, IT staff, senior management, etc.
*   Real-time and historical information about Kaltura live events activities and quality metrics, including interactive dashboards to visualize trends such as -
    *   real-time information on live events that are taking place right now
    *   detailed information about live events after they have taken place
    *   Kaltura Live Analytics enquire those events by presenting audience behavior and live playback characteristics such as the stream bitrate, buffer time or audience geo-locations and others.

<p class="mce-heading-3">
  What type of data is collected, analyzed and presented in aggregated form?
</p>

The Kaltura Player collects real-time player data about the audience experience for any given viewer watching a “Kaltura Live Streaming” or non Kaltura such as - Universal (Akamai), Flash and mobile / Manual URL/ multicast (RTP) event:

*   Start/Stop of live stream playback (including DVR playback, if available)
*   Buffering time (latency of live stream’s loading time on viewer’s device)
*   Bitrate played (actual quality of live stream sent to the viewer’s device)
*   Geo-IP data (viewer’s city location)
*   Hosting pages (one or more website URLs where the live stream’s player is embedded)

The information is captured and analyzed every **10 seconds** throughout the duration of a Kaltura Live Streaming event. Data is aggregated and summarized to include measurements of partner’s <span style="text-decoration: underline;">current</span> live or <span style="text-decoration: underline;">past</span> live events in the last **36 hours**.

[Back to Top][1]

 [1]: #top

<p class="mce-heading-2">
  <span style="font-family: verdana, geneva;">Kaltura Live Analytics Reports</span>
</p>

Kaltura Analytics for live streaming include several views to support the different stages and use-cases for live events.

The following live real-time reports are available:

*   [Live Content Dashboard Report][2]
*   [Specific Entry for Live Content Detailed Report][3]

 [2]: #live_content_dashboard
 [3]: #specific_entry

You can also export your data to a CSV file. See [Exporting Live Analytics to a CSV.][4]

 [4]: #exporting

<p class="mce-heading-2">
  <a name="live_content_dashboard"></a>Live Content Dashboard Report
</p>

The Live Content Dashboard Report displays:

*   **Currently broadcasting live events** (“Kaltura Live Now Only”)
*   **Entries that were live in the past 36 hours**. (“All Viewed Live Entries”)

The following three data elements are presented:

*   Summarized information reflecting ‘All Viewed Live Entries’ or ‘Kaltura Live Now Only’ filtered in the dashboard.
*   Entries that are ‘Kaltura Live Now Only’, where a live session is taking place in real-time.
*   Entries that were live in the past 36 hours:
*   Entries that were recorded and now have a VOD asset for them.
*   Entries that were not recorded.
*   Entries which are currently live and viewed by at least one viewer
*   *Kaltura Live Streaming (HDS / HLS / DASH)*
*   Other live streaming event types: *Universal Streaming, Legacy Flash Streaming [RTMP], *or* Manual Live Stream URLs*

You can access the Specific Entry Live Content detailed report (per entry) through the Live Content Dashboard Report, where you can choose an entry to display detailed information about it.

<div class="WordSection1">
  <p class="Procedure mce-procedure">
    To view the Live Content Dashboard Report
  </p>
  
  <ol>
    <li>
      Select the Analytics tab and then select Live Real-Time Dashboard.
    </li>
    <li>
      Filter the live entries. Select Kaltura Live Now Only or All Viewed Live Entries from the dropdown menu
    </li>
  </ol>
  
  <p class="mce-heading-3">
    Filtering Kaltura Live Analytics
  </p>The Live Content Dashboard Report filter is used to select how to display analytics for ‘live now’ entries only, or for all live entries in the past 36 hours. The summarized information that is shown in the report shows information based on the filter.
  
  <p>
    <img src="{{site.url}}/assets/1952">
  </p>
  
  <h2 class="mce-heading-4">
    Live Content Dashboard Report Display
  </h2>The Live Content Dashboard Report contains the entry name and the time range. The report is divided into the following areas:
</div>

1.  The filter drop down - used to specify the type of report (Kaltura Live Now Only or All Live Viewed Entries).
2.  Statistics (audience and DVR or plays, minutes viewed, buffering time, bitrate)
3.  A list of filtered live entries (up to 10 items may be displayed per page).
4.  An Entry’s specific data: Plays (or Audience for live now), Peak Audience and DVR, Minutes Viewed, Buffering Time, Average Bitrate, First and Last broadcasting time (re-broadcasting).

<h2 class="mce-heading-4">
  Live Content Dashboard Report Summarized Information
</h2>

<p class="Procedure mce-procedure">
  To display analytics for current Kaltura live events
</p>

1.  Select the Analytics tab and then select Live Real-time Dashboard.
2.  Select Kaltura Live Now Only from the filter drop down menu.  
    The following statistics are displayed in the Live Content Dashboard Report summary:

*   **Kaltura Live Now Only**
*   Audience - how many people are watching the broadcast right now
*   Minutes viewed – sum of the minutes viewed by all users from the start of broadcasting. Information is aggregated for the past 36 hours.
*   Average buffering time per minute – average time (in seconds) per minute that users experienced buffering
*   Average bitrate (KBPS) – the average bitrate users consumed during the event (kbps)

<p class="Procedure mce-procedure">
  To display analytics for all live viewed events
</p>

1.  Select the Analytics tab and then select Live Real-time Dashboard.
2.  Select All Viewed Live Entries from the filter drop down menu.  
    The following statistics are displayed in the Live Content Dashboard report summary.  All information is calculated from within the past 36 hour window.

*   **All Viewed Live Entries**
*   Plays (sum of plays on ended streams and plays on ‘live now’ streams)
*   Minutes viewed – sum of minutes viewed by all users
*   Average buffering time per minute – average time (in seconds) per minute that users experienced buffering
*   Average bitrate (KBPS)  – the average bitrate users consumed during the event (kbps)

<h3 class="mce-sub-heading">
  <span style="font-family: verdana, geneva;">Refresh Rate</span>
</h3>

The Live Content Dashboard Report is refreshed with each user action or automatically. If there is no user action, the page content is refreshed every 30 seconds.

[Back to Top][1]

<p class="mce-heading-2">
  <a name="specific_entry"></a>Specific Entry for Live Content Detailed Report
</p>

The Specific Entry Live Content Detailed report is a drill down from the Live Content Dashboard Report and presents the following five data elements:

*   Statistics for a specific entry.
*   A graph that shows the views there were in the last 36 hours.
*   A map that shows views in a geographical location, in a specific point in time (available for the last 36 hours).
*   Player - only if the entry is live now or has been recorded.
*   Top 10 referrers list.

All information is calculated from within the past 36 hour window.

<p class="Procedure mce-procedure">
  To view the Specific Entry for Live Content Detailed Report
</p>

1.  Select the Analytics tab and then select Live Real-Time Dashboard.
2.  Filter the live entries. Select Kaltura Live Now Only or All Viewed Live Entries from the dropdown menu.
3.  Click Details on an entry displayed on the dashboard.  
    <img src="{{site.url}}/assets/1989">
    The Specifc Entry for Live Content Detailed Report is displayed.  
    <img src="{{site.url}}/assets/1992">

<h2 class="mce-heading-4">
  <span style="font-family: verdana, geneva;">Specific Entry for Live Content Detailed Report Summarized Information</span>
</h2>

The report contains the entry name and the time range.

The report is divided into five areas.

1.  **Statistics** for both live now and for ended live. (audience or plays, minutes viewed, buffering time, bitrate)
2.  ****Audience Timeline Graph  
    ****
    *   current live stream (audience in past 36h, showing total viewers per 10 seconds intervals)
    *   past live stream (entire audience since first play till end broadcast, showing total viewers per 10 seconds intervals)
3.  **Player Preview**– displays the live broadcast (on air) content or the VOD content.  There may be entries without recordings that display a message that the event was not recorded
4.  **Location** – shows the audience size in a geographical location at the city level, at a specific point in time (last 36 hours). If you are looking at the map for information about a live or an ended broadcast, a tooltip is displayed showing the name of city and number of audience for the 10 seconds intervals. The user can use the map horizontal scroll thumbnail (or left/right keyboard cursors) to display historical (up to past 36 hours) data. There is also a thumbnail tooltip to help locate a specific time in the past.
5.  **Top 10 Referrers** – a list of URLs that hosted the live stream’s embedded player (sorted by # of visits) 

<span class="mce-heading-2"><span class="mce-heading-4">Investigation Reports</span></span>

There are 3 different entry types, each has a report:

*   **Entries that are ‘live now’, live session is taking place in real-time.**
    *   The preview player in this report displays the live session as it is played for the end-user.
    *   The graph displays information for the entire 36 hours.
*   **Entries that were live in the past 36 hours that were recorded and now have a VOD asset for them.**
    *   The graph in the investigation screen displays only the recorded section that was saved from the start of broadcast until it ended
    *   The player scrollbar moves simultaneously to right minute of recorded entry, when you click on the audience specific graph dot
    *   The location map scrollbar moves to matching time in full sync, providing interesting snapshot of viewers map for any broadcasting minute.
*   **Entries that were live in the past 36 hours and were not recorded.**
    *   Graph / location behave like ‘live now’ entry, no player preview.

<p class="mce-heading-4">
  Statistics - Summarized Information
</p>

Statistics for both current live and past live events (per Partner ID / specific entry) includes:

*   **Audience** - how many people are watching in real-time (for current live events)
*   **Plays** - sum of unique plays on past live events. Users who played the content multiple times are eliminated from this count, however, plays that resulted from users who refreshed/re-opened the browser with the player hosting page are counted as new plays
*   **Minutes viewed** – sum of minutes viewed by all users in aggregate
*   **Peak audience and DVR** – the maximum number of real-time and DVR viewers combined
*   **Buffering time** (per minute) – average time that viewers experienced buffering during the entirety of their viewing. (“0” = ideal playback experience, “60” = worse scenario, full buffering usually means bad network conditions)
*   **Average bitrate** (kbps) – the average bitrate users consumed during the event.

<p class="mce-heading-4">
  Graph and Map Benchmarks
</p>

*   For ‘Kaltura Live Now’ entry, both graph and map display information over <span style="text-decoration: underline;">past 36h</span>.
*   For ended entry, both graph and map display information from start of broadcast as long as it is not exceeded 36h, as currently the <span style="text-decoration: underline;">maximum given time range is 36h</span>.
*   Both the graph and map display number of audience per time, while total number of ‘circles’ will not exceed 1,000 (cities) per each interval view. Top 1000 “big audience cities” will be shown. (sort by descending audience)
*   Map displays circles by size, and color according to the viewer’s audience/DVR counts and ratio, quick glance allow to differ between interesting population groups, detect trends and overhaul behaviour.

<p class="mce-heading-4">
  Plays VS Audience
</p>

**When a viewer presses “play” on the Kaltura player** - it is counted as a play. A play is included in audience analytics only if the content is viewed <span style="text-decoration: underline;">over 10 seconds</span>. A play represents a viewer “join”, and is therefore counted only once into aggregation. If a viewer refreshed the page, and presses play, it will be considered as a new “join” and therefore a new play.

<p class="mce-heading-4">
  Live Audience vs. DVR Audience
</p>

*   **The DVR audience (current live stream)**: viewers watching in real time (but not the live point in time) are presented in separated “DVR” graph audience when the live streaming entry is active
*   **The DVR audience (ended live stream)**: viewers who watched in real time but not the live point in time) are presented in separated “DVR” graph audience (live now) once live stream has ended “DVR” graph audience will include extended part representing timeline of “DVR” viewers watching the stream after the actual live event stream ended (DVR timeline > recorded stream timeline). Extended part is synchronized with the location map, but not with the player preview.
*   Location Map shows Live and DVR audience with varying colours representing the ratio of “live to DVR” count (the tooltip shows both counts).

<h3 class="mce-sub-heading">
  Refresh Rate
</h3>

The Live Content Detailed Report is refreshed with each action of the user or automatically (in case no action took place) every 30 seconds. Only the statistics are updated.

<p class="Procedure mce-procedure">
  To view the audience at different resolutions
</p>

*   Use the scrollbar to view the audience data at different intervals.  
    The point in time in the audience graph is synchronized with the player timeline.  
    This feature is only available for past live broadcasting events that are not rebroadcasted.   
    The time indicates the time interval selected.

<p class="Procedure mce-procedure">
  To preview the broadcast
</p>

*   Click on the player.  
    You can see whether the entry is on air.

<p class="Procedure mce-procedure">
  To view the location
</p>

*   Zoom into the location for the Geographical IP to location.  
    The location tooltip indicates the number of plays at that location.
*   Use the scroll bars to see snapshots in different time intervals.

[Back to Top][1]

<h1 class="mce-heading-2">
  <a name="exporting"></a>Exporting Live Analytics to CSV
</h1>

The Live Content Dashboard Report displays all live entries that are from the last 36 hours. You can export Kaltura Analytics live streaming reports to a CSV file. CSV reports can be created on the partner id level or on the entry id level.

You can create CSV files based on the filters you have chosen from the Live Content Dashboard Reports.

*   [All Entries][5]
*   [Live Now][6]

 [5]: #all_entries
 [6]: #show_live_now

You can display analytics from the Live Content Dashboard Report as well as from the Specific Entry for Live Content Report.

The filename consists of the following information: 

*   Report type
*   Status: All or live-now
*   time range of YYYYMMDD – HHMMSS_Entry ID (for entry level reports)

The drill down CSV filename includes:

*   Status: all or live-now
*   Type of Report: location/referrers/audience/
*   Specific entry id
*   Entry name
*   Time range

The CSV structure includes statistics about the entry.

<h3 class="mce-heading-3">
  Location CSV
</h3>

Aggregation for the location analytics is on the second level descending in time, starting from the point you selected to create the CSV and no more than the last 36 hours.

The location CSV report indicates the city and country, the longitude and latitude and aggregated data in 1-minute window with following columns:

*   **Plays** – contains the sum of plays in that specific minute.
*   **Average audience** – contains the sum of the audience known in that minute, divided by the number of known events
*   **Min audience** – the minimal audience known in that minute.
*   **Max audience** – the maximal known audience in that minute
*   **Average, Min, Max DVR Audience** – the minimal, maximum and average of DVR audience in that minute
*   **Seconds viewed** – will be the sum of seconds viewed
*   **Buffer time** –The average buffer time per minute.

The location statistics start from the first point of available data in the past 36 hour interval.

The following use case provides an example:

10:30 – plays: 1

 

<div class="WordSection1">
  audience: 010:40 – plays: 0
</div>

<div class="WordSection1">
  audience: 110:50- plays: 0 audience: 1
</div>

<div class="WordSection1">
  The report will show plays: 1 audience: 2/3 min audience: 0 max audience: 1<h3 class="mce-heading-3">
    Audience CSV
  </h3>
  
  <p>
    The audience CSV report indicates the number of viewers at specific 10 second intervals.
  </p>
  
  <p>
    Aggregation is on a 10 second, level descending in time, starting from the point you selected to create the CSV. 
  </p>
  
  <p>
    If DVR is enabled for the entry, another DVR column will be included with similar behavior as in the audience column.
  </p>
  
  <h3 class="mce-heading-3">
    Referrers CSV
  </h3>
  
  <p>
    The Referrers CSV includes the list of host sites and the number of visits from the host sites sorted in descending order for the past 36 hours.
  </p>
  
  <p class="mce-heading-3">
    <a name="all_entries"></a>Show All Entries Filter
  </p>
  
  <p>
    Export to CSV - downloads all related entries for a specific partner and includes ALL available entry data (entry name, entry id, Plays, Peak Audience, Minutes viewed, Average buffering time, Average bit rate, first broadcast time and last broadcast time).
  </p>
  
  <p class="Procedure mce-procedure">
    To export analytics to a CSV for all entries
  </p>
  
  <ol>
    <li>
      Select the Analytics tab and then select Live Real-Time Dashboard.
    </li>
    <li>
      Filter the live entries. Select All Viewed Live Entries from the dropdown menu
    </li>
    <li>
      From the Live Content Dashboard Report, click Export to CSV.<br />The following message is displayed.<img src="{{site.url}}/assets/1982">
    </li>
    <li>
      Click OK.
    </li>
  </ol>
  
  <h2 class="mce-heading-3">
    <a name="show_live_now"></a>Show Kaltura Live Now Only Filter
  </h2>
  
  <p>
    Kaltura Live Now only - downloads all related entries for a specific partner and includes ALL available entry data (entry name, entry id, Plays, Peak Audience, Min viewed, average buffering time, average bit rate, first broadcast time, last broadcast time).
  </p>
  
  <p class="Procedure mce-procedure">
    To export analytics to a CSV for actual live entries
  </p>
  
  <ol>
    <li>
      Select the Analytics tab and then select Live Real-Time Dashboard.
    </li>
    <li>
      Filter the live entries. Select Kaltura Live Now Only from the dropdown menu
    </li>
    <li>
      From the Live Content Dashboard Report, click Export to CSV.<br />The following message is displayed.<img src="{{site.url}}/assets/1982">
    </li>
    <li>
      Click OK.
    </li>
  </ol>
  
  <h3 class="mce-heading-3">
    CSV Drill Down Report (for All Viewed Live Entries)
  </h3>
  
  <p class="Procedure mce-procedure">
    To export analytics to a CSV for a specific entry (including ended broadcasts)
  </p>
  
  <ol>
    <li>
      Select the Analytics tab and then select Live Real-Time Dashboard.
    </li>
    <li>
      Filter the live entries. Select All Viewed Live Entries from the dropdown menu.
    </li>
    <li>
      Click on Details to display the Specific Entry Detailed Report.
    </li>
    <li>
      Select an option from Export to CSV drop down.
    </li>
  </ol>
  
  <ul>
    <li>
      <strong>Audience - </strong>downloads all audience. (This is represented as the sum of views on ended streams and views on ‘live now’ streams for the past 36 hours or from the start of the broadcast, with at least 10 sec interval.
    </li>
    <li>
      <strong>Location</strong> – downloads one minute intervals (averaging every six “10 second” samples in the one minute interval) including time, total plays, IP to location fields, country, city, latitude and longitude (at the city level). 
    </li>
    <li>
      <strong>Referrers</strong> - downloads ALL (not just top ten) URLs (for the past 36 hours or from the start of broadcast), each referrer contains the URL, the total number of visits sorted by visit totals in ascending order.
    </li>
  </ul>
  
  <h3 class="mce-heading-3">
    CSV Drill Down report (for Kaltura Live Now Only Entries)
  </h3>
  
  <p class="Procedure mce-procedure">
    To export analytics to a CSV for a specific entry
  </p>
  
  <ol>
    <li>
      Select the Analytics tab and then select Live Real-Time Dashboard.
    </li>
    <li>
      Filter the live entries. Select Kaltura Live Now from the dropdown menu.
    </li>
    <li>
      Click on Details to display the Specific Entry Detailed Report.
    </li>
    <li>
      Select an option from Export to CSV drop down.
    </li>
  </ol>
  
  <ul>
    <li>
      <strong>Audience - </strong>downloads all audience analytics (for the past 36 hours or from the start of broadcast) with at least a 10 second interval.
    </li>
    <li>
      <strong>Location</strong> - downloads one minute interval (averaging 6 to 10 second samples), including time, total audience, IP to location fields, country, city, latitude & longitude (at the city level).
    </li>
    <li>
      <strong>Referrers</strong> - downloads URLs (for the past 36 hours or from the start of broadcast), each referrer contains the URN, the total number of visits sorted by visit totals in ascending order.
    </li>
  </ul>
  
  <h2>
    Verifying and Viewing the CSV Files
  </h2>
  
  <p>
    You should receive a notice that your CSV file was created successfully or whether it failed. Kaltura Customer Care will notify you when the file is ready and provide a link to the CSV file location.The link is valid for three days.
  </p>
  
  <div>
    <p>
      <a href="#top"> Back to Top</a>
    </p>
  </div>
</div>