---
layout: page
title: "Production Player URLs"
date: 2014-10-03 18:01:34
---

**Kaltura Production Player URLs**

In the course of development or testing you make use of kgit.html5video.org or player.kaltura.com style URLs for the player library. These **should** **not be used on production sites. **To tell if your using these urls you can check your browser console, a warning would be displayed there, or inspect the network pannel to ensure no requests are served from those hosts. The correct urls are given to you via the Kaltura Management Console Preview and embed window. 

For HTTP should be structured as follows: 

*   **http://cdnapi.kaltura.com/p/{partnerId}/sp/{partnerId}00/embedIframeJs/uiconf\_id/{uiConfId}/partner\_id/{partnerId}**

For HTTPS or HTTP  should be structured as follows: 

*   **//cdnsecakmi.kaltura.com/p/{partnerId}/sp/{partnerId}00/embedIframeJs/uiconf\_id/{uiConfId}/partner\_id/{partnerId}**

If your site includes the correct style url from above and your still getting the player warning; please check what version of the library is being pointed to using the [player version utility][1]. Using the player version utility you should always select a **"release version"** ( not a pre-release version) for production usage of the player library. 

 [1]: http://player.kaltura.com/kWidget/tests/PlayerVersionUtility.html "player version utility"