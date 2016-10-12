---
layout: page
title: "How to exit full screen mode when playback has ended (V2 player)."
date: 2014-11-17 15:51:32
---

You will need to use JavaScript to exit full screen mode when playback has ended, for V2 players.

1. Edit the page where the player is located, and add the following JavaScript code:

<div class="code panel pdl">
  <div class="codeContent panelContent pdl">
    <div>
      <div id="highlighter_415071" class="syntaxhighlighter nogutter  java">
        <table border="0" cellspacing="0" cellpadding="0">
          <tbody>
            <tr>
              <td class="code">
                <div class="container" title="Hint: double-click to select code">
                  <div class="line number1 index0 alt2">
                    <code class="java plain">&lt;script&gt;</code>
                  </div>
                  
                  <div class="line number2 index1 alt1">
                    <code class="java plain">function jsCallbackReady(objectId) {</code>
                  </div>
                  
                  <div class="line number3 index2 alt2">
                    <code class="java plain">window.kdp = document.getElementById(objectId);</code>
                  </div>
                  
                  <div class="line number4 index3 alt1">
                    <code class="java plain">kdp.addJsListener(</code><code class="java string">"playbackComplete"</code><code class="java plain">,&nbsp;</code><code class="java string">"playerPlayEndHandle"</code><code class="java plain">);</code>
                  </div>
                  
                  <div class="line number5 index4 alt2">
                    <code class="java plain">}</code>
                  </div>
                  
                  <div class="line number6 index5 alt1">
                     
                  </div>
                  
                  <div class="line number7 index6 alt2">
                    <code class="java plain">function playerPlayEndHandle () {</code>
                  </div>
                  
                  <div class="line number8 index7 alt1">
                    <code class="java plain">kdp.sendNotification(</code><code class="java string">'closeFullScreen'</code><code class="java plain">);</code>
                  </div>
                  
                  <div class="line number9 index8 alt2">
                    <code class="java plain">}</code>
                  </div>
                  
                  <div class="line number10 index9 alt1">
                    <code class="java plain">&lt;/script&gt; &nbsp;</code>
                  </div>
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</div>

2. Save the HTML page and validate that the solution is working.