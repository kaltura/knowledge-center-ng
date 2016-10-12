---
layout: page
title: "How to display the Source Selector options in pixels instead of bitrate?"
date: 2014-11-17 15:46:13
---

<div class="columnLayout single" data-layout="single">
  <div class="cell normal" data-type="normal">
    <div class="innerCell">
      <p>
         
      </p>
      
      <p>
        <img src="{{site.url}}/assets/2317">
      </p>
    </div>
  </div>
</div>

<div class="columnLayout single" data-layout="single">
  <div class="cell normal" data-type="normal">
    <div class="innerCell">
      <ol>
        <li>
          Log in to your KMC, then select <strong>Studio</strong> and <strong>Universal Studio</strong>.<br /><br /><img src="{{site.url}}/assets/2318">
        </li>
        <li>
          Click on the player you want to edit(be certain the player is a <a href="http://knowledge.kaltura.com/faq/universal-studio-faq" target="_blank" class="external-link" rel="nofollow">v2 player</a>), then click the plugins icon(shaped like a plug).<br /><br /><img src="{{site.url}}/assets/2319">
        </li>
        <li>
          Enable the Source Selector plugin, then expand the Ui Variables tab.<br /><br /><img src="{{site.url}}/assets/2320">
        </li>
        <li>
          Click add, then add the following keys and value pairs:<br /><br />Key: <span><strong>mediaProxy.displayFlavorPixels </strong><br /></span><span>Value: <strong>true</strong><br /><br />Key:  <strong>flavorComboControllerScreen.usePixels </strong><br />Value: <strong>mediaProxy.displayFlavorPixels </strong><br /><br />Note: Do not copy the words "key" nor "value". <br /><br /><img src="{{site.url}}/assets/2321">
        </li>
        <li>
          <span>After adding the last UI variable, click Save Player Settings to apply the changes.<br /><br /><img src="{{site.url}}/assets/2322">
        </li>
      </ol>The names of the flavors are displayed in pixels instead of bitrate.
    </div>
  </div>
</div>