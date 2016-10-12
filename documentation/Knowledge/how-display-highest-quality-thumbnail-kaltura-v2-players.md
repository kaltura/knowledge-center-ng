---
layout: page
title: "How to display the highest quality thumbnail for Kaltura v2 Players?"
date: 2014-12-02 14:02:27
---

<div id="main-header">
  <div id="title-heading" class="pagetitle with-breadcrumbs">
    <h1 id="title-text" class="with-breadcrumbs">
      <span style="font-size: 1.5em;"><span class="mce-sub-heading">Prerequisites</span><br /></span>
    </h1>
  </div>
</div>

<div id="content" class="page view">
  <div id="main-content" class="wiki-content">
    <div class="contentLayout2">
      <div class="columnLayout single" data-layout="single">
        <div class="cell normal" data-type="normal">
          <div class="innerCell">
            <ul>
              <li>
                <p>
                  Player v2.22 and above.
                </p>
              </li>
            </ul>
            
            <hr />
            
            <p>
               Displaying the highest quality image in a player can be achieved in the following ways:
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

*   **[Embed Method][1] - **useful for single use and effects only the page in which the player is embedded.
*   **[UiVar][2] -** setting the player to always use the highest quality thumbnail, regardless of the entry, effects all pages where the player is embedded.

 [1]: #embed
 [2]: #uivar

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><a name="embed"></a>Embed Method</span>

<p id="Howtodisplaythehighestqualitythumbnail?-TosetmaximumqualitythumbnailusingFlashvar:" class="mce-procedure">
  To set maximum quality thumbnail using Flashvar (embed method)
</p>

1.  See <a href="http://knowledge.kaltura.com/node/1298" target="_blank">How to generate a dynamic embed code</a>, to embed a player in a webpage. 
2.  Add the following Flashvar:
    
    <table border="0" cellspacing="0" cellpadding="0">
      <tbody>
        <tr>
          <td class="gutter">
            1
          </td>
          
          <td class="code">
            <code class="js string">"thumbnailUrl"</code><code class="js plain">:&nbsp;</code><code class="js string">"&lt;a href="http://www.kaltura.com/p/%7BmediaProxy.entry.partnerId%7D/sp/%7BmediaProxy.entry.partnerId%7D00/thumbnail/entry_id/%7BmediaProxy.entry.id%7D/width/height">http://www.kaltura.com/p/{mediaProxy.entry.partnerId}/sp/{mediaProxy.entry.partnerId}00/thumbnail/entry_id/{mediaProxy.entry.id}/width/height"&lt;/a></code><code class="js plain">,</code>
          </td>
        </tr>
      </tbody>
    </table>
    
    **If the thumbnailUrl flashvar has another flashvar after it, make sure to have the comma after the thumbnail URL.  
      
    <img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/46727337/image2014-12-1%2022%3A2%3A1.png?version=1&modificationDate=1417464128078&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/46727337/image2014-12-1%2022%3A2%3A1.png?version=1&modificationDate=1417464128078&api=v2" data-linked-resource-id="47022121" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-12-1 22:2:1.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="46727337" data-linked-resource-container-version="4" /> 

3.  Save the page. The highest quality thumbnail should be displayed. 

 

* * *

 

<div id="Howtodisplaythehighestqualitythumbnail?-SettingtheplayertousethehighestqualitythumbnailbyeditingtheplayerJSONconfig:" class="mce-heading-3">
  <a name="uivar"></a>Setting the Player to Use the Highest Quality Thumbnail by Editing the Player JSON Config
</div>

<p style="padding-left: 30px;">
  1. Access the <a href="http://player.kaltura.com/kWidget/tests/PlayerVersionUtility.html" target="_blank" class="external-link" rel="nofollow">Player Utility page</a>(allows us to edit the JSON of the player) and log in with your Kaltura credentials:<br />    <a href="http://player.kaltura.com/kWidget/tests/PlayerVersionUtility.html" class="external-link" rel="nofollow">http://player.kaltura.com/kWidget/tests/PlayerVersionUtility.html</a><br /><br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/46727316/image2014-12-1%2017%3A26%3A58.png?version=1&modificationDate=1417453035377&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/46727316/image2014-12-1%2017%3A26%3A58.png?version=1&modificationDate=1417453035377&api=v2" data-linked-resource-id="47022101" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-12-1 17:26:58.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="46727316" data-linked-resource-container-version="9" /><br /><br />
</p>

<p style="padding-left: 30px;">
  2. To allow the tool to edit the JSON config of the player, select <strong>Allow Access</strong>, then click <strong>Save and Close.</strong><br /><br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/46727316/image2014-12-1%2017%3A28%3A46.png?version=1&modificationDate=1417453035410&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/46727316/image2014-12-1%2017%3A28%3A46.png?version=1&modificationDate=1417453035410&api=v2" data-linked-resource-id="47022102" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-12-1 17:28:46.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="46727316" data-linked-resource-container-version="9" /><br /><br />
</p>

<p style="padding-left: 30px;">
  3.  Insert the ID of the player you want to edit and click <strong>Edit Player.</strong><br /><br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/46727316/image2014-12-1%2017%3A31%3A53.png?version=1&modificationDate=1417453035420&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/46727316/image2014-12-1%2017%3A31%3A53.png?version=1&modificationDate=1417453035420&api=v2" data-linked-resource-id="47022103" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-12-1 17:31:53.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="46727316" data-linked-resource-container-version="9" /><br /><br />
</p>

<p style="padding-left: 30px;">
  4. Click <strong>Edit JSON config.</strong><br /><br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/46727316/image2014-12-1%2017%3A37%3A48.png?version=1&modificationDate=1417453035439&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/46727316/image2014-12-1%2017%3A37%3A48.png?version=1&modificationDate=1417453035439&api=v2" data-linked-resource-id="47022105" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-12-1 17:37:48.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="46727316" data-linked-resource-container-version="9" /><br /><br />
</p>

<p style="padding-left: 30px;">
  5. Scroll down, and under the <strong>UiVar</strong> section, add the following key and value pairs:
</p>

<p style="padding-left: 30px;">
   
</p>

<table style="padding-left: 30px;" border="0" cellspacing="0" cellpadding="0">
  <tbody style="padding-left: 30px;">
    <tr style="padding-left: 30px;">
      <td class="code" style="padding-left: 30px;">
        <code class="java plain">{</code><code class="java spaces">&nbsp;&nbsp;</code><code class="java string">"key"</code><code class="java plain">:&nbsp;</code><code class="java string">"thumbnailUrl"</code><code class="java plain">,</code><code class="java spaces">&nbsp;&nbsp;</code><code class="java string">"value"</code><code class="java plain">:&nbsp;</code><code class="java string">"&lt;a href="http://www.kaltura.com/p/%7BmediaProxy.entry.partnerId%7D/sp/%7BmediaProxy.entry.partnerId%7D00/thumbnail/entry_id/%7BmediaProxy.entry.id%7D/width/height">http://www.kaltura.com/p/{mediaProxy.entry.partnerId}/sp/{mediaProxy.entry.partnerId}00/thumbnail/entry_id/{mediaProxy.entry.id}/width/height"&lt;/a></code><code class="java plain">,</code><code class="java spaces">&nbsp;&nbsp;</code><code class="java string">"overrideFlashvar"</code><code class="java plain">:&nbsp;</code><code class="java keyword">false</code><code class="java plain">},</code>
      </td>
    </tr>
  </tbody>
</table>

<p style="padding-left: 30px;">
  <br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/46727337/image2014-12-1%2021%3A57%3A1.png?version=1&modificationDate=1417463846825&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/46727337/image2014-12-1%2021%3A57%3A1.png?version=1&modificationDate=1417463846825&api=v2" data-linked-resource-id="47022120" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-12-1 21:57:1.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="46727337" data-linked-resource-container-version="4" /><br /><br />6. Click <strong>Save Changes</strong> to apply the changes.
</p>

<p style="padding-left: 30px;">
  <br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/46727316/image2014-12-1%2017%3A49%3A36.png?version=1&modificationDate=1417453035457&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/46727316/image2014-12-1%2017%3A49%3A36.png?version=1&modificationDate=1417453035457&api=v2" data-linked-resource-id="47022107" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-12-1 17:49:36.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="46727316" data-linked-resource-container-version="9" /><br /><br /><span> </span>
</p>

<p style="padding-left: 30px;">
  <span>7. After the line "<strong>Update OK</strong>" appears at the top of the screen, click </span><strong>Close.</strong>
</p>

<p style="padding-left: 30px;">
  <br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/46727316/image2014-12-1%2017%3A54%3A29.png?version=1&modificationDate=1417453035476&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/46727316/image2014-12-1%2017%3A54%3A29.png?version=1&modificationDate=1417453035476&api=v2" data-linked-resource-id="47022109" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-12-1 17:54:29.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="46727316" data-linked-resource-container-version="9" />
</p>

<p style="padding-left: 30px;">
  <br /><br />
</p>