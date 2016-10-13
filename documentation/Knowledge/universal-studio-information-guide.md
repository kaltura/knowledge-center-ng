---
layout: page
title: "Universal Studio Information Guide "
date: 2014-03-23 01:20:52
---

<a name="top"></a>This article describes the following topics:

*   [Overview of the Universal Studio][1]
*   [Creating a Player in the Universal Studio][2]
*   [Configuring the Player’s Look and Feel][3]
*   [Configuring the Player’s Analytics][4]
*   [Monetization - Configuring the Player Advertising Settings][5]
*   [Plugins][6]

 [1]: #overview
 [2]: #creating_a_player
 [3]: #lookandfeel
 [4]: #configuring_analytics
 [5]: #monetizationsection
 [6]: #plugins

<p class="mce-heading-2">
  <a name="overview"></a>Overview of the Universal Studio
</p>

The Universal Player Studio is a robust HTML based player editor.  It supersedes the Studio Flash Player and natively edits the Kaltura Player Toolkit (v2) players' JSON based configuration. Kaltura Toolkit players can be embedded into responsive HTML web pages and native iOS and Android applications. For more information see [Kaltura Player Toolkit ][7].

 [7]: http://knowledge.kaltura.com/kaltura-player-v2-toolkit-theme-skin-guide

Architecturally, the Kaltura Universal Studio Player works with non-destructive JSON editing that enables both manual edits of the JSON file as well as editing the JSON file with the player studio GUI. This guide is exclusively focused on the user interface. If you want to edit a player’s JSON source directly, you can do so in the <a href="http://player.kaltura.com/kWidget/tests/PlayerVersionUtility.html" target="_blank">Kaltura Player Version Utility Page</a>.

For frequently asked questions per transitioning between the Flash Studio and the Universal Studio, see the <a href="http://knowledge.kaltura.com/node/1147" target="_blank">Universal Studio FAQ</a>. Pay close attention to the limitations in transitioning to the Universal Studio and using a Kaltura Player Toolkit v2 Player. 

<p class="mce-heading-3">
  Desgining and Configuring a Player
</p>

<p class="mce-note-graphic">
  When upgrading a player that was created in the Flash Studio, be sure to duplicate the player. Not all of the Flash features are directly supported in the Universal Studio players, and unexpected results may occur.
</p>

Use the Universal Studio tab in the KMC to create configurations and design players and playlists. You can add, remove and adjust multiple buttons and features, and design a player to match the look of your site. 

<h3 class="mce-heading-4">
  Updating the Player List in the Universal Studio
</h3>

The Universal Studio tab displays the complete list of the players defined in your account. This includes players created with the Flash studio. To edit any player in the Universal Studio, the player must be updated to the new Universal Studio Players. This includes any players previously created via API and even early versions of v2 players.

All players created using the previous KMC Studio are automatically available to be upgraded in the new Universal Studio.

<p class="Procedure mce-procedure">
  To update the players
</p>

1.  Select the Studio tab and then click Universal Studio.  
    The list of existing players is displayed.
2.  Click Update to update the player to the Universal Studio player.  
    <img src="{{site.url}}/assets/1657">
    An Update confirmation box is displayed.  
    <img src="{{site.url}}/assets/1668">
3.  Click Update.
4.  Click Upgrade to upgrade the player to the latest version of Universal Studio players.  
    <img src="{{site.url}}/assets/1659">
    An Upgrade confirmation box is displayed.
5.  Begin to configure the Universal Studio player settings.

<h3 class="mce-heading-4">
  Reverting to the Flash Studio Player
</h3>

Since some of the Flash features are not directly supported in the Universal Studio players, you may want to revert to the originally configured Flash player.

<p class="Procedure mce-procedure">
  To revert back to the original studio player
</p>

1.  Clone a player in before you upgrade it.
2.  Delete the upgraded player.

<div>
  <h2 class="mce-heading-3">
    Universal Studio Icons
  </h2>
  
  <p>
    The Universal Studio icons represent the following configuration options:
  </p>
  
  <table border="1" cellspacing="0" cellpadding="0" align="left">
    <thead>
      <tr align="center" valign="middle">
        <td valign="top" width="248">
          Icon
        </td>
        
        <td valign="top" width="248">
          <p class="TableBodyText">
            Name
          </p>
        </td>
        
        <td valign="top" width="543">
          <p class="TableBodyText">
            Description
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr align="left" valign="middle">
        <td valign="top" width="248">
          <p class="TableBodyText">
            <img src="{{site.url}}/assets/1522">
          </p>
        </td>
        
        <td valign="top" width="248">
          <p class="TableBodyText">
             Search icon.
          </p>
        </td>
        
        <td valign="top" width="543">
          <p class="TableBodyText">
            Use this section to search for configurable properties across all player plugins. Opens the Menu Search window.
          </p>
        </td>
      </tr>
      
      <tr align="left" valign="middle">
        <td valign="top" width="248">
          <p class="TableBodyText">
            <img src="{{site.url}}/assets/1523">
          </p>
        </td>
        
        <td valign="top" width="248">
          <p class="TableBodyText">
            <a href="#basic">Basic Display</a> icon
          </p>
        </td>
        
        <td valign="top" width="543">
          <p class="TableBodyText">
            Use this section to set the player name, entry and aspect ratio. Opens the Basic Display window.
          </p>
        </td>
      </tr>
      
      <tr align="left" valign="middle">
        <td valign="top" width="248">
          <p class="TableBodyText">
            <img src="{{site.url}}/assets/1524">
          </p>
        </td>
        
        <td valign="top" width="248">
          <p class="TableBodyText">
            <a href="#lookandfeel">Look and Feel</a> icon
          </p>
        </td>
        
        <td valign="top" width="543">
          <p class="TableBodyText">
            Use this section to adjust the visual appearance of the player. Opens the Look and Feel window.
          </p>
        </td>
      </tr>
      
      <tr align="left" valign="middle">
        <td valign="top" width="248">
          <p class="TableBodyText">
            <img src="{{site.url}}/assets/1525">
          </p>
        </td>
        
        <td valign="top" width="248">
          <p class="TableBodyText">
            <a href="#configuring_analytics">Analytics</a> icon
          </p>
        </td>
        
        <td valign="top" width="543">
          <p class="TableBodyText">
            Use this section to configure analytics via the Kaltura platform as well as via 3rd party analytics providers. Opens the Analytics window.
          </p>
        </td>
      </tr>
      
      <tr align="left" valign="middle">
        <td valign="top" width="248">
          <p class="TableBodyText">
            <img src="{{site.url}}/assets/1537">
          </p>
        </td>
        
        <td valign="top" width="248">
          <p class="TableBodyText">
            <a href="#monetization">Monetization icon</a>
          </p>
        </td>
        
        <td valign="top" width="543">
          <p class="TableBodyText">
            Use this section to configure content monetization plugins. Opens the Monetization window.
          </p>
        </td>
      </tr>
      
      <tr align="left" valign="middle">
        <td valign="top" width="248">
          <p class="TableBodyText">
            <img src="{{site.url}}/assets/1541">
          </p>
        </td>
        
        <td valign="top" width="248">
          <p class="TableBodyText">
            <a href="#plugins">Plugins</a> icon
          </p>
        </td>
        
        <td valign="top" width="543">
          <p class="TableBodyText">
            Use this section to configure additional plugins. Opens the Plugins window.
          </p>
          
          <div>
             
          </div>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    <a href="#top">Back to top.</a>
  </p>
  
  <h1 class="mce-heading-2">
    <a name="creating_a_player"></a>Creating a Player in the Universal Studio
  </h1>
  
  <p>
    Each player contains a collection of features of a specific Kaltura Player configuration. In addition to the Kaltura defined features, a player can include a custom plugin configuration.
  </p>
  
  <p class="Procedure mce-procedure">
    To create a player
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab.
    </li>
    <li>
      Click Add New player.<br />The Basic Display window is displayed.<img src="{{site.url}}/assets/1483">
    </li>
    <li>
      Configure the <a href="#basic">Basic settings</a>.
    </li>
    <li>
      Configure the <a href="#lookandfeel">Universal Studio Player Look and Feel Features.</a>
    </li>
    <li>
      Configure the <a href="file:///C:/Users/debbie.zioni/Documents/KMC/IX/Studiov2/Universal_Studio_Configuration_Guide-dzMarch23.docx#_Configuring_the_Player’s_1">Analytics</a>. (Optional)
    </li>
    <li>
      Configure the <a href="file:///C:/Users/debbie.zioni/Documents/KMC/IX/Studiov2/Universal_Studio_Configuration_Guide-dzMarch23.docx#_Monetization_-_Configuring_1">Monetization</a>. (Optional)
    </li>
    <li>
      Configure the <a href="file:///C:/Users/debbie.zioni/Documents/KMC/IX/Studiov2/Universal_Studio_Configuration_Guide-dzMarch23.docx#_Plugins">Plugins</a> (Optional)f
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <h3 class="mce-heading-4">
    <a name="basic"></a>Basic Display
  </h3>
  
  <p>
    Use the Basic Settings to set the player name, entry and aspect ratio.
  </p>
  
  <p>
    Enter the following information:
  </p>
  
  <table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td style="text-align: left;" valign="top" width="133">
          <p class="TableHeading">
            Field
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="120">
          <p class="TableHeading">
            Description
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="489">
          <p class="TableHeading">
            Values
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="133">
          <p class="TableBodyText">
            Player’s Name
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="120">
          <p class="TableBodyText">
            Enter an informative Player Name (required).
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="489">
          <p class="TableBodyText">
             
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="133">
          <p class="TableBodyText">
            <a name="preview_playlist"></a>Preview entry / playlist
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="120">
          <p class="TableBodyText">
            Choose an entry/playlist to preview using the player. Some features may be dependent for specific entries.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="489">
          <p class="TableBodyText">
            A list of entries/playlists for your account. The Playlist plugin can be found in the 'Look and Feel' section.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="133">
          <p class="TableBodyText">
            Player Dimensions
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="120">
          <p class="TableBodyText">
            The default player size is 560 px by 395 px. Use this option to create a custom player size that is constrained to the selected aspect ratio.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="489">
          <p>
             <img src="{{site.url}}/assets/2356">
          </p>
          
          <p>
            When you select an aspect ratio, the height is automatically calculated according to the selected aspect ratio. You can select Custom from the drop down menu and enter the custom width, the height is derived automatically.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="133">
          <p class="TableBodyText">
            <span style="color: #000000;">Enable mobile skin</span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="120">
          <span style="color: #000000;">Use this option to enable the new, touch friendly player design for mobile devices. Note that enabling the new skin will override any existing custom CSS.<br /></span>
        </td>
        
        <td style="text-align: left;" valign="top" width="489">
          See <a href="{{site.url}}/documentation/Knowledge/using-kaltura-v2-player-mobile-skin.html" target="_blank">Using the Kaltura V2 Player Mobile Skin</a> for more information. 
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="133">
          <p class="TableBodyText">
            Automatically play video on page load
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="120">
          <p class="TableBodyText">
            If the player should automatically start playback.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="489">
          <p class="TableBodyText">
            True or false
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="133">
          <p class="TableBodyText">
            Start player muted
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="120">
           
        </td>
        
        <td style="text-align: left;" valign="top" width="489">
           
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="133">
          Hovering Controls
        </td>
        
        <td style="text-align: left;" valign="top" width="120">
           
        </td>
        
        <td style="text-align: left;" valign="top" width="489">
           
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    <img src="{{site.url}}/assets/1486">
  </p>
  
  <p>
    <a href="#top">Back to top.</a>
  </p>
  
  <h4 class="mce-heading-4">
    Editing a Player
  </h4>
  
  <p>
    All changes you make to an existing player will propagate to all sites where the player has been embedded, including syndicated players on other sites.
  </p>
  
  <p class="Procedure mce-procedure">
    To edit a player
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab.
    </li>
    <li>
      Click on the relevant player in the Player List.
    </li>
    <li>
      Select an icon to modify the current player configuration.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <h3 class="mce-heading-4">
    Duplicating a Player
  </h3>
  
  <p class="Procedure mce-procedure">
    To duplicate a player
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab.
    </li>
    <li>
      Click on the relevant player in the Player List.
    </li>
    <li>
      Click Duplicate.<br /> The player configuration Basic Configuration window is displayed and the player is rendered as a copy of the existing player.
    </li>
    <li>
      Modify the player’s Basic Display settings to give the new player a distinct name
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <h3 class="mce-heading-4">
    Deleting a Player
  </h3>
  
  <p>
    Deleting a player eliminates it from all the locations where the player has been previously embedded. For example, if you have embedded a player using this design on your site or an external site, after you delete it from the Player List, the player will no longer appear and a blank area is displayed on the website.
  </p>
  
  <p class="Procedure mce-procedure">
    To delete a player
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab.
    </li>
    <li>
      In the Actions column of the relevant player, click Delete.<br />A Delete confirmation prompt is displayed.
    </li>
    <li>
      Confirm the deletion.
    </li>
  </ol>
  
  <h3 class="mce-heading-3">
    508 Compliancy
  </h3>
  
  <p>
    All Universal Studio players are 508 compliant. The player’s features include:
  </p>
  
  <ul>
    <li>
      Support for captions file in timed text or SRT formats for the video/audio file 
    </li>
    <li>
      Support for an audio description in a standardized format for the video/audio file
    </li>
    <li>
      Hidden text elements for every non-text element (for screen readers)
    </li>
    <li>
      Tooltips
    </li>
    <li>
      Keyboard tabbing and controls
    </li>
  </ul>
  
  <p>
    For more information see <a href="{{site.url}}/documentation/Knowledge/508-support-within-kaltura-player-toolkit.html" target="_blank">508 Support within the Kaltura Player Toolkit</a>.
  </p>
  
  <p class="mce-heading-3">
    <a name="cvaa_compliancy"></a>CVAA Compliancy
  </p>
  
  <p>
    All Universal Studio players are CVAA compliant. The player’s features include:
  </p>
  
  <ul>
    <li>
      Studio support - Enable options menu
    </li>
    <li>
      Captions types: XML, SRT/DFXP, VTT(outband)
    </li>
    <li>
      Displaying and changing fonts in 64 color combinations using eight standard caption colors currently required for television sets.
    </li>
    <li>
      Adjusting character opacity
    </li>
    <li>
      Ability to adjust caption background in eight specified colors.
    </li>
    <li>
      Ability to adjust character edge (i.e., non, raised, depressed, uniform or drop shadow).
    </li>
    <li>
      Ability to adjust caption window color and opacity.
    </li>
    <li>
      Support for displaying multiple language tracks and simplified or reduced captions.
    </li>
    <li>
      Ability to preview setting changes, have display setting remembered between viewings and turn captions on or off as easily as muting or adjusting the volume.
    </li>
    <li>
      Capability of displaying various caption formats (i.e., pop-on, roll-up and paint-on)
    </li>
  </ul>All captions configuration options must be set prior to beginning playback. Caption settings are put into the player when it is setup.
  
  <br /><p>
    For more information about the closed captions editor see <a href="#cvaa">Closed Captions</a>.
  </p>
  
  <p>
    <a href="#top">Back to top.</a>
  </p>
  
  <p class="mce-heading-2">
    <a name="lookandfeel"></a>Configuring the Player’s Look and Feel 
  </p>
  
  <p>
    The Look and Feel tab is made up of different sections, controlling the various features of the player.
  </p>
  
  <p>
    Use the options in this window to select the features (buttons, layers and modules) to be included in your player. As you select your features from the list, you can preview the changes in real time in the preview pane on the right.
  </p>
  
  <h2 class="mce-heading-3">
    Universal Studio - Player Look and Feel Features
  </h2>
  
  <p>
    The look and feel features include configurable features (buttons, layers and modules) available for the Universal Studio Player. Checking the box next to any feature allows you to preview it in the Preview Pane. Most of the features have in-depth configuration options.
  </p>
  
  <ul>
    <li>
      <a href="#tooltips">Displaying/Hiding Tooltips</a> – Use to enable or disable tooltips display.
    </li>
    <li>
      <a href="#title_label">Title Label </a>- Use to set the title text within the hover.
    </li>
    <li>
      <a href="#logo">Logo</a> – Use to load the image URL.
    </li>
    <li>
      <a href="#laoding_spinner">Loading Spinner</a> – Use to set the Loading Spinner.
    </li>
    <li>
      <a href="#volume_control">Volume Control </a>- Use to control the player volume using mute/unmute buttons and a volume slider.
    </li>
    <li>
      <a href="#closed_captions">Closed Captions </a>- Use to set up closed captions and the caption display. Kaltura includes multi-lingual closed captions support that comply with FCC regulations.
    </li>
    <li>
      <a href="#watermark">Watermark </a>- The Kaltura watermark plugin.
    </li>
    <li>
      <a href="#custom_styles">Custom Styles </a>– Modify the theme CSS style.
    </li>
    <li>
      <a href="#info_screen">Info screen</a> - Add Information screen about the video.
    </li>
    <li>
      <a href="#share">Share and Embed</a> - Add the Share and embed interface to the player.
    </li>
    <li>
      <a href="#embed_ly">Enable embed.ly embeds</a> - <span>Enable embed.ly sharing of the Kaltura player. </span>
    </li>
    <li>
      <a href="#related">Related</a> - Add the Related Videos screen at the end of the video to attract users to watch additional videos.
    </li>
    <li>
      <a href="#dual_screen">Dual Screen</a> - Provides you with multiple interactive viewing options.
    </li>
    <li>
      <a href="#playlist_setup">Playlist Setup</a> - Use to configure and setup a playlist.
    </li>
  </ul>
  
  <p class="Procedure mce-procedure">
    To view and customize the player’s different features
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and then select a player.
    </li>
    <li>
      Select the Look and Feel icon.
    </li>
    <li>
      Click on the feature to configure. <br /><img src="{{site.url}}/assets/3245">
    </li>
  </ol>
  
  <p class="mce-heading-3">
    <a name="tooltips"></a>Displaying/Hiding Tooltips
  </p>
  
  <p>
    Many of the player’s features include tooltips, a small pop-up window that appears when a user pauses the mouse pointer over an element, such as over a button
  </p>
  
  <p class="Procedure mce-procedure">
    To enable or disable tooltips
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Show tooltips to enable this option. Uncheck the box to disable the tooltips display.
    </li>
  </ol>
  
  <p class="mce-heading-3">
    <a name="title_label"></a>Title Label
  </p>
  
  <p>
    Use the Title label to set the location and text of the title label.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/1500">
  </p>
  
  <p class="mce-procedure">
    To set the title label
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Title label to enable this option.
    </li>
    <li>
      Select the alignment location from the drop down menu.
    </li>
    <li>
      Enter the Text for the label. The default is the mediaProxy entry name. (That is the original name you gave to the content when you uploaded it to the KMC.)
    </li>
    <li>
      Click Apply Changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <h3 class="mce-heading-3">
    <a name="logo"></a>Logo
  </h3>
  
  <p>
    Use the Logo label to set the custom logo plugin.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/1499">
  </p>
  
  <p class="Procedure mce-procedure">
    To set the logo
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Logo label to enable this option.
    </li>
    <li>
      Enter the Logo image URL.
    </li>
    <li>
      Enter the Logo link.
    </li>
    <li>
      Enter a Title.
    </li>
    <li>
      Click Preview changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <h3 class="mce-heading-3">
    <a name="laoding_spinner"></a>Loading Spinner
  </h3>
  
  <p>
    Use the Loading spinner options to customize the look of the loading spinner.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/1502">
  </p>
  
  <p class="Procedure mce-procedure">
    To configure the loading spinner
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Loading Spinner to enable this option.
    </li>
    <li>
      Enter the image URL.
    </li>
    <li>
      Enter the Logo link.
    </li>
    <li>
      Set the parameters.
    </li>
    <li>
      Click Preview changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <p class="mce-heading-3">
    <a name="volume_control"></a>Volume Control
  </p>
  
  <p>
    Use the Volume Control option to control the player volume using mute/unmute buttons and a volume slider.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/1505">
  </p>
  
  <p class="Procedure mce-procedure">
     To set the volume control
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Volume Control to enable this option.
    </li>
    <li>
      Check Show slider to display the column slider.
    </li>
    <li>
      Check Accessible controls to enable them.
    </li>
    <li>
      Select the accessible volume change value from the drop down.
    </li>
    <li>
      Click Preview changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <h3 class="mce-heading-3">
    <a name="closed_captions"></a>Closed Captions
  </h3>
  
  <p>
    Use the Closed Captions option to set up closed captions support and the caption display.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/3402">
  </p>
  
  <p class="Procedure mce-procedure">
    To configure the closed captions display on the player
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Closed Captions to enable this option.
    </li>
    <li>
      Select the layout (location on the video) from the drop down menu.
    </li>
    <li>
      Modify other closed captions’ options as required.
    </li>
    <li>
      Click Apply Changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <a href="#top"></a>
</div>

<div>
  <p class="Procedure mce-procedure">
    <a name="cvaa"></a>To enable the closed captions styling editor (CVAA Compliancy)
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Closed Captions to enable this option.
    </li>
    <li>
      Check the Enable Options Menu box to enable the captions styling menu.
    </li>
    <li>
      Click Preview Changes. The Options menu in the Closed Captions popup menu is displayed.<br /><img src="{{site.url}}/assets/3403">
    </li>
    <li>
      Click on Options to display the caption styling editor.<br /><img src="{{site.url}}/assets/3405">
    </li>
    <li>
      Select your caption display preferences using the scrolls and menus and click Save Settings.<br />The video player renders the captions with the configured settings.
    </li>
  </ol>
</div>

<div>
  <a href="#top">Back to top.</a><br /><p class="mce-heading-3">
    <a name="watermark"></a>Add or Modify the Watermark
  </p>
  
  <p>
    Use the Watermark option to set the watermark image and location of the watermark.
  </p>
  
  <p class="Procedure mce-procedure">
    To select the watermark and the display location
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Watermark to enable this option.
    </li>
    <li>
      Select the position of the watermark location from the drop down menu.
    </li>
    <li>
      Enter the watermark image URL.
    </li>
    <li>
      Enter the Click URL.
    </li>
    <li>
      Select the Padding CSS to determine the padding from the edge of the play screen. Enter the value in pixels. 
    </li>
    <li>
      Click Preview changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <p class="mce-heading-3">
    <a name="custom_styles"></a>Create and Modify Custom Styles
  </p>
  
  <p>
    Use the Custom Styles option to modify CSS styles.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/1532">
  </p>
  
  <p class="Procedure mce-procedure">
    To modify custom styles
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Custom Styles to enable this option.
    </li>
    <li>
      Modify the parameters.
    </li>
    <li>
      Click Preview changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <p class="mce-heading-3">
    <a name="info_screen"></a>Info Screen
  </p>
  
  <p>
    Use to add information screen about the video.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/1557">
  </p>
  
  <p class="Procedure mce-procedure">
    To modify the Info screen
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Info screen to enable this option.
    </li>
    <li>
      Modify the parameters.
    </li>
    <li>
      Click Preview changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <a href="#top">Back to top.</a><br /><h3 class="mce-heading-3">
    <a name="share"></a>Share and Embed
  </h3>
  
  <p>
    Use the Share and Embed feature to add the Share and Embed interface to the player and to share and embed a video in social websites and email.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/2166">
  </p>
  
  <p class="mce-heading-4">
    <a name="share_embed_config"></a>Share and Embed Configuration Fields
  </p>Use the fields to configure the Share and Embed interface to the player.
  
  <table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableHeading">
            Field
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableHeading">
            Description
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          Parent
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Parent container for component. Components include default placement, leave as null if unsure.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Align
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Alignment for component, can be left or right.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Order
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Draw order of the component within the container. Together with alignment, determines component placement of the component. Order is set with respect to siblings on the parent container.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Social Share URL
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Allows you to define the URL shared for this player:
          </p>
          
          <ul>
            <li>
              <strong>smart</strong> - maximizes inline social sharing playback, by using the page URL or Kaltura URL, and depend on whether opengraph tags are present on the page
            </li>
            <li>
              <strong>parent</strong> - shares the parent page URL.
            </li>
            <li>
              <strong>http://my-custom-domain.com/?v={mediaProxy.entry.id}</strong> - this is a custom URL with magic substitution that also be used.
            </li>
          </ul>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Social Networks
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Define included networks, separated by commas.Networks currently supported: facebook,twitter,googleplus,email,linkedin,sms
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Social Share Enabled
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Display Share link. True or False.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Embed Enabled
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Display Embed code.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Allow Time Offset
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Allow setting a time offset for the entry.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Allow Secured Embed
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Display secured embed option.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Email Enabled
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Display Email in the share options.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Share uiconf ID
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Specify a UIConf ID for the shared link. Leave empty to use the current UIConf.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Share Config
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Configuration options for all share networks. Use these fields to define each social network's icon, tooltips and  template.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="252">
          <p class="TableBodyText">
            Embed options
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="503">
          <p class="TableBodyText">
            Embed code configuration options.
          </p>
          
          <p class="TableBodyText">
            <strong>borderWidth</strong> - Enter the embed frame border wdth in pixels.
          </p>
          
          <p class="TableBodyText">
            <strong>height</strong> - Enter the video frame height
          </p>
          
          <p class="TableBodyText">
            <strong>streamerType</strong> - Select a Kaltura video delivery streaming type.
          </p>
          
          <p class="TableBodyText">
            <strong>uiconfID</strong> - Use to define a specific uiconf ID for the embedded video. Leave this field emplty to use the current player's uiconfID.
          </p>
          
          <p class="TableBodyText">
            <strong>width</strong> - Enter the video frame width.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p class="mce-procedure">
    To set the Share and Embed button
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select a player to edit or create a new one.
    </li>
    <li>
      Select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Share and Embed  feature to enable this option.
    </li>
    <li>
      Select the parent (where the Share and Embed button should be placed) from the drop down menu.
    </li>
    <li>
      Use the <a href="#share_embed_config">table</a> to configure the fields.
    </li>
    <li>
      Click Preview changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <p class="mce-heading-3">
    Using the Share Button
  </p>
  
  <p>
    After you configured the Share and Embed option in your player you can use the links provided in the player to embed your video.
  </p>
  
  <p class="Procedure mce-procedure">
    To use the embed links in the player:
  </p>
  
  <ol>
    <li>
      Click on the Share icon. The location of the icon depends on your configuration.<br />The following share and embed window is displayed on the player.<br /><img src="{{site.url}}/assets/2164">
    </li>
    <li>
      Click on the social media or email icon to open the relevant social media windows or email for sharing.<br /><img src="{{site.url}}/assets/2163">
    </li>
    <li>
      For additional embed code and JSON configuration information see the <a href="http://kgit.html5video.org/tags/v2.28/modules/KalturaSupport/components/share/ShareAPI.html">Share Plugin API</a>.
    </li>
  </ol>
  
  <a href="#top">Back to top.</a>
</div>

<div>
  <a href="#top"></a><span class="mce-heading-3"><a name="embed_ly"></a>Enable embed.ly embeds </span>
</div>

<div>
  Enable embed.ly sharing of the Kaltura player. <span>Enables embed.ly sharing of the Kaltura player. Embed.ly is generic embed service used by many web platfroms such as Linkedin, Salesforce and Yammer. You can lean more at </span><a href="http://embed.ly/" target="_blank">embed.ly</a>
</div>

<div>
  <br /><p class="mce-heading-3">
    <span style="font-size: 1.17em;"><a name="related"></a>Related Videos</span>
  </p>
  
  <p>
    Use this option to add the related videos screen at the end of the video to attract users to watch additional videos.
  </p>
  
  <p>
    <img src="{{site.url}}/assets/2355">
  </p>
  
  <p class="Procedure mce-procedure">
    To set the Related Videos screen
  </p>
  
  <ol>
    <li>
      Select the Universal Studio tab and select the Look and Feel icon.
    </li>
    <li>
      Check the box next to Related feature to enable this option.
    </li>
    <li>
      Select the parent (where the Related Videos button should be placed) from the drop down menu.
    </li>
    <li>
      Select the alignment location.
    </li>
    <li>
      Enter the Order where the icon should be displayed.
    </li>
    <li>
      Enter the Related Entries Source to select data the source for the related videos.<br />The options are:<ul>
        <li>
          Related to Entry – the server side determines which entries are related to the entry using the system logic. Entries related to the current entry are displayed. If there are no related entries, the plugin is disabled.
        </li>
        <li>
          Playlist ID – select from the dropdown for available playlists.
        </li>
        <li>
          Entries List – enter a comma delimited list of entries.
        </li>
      </ul>
    </li>
    
    <li>
      Enter the configuration settings.<br /><ul>
        <li>
          Click URL – Enter the URL to click on to get to the related items. If this field is left blank, clicking will replace the current video with a new one. For example:
        </li>
        <li>
          Auto continue time – Enter the number of seconds for auto play.
        </li>
        <li>
          Items limit – Enter the maximum number of items to show on the related screen.
        </li>
        <li>
          Display on playback done- display related screen automatically when playback is done.
        </li>
        <li>
          Auto continue enabled – should the next item automatically play.
        </li>
        <li>
          Store session – store the played entries across the page views in the related clips display.
        </li>
      </ul>
    </li>
    
    <li>
      Click Preview changes to preview your modifications.
    </li>
    <li>
      Click Save Player Settings.
    </li>
  </ol>
  
  <a href="#top">Back to top.</a>
</div>

<div>
   
</div>

<div class="mce-heading-3">
  <a name="dual_screen"></a>Dual Screen
</div>

The Kaltura Player is the front-end interface used to view captured videos and/or presentations. The Kaltura Player provides you with multiple interactive viewing options, such as Picture-in-Picture, Side-by-Side, and other displays. Select one of the display options from the drop down menu as your display preference.

[][8]<span class="mce-heading-3"><a name="playlist_setup"></a>Playlist Setup</span>

 [8]: #top

Use the Playlist setup options to configure the playlist’s settings and configure the playlist controls. You can set a playlist [Preview id][9] in the Basic Settings.

 [9]: #preview_playlist

### Playlist Configuration

The Kaltura playlist plugin supports associating multiple clips in sequence.  
<img src="{{site.url}}/assets/1993">

<p class="mce-procedure">
  To configure the playlist’s settings
</p>

1.  Select the Universal Studio tab and select the Look and Feel icon.
2.  Check the box next to the Playlist Configuration feature to enable this option.
3.  Select the position where the playlist should display. The options are to the right, left, above or beneath the video.
4.  Select the layout, vertical or horizontal.
5.  Enable the playlist features by checking the relevant boxes.
6.  Check On (Publisher's) Page to display the playlist on the publisher's page. If unchecked, the playlist is displayed on the player's iFrame. (Recommended)
7.  Enter the minimum amount of clips of display. The number represents the minimum number of clips to show in the playlist without scrolling. If the playlist has fewer entries than the specified Min Clips value, all the clips in the playlist are displayed. If the MinClips value specified prevents optimal viewing, (may cover the video or shrink the player display) - the Min clips value for display are determined to provide optimal video viewing.
8.  Enter the initial entry ID that should be played first. In the Init item entry id.

<p class="mce-procedure">
  To add additional playlists
</p>

1.  Enter the Playlist Name and the Playlist ID.
2.  Click Add.

[Back to top.][8]

<p class="mce-heading-3">
  Playlist Controls
</p>

Use to configure the Next and Previous buttons on the playlist.

<p class="mce-procedure">
  To configure the playlist’s controls
</p>

1.  Select the Universal Studio tab and select the Look and Feel icon.
2.  Check the box next to the Playlist Controls feature to enable this option.
3.  Select where you want to display the Next and Previous buttons. The choice are the Top bar container or the Controls container. Leave this field empty if you are uncertain where you want these buttons displayed.

[Back to top.][8]

# <span class="mce-heading-2"><a name="configuring_analytics"></a>Configuring the Player’s Analytics</span>

Kaltura supports robust analytics via the Kaltura platform as well as via 3rd party analytics providers.

The following Analytics options are supported:

*   [Akamai Media Analytics][10] - Supports sending player analytics events to Akamai.
*   [Google Analytics ][11]- Supports sending player analytics events to Google.  
    For full implementation guide see <a href="http://knowledge.kaltura.com/google-analytics-kaltura-player" target="_new">Google Analytics</a> in the Knowledge Center.
*   [comScore][12] -  Supports sending player analytics events to comScore
*   [Nielsen Combined ][13]- Supports sending player analytics events to Nielsen Combined
*   [Omniture on page ][14]- The Omniture s\_code config version of the plugin allows you to connect the Omniture plugin to your existing s\_code.js configuration for easy integration of video analytics into an Omniture site.
*   [Kaltura Analytics/Statistics][15]  - Use Kaltura analytics to <a href="http://knowledge.kaltura.com/creating-and-tracking-analytics-kmc-0" target="_blank">track Kaltura player events.</a> Statistics are enabled by default. Configuration consists of adding additional tracking info.
*   [Youbora Analytics][16] - The Youbora plugin listens and reports all the different player states in the current video session to Youbora Analytics.

 [10]: #akamai
 [11]: #google
 [12]: #comscore
 [13]: #Nielsen_combined
 [14]: #omniture
 [15]: #kaltura_analytics
 [16]: #youbora

<p class="mce-procedure">
  To configure the player analytics settings
</p>

1.  Select the Universal Studio tab and then select or create a player.
2.  Select the Analytics icon.
3.  Check the Analytics option you want to configure.
4.  Enter the relevant parameters for the chosen option.
5.  Click Save Player Options.

<h2 class="mce-heading-3">
  <a name="akamai"></a>Akamai Media Analytics
</h2>

Akamai Media Analytics are designed to provide consistent and accurate data about the playback and quality your audience is experiencing on any device.

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <strong>Field</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <strong>Attribute</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <strong>Value</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <strong>Description</strong>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Configuration XML path
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        configPath
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        http://ma193-r.analytics.edgesuite.net/config/beacon-3431.xml
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        URL for Akamai's configuration XML.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Media Analytics SWF path
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        swfPath
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        http://79423.analytics.edgesuite.net/csma/plugin/csma.swf
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        URL for Akamai Media Analytics SWF.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Track event monitor
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        trackEventMonitor
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        trackAkamaiAnalyticsEvent
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Track Akamai media analytics events with a named callback.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Player id
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        playerId
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <em>null</em>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Override the default value for the playerId field, By default it is the uiconf_id.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Title
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        title
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <em>null</em>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Override the default value for the title field. By default it is the entry title.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Category
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        category
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <em>null</em>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Override the default value for the category field, By default it is the media type. For example, image, video, audio.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Sub Category
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        subCategory
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <em>null</em>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Override the default value for the subCategory field. The default value is null. This field can be used for additional segmentation.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Event Name
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        eventName
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <em>null</em>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Override the default value for the eventName field, custom set by event
      </td>
    </tr>
  </tbody>
</table>

[Back to top.][8]

<h2 class="mce-heading-3">
  <a name="googleanalytics"></a>Google Analytics
</h2>

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="141">
        <strong>Field</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="143">
        <strong>Attribute</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <strong>Value</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <strong>Description</strong>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="141">
        Google urchin code
      </td>
      
      <td style="text-align: left;" valign="top" width="143">
        urchinCode
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The Google urchin code i.e. UA-30149691-1
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="141">
        Event monitor function name
      </td>
      
      <td style="text-align: left;" valign="top" width="143">
        customEvent
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        doPlay
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Function called on parent page for every event.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="141">
        Custom events list
      </td>
      
      <td style="text-align: left;" valign="top" width="143">
        doPlayCategory
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        My Custom event
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Comma separated list of events you want to track.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="141">
        Category for event
      </td>
      
      <td style="text-align: left;" valign="top" width="143">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Category sent to Google Analytics for prefixed event.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="141">
        Action for event
      </td>
      
      <td style="text-align: left;" valign="top" width="143">
        doPlayAction
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        player is playing
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Action sent to Google Analytics for prefixed event.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="141">
        Value for event
      </td>
      
      <td style="text-align: left;" valign="top" width="143">
        doPlayValue
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        1
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Value sent to Google Analytics for prefixed event
      </td>
    </tr>
  </tbody>
</table>

[Back to top.][8]

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><a name="comscore"></a>comScore</span>

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <strong>Field</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <strong>Description</strong>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        comScore XML tag mapping file path
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        URL to a ComScore XML tag mapping file.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Event function name
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Function called on parent page for every event.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Content party
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Party that delivered the content
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Content owner
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Owner of the content - Content producer<a href="file:///C:/Users/debbie.zioni/Documents/KMC/IX/Studiov2/Universal_Studio_Configuration_Guide-dzMarch23.docx#_msocom_4"><br /></a>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Content owner attribute key
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Mapping the attribute key for content owner
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Content owner value key
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Value key for content owner
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Content view site
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Location/site where content was viewed
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Site mapping attribute key
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Mapping the attribute key for site/locationit
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Site value key
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Value key for site location
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Content type
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Genre and type of content
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Type attribute key
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Mapping the attribute key for genre and type
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Site value key
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Value key for site location<a href="file:///C:/Users/debbie.zioni/Documents/KMC/IX/Studiov2/Universal_Studio_Configuration_Guide-dzMarch23.docx#_msocom_5"><br /></a>
      </td>
    </tr>
  </tbody>
</table>

[Back to top.][8]

 <a name="Nielsen_combined"></a><span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Nielsen Combined</span>

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <strong>Field</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        <strong>Attribute</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <strong>Sample Value</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <strong>Description</strong>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Client ID
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        clientId
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        us-502202
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The client ID.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Video IS
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        vcid
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        c15
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The video ID.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Title tag
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        tag_title
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        {mediaProxy.entry.name}
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The title tag.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Category Tag
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        tag_category
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        {mediaProxy.entry.categories}
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The category tag.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Sub-category tag
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        tag_subcategory
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        {mediaProxy.entryMetadata.subcategories}
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The subcategory tag.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Census Category tag
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        tag_censuscategory
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        {mediaProxy.entry.censuscategories}
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The census category tag.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Thumbnail URL tag
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        tag_imgurl
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        {mediaProxy.entry.thumbnailUrl}
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The thumbnail URL tag.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Event Function name
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        trackEventMonitor
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        trackEvent
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Function called on parent page for every event.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        clientId
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        us-502202
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The client ID.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        vcid
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        c15
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The video ID.
      </td>
    </tr>
  </tbody>
</table>

[Back to top.][8]

 <a name="omniture"></a><span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Omniture on Page</span>

The Omniture s\_code config version of the plugin allows you to connect the Omniture plugin to your existing s\_code.js configuration for easy integration of video analytics into an Omniture site.

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <strong>Field</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        <strong>Value</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <strong>Description</strong>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Code URL
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The URL to the Ominture generated sCode file. If null, a local copy of s_code.js is used. Must be set in uiConf not via flashvar
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Entry code name
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        . “s’ by default.
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <span>The name of the s_code entry point in the global window scope. ("s" by default ).</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Monitor event tracking interval
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <span>Set to an interval (in seconds) for tracking the Omniture 'monitor' event.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Omniture events function name
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        A global callback function for logging Omniture events.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Media name concatentation rules
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        Default should be left null.
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <span>A per partner key for special media name concatenation rules. By default this parameter should be left null.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Kaltura player events
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        A comma separated list of Kaltura events you want to track.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Omniture variables and properties
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        A<span> comma separated list of Omniture evars and props, you wish to pass along with every media event.</span>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Kaltura <span>values</span>
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        A comma separated list of Kaltura values to pass along with every media event. <span>Values will correspond to the evars and props comma separated map defined in the "Omniture variables and properties" field.</span>
      </td>
    </tr>
  </tbody>
</table>

<h2 class="mce-heading-3">
  <a name="kaltura_analytics"></a>Kaltura Analytics - Statistics
</h2>

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Field
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        Attribute
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        Value
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Description
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Track Event Monitor
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        trackEventMonitor
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        kalturaSendAnalyticEvent
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Enables you to audit Kaltura events with a named callback function.
      </td>
    </tr>
  </tbody>
</table>

 [Back to top.][8]

<h2 class="mce-heading-3">
  <a name="youbora"></a>Youbora Analytics
</h2>

Youbora Real Time Analytics & Monitoring uses a plugin on every player on every device of every user to track and monitor all information relevant to every view (real time for VoD and live video).

For additional information on Youbora Analytics see the <a href="{{site.url}}/documentation/Knowledge/youbora-player-plugin-setup-and-information-guide.html" target="_blank">Youbora Player Plugin Setup and Information Guide</a> on the Knowledge Center.

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Field
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        Attribute
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        Value
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Description
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        userId
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        string
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
         
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The Youbora user ID of the current user.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        bufferUnderrunThreshold
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        number
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        The default is 1000.
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The minimum buffering time (in milliseconds) required to trigger the buffer under-run beacon.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Track Event Monitor
      </td>
      
      <td style="text-align: left;" valign="top" width="135">
        trackEventMonitor
      </td>
      
      <td style="text-align: left;" valign="top" width="210">
        kalturaSendAnalyticEvent
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Enables you to audit Kaltura events with a named callback function.
      </td>
    </tr>
  </tbody>
</table>

 [Back to top.][8]

[][8]<span class="mce-heading-2" style="font-size: 2em;"><a name="monetizationsection"></a>Monetization - Configuring the Player Advertising Settings</span>

The Kaltura platform supports VAST 3.0 as well as 3rd party ad plugins to facilitate content monetization.

The following monetization options are available:

*   [Bumper][17]
*   [VAST][18]
*   [DoubleClick][19]
*   [FreeWheel][20]
*   [Skip Button][21]
*   [Skip Notice][22]
*   [Notice Message][23]

 [17]: #bumpers
 [18]: #vast
 [19]: #doubleclick
 [20]: #Freewheel
 [21]: #skip_button
 [22]: #skip_notice
 [23]: #notice_message

<p class="mce-procedure">
   To configure the player advertising settings
</p>

1.  Select the Universal Studio tab and then select or create a player.
2.  Select the Monetization icon.
3.  Configure the VAST 3.0 or third party plugin advertising settings.
4.  Save your changes.

## <a name="bumpers"></a><span style="color: #828a8c; font-size: 14pt;">Bumpers</span>

Bumpers are videos that act as ads and do not use an ad server. Bumper videos uploaded to Kaltura can be inserted before or after a video, to function as pre-rolls or post-rolls. Bumper videos are associated with a player, and not associated with a specific video. Bumper videos are independent of actual pre/post-rolls and can be played in addition to ads. Bumper videos are helpful for Kaltura partners that would like to advertise their logo, or other information, before or after a video, and for smaller partners that would like to advertise, but do not need advanced tracking tools that ad servers provide.

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <strong>Field</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <strong>Description</strong>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Bumper Entry Id
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The Entry Id of the bumper to be played.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Click URL
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The URL to open when the user clicks the bumper video
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Pre Sequence index
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The pre-seqeunce number for sequencing the bumper before or after ads before content. For example can be set to 0 and set an add pre-sequence index to 1, to have the bumper play then the ad.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Post Sequence index
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The post-sequence number for sequencing the bumper after the content.
      </td>
    </tr>
  </tbody>
</table>

## <a name="vast"></a><span style="color: #828a8c; font-size: 14pt;">VAST</span>

VAST, (Video Ad Serving Template), includes a standard XML-based ad response for in-stream video as well as an XML Schema Definition (“XSD”) for developers. It is meant to accommodate the majority of current practices within the online digital video advertising business. 

(<a href="http://www.iab.net/iab_products_and_industry_services/508676/compliance/679253" target="_blank">http://www.iab.net/iab_products_and_industry_services/508676/compliance/679253</a> )

<h3 class="mce-heading-4">
  VAST Support
</h3>

Here is a list of some of the largest video ad servers/networks that are VAST-compliant: 

<a href="http://www.iab.net/iab_products_and_industry_services/508676/compliance/679253" target="_blank">http://www.iab.net/iab_products_and_industry_services/508676/compliance/679253</a> .

<h3 class="mce-heading-4">
  VPAID Support
</h3>

Kaltura’s plugin for *VAST* supports VPAID ads.

<h3 class="mce-heading-4">
  VAST Configuration Parameters
</h3>

Kaltura player features robust VAST support for prerolls, midrolls, overlays, companions and postrolls.  
<img src="{{site.url}}/assets/1663">

 

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          <strong>Field</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Skip button label
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          Skip button label, for example “Skip Ad”
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Skip offset
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The time in seconds before the skip ad link is activated.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Track cue points
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          Check if entry cue points should be tracked
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Allow seek with native controls
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          Allow to catch seek requests during ad  and return the player to the original play time.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Store session
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          If the frequency playback should be stored across player reloads. By default, only playlists repect frequency intervals. If set to true, the preroll interval is repected across player views.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Preroll URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The VAST ad tag XML URL for the preroll ad. For midroll ad requests.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Preroll JS URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The VAST tag URL used where platform does not support Flash. If undefined, all platforms use the base preroll URL for ad requests.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" colspan="2" valign="top" width="651">
        <p>
          <strong>Preroll tab</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Preroll(s) amount
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The number of prerolls to be played.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Number of prerolls to start with
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          How many prerolls to start with
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Preroll interval
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          How often to show prerolls
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          VAST pre-sequence index
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          Allows for sequencing the vast ad within the pre-sequence. 1 for ads then 2 for a bumper plugin, would result in an ad and then a bumper
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" colspan="2" valign="top" width="651">
        <p>
          <strong>Overlay tab</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Overlay start time
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          Start time in seconds for overlay
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Overlay interval
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          How often should the overlay be displayed
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Overlay URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The VAST xml overlay ad xml.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Timeout
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The time out in seconds, for displaying an overlay VAST ad.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" colspan="2" valign="top" width="651">
        <p>
          <strong>Postroll tab</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Postroll URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The VAST ad tag XML URL for the postroll ad.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Postroll JS URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The VAST tag URL used where platform does not support Flash. If undefined, all platforms use the base postroll URL for ad requests.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Postroll(s) amount
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          The number of postrolls to be played.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Number of postrolls to start with
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          How many posttolls to start with
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          Postroll interval
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          How often to show postrolls
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          VAST post-sequence index
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          Allows for sequencing the vast ad within the post-sequence
        </p>
      </td>
    </tr>
  </tbody>
</table>

<h2 class="mce-heading-3">
  <span style="font-size: 14pt;"><a name="dfp"></a>DoubleCli</span><a name="doubleclick" style="color: #000000; font-size: 10px; background-color: #ffffff;"></a><span style="font-size: 14pt;">ck</span>
</h2>

DoubleClick for Publishers (DFP) Video provides publishers with a platform to increase revenue from video advertising as well as manage costs. Fully integrated with DFP, publishers can manage their entire display advertising through one platform, with video at its core. Learn more about [DFP video solutions][24].

 [24]: http://www.google.com/doubleclick/publishers/solutions/video.html

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p>
          <strong>Field</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Pause ad on clicked
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          When checked, the ad pauses when the user clicks on it.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Lead with Flash
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          Check if the Flash based DFP runtime should be used where Flash is available.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Content Id
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          The contentId, used by DoubleClick plugin API, generally the entry ID, but can also be custom metadata mapping
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Custom params
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          Custom parameters passed to the DoubleClick adTag URL. Should be listed as URL parameters key=value&key2=value2 pairs.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          CMS id
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          Appended to the VAST URL, used by the DoubleClick plugin API
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          HTML Companions
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          Companions list. For each companion, please specify the ad container div ID and the expected ad width and height. Use the add link to open new DivID fields.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          <strong>DFP Trafficking tab</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          DFP Trafficking – uses the Google DFP ad server. If you use this platform the DFP ad Tag is created
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Ad tag URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          The DoubleClick DFP VAST ad tag URL (can include multiple nested VAST URLs) (see <a href="{{site.url}}/documentation/Knowledge/integrating-kaltura-vast-adtag-url.html">Integrating Kaltura with a VAST adTag URL</a> Enter the ad Tag URL in this field.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          <strong>VAST Trafficking tab</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          VAST Trafficking – uses regular VAST ad tags. You can specify your ad tags as a pre roll or post roll.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Track cue points
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          Searches for cue points at the entry level. If you define a VAST cue point in your entry, it is triggered when this check box is checked.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Preroll URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          The pre-roll VAST ad Tag XML URL.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Postroll URL
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          The post-roll VAST ad Tag XMLURL.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <p class="TableBodyText">
          Timeout
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <p class="TableBodyText">
          The timeout in seconds for displaying an overlay VAST ad. The timeout is used for over lays. If you are using an overlay VAST tag, the ad will displayed as an overlay (on top) of the video. The timeout value entered represents the number of seconds the overlay VAST ad is displayed after which the ad will automatically be removed.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<a name="Freewheel" style="color: #828a8c; font-size: 14pt; font-weight: bold; background-color: #ffffff;"></a><span style="color: #828a8c; font-size: 14pt; font-weight: bold;">FreeWheel</span>

FreeWheel gives enterprise-level media companies the infrastructure they need to create scaled, profitable content businesses in the new media landscape. Learn more about [FreeWheel offerings][25]. Kaltura supports a full featured FreeWheel ad network integration for both HTML5 and Flash players.

 [25]: http://www.freewheel.tv/

<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        <strong>Field</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        <strong>Description</strong>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Ad manager SWF URL
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The FreeWheel ad manager SWF URL.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Ad manager JavaScript URL
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The FreeWheel ad manager JavaScript URL. Must be set in uiConf not via flashvar.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Ad server URL
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The FreeWheel ad server
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Network Id
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The network ID property, for retrieving FreeWheel ads
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Player Profile ID
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The player profile ID for Flash, for identifying the Flash player.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Player HTML5 Profile Id
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The player profile ID for HTML5, for identifying the HTML5 player
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Site section Id
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        The site section ID used to segment ad retrieval per site section.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Use Kaltura Cue Points
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        If Kaltura cuePoints should be used for ad opportunities.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Video asset Id
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Asset ID, for FreeWheel ad targeting.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="148">
        Video asset fallback Id
      </td>
      
      <td style="text-align: left;" valign="top" width="293">
        Fallback asset ID, if the initial asset does not have targeting info.
      </td>
    </tr>
  </tbody>
</table>

<a name="skip_button"></a><span class="mce-heading-2 mce-heading-3">Skip Button</span>

<table style="width: 651px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="148">
        <p>
          <strong>Field</strong>
        </p>
      </td>
      
      <td valign="top" width="210">
        <p>
          <strong>Value</strong>
        </p>
      </td>
      
      <td valign="top" width="293">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="148">
        <p>
          Skip button label
        </p>
      </td>
      
      <td valign="top" width="210">
        <p>
           
        </p>
      </td>
      
      <td valign="top" width="293">
        <p>
          Skip button label, for example “Skip Ad”.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="148">
        <p>
          Skip offset
        </p>
      </td>
      
      <td valign="top" width="210">
        <p>
           
        </p>
      </td>
      
      <td valign="top" width="293">
        <p>
          The time in seconds before the skip ad link is activated.
        </p>
      </td>
    </tr>
  </tbody>
</table>

<h2 class="mce-heading-2">
  <a name="skip_notice"></a><span class="mce-heading-3">Skip Notice</span>
</h2>

<table style="width: 651px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="148">
        <p>
          <strong>Field</strong>
        </p>
      </td>
      
      <td valign="top" width="210">
        <p>
          <strong>Value</strong>
        </p>
      </td>
      
      <td valign="top" width="293">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="148">
        <p>
          Skip notice text
        </p>
      </td>
      
      <td valign="top" width="210">
        <p>
           
        </p>
      </td>
      
      <td valign="top" width="293">
        <p>
          Skip notice text
        </p>
      </td>
    </tr>
  </tbody>
</table>

 

<h2 class="mce-heading-2">
  <a name="notice_message"></a><br /><span class="mce-heading-3">Notice Message</span>
</h2>

<table style="width: 651px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="148">
        <p>
          <strong>Field</strong>
        </p>
      </td>
      
      <td valign="top" width="210">
        <p>
          <strong>Value</strong>
        </p>
      </td>
      
      <td valign="top" width="293">
        <p>
          <strong>Description</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="148">
        <p>
          Skip notice text
        </p>
      </td>
      
      <td valign="top" width="210">
        <p>
           
        </p>
      </td>
      
      <td valign="top" width="293">
        <p>
          Skip notice text (can use evaluated expressions)
        </p>
      </td>
    </tr>
  </tbody>
</table>

 

[Back to top.][8]

<span style="color: #484848; font-size: 18pt; font-weight: bold;"><a name="plugins"></a>Plugins</span>

Use the Plugins tab to configure additional plugins.

The following plugins are available:

*   [Keyboard Shortcuts][26] - Use to control the player using keyboard shortcuts
*   [Moderation][27] - Allow your users to flag content as inappropriate.
*   [Playback Rate Selector][28] - <span>Enables users to select the video playback rate.</span>
*   [Restrict User Agent][29] - <span>Allows you to block the player to specific user agents.</span>
*   [Universal DRM][30] - Kaltura Universal DRM enables multiple DRM engines to run within the Kaltura player based on the capabilities of the browser or packaged native applications.
*   [Source Selector][31] - <span>Enables users to select the video quality.</span>
*   [Audio Selector][32] - Enbales users to select multiple audio tracks.
*   [Download][33] - Enables users to add a download button to the player controls. The download button enables users to download the media to a local file.
*   [Strings][34] - Use to over write player strings.
*   [UI Variables][35] - Allows you to add UI variables to the player configuration.

 [26]: #keyboard_shortcuts
 [27]: file:///C:/Users/debbie.zioni/Documents/KMC/Iris/Studiov2/Universal_Studio_Configuration_Guide_v2_update.docx#_Moderation_1
 [28]: #playback_rate_selector
 [29]: #restrict
 [30]: #universal_drm
 [31]: #source_selector
 [32]: #audio_selector
 [33]: #download
 [34]: #strings
 [35]: #uivars

<h3 class="mce-heading-3">
  <a name="keyboard_shortcuts"></a><a name="keyboard_shortcuts"></a>Keyboard Shortcuts
</h3>

Use the Keyboard Shortcuts option to control the player using keyboard shortcuts. See JavaScript <a href="https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent" target="_new">key mappings</a> for more information. 

<img src="{{site.url}}/assets/1458">

<p class="mce-procedure">
   To set keyboard shortcuts
</p>

1.  Select the Universal Studio tab and select the Look and Feel icon.
2.  Check the box next to Keyboard Shortcuts to enable this option.
3.  Enter values for the following parameters:  
     <table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Name
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            <strong>Description</strong>
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            <strong>Values</strong>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Volume Precent Change
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            Controls the interval of Volume Change
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            0-1, .2 for example defines 5 steps of keyboard volume control
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Short Seek Time
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            In seconds
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Long Seek Time
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            In seconds
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Volume Up Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Volume Down Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Toggle Playback Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Short Seek Back Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Long Seek Back Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Short Seek Forward Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Long Seek Forward key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Open Full Screen Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Close Full Screen Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Go to beginning Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            Seeks to the start of the content.
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Go To End Key
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            Seeks to the end of the stream.
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Percentage Seek Keys
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            Comma delimited list of keys used to seek to fixed percentages in the stream.
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
      </tbody>
    </table>

4.  Click Apply Changes to preview your modifications.
5.  Click Save Player Settings.

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><a name="moderation"></a>Moderation</span>

Use the Moderation option to allow users to moderate content and flag content as inappropriate.

<img src="{{site.url}}/assets/1469">

<p class="mce-procedure">
  To set the Moderation options
</p>

1.  Select the Universal Studio tab and select the Look and Feel icon.
2.  Check the box next to Moderation to enable this option.
3.  Enter the following parameters:<table style="width: 630px;" border="1" cellspacing="0" cellpadding="0">
      <thead>
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            <strong>Name</strong>
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
            <strong>Description</strong>
          </td>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Header
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Text
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Tooltip
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Reason:Sexual Content
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            ReasonL Violent Content
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Reason: Harmful Content
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="248">
            Reason: Spam
          </td>
          
          <td style="text-align: left;" valign="top" width="208">
             
          </td>
        </tr>
      </tbody>
    </table>

4.  Click Apply Changes to preview your modifications.
5.  Click Save Player Settings.

<h2 class="mce-heading-3">
  <a name="playback_rate_selector"></a>Playback Rate Selector
</h2>

<p class="mce-procedure">
  To select the video playback rate
</p>

1.  Select the Universal Studio tab and select the Plugins icon.
2.  Check the box next to the option and enter the default speed for the player.
3.  Enter the set of selectable speeds separated by commas, where 1 = 100% speed.

### <a name="restrict"></a><span style="color: #828a8c; font-size: 14pt;">Restrict User Agent</span>

Use to block the player to specific user agents. Use these settings for the player display only. For general purpose access controls, see <a href="{{site.url}}/documentation/Knowledge/how-assign-access-control-profile-entry.html" target="_blank">entry level access controls</a>.   

<p class="mce-procedure">
  To restrict the User Agent
</p>

1.  Select the Universal Studio tab and select the Plugins icon.
2.  Check the box next to the option.
3.  Enter the Restricted user agents. Enter a comma-separated list of browsers to search for.
4.  Enter the Restricted user agent title (error title).
5.  Enter the Restricted user agent message (error message). 

<p class="mce-heading-3">
  <a name="universal_drm"></a>Universal DRM
</p>

Kaltura Universal DRM enables multiple DRM engines to run within the Kaltura player based on the capabilities of the browser or packaged native application.

<p class="mce-procedure">
  To configure Universal DRM
</p>

1.  Contact your Kaltura representative to request Universal modular DRM to be activated for your account.
2.  Enable Universal DRM on your player.
<ol style="list-style-type: lower-alpha;">
  <li>
    Select the Universal Studio tab and select the Plugins icon,
  </li>
  <li>
    Check the box next to Universal DRM.
  </li>
  <li>
    Click Save Player Settings.
  </li>
</ol>

3.  Enable the DRM access control profile for entries you would like protected. See [How to enable the DRM access control profile for entries you would like protected][36]. 

 [36]: http://knowledge.kaltura.com/node/1481

<p class="mce-heading-3">
  <a name="source_selector"></a>Source Selector
</p>

Use to select the video quality.

<img src="{{site.url}}/assets/3358">

 

<table style="width: 663px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="248">
        <p class="TableHeading">
          Name
        </p>
      </td>
      
      <td valign="top" width="208">
        <p class="TableHeading">
          Description
        </p>
      </td>
      
      <td valign="top" width="208">
        <p class="TableHeading">
          Values
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="248">
        Switch on resize
      </td>
      
      <td style="text-align: left;" valign="top" width="208">
        When the player changes size or goes into full screen the source will update per playback resolution. By default, the embed size is only taken into consideration at startup.
      </td>
      
      <td style="text-align: left;" valign="top" width="208">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="248">
        Simple format
      </td>
      
      <td style="text-align: left;" valign="top" width="208">
        Use this format to restrict to two sources only per name size and not list content type.
      </td>
      
      <td style="text-align: left;" valign="top" width="208">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="248">
        Display Mode
      </td>
      
      <td style="text-align: left;" valign="top" width="208">
        Set the type of information to display in the source selector’s menu.
      </td>
      
      <td style="text-align: left;" valign="top" width="208">
         Size, Biit-rate, Size and Bit-rate.
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-procedure">
  To configure the Source Selector
</p>

1.  Select the Universal Studio tab and select the Plugins icon.
2.  Check the box next to Source Selector.
3.  Set the parameters.
4.  Click Preview changes to preview your modifications.
5.  Click Save Player Settings.

<p class="mce-heading-3">
  <span><a name="audio_selector"></a>Audio Selector</span>
</p>

Use to enable multiple audio tracks<span>.</span>

<img src="{{site.url}}/assets/3357">

<p class="mce-procedure">
  To configure the Audio Selector
</p>

1.  Select the Universal Studio tab and select the Plugins icon.
2.  Check the box next to Audio Selector.
3.  Click Save Player Settings.

<p class="mce-heading-3">
  <a name="download"></a>Download
</p>

Use to add a download button to the player controls. The download button enables users to download the media to a local file.

 <img src="{{site.url}}/assets/1661">

<p class="mce-procedure">
  To add the Download button
</p>

1.  Select the Universal Studio tab and select the Plugins icon.
2.  Check the box next to Download.
3.  Check Plugin to enable the Download plugin.
4.  Configure the parent container for the component.
5.  Configure the alignment.
6.  Set the order.
7.  Enter the Flavor ID for the downloaded movie source. When specified this flavour overrides any preferred bitrate settings.
8.  Set the Preferred bitrate. Leave empty for the highest bitrate. Set to zero for the original movie source file.
9.  Click Preview changes to preview your modifications.
10. Click Save Player Settings.

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"></span><span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><a name="strings"></a>Strings</span>

Use this option to over write player strings. For full string keys listing, review the [Strings documentation page][37].

 [37]: http://player.kaltura.com/docs/Strings

<p class="mce-heading-3">
  <a name="uivars"></a>UI Variables
</p>

Use to add UI variables to the player configuration.

 <img src="{{site.url}}/assets/1560">

To simplify the management of many of the player features, Kaltura has implemented the “*UIVars*” to override and configure player features.

Kaltura *UIVars* are an incredibly powerful feature of the Kaltura Players which allow publishers to pre-set or override the value of any FlashVar (object level parameters), show, hide and disable existing UI element, add new plugins and UI elements to an existing player, and modify attributes of all the player's elements.

The most updated list of UIVars is [here][38].

 [38]: http://player.kaltura.com/docs/api#uiVars

[Back to Top][8]

<p class="mce-heading-3">
  Create New Plugin
</p>

This option allows you to create a custom plugin configuration. For more information, contact <a href="mailto:customercare@kaltura.com" target="_blank">Kaltura Customer Care</a>.

<h2 class="mce-heading-3">
  Import Plugin
</h2>

This option allows you to import a Kaltura player plugin using a one line string. For more information, contact <a href="mailto:customercare@kaltura.com" target="_blank">Kaltura Customer Care</a>.

[Back to Top][8]