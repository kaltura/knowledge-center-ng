---
layout: page
title: "Kaltura Universal Digital Rights Management (DRM)"
date: 2015-06-19 08:52:23
---

<p>
    For updated information about Kaltura's DRM Solution please see the article <a href="https://knowledge.kaltura.com/node/1726" target="_blank">Kaltura Online Video Security Capabilities</a>.
  </p>
  
  <p>
    <span style="color: #484848; font-size: 18pt; font-weight: bold;">Introduction to Kaltura's Universal DRM</span><span style="color: #ff0000;"><br /></span>
  </p>
  
  <p>
    Kaltura's Universal DRM (Digital Rights Management) module is the Kaltura solution for the multi DRM eco system, which enables media companies, content rights owners and OTT providers to stream premium content without needing to worry about which browser, device or platform is being used - by supporting all major DRM schemas including Playready (over Smooth Stream and Dash CENC), Widevine (Classic and Modular over Dash CENC) and Apple Fairplay. The solution also reduces storage costs and integration fees, by supporting on the fly DRM - tightly integrated with the Kaltura on the fly packager.
  </p>
  
  <p>
    With Google and others moving to deprecate or disable existing content protection systems (for example, Widevine Classic and Silverlight plugins), and Google choosing to disable NPAPI (Netscape Plugin Application Programming Interface) support in the Chrome browser as of April 2015, Kaltura’s Universal DRM solution allows video service providers to easily transition to Universal DRM from other delivery protocols, without disrupting service, and uses one unified secure player, the <a href="http://knowledge.kaltura.com/node/1148">Kaltura Universal Studio Player</a>, to resolve the end-of-life challenge of existing player technology.  
  </p>
  
  <div>
    Kaltura’s Universal DRM supports on the fly DRM, allowing for automatic setection of the most cost effective and supported DRM schema across all browsers and platforms - including in older browsers supporting Adobe and Silverlight via a plugin translation layer. The Kaltura Universal Studio player also now supports client-side translation of existing Smooth Streaming streams into DASH Common Encryption (CENC) for playback in Chrome/Internet Explorer browsers that support the HTML5 EME standard. 
  </div>
  
  <p>
    The move to support DASH and Common Encryption (CENC) is necessary for anyone that wants to provide premium video content that is playable on all of the major browsers, platforms, and devices now available, while continuing to comply with content owners’ DRM requirements. 
  </p>
  
  <p>
    Where old methods of handling DRM demanded separate files and separate players for each DRM technology, Kaltura’s solution uses a single unified player. the <a href="http://knowledge.kaltura.com/node/1148" target="_blank">Kaltura Universal Studio Player</a> across browsers and native apps to ensure seamless support for analytics, business rules, and the user experience. Using this single standard also reduces the storage space required for files, the effort needed for content management, and the fees associated with multiple delivery technologies. 
  </p>
  
  <p>
    With Kaltura’s Universal DRM solution, content providers can make a smooth transition to the new digital ecosystem. When delivering premium content, it is critical that the end user continues to receive a consistent, high quality experience, no matter which device they use.
  </p>
  
  <p class="mce-heading-3">
    Publishers' Challenges
  </p>
  
  <ol>
    <li>
      Every piece of content goes through a packager and is then pre-encrypted. Every entry is transcoded, encrypted, and then packaged to support <strong>each</strong> DRM technology. The result: huge storage costs and file maintenance is challenging.
    </li>
    <li>
      High prices and plugin installation.  Plugins are usually priced per device. The requirements for end -users is to download a plugin to view DRM content.
    </li>
    <li>
      Market is changing. As of April 2015 -  Silverslight/Playready on Chrome has been deprecated.
    </li>
  </ol>
  
  <p class="mce-heading-2">
    The Kaltura Universal DRM Solution
  </p>
  
  <p>
    To keep up with shifts in browser platforms, DRM solutions must now include support for the HTML5 Encrypted Media Extension standard, delivered through the new streaming protocol MPEG-DASH. In a universal modular DRM solution, the same solution supplies the appropriate protocol for whichever browser is being used. Switching to modular DRM allows the use of a single standard to deliver to newer HTML5 EME enabled browsers. In its most basic form, this means using CENC and DASH to deliver content exclusively to HTML5 EME browsers.
  </p>
  
  <p>
    The Kaltura Universal DRM solution bridges this gap by supporting all major DRM schemas as well as supporting on the fly DRM packaging - allowing for automatic detection of the needed DRM schema - based on platform/browser capabilities and security consideration (hardware based DRM support will be preferred - for instance Fairplay for iOS, WIdevine for Android, and in browser default CDM support considerations - for instance Playready for Microsoft Edge browsers).
  </p>
  
  <p>
    The Kaltura Universal Studio Player bridges the changes that have arisen due to disabling existing content protection systems and supports legacy files encrypted using Smooth Streaming/Playready as well as HTML5 encrypted files.  The Kaltura Universal Studio player can handle both types of files. The player makes the call based on the device and decides whether to serve the legacy or HTML5 Common Encryption DRM.
  </p>
  
  <p>
    All HTML5 browsers, Adobe and Silverlight and all the native applications are supported. You can keep doing what you did before with you old libraries of content without changing your current deployment.<img src="{{site.url}}/assets/2369">
  </p>
  
  <p class="mce-heading-2">
    <span>Why DRM?</span>
  </p>
  
  <div>
    <ul>
      <li>
        Common requirement to distribute premium studio content
      </li>
      <li>
        Protect private enterprise content from duplication
      </li>
      <li>
        Control monetization options; subscription VOD, Video Rentals & custom entitlement rules.
      </li>
      <li>
        Offline content with regular permission checks.
      </li>
    </ul>
  </div>
  
  <p class="mce-heading-2">
    What is Modular DRM?
  </p>
  
  <p>
    Modular DRM replaces Widevine Classic, and Smooth Streaming PlayReady DRM. Modular DRM is used in the HTML5 Encrypted Media Extension Standard
  </p>
  
  <p>
    DRM has consolidated into a “Platform feature”.
  </p>
  
  <div>
    <ul>
      <li>
        To play in this space you need “a phone”; “an operating system” and a “browser”
      </li>
      <li>
        Google Widevine,Microsoft PlayReady, Apple Fairplay are main modular DRM systems.
      </li>
      <li>
        Other DRMs exist but are inherently less useful without a browser.
      </li>
    </ul>
  </div>
  
  <p>
    <img src="{{site.url}}/assets/2364">
  </p>
  
  <div>
     
  </div>
  
  <p>
    The transition to Universal DRM has been based on moving to platforms becoming the primary providers of DRM.
  </p>
  
  <p>
    The ecosystem as it exists today includes  the old way of distributing content through PlayReady/Smooth Streaming vs CENC. New protocols were introduced with their limitations.
  </p>
  
  <p>
    The Kaltura Universal/Modular DRM approach uses a consolidated option, you can use either Playready or CENC, whereas the Kaltura Universal Player intelligently selects the rendering modes, instead of supporting different pipelines, and provides support for analytics, business rules, and the user experience across platforms.
  </p>
  
  <p>
    Basic Modular DRM must re-encrypt all videos to CENC. The Kaltura Universal DRM can keep using legacy PlayReady content and begins encrypting new content to CENC.
  </p>
  
  <p>
    Companies that want to transition to the must set a target date to switch to MPEG - DASH only after updating all apps. Kaltura Universal DRM gives you flexibility to transition at your own pace. You can continue to deliver content with your existing infrastructure as you introduce the new infrastructure. There will be visitors to your sites that do not have the ability to support the new HTML5 encrypted DRM system.  Universal DRM works in both directions from old to new, and from new to old, so that viewers are able to view their content.
  </p>
  
  <p>
    The Universal Studio Player does universal translation. The components supports the standard DRM feature sets.
  </p>
  
  <p class="mce-heading-3">
    <span>What </span><span>is Kaltura Universal </span><span>DRM?</span>
  </p>
  
  <div>
    <ul>
      <li>
        A way to seamless transition to modular DRM from other delivery protocols
      </li>
      <ul>
        <li>
          Play Smooth Streaming + PlayReady streams with Google Chrome
        </li>
        <li>
          Play HLS Fairplay DRM protected content on iOS and Safari
        </li>
      </ul>
    </ul>
  </div>
  
  <div>
    <ul>
      <li>
        Unified DRM-license server for multiple license services
      </li>
      <ul>
        <li>
          Opportunistically control costs against license server used.
        </li>
      </ul>
    </ul>
  </div>
  
  <div>
    <ul>
      <li>
        DASH everywhere
      </li>
      <ul>
        <li>
          Consolidated server packing and encryption
        </li>
        <li>
          Client side Dash playback engine
        </li>
        <li>
          Client side tranitioning between legacy Smoothstream to Dash for support of legacy content on newer browsers
        </li>
      </ul>
      
      <li>
        Robust consolidated playback engine ( Kaltura Player )
      </li>
      <ul>
        <li>
          Unified business logic, and visual theme.
        </li>
      </ul>
    </ul>
  </div>
  
  <p>
    <span><img src="{{site.url}}/assets/2371">
  </p>
  
  <p>
    The Kaltura Universal Studio Player provides a single HTML5-based runtime that wraps multiple, underlining Chrome-less player engines. This enables a single player to deliver DRM playback with different underlining playback technologies.
  </p>
  
  <p>
    The following illustration displays the Kaltura Universal DRM architecture. Different underlining player engines support different CDMs across platforms with/against a unified player API.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/2372">
  </p>
  
  <p>
    <span style="color: #ff0000;"> </span>
  </p>
  
  <p>
     
  </p>
  
  <p class="mce-heading-3">
    <img src="{{site.url}}/assets/2368">
  </p>
  
  <p>
    <span> </span>
  </p>
  
  <p>
    <span> </span>
  </p>
  
  <p>
    <span> See  the</span><a href="http://knowledge.kaltura.com/node/1685" target="_blank"> Universal DRM (uDRM) Technical Specification </a>article for additional information.<a href="http://knowledge.kaltura.com/node/1685" target="_blank"></a>
  </p>
  
  <p>
    <span> </span>
  </p>
  
  <p>
    <span> </span>
  </p>
  
  <p class="mce-heading-3">
    <span> </span>
  </p>
  
  <div>
     
  </div>
  
  <div>
     
  </div>
  
  <div>
     
  </div>
  
  <div>
     
  </div>
  
  <div>
     
  </div>
  
  <div>
     
  </div>