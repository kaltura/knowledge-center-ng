---
layout: page
title: "Kaltura’s Generic Ads Player Plugin for VAST"
date: 2012-03-13 17:41:59
---

## About Kaltura's Ad Plugins

<div>
  Kaltura currently offers third party ads player plugins for Tremor Media, Adap.tv, YuMe, FreeWheel, DFP, EyeWonder, and AdoTube.
</div>

### Purpose

<div>
  As a result of the fact that Kaltura offers various ad server support both via Kaltura’s plugin for VAST, as well as third party ads player plugins, the question can arise as to which plugin(s) is preferable. The purpose of this article is to outline the functionality of Kaltura’s plugin for VAST and understand the differences between Kaltura’s plugin for VAST and Kalturas’ third party ad player plugins.
</div>

## About VAST

<div>
  VAST, Video Ad Serving Template, includes a standard XML-based ad response for in-stream video as well as an XML Schema Definition (“XSD”) for developers. It is meant to accommodate the majority of current practices within the online digital video advertising business. 
</div>

<div>
  (<a href="http://www.iab.net/iab_products_and_industry_services/508676/compliance/679253" target="_blank">http://www.iab.net/iab_products_and_industry_services/508676/compliance/679253</a> )
</div>

### VAST Support

<div>
  Here is a list of some of the largest video ad servers/networks that are VAST-compliant: 
</div>

<div>
  <a href="http://www.iab.net/iab_products_and_industry_services/508676/compliance/679253" target="_blank">http://www.iab.net/iab_products_and_industry_services/508676/compliance/679253</a> . Adap.TV, Tremor Media, FreeWheel, and YuMe are all VAST-compliant.Flash/HTML5 compatibility
</div>

### Flash Support

<div>
  Kaltura’s plugin for VAST supports: pre-rolls, post-rolls, mid-rolls as cue points (this is on a per-entry  basis; a user can define when in the video mid-rolls should appear based on cue points defined in Kaltura), overlays as cue points (this is either per-player basis or per-entry basis; a user can define when and for how long in the video overlays should appear based on cue points defined in Kaltura), and companion ads.
</div>

### HTML5 Support

<div>
  Kaltura’s plugin for VAST supports: pre-rolls, post-rolls, mid-rolls (as long as the video ad is HTML5- compliant), overlays (as long as the overlay is an image and not a .swf, and not in iPhones) and  companion ads (as long as the companion ad is in HTML and not Flash, and not in iPhones).
</div>

### VPAID Support

Kaltura’s plugin for VAST supports VPAID ads.

## VAST Versus Individual Ad Plugins

<div>
  Kaltura’s plugin for VAST functions differently than Kaltura’s third party ads player plugins in that the  plugin for VAST plays its pre-, mid-, and post-rolls on the same screen that video content is played on the Flash KDP, whereas individual third party ads player plugins play their ads on a screen that sits above the video screen of the Flash KDP. What this means is that VAST support works with the KDP’s scrubber and timer.
</div>

## Advantages of VAST

<div>
  <ul>
    <li>
      Fully HTML5 compatible.
    </li>
    <ul>
      <li>
        Kaltura’s Tremor, Adap.tv, YuMe, and FreeWheel plugins are not currently HTML5-compatible.
      </li>
    </ul>
    
    <li>
      Mid-rolls and overlays are available as out-of-the-box features in the plugin for VAST.
    </li>
    <ul>
      <li>
        Mid-rolls are defined on a per-entry basis.
      </li>
      <li>
        Overlays can be defined either as a per-entry basis or per-player.
      </li>
      <li>
        New plugins would need to be created in order to support mid-rolls and overlays in individual ad plugins.
      </li>
    </ul>
    
    <li>
      Ability to configure settings that will look uniform across all ad servers.
    </li>
    <ul>
      <li>
        Settings include:
      </li>
      <ul>
        <li>
          Show Notice text: ability to configure text that is displayed during ads. An example of what to display is: Video will start in: X seconds (X being the number of seconds remaining in the ad).
        </li>
        <li>
          Allow Skip: a button that allows the user to skip the ad. This can be enabled or disabled.
        </li>
        <li>
          Skip text: if Allow Skip is enabled, user can configure the text.
        </li>
        <li>
          Timeout configuration.
        </li>
        <li>
          Text colors and fonts configurations.
        </li>
      </ul>
    </ul>
    
    <li>
      Ad targeting capabilities
    </li>
    <ul>
      <li>
        User has the ability to target ads based on Kaltura metadata. User defines how ads should be targeted based on specific Kaltura metadata via the ad server. Then, the metadata field is inserted into Ad Tag URL provided to Kaltura. Ads are then targeted on a per-entry basis based on this metadata and what has been defined in the ad server.
      </li>
    </ul>
    
    <li>
      Extensive analytics capabilities
    </li>
    <ul>
      <li>
        Kaltura’s plugin for VAST plugin currently offers the following capabilities:
      </li>
      <ul>
        <li>
          Clicks
        </li>
        <li>
          25%, 50%, 75%, 100% of ad – notifications are sent that can be caught by a hook.
        </li>
        <li>
          Ad opportunity
        </li>
        <li>
          Type of ad – pre-roll, mid-roll, post-roll.
        </li>
      </ul>
      
      <li>
        Ability to create notifications for companion ads.
      </li>
      <li>
        No current analytics for overlays – but can be added via the plugin.
      </li>
    </ul>
    
    <li>
      Plugin for VAST is easily configurable.
    </li>
    <ul>
      <li>
        User can open a workspace of KDP and add events/functionality to the VAST plugin.
      </li>
    </ul>
  </ul>
</div>

<div>
  It is important to note that Kaltura’s Tremor plugin has advanced features such as mid-roll support based on a defined time setting (% of video duration, timecode, etc.) and dynamic ad targeting via Kaltura metadata. Most of Kaltura’s other individual ad plugins do not support these advanced features.
</div>

## Disadvantages of VAST

Some individual third party ads player plugins do support VPAID ads.