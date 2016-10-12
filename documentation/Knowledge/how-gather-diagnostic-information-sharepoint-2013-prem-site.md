---
layout: page
title: "How to gather diagnostic information from a SharePoint 2013 On-Prem  site"
date: 2015-06-09 23:33:46
---

This article provides an outline on how to gather diagnostic information from a SharePoint 2013 On-Prem  site, usually for instances where the installation or a component may fail.

1.  Log-in to the SharePoint server. If multiple SharePoint servers exist - the following steps should be execcuted over each server.
2.  Download Microsoft's free diagnostic tool "Debug View", save it in a folder on the server and extract the package files:  
    <a href="https://technet.microsoft.com/en-us/library/bb896647.aspx" class="external-link" rel="nofollow">https://technet.microsoft.com/en-us/library/bb896647.aspx</a>
3.  Open DebugView tool as administrator.
4.  Within DebugView, click on the menu item "Capture" and ensure that the option "Capture Global Win32" is selected.
5.  Run the component that you want to diagnose, usually it ishe one that's causing trouble:<ol style="list-style-type: lower-alpha;">
      <li>
        If the installer fails at some stage - execute that stage again now
      </li>
      <li>
        If the search crawler fails to crawl - start the crawling process once again (i.e. in the search service application visit "Content Sources", locate the item "Kaltura CS", click on the item and choose "Crawl Now"
      </li>
      <li>
        If an issue occurs within some site page, for example if Kaltura widgets are not loading, load the faulty page again
      </li>
    </ol>

6.  Diagnostic information should appear within the DebugView program, mark all the entries and copy them.

<div id="kaltura_player_1433954071" style="width: 400px; height: 333px;">
  <span></span> <span></span> <span></span> <span></span> <span></span> <span></span> <a href="http://corp.kaltura.com/products/video-platform-features"><br /></a>
</div>

<div id="kaltura_player_1433976420" style="width: 400px; height: 333px;" itemprop="video" itemscope itemtype="http://schema.org/VideoObject">
  <span itemprop="name" content="gathering logs at customers site"></span> <span itemprop="description" content=""></span> <span itemprop="duration" content="371"></span> <span itemprop="thumbnail" content="http://cfvod.kaltura.com/p/1870482/sp/187048200/thumbnail/entry_id/0_c3apzrvb/version/100000/acv/102"></span> <span itemprop="width" content="400"></span> <span itemprop="height" content="333"></span>