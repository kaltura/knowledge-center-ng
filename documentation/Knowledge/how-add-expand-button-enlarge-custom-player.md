---
layout: page
title: "How to add an Expand button to enlarge a custom player"
date: 2012-12-27 11:47:31
---

This article explains how to add an Expand button to enlarge a custom Kaltura Dynamic Player version 3 (KDP3) player in a web page.

<p class="mce-heading-2">
  <a name="Whyenlargeaplayer"></a>Why enlarge a player?
</p>

Usually a player is displayed on a web page with many other elements.  <img src="{{site.url}}/assets/913">

Full screen mode allows the user to view only the player without being able to use any other part of the web page. 

Enlarging the player enables easier viewing of the player while allowing the user to continue working in your web page.  

<img src="{{site.url}}/assets/914">

<p class="mce-heading-2">
  Adding an Expand button to a custom player
</p>

You can add an Expand button to a player to enable a user to enlarge the player on the web page. <img src="{{site.url}}/assets/910">

<p class="mce-note-graphic">
  <strong>Note:</strong> In Kaltura MediaSpace, a standard player includes an Expand button. A custom player does not include an Expand button by default. 
</p>

<p class="mce-procedure">
  <span>To add an Expand button to a custom player</span>
</p>

1.  <a name="JavaScriptfunction"></a>Implement a JavaScript function that modifies your CSS to accommodate a larger player by modifying the size and layout of web page elements adjacent to the player. For example, in the web page examples in [Why enlarge a player?][1], a JavaScript function causes the gallery on the left of the player to move below the player when the player is expanded.  
    **Note**: MediaSpace provides the *kmh.expandShrinkPlayer* JavaScript function. No additional JavaScript function is required for MediaSpace.
2.  In the Kaltura Management Console (KMC), select the <a href="http://www.kaltura.com/index.php/kmc/kmc4#studio%7CplayersList" target="_blank">Studio</a> tab.
3.  Highlight a player and select **Edit** from the Actions menu, or select a new player.
4.  In the Edit Player or Create New Player window, select the Features tab and click **Additional parameters and plugins**. <span><br /></span><img src="{{site.url}}/assets/916">
    The Additional parameters and plugins menu, including a plug-in field, is displayed.  
    <img src="{{site.url}}/assets/915">
      
    
5.  For MediaSpace players: Paste the [Expand button code][2] in the plug-in field and click **go**.  
    For other players:   
    a. In the [Expand button code][2], replace *kmh.expandShrinkPlayer *in the JavaScript call with the name of your JavaScript function (see step [1][3]).   
    b. Paste the modified [Expand button code][2] in the plug-in field and click **go**.
6.  (Optional) In the Additional parameters and plugins Preview pane, click the **Preview** button to display the player with the Expand button.
7.  Click **Save Changes**.

 [1]: #Whyenlargeaplayer
 [2]: #Expandbuttoncode
 [3]: #JavaScriptfunction

<p class="mce-heading-3">
  <a name="Expandbuttoncode"></a>Code for the Expand button 
</p>

<p class="mce-sub-heading">
  v2 HTML5 Player: 
</p>

expandToggleBtn.plugin=true&expandToggleBtn.kClick=kmsExpandShrinkPlayer

<p class="mce-sub-heading">
  Legacy Flash Player (aka KDP3):
</p>

expandToggleBtn.plugin=false&expandToggleBtn.className=Button&expandToggleBtn.maxWidth=20&expandToggleBtn.toggle=true&expandToggleBtn.upIcon=openWideScreenIcon&expandToggleBtn.downIcon=openWideScreenIcon&expandToggleBtn.overIcon=openWideScreenIcon&expandToggleBtn.disabledIcon=openWideScreenIcon&expandToggleBtn.selectedUpIcon=closeWideScreenIcon&expandToggleBtn.selectedDownIcon=closeWideScreenIcon&expandToggleBtn.selectedOverIcon=closeWideScreenIcon&expandToggleBtn.selectedDisabledIcon=closeWideScreenIcon&expandToggleBtn.color2=0xDDDDDD&expandToggleBtn.color1=0xFFFFFF&expandToggleBtn.buttonType=iconButton&expandToggleBtn.relativeTo=ControllerScreen&expandToggleBtn.position=lastChild&expandToggleBtn.tooltip=Expand player&expandToggleBtn.upTooltip=Expand player&expandToggleBtn.selectedTooltip=Shrink player&expandToggleBtn.kClick=jsCall('<span style="color: #ff0000;">kmh.expandShrinkPlayer</span>')

 