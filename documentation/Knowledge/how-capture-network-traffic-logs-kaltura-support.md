---
layout: page
title: "How to capture network traffic logs for Kaltura Support?"
date: 2013-01-03 14:39:54
---

<p class="mce-sub-heading" dir="LTR">
  Contents:
</p>

<p dir="LTR">
  <a href="#fiddler">Fiddler</a>
</p>

<p dir="LTR">
  <a href="#charles">Charles Proxy</a>
</p>

<p dir="LTR">
  <a href="#firebug">Firebug</a>
</p>

<p dir="LTR">
  <a href="#chromedevconsole">Chrome Dev console</a>
</p>

<p dir="LTR">
  <strong> </strong>
</p>

<p dir="LTR">
  <strong class="mce-heading-1">What is a web debugging tool?</strong>
</p>

<p dir="LTR">
  A web debugging tool is a web proxy (HTTP Proxy / HTTP Monitor) that runs on your own computer. Your web browser (or any other Internet application) is configured to access the Internet through the proxy, and this proxy is then able to record and display the network traffic data coming in and out of your computer.
</p>

<p dir="LTR">
  Kaltura recommends using Fiddler for Windows, and Charles Proxy for Mac.
</p>

<p class="mce-heading-1" dir="LTR">
  <strong>When should you capture traffic logs?</strong>
</p>

<p dir="LTR">
  Since traffic logs record communication from and to Kaltura, they can help identify the real cause behind issues that end users see in the front end.<br /> Traffic logs are especially useful for Kaltura Support to investigate issues that are specific to the user’s network or that are not reproducible.
</p>

<p class="mce-heading-1" dir="LTR">
  <strong><a name="fiddler"></a>Fiddler</strong>
</p>

<p class="mce-heading-3" dir="LTR">
  <strong>How to capture web traffic using fiddler</strong>
</p>

1.  Download 'Fiddler' software from <a href="http://www.fiddler2.com/Fiddler2/version.asp" target="_blank">http://www.fiddler2.com/Fiddler2/version.asp</a>
2.  Open the installer file and follow the installation instructions.
3.  Once installed, open the software and make sure it is Capturing traffic:<img src="../../assets/946.img">
    Firefox may be configured to use its own Proxy settings. If you see no traffic recorded, please see [http://www.fiddlertool.com/fiddler/help/hookup.asp#Q-NonIE.  
    ][1]  
    <span class="mce-procedure">To capture traffic that is transferred through HTTPs / SSL use the followings instructions:</span>
<ol style="list-style-type: lower-alpha;">
  <li>
    Go to Fiddler open Tools->Fiddler options.<img src="../../assets/951.img">
  </li>
  <li>
    In the Fiddler options menu, select the HTTPS tab and mark the "capture HTTPS CONNECTs and Decrypt HTTPS traffic" options.<img src="../../assets/947.img">
  </li>
</ol>

4.  [][1]Clear the browser cache.
5.  Recreate the issue while Fiddler is running and Capturing.
6.  After capturing the event please save it as a .saz file.<img src="../../assets/948.img">

 [1]: http://www.fiddlertool.com/fiddler/help/hookup.asp#Q-NonIE

<p dir="LTR">
   * Additional assistance on how to use the software can be found here: <a href="http://www.fiddlertool.com/fiddler/help/ui.asp">http://www.fiddlertool.com/fiddler/help/ui.asp</a>  
</p>

<p class="mce-heading-1" dir="LTR">
  <strong><a name="charles"></a>Charles Proxy</strong>
</p>

<p class="mce-heading-3" dir="LTR">
  <strong>How to capture web traffic using Charles Proxy</strong>
</p>

1.  Download the software 'Charles Proxy' from <a href="http://www.charlesproxy.com/download/" target="_blank">http://www.charlesproxy.com/download/</a>
2.  Install the software and run it.
3.  When the software opens, in the upper left corner of the window the red dot "recording" should be highlighted – if it isn’t, click the button to “Start/Stop recording".  
    <img src="../../assets/943.img">
      
    If you need to capture HTTP / SSL traffic, see <http://www.charlesproxy.com/documentation/proxying/ssl-proxying/>
4.  [][2]Clear the browser cache.
5.  Recreate the issue you are experiencing while Charles is running.
6.  Once done, click on File->Save As, and select a unique name.  
    <img src="../../assets/944.img">
    * additional information about 'Charles' can be found @ <a href="http://www.charlesproxy.com/documentation/" target="_blank">http://www.charlesproxy.com/documentation/</a>

 [2]: http://www.charlesproxy.com/documentation/proxying/ssl-proxying/

<p class="mce-heading-1" dir="LTR">
  <strong><a name="firebug"></a>FireBug (for Firefox only)</strong>
</p>

<p class="mce-heading-3" dir="LTR">
  <strong>How to capture network traffic using Firebug?</strong>
</p>

1.  Download and install Firebug: (in FireFox only)<ol style="list-style-type: lower-alpha;">
      <li>
        From addons.mozilla.org (AMO( - Tools>Addons>Get Addons>Search["firebug"]
      </li>
      <li>
        From Firebug's releases page - <a href="https://getfirebug.com/releases/">https://getfirebug.com/releases/</a>
      </li>
    </ol>

2.  An additional extension is needed for exporting all network Traffic – **'NetExport'**. Download the latest stable version from <a href="https://getfirebug.com/releases/netexport/" target="_blank">https://getfirebug.com/releases/netexport/</a>.
3.  Restart Firefox.  
    If you need to capture traffic that is transferred through HTTPs / SSL use the followings instructions:<ol style="list-style-type: lower-alpha;">
      <li>
        Go to Fiddler open Tools->Fiddler options.<br /><img src="../../assets/951.img">
      </li>
      <li>
        In the Fiddler options menu, select the HTTPS tab and mark the "capture HTTPS CONNECTs and Decrypt HTTPS traffic" options.<img src="../../assets/947.img">
      </li>
    </ol>

4.  To activate 'Firebug',  click 'F12',  or  the FireBug icon located at the top panel.  
    <img src="../../assets/939.img">
    A console will open at the bottom of the screen.
5.  Click on 'Net' > 'All'  to capture all web traffic. You should see HTTP traffic being logged at the console.<img src="../../assets/941.img">
6.  Recreate the issue and export it as 'HAR' file. Send us the .har file.

<p dir="LTR">
  * Additional information about Firebug can be found @ <a href="https://getfirebug.com/wiki/index.php">https://getfirebug.com/wiki/index.php</a>
</p>

 

<p class="mce-heading-1" dir="LTR">
  <strong><a name="chromedevconsole"></a>Google Chrome Dev Console</strong>
</p>

<p class="mce-heading-3" dir="LTR">
  <strong>How to capture web traffic using Chrome Dev Console</strong>
</p>

1.  Push F12 on your keyboard (or right click on the page and select ‘Inspect Element’). The console appears on the bottom of the screen.  
    <img src="../../assets/931.img">
      
    
2.  On the console, select the network tab.  
    <img src="../../assets/932.img">
      
    
3.  Clear the browser cache.
4.  Recreate the issue while the console is open. You will see the HTTP traffic being logged.
5.  Right click on any of the lines and select ‘Save all as HAR’.
6.  Send us the .har file.  
    <img src="../../assets/933.img">

<p dir="LTR">
  * Additional information about 'Chrome web debugger' can be found @ <a href="https://developers.google.com/chrome-developer-tools/docs/network">https://developers.google.com/chrome-developer-tools/docs/network</a>
</p>

<p dir="LTR">
   
</p>

<p dir="LTR">
    
</p>