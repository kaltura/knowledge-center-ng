---
layout: page
title: "Creating and Using a Player Skin"
date: 2011-12-29 13:32:47
---

<span class="mce-heading-1">Adding Kaltura Skins</span>  
KDP3 supports FLA-based skins. FLA skins are compiled to swf files using Flash IDE, and are loaded by the KDP during runtime. The loaded skin is designated in the uiConf under the layout element as the skinPath attribute.  
Designers can download the default-skin.fla file (see Resources for download) or use the skin.fla in the KDP3 project. You can modify the FLA, compile it using the <a href="http://www.adobe.com/products/flash.html" target="_blank">Adobe Flash IDE</a>, and reference the KDP3 to load the plugin. Use the Additional Parameters and Plugins section in the Kaltura Application <a href="http://www.kaltura.com/index.php/kmc/kmc4#studio%7CplayersList" target="_blank">Studio</a> (KMC > Studio > Edit a player > Features > Additional Parameters and Plugins) to add the skinPath value in flashvars or modify the KDP3 uiConf.

  
<span class="mce-heading-1">Creating a Skin swf File</span>  
The Skin .fla file (see Resources for download) contains all the default KDP3 component skins. On the stage of the FLA, the components are organized by their position in the player (for example, scroll bar, buttons, playlist, etc.) and each component is inside a designated MovieClip. Double-click a MovieClip to edit the design. When you finish modifying the components, save the FLA.  
Compile the skin swf file (File menu > Publish).

  
<span class="mce-heading-1">Testing your Skin</span>  
The easiest way to test your skin before uploading it is to add the full.skinPath to your KDP flashvars.  
<span class="mce-note-graphic">“full” is the layout ID as defined in the KDP uiConf. If you are using a default KDP, you can use “full”. If your KDP is based on a custom uiConf, check the uiConf's id attribute in the layout element.</span>

<span class="mce-note-graphic"></span>  
<span class="mce-procedure">To Test Your Skin Locally</span>

1.  Download the KDP Skins for the desired KDP version and set it up on your localhost.
1.  KDP\_Dragonfly\_Skins.zip - Holds Skins for the "Basic Template" Player introduced in Dragonfly version (the player with the thin control bar).
2.  KDP\_Falcon\_Skins.zip - Holds Skins for the "New Player" Player introduced in Falcon version (the player with the thick control bar).

2.  Copy the skin swf file you created to the same library as the checkKdp3Skin.html file.
3.  Edit the checkKdp3Skin.html file.
4.  Find the following line: //DEFINE CUSTOM SKIN URL -
5.  Below the above comment, you will find the URL linking to the skin swf file to load (variable: flashvars['full.skinPath']).
6.  Change the value of flashvars['full.skinPath'] to the name of your skin swf file.
7.  Load the page in your browser.  
    The KDP is displayed with your new skin.

<span class="mce-heading-2">Upload the Skin swf File (Kaltura Exchange)</span>  
If you want to share your skin with other Kaltura users, you can publish your skin on the Kaltura Exchange. You can host the skin file by creating a new KDP3 skin on the [Kaltura Exchange][1].

 [1]: http://exchange.kaltura.com

<p class="mce-procedure">
  To share your skin with other Kaltura Users
</p>

1.  Open the [Kaltura Exchange][2].
2.  Login with your Exchange credentials or register for a new account.
3.  Click **Add your Application to the Exchange** in the Add your Application menu.
4.  Complete as many details as possible, and describe your new skin.
5.  In the "Application Category:" menu, select **Themes and Skins**.
6.  On the second page of the "Add your Application to the Exchange" wizard, click **Browse** and select your SWF file as the first resource under Resources.
7.  Click **Upload** to upload the skin file.
8.  Complete the wizard by adding information about your skin and click **Save**.

 [2]: http://exchange.kaltura.com/user/login?destination=node/add/application

Your skin is now ready to be used. Refer to the application Overview tab for an example and instructions of how to use the new skin in your players.  
<span class="mce-note-graphic">If you want to keep you skin private, email the swf file as an attachment to your Kaltura project manager and request that the skin be available only to you.</span>