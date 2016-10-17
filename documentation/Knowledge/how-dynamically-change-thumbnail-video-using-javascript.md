---
layout: page
title: "How to dynamically change the thumbnail of video using JavaScript?"
date: 2014-11-17 14:23:36
---

<p id="HowtodynamicallychangethethumbnailofvideousingJavascript?-Retrievingthecorrectembedcode" class="mce-heading-3">
  Retrieving the Embed Code
</p>

If you are familiar with the process of finding the relevant embed code, go to [change thumbnail][1].

 [1]: #changeThumbnail

1.  In the Kaltura Management Console, select the Content tab and then select the entry you want to embed.  
      
    <img src="../../assets/2339.img">
      
    
2.   Click the Preview & Embed link.  
      
    <img src="../../assets/2340.img">
      
    
3.   Click Show Advanced Options, then change the embed type to Dynamic Embed.  
      
    <img src="../../assets/2341.img">
      
    
4.  Click the Copy button to copy the embed code to the clipboard and add the code to the source code of the specific webpage.  
      
    <img src="../../assets/2342.img">

<p id="HowtodynamicallychangethethumbnailofvideousingJavascript?-Changingthethumbnail">
  <a name="changeThumbnail"></a><span class="mce-heading-3">Changing the Thumbnail</span>
</p>

After embedding the player, the JavaScript code needs to be added to the page.

1.  Add the following code to the bottom of your page:  
      
    <table border="0" cellspacing="0" cellpadding="0">
      <tbody>
        <tr>
          <td class="gutter">
            <div class="line number1 index0 alt2">
              1
            </div>
            
            <div class="line number2 index1 alt1">
              2
            </div>
            
            <div class="line number3 index2 alt2">
              3
            </div>
            
            <div class="line number4 index3 alt1">
              4
            </div>
            
            <div class="line number5 index4 alt2">
              5
            </div>
            
            <div class="line number6 index5 alt1">
              6
            </div>
            
            <div class="line number7 index6 alt2">
              7
            </div>
          </td>
          
          <td class="code">
            <div class="container" title="Hint: double-click to select code">
              <div class="line number1 index0 alt2">
                <code class="js plain">&lt;script&gt;&nbsp;</code>
              </div>
              
              <div class="line number2 index1 alt1">
                <code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js plain">kWidget.addReadyCallback(&nbsp;</code><code class="js keyword">function</code><code class="js plain">( playerId ){&nbsp;</code>
              </div>
              
              <div class="line number3 index2 alt2">
                <code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js plain">kdp = document.getElementById( playerId );&nbsp;</code>
              </div>
              
              <div class="line number4 index3 alt1">
                <code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js keyword">var</code> <code class="js plain">imageUrl =&nbsp;</code><code class="js string">"LOCATION OF THE IMAGE"</code><code class="js plain">;&nbsp;</code>
              </div>
              
              <div class="line number5 index4 alt2">
                <code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js plain">kdp.setKDPAttribute(</code><code class="js string">"mediaProxy.entry"</code><code class="js plain">,&nbsp;</code><code class="js string">"thumbnailUrl"</code><code class="js plain">, imageUrl);&nbsp;</code>
              </div>
              
              <div class="line number6 index5 alt1">
                <code class="js spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="js plain">});&nbsp;</code>
              </div>
              
              <div class="line number7 index6 alt2">
                <code class="js plain">&lt;/script&gt;</code>
              </div>
            </div>
          </td>
        </tr>
      </tbody>
    </table>

2.  In the above code, change the imageUrl value to match the URL of the image.
3.  Save the file. The thumbnail is changed despite the default settings set in the Kaltura Management Console. 

<p style="padding-left: 30px;">
  <img src="../../assets/2343.img">
</p>

 