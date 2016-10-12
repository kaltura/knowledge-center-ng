---
layout: page
title: "Embedding Kaltura Media Players in Your Site"
date: 2011-12-29 09:46:36
---

<p class="mce-heading-2">
  Understanding Kaltura Media Players
</p>

<p class="mce-heading-3">
  Kaltura's Media Players
</p>

Kaltura’s flexible HTML5- and Flash-based media players provide media online publishing solutions that are easy to use and embed. Kaltura offers:

*   <a href="http://html5video.org/wiki/Kaltura_HTML5_Video_Player" target="_blank">Kaltura HTML5 Video Library </a>– provides seamless cross-platform video playback.

*   [Kaltura Dynamic Player version 3 (KDP3) ][1]– an Adobe OSMF (Flash/ActionScript 3)-based, highly flexible media player.

 [1]: http://www.kaltura.org/demos/kdp3/docs.html

To learn more about Kaltura media player features, refer to <a href="/introduction-kalturas-cross-platform-media-players" target="_blank">Introduction to Kaltura's Cross-Platform Media Players</a>.

<p class="mce-heading-3">
  In this article you will learn:
</p>

*   [How to embed the Kaltura Player][2].

*   [Kaltura embed options][3]: [AutoEmbed][4], [Dynamic Embed][5], [ThumbEmbed][6], [Legacy Embed][7].

*   Learn about Runtime Embedding options 

*   KDP3. See [Embedding the KDP3 Player Using Static HTML][2] and [Dynamically Embedding the KDP3 Player Using JavaScript.][5]

 [2]: #EmbeddingPlayerUsingStaticHTML
 [3]: #kaltura_embed_options
 [4]: #AutoEmbed
 [5]: #DynamicEmbed
 [6]: #ThumbEmbed
 [7]: #LegacyEmbed

<p class="mce-heading-2">
  <a name="EmbeddingPlayerUsingStaticHTML"></a>How to embed the Kaltura Player
</p>

<p class="mce-heading-4">
  <a name="embed-kmc"></a>Embedding a Player for a Single Video
</p>

<p class="mce-procedure">
  To use embed code from the Kaltura Management Console (KMC) for a single video:
</p>

1.  Open the KMC and go to <a href="http://www.kaltura.com/index.php/kmc/kmc4#content%7Cmanage" target="_blank">Content>Manage</a>.
2.  In the Entries Table, click **Preview & Embed** in the Publish column of the video that you want to embed.  
    <img src="../../assets/206">
3.  (Optional) In the Embedding window, select a specific player from the **Select Player** menu.  
      
    <img src="../../assets/1573">
      
    
4.  In the Embedding window, click **Copy** to copy the embed code from the Embed Code field. 
5.  In your web page, paste the code to embed the player with the video.

<p class="mce-heading-3">
  <a name="kaltura_embed_options"></a>Kaltura Embed Options
</p>

By default the embed codes support both Flash and HTML5 players. The Embed Code type includes several options Auto Embed, Dynamic Embed, Legacy Flash Embed, Iframe Embed. You may want to use diffrent embed code types in diffrent situations. Here is a summary of the types. 

<p class="mce-note-graphic">
  Note: Substitute {PARTNER_ID} for your Kaltura partner id, {UICONF_ID} for an actual player id, also known as the uiconf id and {entryId} for an actual entry id. See the full list of <a href="http://knowledge.kaltura.com/node/219#ParamsSettings">params here</a>
</p>

<p class="mce-heading-4">
  <span><a name="AutoEmbed"></a>Auto Embed</span>
</p>

<span>This is the default recommended embed code for the Kaltura Player. <span>Auto embed </span><span>is concise </span><span>code</span><span> and</span><span> is good for quickly getting a player or widget onto the page without any runtime customizations. Auto embed has been heavily optimized for packing lots of resources into the initial request, allowing the player to be rendered quickly. </span></span>

<pre class="brush: xml;light: true; fontsize: 100; first-line: 1; ">&lt;script type="text/javascript" src="http://cdnapi.kaltura.com/p/{PARTNER_ID}/sp/{PARTNER_ID}00/embedIframeJs/uiconf_id/{UICONF_ID}/partner_id/{PARTNER_ID}?entry_id={ENTRY_ID}&playerId={UNIQUE_OBJ_ID}&cache_st=1362074486&autoembed=true&width=400&height=333&"&gt;&lt;/script&gt;</pre>

<p class="mce-heading-4">
  <span><span><a name="DynamicEmbed"></a>Dynamic Embed</span></span>
</p>

<span><span>Dynamic embed is recommended for cases where you want to dynmaically control runtime configuration and or have more control over the embed call. This incluces setting plugin overides, and setup callbacks. Basic Embed codes look like this: </span></span>

<pre class="brush: jscript;light: true; fontsize: 100; first-line: 1; ">&lt;div id="{UNIQUE_OBJ_ID}" style="width:400px;height:330px;"&gt;&lt;/div&gt; 
&lt;script src="http://cdnapi.kaltura.com/p/{PARTNER_ID}/sp/{PARTNER_ID}00/embedIframeJs/uiconf_id/{uiConfId}/partner_id/{PARTNER_ID}"&gt;&lt;/script&gt;
&lt;script&gt;
      kWidget.embed({
         'targetId': '{UNIQUE_OBJ_ID}',
         'wid': '_{PARTNER_ID}',
         'uiconf_id' : '{UICONF_ID}',
         'entry_id' : '{ENTRY_ID}',
         'flashvars':{ // flashvars allows you to set runtime uiVar configuration overrides. 
              'autoPlay': false
         },
         'params':{ // params allows you to set flash embed params such as wmode, allowFullScreen etc
              'wmode': 'transparent' 
         },
         readyCallback: function( playerId ){
              console.log( 'Player:' + playerId + ' is ready '); 
         }
 });
&lt;/script&gt;</pre>

<span><span> </span></span>

<span>More info on dynamic embed can be obtained on the <a href="http://player.kaltura.com/docs/index.php?path=kwidget" target="_blank">dynamic embed page</a>. </span>

<p class="mce-heading-4">
  <span><a name="ThumbEmbed"></a>Thumb Embed</span>
</p>

<span><span>This </span><span>method takes the same arguments as the dynamic embed. Thumbnail embed pass</span><span>es</span><span> the entire configuration to the kWidget.embed when the user "click</span><span>s</span><span>" on the play button. This is the recommended method to use when you need to embed multiple players/entries in the same web page. The syntax for ThumbEmbed is identical to kWidget.embed ( dynamic embed ) except we call "kWidget.thumbEmbed" instead of "kWidget.embed" </span><br /></span>

<p class="mce-heading-4">
  <span><span><a name="iframeEmbed"></a>IFrame Embed</span></span>
</p>

iframe embed is good for sites that do not allow 3rd party JavaScript to be embed on their pages. This mode fits more stringent page security requirements. If using this iframe only embed mode, the page won't be able to  access the KDP player API.

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;iframe src="http://www.kaltura.com/p/{PARTNER_ID}/sp/{PARTNER_ID}00/embedIframeJs/uiconf_id/{UICONF_ID}/partner_id/{PARTNER_ID}?iframeembed=true&playerId={UNIQUE_OBJ_ID}&entry_id={ENTRY_ID}" width="400" height="330" allowfullscreen webkitallowfullscreen mozAllowFullScreen frameborder="0"&gt;&lt;/iframe&gt;</pre>

<span><a name="LegacyEmbed"></a></span><span style="color: #666560; font-size: 12pt; font-weight: bold;">Legacy Flash Embed Code</span>

Kaltura continues to support the Legacy Flash embed code. This code is best for legacy systems that can only accept Flash object code for player embeds. In general you should not use this embed code unless you have to. For cases where you can't inject JavaScript you should instead use the iframe embed, so that both Flash and HTML5 can be supported with a single embed code. 

Replace variables in braces {} – including the braces themselves – with the actual value used for each site and media. 

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;object 
  id="{UNIQUE_OBJ_ID}" 
  name="{UNIQUE_OBJ_ID}" 
  type="application/x-shockwave-flash" 
  height="{HEIGHT}" 
  width="{WIDTH}" 
  allowFullScreen="true" 
  allowNetworking="all" 
  allowScriptAccess="always" 
  data=" http://www.kaltura.com/kwidget/wid/_{PARTNER_ID}/uiconf_id/{UICONF_ID}/entry_id/{ENTRY_ID}" 
  xmlns:dc="http://purl.org/dc/terms/" 
  xmlns:media="http://search.yahoo.com/searchmonkey/media/" 
  rel="media:video" 
  resource=" http://www.kaltura.com/kwidget/wid/_{PARTNER_ID}/uiconf_id/{UICONF_ID}/entry_id/{ENTRY_ID}"&gt;
  &lt;param name="allowFullScreen" value="true" /&gt;
  &lt;param name="allowNetworking" value="all" /&gt;
  &lt;param name="allowScriptAccess" value="always" /&gt;
  &lt;param name="bgcolor" value="#000000" /&gt;
  &lt;param name="flashVars" value="" /&gt;
  &lt;param name="movie" value=" http://www.kaltura.com/kwidget/wid/_{PARTNER_ID}/uiconf_id/{UICONF_ID}/entry_id/{ENTRY_ID}" /&gt;
&lt;!--You can enter alternate content here. --&gt;
&lt;/object&gt;</pre>

<p class="mce-heading-4">
  Generating Embed Codes
</p>

Kaltura has built a simple library for <a href="http://kaltura.github.com/EmbedCodeGenerator/demo/" target="_blank">generating embed codes via javascript</a>. ( for example for a CMS that needs to generate these embed codes ). You can learn more about the project on its [github project page][8]. 

 [8]: https://github.com/kaltura/EmbedCodeGenerator

<p class="mce-heading-4">
  <a name="ParamsSettings"></a>Params and settings
</p>

To use an HTML-based embed code for a KDP3 player, populate an <object> tag (like above) with the following values:

Replace variables in braces {} – including the braces themselves – with the actual value used for each site and media. 

<table class="kaltura-table" style="width: 100%;">
  <thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 20%; text-align: center;">
         Parameter
      </th>
      
      <th class="kaltura-table-head-item" style="width: 20%; text-align: center;">
         Value/Variable
      </th>
      
      <th class="kaltura-table-head-item" style="width: 20%; text-align: center;">
        Description<span class="Apple-tab-span" style="white-space: pre;"> </span>Comments 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 20%; text-align: center;">
        Comments 
      </th>
      
      <th class="kaltura-table-head-item" style="width: 20%; text-align: center;">
        Example 
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         <a name="idparameter"></a>id
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        {UNIQUE_OBJ_ID}
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        HTML element unique identifier - this id will later be used to access this player instance via JavaScript
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <p>
           UNIQUE_OBJ_ID:
        </p>
        
        <ul>
          <li>
            Is a unique identifier, which enables referencing a specific player from JavaScript and a cascading style sheet (CSS)
          </li>
          <li>
            On a web page, assign a unique object identifier to each player. On different web pages, players may be assigned the same identifier
          </li>
          <li>
            To ensure cross-browser compatibility, set the same identifier for both id and name
          </li>
        </ul>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        id="{UNIQUE_OBJ_ID}"
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        name
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        {UNIQUE_OBJ_ID}
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        This should be equal to the value of the <em><strong>id</strong></em> parameter
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <strong>Must be identical</strong> to the value of the <a href="#idparameter"><em><strong>id</strong></em></a> parameter
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        name="{UNIQUE_OBJ_ID}"
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        type
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        application/x-shockwave-flash
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <p>
          HTML element type of object embedded.
        </p>
        
        <p>
          Defines the HTML element as a Flash object
        </p>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Value is always the same as specified in the Example
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        type="application/x-shockwave-flash" 
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <a name="height"></a>height
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        {HEIGHT}
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         The height of the player
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <p>
          Player dimensions: You can set and override values from a CSS.
        </p>
        
        <p>
          (Optional):
        </p>
        
        <ul>
          <li>
            Wrap the player embed code in  a division (<div>)
          </li>
          <li>
            Set the HEIGHT and WIDTH values in the embed code to 100%
          </li>
          <li>
            Set the actual size in the <div>
          </li>
        </ul>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        height="{HEIGHT}"
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        width
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        {WIDTH}
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         The width of the player
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         See the <a href="#height"><em><strong>height</strong></em></a> parameter
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        width="{WIDTH}"
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <a name="allowFullScreen"></a>allowFullScreen
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        true
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Enables Flash to enter Full Screen mode outside of the Browser window
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        If this parameter is omitted or equal to false, the Player's Full Screen button will not respond 
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        allowFullScreen="true"
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <a name="allowNetworking"></a>allowNetworking
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        all
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Refer to the <a href="http://help.adobe.com/en_US/ActionScript/3.0_ProgrammingAS3/WS1EFE2EDA-026D-4d14-864E-79DFD56F87C6.html#WS5b3ccc516d4fbf351e63e3d118a9b90204-7c5b" target="_blank">official Adobe Flash docs</a>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        allowNetworking="all"
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <a name="allowScriptAccess"></a>allowScriptAccess
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        always
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Refer to the <a href="http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b90204-7c9b.html" target="_blank">official Adobe Flash docs</a>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        allowScriptAccess="always"
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <a name="data"></a>data
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <p>
          The path for a Kaltura widget that represents the player and media, and includes the variables:
        </p>
        
        <ul>
          <li>
            {PARTNER_ID}
          </li>
          <li>
            {UICONF_ID}
          </li>
          <li>
            {ENTRY_ID} 
          </li>
        </ul>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <p>
          PARTNER_ID: Your unique Kaltura Publisher Account identifier
        </p>
        
        <p>
          UICONF_ID: Your player's unique identifier in the Kaltura system
        </p>
        
        <p>
          ENTRY_ID: A unique identifier for your media in the Kaltura system
        </p>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <p>
          Use the same path for the <em><strong>data</strong></em>, <em><strong>resource</strong></em> and  <em><strong>movie</strong></em> parameters
        </p>
        
        <p class="mce-procedure">
          To find your partner ID:
        </p>
        
        <ul>
          <li>
            Open the KMC and go to <a href="http://www.kaltura.com/index.php/kmc/kmc4#account%7Coverview" target="_blank">Settings>Account Settings</a>
          </li>
          <li>
            Under Account Info, copy the Partner ID value
          </li>
        </ul><img src="../../assets/210">
        
        <p class="mce-procedure">
          To find your player ID:
        </p>
        
        <ul>
          <li>
            Open the KMC and go to <a href="http://www.kaltura.com/index.php/kmc/kmc4#studio%7CplayersList" target="_blank">Studio</a>.
          </li>
          <li>
            Find the player and copy the ID value.
          </li>
        </ul><img src="../../assets/211">
        
        <p class="mce-procedure">
          To find your entry ID:
        </p>
        
        <ul>
          <li>
            Open the KMC and go to <a href="http://www.kaltura.com/index.php/kmc/kmc4#content%7Cmanage" target="_blank">Content>Manage</a>.
          </li>
          <li>
            In the Entries Table, find the media entry and copy the ID value.
          </li>
        </ul>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Refer to the <a href="#sample-html-embed">code example above</a>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        SEO code
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Enables Google and Yahoo to recognize that the embed code represents a video and its metadata.
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Refer to the <a href="#sample-html-embed">code example above</a>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        SEO resource
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        The path for a Kaltura widget that represents the player and media.
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         See the <em><a href="#data"><strong>data</strong></a> </em>parameter
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Refer to the <a href="#sample-html-embed">code example above</a>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        param name
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        allowFullScreen
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Defines the <em><strong><a href="#allowFullScreen">allowFullScreen</a></strong></em> parameter and value
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <param name="allowFullScreen" value="true" />
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        param name
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        allowNetworking
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Defines the <em><strong><a href="#allowNetworking">allowNetworking</a></strong> </em>parameter and value
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <param name="allowNetworking" value="all" />
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        param name
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        allowScriptAccess
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Defines the <em><strong><a href="#allowScriptAccess">allowScriptAccess</a> </strong></em>parameter and value
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <param name="allowScriptAccess" value="always" />
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        param name
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        bgcolor
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Defines the player's  background color parameter and value
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <param name="bgcolor" value="#000000" />
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        param name
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        flashVars
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Defines the flashVars parameter and value
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        Using the flashVars it is possible to override many player settings and customize the player
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        <param name="flashVars" value="" />
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        param name
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         movie
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
        The path for a Kaltura widget that represents the player and media
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         See the <em><a href="#data"><strong>data</strong></a> </em>parameter
      </td>
      
      <td class="kaltura-table-row-item" style="width: 20%; text-align: left;">
         Refer to the <a href="#sample-html-embed">code example above</a>
      </td>
    </tr>
  </tbody>
</table>

 

To learn how to use the <embed> syntax with the Twice-Cooked Method and the Satay Method, refer to <a href="http://www.alistapart.com/articles/flashsatay/" target="_blank">Flash Satay Embedding Flash While Supporting Standards</a>.  

 

 

 