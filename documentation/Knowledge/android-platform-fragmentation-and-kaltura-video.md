---
layout: page
title: "Android Platform Fragmentation and Kaltura Video"
date: 2012-07-30 05:56:38
---

<span><img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/dontpanic_01.jpg" alt="android fragmentation don't panic " width="180" height="236" style="float: left; padding: 5px;" /><span style="font-size: medium;">Much has been written regarding </span></span><span style="font-size: medium;">fragmentation in the Android platform. Behind all these <span class="c0"><a href="http://www.businessinsider.com/chart-of-the-day-ios-vs-android-fragmentation-2012-6" class="c2">ugly</a></span> <span class="c0"><a href="http://theunderstatement.com/post/11982112928/android-orphans-visualizing-a-sad-history-of-support" class="c2">charts</a></span>, <span class="c0"><a href="http://opensignalmaps.com/reports/fragmentation.php" class="c2">maps</a></span> and <span class="c0"><a href="http://www.androidfragmentation.com/news;jsessionid=51DBB55A3272D14DC786407B89254BCB#" class="c2">databases of inconsistencies</a></span> lies the challenge of building consistent user experiences for your visitors. This is especially true for web video where html5 sometimes works and sometimes does not, where Flash is sometimes supported and <span class="c0"><a href="http://arstechnica.com/gadgets/2012/06/no-flash-for-android-4-1-no-new-installs-after-august-15/" class="c2">increasingly not</a></span>.</span>

<p class="c5">
  <span style="font-size: medium;">At Kaltura we aim to deliver video everywhere and we are increasingly testing a broad set of Android devices across the major release versions across emulators, physical devices and live device testing tools like <span class="c0"><a href="http://www.perfectomobile.com/" class="c2">perfecto mobile</a></span>. While we are always working to stay ahead of evolving technologies, here we outline some of our findings to help Kaltura users and video producers better manage expectations around Android web video delivery.</span>
</p>

<p class="c5">
  <span style="font-size: medium;">Kaltura also supports <span class="c7">native Android applications</span>; which provide a lower level media framework along with the ability to build your own tools for end to end control of the experience from everything to DRM to player UI. But the focus in this document is exclusively on Android Web views without the installation of any additional software on the respective devices. This means we don’t consider telling the user to “upgrade flash” or “install mobile Firefox” even if it would greatly improve their experience.</span>
</p>

<p class="c5">
  <span style="font-size: medium;">This document is broken into sections per major Android releases and includes examples and screenshots of popular phones running each version of the platform along with explanations of the limitations and trade offs of each device respective of the version of Android its running.</span>
</p>

<p class="c5">
   
</p>

<div style="clear: both;">
   
</div>

<a name="android1"></a><span class="mce-heading-1">Android 1.x</span>

 

<p class="c5">
  <span><img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/HTC_Sprint.jpg" alt="htc sprint phones" width="160" height="225" style="float: left; padding: 5px;" /><span style="font-size: medium;">Android 1.x is practically speaking </span></span><span style="font-size: medium;"><span class="c4">not supported</span>, these devices often did not have HTML5 or Flash installed, for these devices we provide a direct link to download the asset that is the least common denominator variant of h.264 file. In terms of analytics this means only the video “play” event is registered and details of player progress are not available. Likewise ads are not possible unless they are burned into the stream.</span>
</p>

<p class="c5">
  <span style="font-size: medium;">Featured to the left is the <strong><span class="c3">Sprint HTC Hero</span></strong> running <strong><span class="c3">Android 1.5</span></strong>, it includes Flash but stuck with an old version Flash 9, won’t run the flash KDP player, so we provide a direct link to the asset for playback.<span class="c4"> ( </span>It appears to sometimes crash playing videos in the native player. )</span>
</p>

<p class="c5">
   
</p>

<div style="clear: both;">
  <span style="font-size: medium;"> <img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/Acer_Liquid_01.jpg" alt="acer" width="160" height="173" style="float: right; padding: 5px;" />Featured to the right, the <strong><span class="c3">Acer liquid A1</span></strong> running  <span class="c3"><strong>Android 1.6</strong>, </span>also does not support HTML5 directly, and this Acer does not support Flash either, so again we go with direct links to base profile 360P h.264 asset. The updated Android seems to handle the qunit test files better and supports the css properties needed to display the player image thumbnail.</span><p>
     
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <p class="c5 mce-heading-1">
    <span><a name="android2"></a>Android 2.x</span>
  </p>
  
  <p>
    <img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/AndroidUsers_Pie.jpg" width="300" style="float: left; padding: 5px;" /><span style="font-size: medium;">As of September 2012 Android 2.x still makes up <a href="http://www.tmonews.com/2012/09/google-releases-september-distribution-chart-for-android-version-breakdown/">the majority</a> of the Android platform market share. Unlike 1.x, 2.x often features the latest mobile flash and rudimentary HTML5 support. While this offers advantages in terms of analytics and player api support,</span><span style="font-size: medium;"><span class="c3"> </span><span class="c3 c4">it creates complicated trade offs.</span></span>
  </p>
  
  <p class="c5">
    <span style="font-size: medium;">These trade offs have the HTML5 native device player on one end offering hardware accelerated playback, a native player ui but little flexibility in controlling the experience, vs flash player that provides more control over experience (ads, branded player), but sometimes lacks hardware acceleration / kills battery life, is difficult to use desktop ui’s on mobile, and sometimes fails in subtle ways such as not properly supporting landscape vs portrait device orientation transitions.</span>
  </p>
  
  <p class="c5">
    <span style="font-size: medium;">Kaltura provides tools for managing these trade offs; such as the "<span class="c0"><a href="http://html5video.org/wiki/Kaltura_HTML5_Configuration#Lead_with_HTML5_on_Android" class="c2">use html5 first on android option</a>"</span>, as well as fine grain per-device controls via the <span class="c0"><a href="http://html5video.org/wiki/KalturaPlugins:UserAgentPlayerRules" class="c2">user agent player controls plugin</a></span>. Integrators can manage trade offs with rules such as “use flash on android”, or provide an html message pointing viewers to download a native app for particular mobile user agents.</span>
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <p class="mce-heading-2">
    <span class="c3 c4">Android 2.2</span>
  </p>
  
  <p>
    <span class="c3 c4"><span><img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/Smasung_GalaxyS_01.jpg" alt="samsung android 2.2" width="160" height="177" style="float: right; padding: 5px;" /><span style="font-size: medium;">The </span></span><span style="font-size: medium;"><strong><span class="c3">Samsung Galaxy S</span> </strong>running </span></span><span style="font-size: medium;"><strong><span class="c3">Android 2.2</span></strong>, includes both Flash and HTML5 support. Via configuration options we can choose the html5 player or the Flash player.  On the left we see the html5video.org site which aims to promote html5 video so chooses to lead with HTML5. Further to the left Disney’s Lady and the Tramp site, where they want more fine grain control over the player experience on the device and use the Kaltura flash kdp on the android device by leading with flash on android.</span>
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <span><span> <img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/HTC_EvoShift_01.jpg" width="160" height="225" style="float: left; padding: 5px;" /><span style="font-size: medium;">The </span></span><span style="font-size: medium;"><span class="c3"><strong>HTC Evo Shift</strong> 4G</span> running <strong><span class="c3">Android 2.2</span></strong> includes android 2x style native playback html5 support and flash 10,1,95, so it has no trouble running <span class="c4">both</span> flash and html5 style players.</span></span><p>
     
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <p class="mce-heading-2">
    <span class="c3 c4"><span><span><span>Android 2.3</span></span></span></span>
  </p>
  
  <p>
    <span class="c3"><img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/HTC_Evo3D_01.jpg" width="160" height="145" style="float: right; padding: 5px;" /><span style="font-size: medium;"><strong>Motorola Droid Razor</strong> </span></span><span style="font-size: medium;">running<strong> <span class="c3">Android 2.3.6</span></strong> and <strong><span class="c3">Flash 10,3,185</span></strong>, tells a similar story to the other 2.2 android phones with flash and HTML5 support. The player ui is overlayed even during the display of the poster, <span class="c4">we may work around this issue in the future by hiding the native player offscreen until playback starts</span>.</span>
  </p>
  
  <p>
     
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <span><span><img src="http://cdnknowledge.kaltura.com//sites/default/files/styles/large/public/image11.png" width="70" height="137" style="float: left; padding: 5px;" /><span style="font-size: medium;">The </span></span><span style="font-size: medium;"><span class="c3">Evo 3D</span> running <span class="c3">android 2.3.4</span> also supports HTML5 and flash so again the choice is yours.</span></span><p>
     
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <p class="mce-heading-1">
    <span><span><a name="android3"></a>Android 3.x</span></span>
  </p>
  
  <p>
    <span style="font-size: medium;">Android 3 was largely focused on tablets and was the first android to (supposedly) support the apple live http (HLS) streaming protocol for live and on demand adaptive streaming. In the rush to get to these tablets to market HTML5 video support clearly suffered.</span>
  </p>
  
  <p>
    <span><img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/Samsung_GalaxyTab_01.jpg" width="400" height="249" /></span>
  </p>
  
  <p>
    <span style="font-size: medium;"> </span>
  </p>
  
  <p>
    <span style="font-size: medium;">The <strong><span class="c3">Samsung Galaxy Tab 10.1</span></strong>, running <strong><span class="c3">Android 3.1</span> </strong>suffers from no flash and pretty broken html5 support. What is worse when in “desktop view” mode its user agent matches OSX Safari. Additionally diffrent builds have diffrent borken behavior as seen above for the same html5video.org page SCH-I950 vs P750 both “Galaxy Tab 10.1, Android 3.1 but a diffrent build with diffrent errors. Your best hope with the Galaxy tab is that the user has <em>installed flash.</em></span>
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <p class="mce-heading-1">
    <span><a name="android4.1"></a>Android 4.1</span>
  </p>
  
  <p class="c5">
    <span style="font-size: medium;">Looking to the future Google and Adobe are phasing out mobile flash and with 4.1 grade A html5 support arrives to the android platform in the form of <span class="c0"><a href="http://www.pcmag.com/article2/0,2817,2406535,00.asp" class="c2">flash free chrome replacing the stock browser</a></span>. This means we can expect near desktop quality html5 support in android tablets and smartphones going forward. While the future is bright there still some stock android browsers in android 4 that while are an improvement over previous iterations can’t not handle all the features of mobile chrome.</span>
  </p>
  
  <p class="c5">
    <span style="font-size: medium;"><img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/Smasung_GalaxySIII_01.jpg" width="400" height="235" style="float: left; padding: 5px;" />The <span class="c3"><strong>Samsung Galaxy S III</strong>, </span>is one of the premier Android 4<span class="c3"> </span>devices, running <span class="c3">Android 4.0.4</span> chrome is not yet the stock browser so it suffers from some peculiarities in intensive tests like ad overlays and ad inserts. If you're using mobile Chrome however, which will be the (default going forward), the experience is comparable to desktop html5 with support for overlays and ads.</span>
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <p class="c5">
    <span style="font-size: medium;"> </span>
  </p>
  
  <p class="c5">
    <span style="font-size: medium;"> <img src="http://cdnknowledge.kaltura.com//sites/default/files/pictures/nexus_ads.png" width="100" style="width: 300px; float: left; padding: 5px;" />To the left a <strong>nexus 7</strong> runing <strong>android 4.1</strong> displays a double click dfp preroll ad similar to its big brother <em>desktop chrome</em>. </span>
  </p>
  
  <div style="clear: both;">
     
  </div>
  
  <div style="clear: both;">
     
  </div>
  
  <p class="c5 mce-heading-1">
    <a name="summary"></a>In Summary
  </p>
  
  <p>
    <span style="font-size: medium;">Android 1.x does not support flash or html5, so we provide direct download link to play, this means no ads or player branding and limited analytics. Android 2.2 / 2.3 devices often include flash, by default Kaltura uses the flash runtime providing robust ads, player branding, and analytics support, but you may experience some UI issues and the interface can be hard to use on a phone. Android 2 also has native player html5 support, where the page invokes the native phone friendly player ui, while supporting most of the html5 api. Android 3 is similar to Android 2 in terms of flash and calling out to native players, but also adds limited support for Http Live Streaming ( apples adaptive streaming protocol ). Android 4 adds support for grade A HTML5 with mobile chrome; enabling inline players, ads, branded experiences. Android 4 also more aggressively deprecates flash support.</span>
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
</div>