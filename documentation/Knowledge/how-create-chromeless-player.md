---
layout: page
title: "How to create a chromeless player"
date: 2012-01-09 18:12:00
---

<p class="mce-note-graphic">
  <span><span>To learn how to create players, refer to the <a href="http://knowledge.kaltura.com/sites/default/files/Kaltura_%20Management_Console_%28KMC%29_User_Manual.pdf">Kaltura Management Console (KMC) User Manual</a>, Creating and Customizing Playlists and Players.</span><br />To learn about UIVars and how to set player variables, refer to <a href="http://knowledge.kaltura.com/faq/how-use-kaltura-player-studios-additional-parameters-and-plugins">How to use the Kaltura Player Studio's Additional parameters and plugins</a>.</span>
</p>

<p class="mce-procedure-text mce-procedure">
  To create a chromeless player:
</p>

1.  Open the KMC and go to [Studio][1].
2.  Select the type of player to create.
3.  Configure the **Basics** settings.
4.  On the **Features** tab, expand the** Additional parameters and plugins** panel.
5.  In the **Paste your plug-in line here** field, insert the following UIVars code and click **go**:  
    {% highlight plaintext %}controlsHolder.includeInLayout=false&controlsHolder.visible=false&externalInterfaceDisabled=false{% endhighlight %}**
6.  (Optional) Modify the **Key-value table** values.
7.  Click **Save Changes**.

 [1]: http://www.kaltura.com/index.php/kmc/kmc4#studio%7CplayersList