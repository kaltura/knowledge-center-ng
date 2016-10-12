---
layout: page
title: "KRecord Customization"
date: 2012-04-15 15:11:53
---

<p class="mce-heading-2">
  Customizing the KRecord Look and Feel
</p>

This article explains how integrators and project managers can customize KRecord. KRecord does not require a uiConf. 

<p class="mce-heading-3">
  Changing Configuration Values
</p>

The <a href="https://github.com/kaltura/krecord/blob/master/KalturaRecord/html-template/index.template.html" target="_blank">index.template.html</a> file (under the <a href="https://github.com/kaltura/krecord/tree/master/KalturaRecord" target="_blank">KRecord project</a> -> html-template) contains JavaScript and FlashVars. To adapt KRecord to your needs, you can change the following FlashVars: 

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        <strong>Variable</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        <strong>Description</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        ks
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        A unique string that represents the user. Valid for 24 hours.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        kshowId
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The identifier of the kshow
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        uid
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The internal identifier of the end user
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        pid
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The identifier of the partner
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        subPid
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The identifier of the sub partner
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        fmsApp
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The fms application, The default is oflaDemo.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        showUi
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        If false, the skin is disabled.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        themeUrl
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The skin file. The default file is skin.swf.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        localeUrl
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        An XML file that represents locales.  The default file is locale.xml.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        host
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The host of the application
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        rtmpHost
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The rtmp host of the application
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        autoPreview
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The default value is true.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        entryName
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The name of the created entry
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        entryTags
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The tags of the created entry
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        entryDescription
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The description of the created entry
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        creditsScreenName
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The name of the Credits screen
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        groupId
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The identifier of the group
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        partnerData
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        Custom data, passed from the partner, to be attached to each entry that is added
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        creditsSiteUrl
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The URL of the credits site
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        thumbOffset
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        The offset of the thumbnails
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        adminTags
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        Admin tags of the created entry
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        licenseType
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        License type of the created entry
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="156">
        credit
      </td>
      
      <td style="text-align: left;" valign="top" width="527">
        Credit for the created entry
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  Customizing Skin and Locale
</p>

You can create your own skin and locale files.

<p class="mce-procedure">
  To apply your skin and locale files to KRecord
</p>

Send the following FlashVars:

*   themeUrl = [style swf filename]
*   localeUrl = [locale XML filename]

<p class="mce-heading-3 mce-heading-4">
  Skins
</p>

To adapt your skin to the KRecord default skin, refer to KalturaRecord-> library-> skin.fla.

<p class="mce-heading-3 mce-heading-4">
  Defining Locales
</p>

Define each KRecord locale value in the following XML file format:{syntaxhighlighter brush: xml;fontsize: 100; first-line: 1; }<setting> <key>localeKey</key> <value>Value String</value> </setting>{/syntaxhighlighter}

To change the locale, edit the locale.xml file.