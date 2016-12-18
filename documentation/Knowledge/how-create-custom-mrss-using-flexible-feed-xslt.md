---
layout: page
title: "How to Create Custom MRSS Using The Flexible Feed XSLT"
date: 2012-08-25 03:14:49
---

Kaltura provides various out of the box syndication feeds (variations of MRSS) to suite different syndication destinations such as Google's WebMasters Tools, Yahoo!, Bing, iTunes and more. Often, publishers will need a customized syndication feed to suite a different format and destination. Using Kaltura's "Flexible Feed" Syndication format, developers are able create custom syndication feeds. It is possible to customize a syndication feed by submiting an <a href="http://en.wikipedia.org/wiki/XSLT" target="_blank" title="XSLT (Extensible Stylesheet Language Transformations)">XSLT</a> to Kaltura.

For example -

*   Currently there is no one agreed-upon standard for syndication feeds. Although the MRSS format is gaining popularity it is not strictly defined, and there are different ways to implement MRSS as well as various variations of it in use in the market. Issues with the standard includes: optional elements that will not always be validate and the structure/hierarchy of elements is varied. To learn more about the MRSS spec visit: <a href="http://video.search.yahoo.com/mrss" target="_blank">http://video.search.yahoo.com/mrss</a>.
*   In addition to MRSS <a href="http://www.apple.com/itunes/podcasts/specs.html" target="_blank">iTunes's format</a> has also gained popularity. Much like the MRSS format there are slight variations for <a href="http://deimos.apple.com/rsrc/doc/iTunesUAdministrationGuide/AddingContent/chapter_12_section_3.html#//apple_ref/doc/uid/AdminGuide-CH22-SW6" target="_blank">iTunesU</a> that require additional tags.
*   <a href="http://developer.boxee.tv/RSS_Specification" target="_blank">Boxee's compliant MRSS feed specification</a> include slight variations from Yahoo!'s original format.

The Flexible Feed provides support for different feed formats, including MRSS variations, itunes variations and etc. with minimal development work. By applying XSLT transformation to the base Kaltura feed, custom feeds can be created without the need to write server code. The XSLT transformation is performed separately on each item (entry) in the feed, improving transformation performance.

The XSLT is executed item by item in order to support large XMLs (up to 10K items), therefore:

*   There must be an item tag for each item.
*   No values will be retrieved prior to the item tag.

<p class="mce-note-graphic">
  Kaltura does not support XSL 2.0 because it is not supported by PHP’s XSLT engine.
</p>

<span class="mce-heading-2">The KalturaGenericSyndicationFeed</span>

For every Kaltura account, a generic feed is created outlining all the available fields in the specific account. Fields include Custom Metadata fields associated with the Kaltura account, information about video flavors (renditions) and more.  
The KalturaGenericSyndicationFeed is the base feed from which the Flexible Feed will perform the desired transformation (by applying the given XSLT file) and generate the custom feed format desired.

<p class="mce-procedure">
  To retrieve the Generic Kaltura Syndication Feed, open the <a href="https://developer.kaltura.com/console/" target="_blank">Kaltura API Test Console</a> and follow these steps:
</p>

1.  Generate a valid Kaltura Session using the session.start or user.loginByLoginId actions. To learn more on how to use the API Test Console, read: <a href="{{site.url}}/documentation/Knowledge/using-kalturas-api-test-console-introduction.html" target="_blank">Using Kaltura's API Test Console</a>.
2.  Select the ***syndicationFeed*** service.
3.  Select the ***add***** **action.
4.  <span><span>Under syndicationFeed, select <strong><em>KalturaGenericSyndicationFeed </em></strong>and click Edit next to it.</span></span>
5.  <span><span>In the <em><strong>syndicationFeed:name</strong></em><strong> </strong>field, enter a name (e.g: myGenericFeed) and make sure the checkmark next to the field is marked.</span></span>
6.  <span><span>If you are not using End-User Entitlements, make sure to set <strong>syndicationFeed:enforceEntitlement</strong> to 0 (default is 1).</span></span>
7.  <span><span>Click the <em><strong>Send</strong></em><strong> </strong>button.</span></span>
8.  <span><span><span>In the result, locate the <em><strong>feedUrl</strong></em><strong> </strong>node, and copy the URL inside it (it should look like this: <span>http://www.kaltura.com/api_v3/getFeed.php?partnerId=309&feedId=1_xw6gi6b4)</span></span></span></span>
9.  <span><span><span><span>Download the XML from the URL described in <em><strong>feedURL</strong></em>. This is the Generic Feed of that Kalura account.</span></span></span></span>

<p class="mce-heading-2">
  <span><span><span><span>Creating The Flexible Feed (The XSLT)</span></span></span></span>
</p>

<span><span><span><span>After using the KalturaGenericSyndicationFeed to generate a base feed for the Kaltura account, use it to map the desired fields to any custom format of choice by creating an XSLT file.</span></span></span></span>

<span><span><span>Additionally, Kaltura provides a <a href="http://www.kaltura.com/api_v3/xsdDoc/?type=syndication" target="_blank" title="Kaltura - Syndication Feed Schema Documentation">generic schema for the syndication feed</a>. The schema can be used as a reference to map field names and structure.</span></span></span>

<span><span><span><span>The XSLT should be divided to 2 templates: </span></span></span></span>

*   The Feed Header and Footer part:  
    <pre class="brush: xml;gutter: false; light: true; fontsize: 100; first-line: 1; ">&lt;xsl:template name="rss" match="/"&gt;
&lt;xsl:apply-templates name="item" select="channel/items/item" /&gt;</pre>

*   The Feed Item part (Item = each entry processed):  
    <pre class="brush: xml;gutter: false; light: true; fontsize: 100; first-line: 1; ">&lt;xsl:template name="item" match="item"&gt;</pre>

Click below to see full example of valid XSLT including both Header and Item templates:

<pre class="brush: xml;collapse: true; fontsize: 100; first-line: 1; ">&lt;?xml version="1.0" encoding="utf-8"?&gt;
&lt;xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform"
xmlns:media="http://search.yahoo.com/mrss/"
xmlns:xs="http://www.w3.org/2001/XMLSchema"
exclude-result-prefixes="xs"&gt;
  &lt;xsl:output method="xml" encoding="UTF-8" indent="yes" /&gt;
  &lt;xsl:template name="rss" match="/"&gt;
    &lt;rss xmlns:media="http://search.yahoo.com/mrss/"&gt;
      &lt;xsl:for-each select="rss"&gt;
        &lt;xsl:attribute name="version"&gt;
          &lt;xsl:value-of select="string(number(string(@version)))" /&gt;
        &lt;/xsl:attribute&gt;
        &lt;xsl:apply-templates name="item"
        select="channel/items/item" /&gt;
      &lt;/xsl:for-each&gt;
    &lt;/rss&gt;
  &lt;/xsl:template&gt;
  &lt;xsl:template name="item" match="item"&gt;
    &lt;xsl:variable name="var1_content" select="content" /&gt;
    &lt;xsl:variable name="var2_resultof_cast"
    select="string(title)" /&gt;
    &lt;item&gt;
      &lt;title&gt;
        &lt;xsl:value-of select="$var2_resultof_cast" /&gt;
      &lt;/title&gt;
      &lt;link&gt;
        &lt;xsl:value-of select="string(link)" /&gt;
      &lt;/link&gt;
      &lt;xsl:for-each select="$var1_content"&gt;
        &lt;media:content&gt;
          &lt;xsl:attribute name="url"&gt;
            &lt;xsl:value-of select="string(@url)" /&gt;
          &lt;/xsl:attribute&gt;
        &lt;/media:content&gt;
      &lt;/xsl:for-each&gt;
      &lt;media:title&gt;
        &lt;xsl:value-of select="$var2_resultof_cast" /&gt;
      &lt;/media:title&gt;
      &lt;media:thumbnail&gt;
        &lt;xsl:value-of select="string(thumbnailUrl)" /&gt;
      &lt;/media:thumbnail&gt;
      &lt;media:description&gt;
        &lt;xsl:value-of select="string(description)" /&gt;
      &lt;/media:description&gt;
      &lt;media:keywords&gt;
        &lt;xsl:call-template name="implode"&gt;
          &lt;xsl:with-param name="items"
          select="$var1_content/tags/tag" /&gt;
        &lt;/xsl:call-template&gt;
      &lt;/media:keywords&gt;
    &lt;/item&gt;
  &lt;/xsl:template&gt;
  &lt;xsl:template name="implode"&gt;
    &lt;xsl:param name="items" /&gt;
    &lt;xsl:param name="separator" select="','" /&gt;
    &lt;xsl:for-each select="$items"&gt;
      &lt;xsl:if test="position() &gt; 1"&gt;
        &lt;xsl:value-of select="$separator" /&gt;
      &lt;/xsl:if&gt;
      &lt;xsl:value-of select="." /&gt;
    &lt;/xsl:for-each&gt;
  &lt;/xsl:template&gt;
&lt;/xsl:stylesheet&gt;</pre>

<p class="mce-note-graphic">
  NOTE: To ease the process of creating the XSLT file from the generic base feed, it is recommeneded to utilize tools such as <a href="http://www.altova.com/mapforce.html" target="_blank">Altova MapForce</a> or <a href="http://www.stylusstudio.com/xslt_editor.html" target="_blank">Stylus Studio's XSLT Editor</a>.
</p>

<p class="mce-heading-2">
  Submitting the XSLT to a new <span>KalturaGenericXsltSyndicationFeed</span>
</p>

<p class="mce-procedure">
  <span>When the XSLT is ready to be submitted to Kaltura, follow the following steps to create your new Flexible Feed:</span>
</p>

1.  Open the KMC in the <a href="http://www.kaltura.com/index.php/kmc/kmc4#content|syndication" target="_blank">Syndication tab under Content</a>.
2.  Click the ***Create New Feed*** button.
3.  In the ***Feed Type*** field, select ***Flexible Format Feed***.
4.  Click ***Browse*** and select the XSLT file you created.
5.  Specify a ***name*** for the field.
6.  Click the ***Add Feed*** button.
7.  The new feed is now available in the list of feeds in the syndication tab.

<p class="mce-heading-2">
  Ready XSLT files for Common Transformations
</p>

Below you will find a few ready-to-use XSLT templates for common use-cases. Use these as sample and reference to create your own custom transformations.

<span class="mce-heading-3">Roku Channel MRSS</span>

Roku uses a standard Yahoo! MRSS format, with slight additions. The following XSLT provides the correct format for syndication of content in a Ruko channel.

This XSLT is provided as a sample reference only, note that there are more steps required to enable sharing of content in a Roku channel. Please contact your Kaltura Account Manager for more details.

<pre class="brush: xml;collapse: true; fontsize: 100; first-line: 1; ">&lt;?xml version="1.0" encoding="utf-8"?&gt;
&lt;xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform"
xmlns:media="http://search.yahoo.com/mrss/"
xmlns:xs="http://www.w3.org/2001/XMLSchema"
xmlns:dcterms="http://purl.org/dc/terms/"
xmlns:php="http://php.net/xsl"
exclude-result-prefixes="xs"&gt;
  &lt;xsl:output method="xml" /&gt;
  &lt;xsl:template match="*"&gt;
   &lt;xsl:element name="{local-name()}"&gt;
     &lt;xsl:apply-templates/&gt;
   &lt;/xsl:element&gt;
&lt;/xsl:template&gt;

  &lt;xsl:template name="rss" match="/"&gt;
    &lt;rss xmlns:media="http://search.yahoo.com/mrss/"&gt;
      &lt;xsl:for-each select="rss"&gt;
        &lt;xsl:variable name="var1_channel" select="channel" /&gt;
        &lt;xsl:attribute name="version"&gt;
          &lt;xsl:value-of select="string(@version)" /&gt;
        &lt;/xsl:attribute&gt;
        &lt;channel&gt;
          &lt;title&gt;
            &lt;xsl:value-of select="string($var1_channel/title)" /&gt;
          &lt;/title&gt;
          &lt;link&gt;
            &lt;xsl:value-of select="string($var1_channel/link)" /&gt;
          &lt;/link&gt;
          &lt;description&gt;
            &lt;xsl:value-of select="string($var1_channel/description)" /&gt;
          &lt;/description&gt;
          &lt;xsl:apply-templates name="item"
          select="channel/items/item" /&gt;
        &lt;/channel&gt;
      &lt;/xsl:for-each&gt;
    &lt;/rss&gt;
  &lt;/xsl:template&gt;
  &lt;xsl:template name="item" match="item"&gt;
    &lt;xsl:variable name="var1_content" select="content" /&gt;
	&lt;xsl:variable name="var1_media" select="media" /&gt;
    &lt;xsl:variable name="var2_resultof_cast" select="string(title)" /&gt;
    &lt;xsl:variable name="var2_thumbnailUrl" select="thumbnailUrl" /&gt;
	&lt;xsl:variable name="var2_createdAt" select="createdAt" /&gt;
	&lt;xsl:variable name="var2_player" select="player" /&gt;
    &lt;item&gt;
      &lt;title&gt;
        &lt;xsl:value-of select="$var2_resultof_cast" /&gt;
      &lt;/title&gt;
      &lt;link&gt;
        &lt;xsl:value-of select="string(link)" /&gt;
      &lt;/link&gt;
      &lt;xsl:for-each select="$var1_content"&gt;
          &lt;media:content&gt;
            &lt;xsl:attribute name="url"&gt;
              &lt;xsl:value-of select="string(@url)" /&gt;
            &lt;/xsl:attribute&gt;
			&lt;xsl:attribute name="duration"&gt;              
				&lt;xsl:value-of select="string(floor(number(string($var1_media/duration))))" /&gt;             
			&lt;/xsl:attribute&gt;  
          &lt;/media:content&gt;
      &lt;/xsl:for-each&gt;
      &lt;media:title&gt;
        &lt;xsl:value-of select="$var2_resultof_cast" /&gt;
      &lt;/media:title&gt;
	  &lt;media:description&gt;
        &lt;xsl:value-of select="string(description)" /&gt;
      &lt;/media:description&gt;
	  &lt;media:keywords&gt; 
        &lt;xsl:call-template name="implode"&gt;
          &lt;xsl:with-param name="items" select="tags/tag" /&gt;
        &lt;/xsl:call-template&gt;
      &lt;/media:keywords&gt;
      &lt;media:thumbnail&gt;
        &lt;xsl:copy-of select="$var2_thumbnailUrl/@node()" /&gt;
        &lt;xsl:copy-of select="$var2_thumbnailUrl/node()" /&gt;
      &lt;/media:thumbnail&gt;
	  &lt;media:player&gt;
	  &lt;xsl:attribute name="url"&gt;
              &lt;xsl:value-of select="string($var2_player/@url)" /&gt;
            &lt;/xsl:attribute&gt;
        &lt;xsl:copy-of select="$var2_player/node()" /&gt;
      &lt;/media:player&gt;
	  &lt;media:rating scheme="urn:simple"&gt;b&lt;/media:rating&gt;
	  &lt;pubdate&gt;
        &lt;xsl:value-of select="php:function('date', 'Y-m-d\ H:i:s\', sum($var2_createdAt))"/&gt;
      &lt;/pubdate&gt;
    &lt;/item&gt;
  &lt;/xsl:template&gt;
  &lt;xsl:template name="implode"&gt;
    &lt;xsl:param name="items" /&gt;
    &lt;xsl:param name="separator" select="','" /&gt;
    &lt;xsl:for-each select="$items"&gt;
      &lt;xsl:if test="position() &gt; 1"&gt;
        &lt;xsl:value-of select="$separator" /&gt;
      &lt;/xsl:if&gt;
      &lt;xsl:value-of select="." /&gt;
    &lt;/xsl:for-each&gt;
  &lt;/xsl:template&gt;
&lt;/xsl:stylesheet&gt;</pre>

<p class="mce-heading-3">
  Boxee Channel MRSS
</p>

To successfully submit Kaltura feeds to Boxee's library, a new format has to be created, pointing the user to a hosted player page and including Boxee's special fields.

This XSLT is provided as a sample reference only, note that there are more steps required to enable sharing of content in Boxee. Please contact your Kaltura Account Manager for more details.

<pre class="brush: xml;collapse: true; fontsize: 100; first-line: 1; ">&lt;xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform"
xmlns:boxee="http://boxee.tv/spec/rss/"
xmlns:media="http://search.yahoo.com/mrss/"
xmlns:xs="http://www.w3.org/2001/XMLSchema"
xmlns:dcterms="http://purl.org/dc/terms/"
xmlns:php="http://php.net/xsl" version="1.0"
exclude-result-prefixes="xs"&gt;
  &lt;xsl:output method="xml" /&gt;
  &lt;xsl:template match="*"&gt;
    &lt;xsl:element name="{local-name()}"&gt;
      &lt;xsl:apply-templates /&gt;
    &lt;/xsl:element&gt;
  &lt;/xsl:template&gt;
  &lt;xsl:template name="rss" match="/"&gt;
  	&lt;rss&gt;
      &lt;xsl:for-each select="rss"&gt;
        &lt;xsl:variable name="var1_channel" select="channel" /&gt;
        &lt;xsl:attribute name="version"&gt;
          &lt;xsl:value-of select="string(@version)" /&gt;
        &lt;/xsl:attribute&gt;
        &lt;channel&gt;
          &lt;title&gt;
            &lt;xsl:value-of select="string($var1_channel/title)" /&gt;
          &lt;/title&gt;
          &lt;link&gt;
            &lt;xsl:value-of select="string($var1_channel/link)" /&gt;
          &lt;/link&gt;
          &lt;description&gt;
            &lt;xsl:value-of select="string($var1_channel/description)" /&gt;
          &lt;/description&gt;
          &lt;xsl:apply-templates name="item"
          select="channel/items/item" /&gt;
        &lt;/channel&gt;
      &lt;/xsl:for-each&gt;
    &lt;/rss&gt;
  &lt;/xsl:template&gt;
  &lt;xsl:template name="item" match="item"&gt;
    &lt;xsl:variable name="var1_content" select="content" /&gt;
    &lt;xsl:variable name="var1_media" select="media" /&gt;
    &lt;xsl:variable name="var2_resultof_cast"
    select="string(title)" /&gt;
    &lt;xsl:variable name="var2_thumbnailUrl" select="thumbnailUrl" /&gt;
    &lt;xsl:variable name="var2_createdAt" select="createdAt" /&gt;
    &lt;item&gt;
      &lt;title&gt;
        &lt;xsl:value-of select="$var2_resultof_cast" /&gt;
      &lt;/title&gt;
      &lt;boxee:media-type&gt;
        &lt;xsl:attribute name="type"&gt;movie&lt;/xsl:attribute&gt;
        &lt;xsl:attribute name="name"&gt;Feature&lt;/xsl:attribute&gt;
        &lt;xsl:attribute name="expression"&gt;full&lt;/xsl:attribute&gt;
      &lt;/boxee:media-type&gt;
      &lt;link&gt;
        &lt;xsl:value-of select="string(link)" /&gt;
      &lt;/link&gt;
      &lt;media:content&gt;
        &lt;xsl:attribute name="url"&gt;
          &lt;xsl:value-of select="string(link)" /&gt;
        &lt;/xsl:attribute&gt;
        &lt;xsl:attribute name="type"&gt;
          &lt;xsl:value-of select="'application/x-shockwave-flash'" /&gt;
        &lt;/xsl:attribute&gt;
        &lt;xsl:attribute name="duration"&gt;
          &lt;xsl:value-of select="string(number(string($var1_media/duration)) div number('1000'))" /&gt;
        &lt;/xsl:attribute&gt;
      &lt;/media:content&gt;
      &lt;media:title&gt;
        &lt;xsl:value-of select="$var2_resultof_cast" /&gt;
      &lt;/media:title&gt;
      &lt;media:description&gt;
        &lt;xsl:value-of select="string(description)" /&gt;
      &lt;/media:description&gt;
      &lt;media:keywords&gt;
        &lt;xsl:call-template name="implode"&gt;
          &lt;xsl:with-param name="items" select="tags/tag" /&gt;
        &lt;/xsl:call-template&gt;
      &lt;/media:keywords&gt;
      &lt;media:thumbnail&gt;
        &lt;xsl:copy-of select="concat($var2_thumbnailUrl/@node(),'/width/300')" /&gt;
        &lt;xsl:copy-of select="concat($var2_thumbnailUrl/node(),'/width/300')" /&gt;
      &lt;/media:thumbnail&gt;
      &lt;media:rating scheme="urn:simple"&gt;b&lt;/media:rating&gt;
      &lt;pubdate&gt;
        &lt;xsl:value-of select="php:function('date', 'Y-m-d\ H:i:s\', sum($var2_createdAt))" /&gt;
      &lt;/pubdate&gt;
    &lt;/item&gt;
  &lt;/xsl:template&gt;
  &lt;xsl:template name="implode"&gt;
    &lt;xsl:param name="items" /&gt;
    &lt;xsl:param name="separator" select="','" /&gt;
    &lt;xsl:for-each select="$items"&gt;
      &lt;xsl:if test="position() &gt; 1"&gt;
        &lt;xsl:value-of select="$separator" /&gt;
      &lt;/xsl:if&gt;
      &lt;xsl:value-of select="." /&gt;
    &lt;/xsl:for-each&gt;
  &lt;/xsl:template&gt;
&lt;/xsl:stylesheet&gt;</pre>

<p class="mce-heading-3">
  JSONified Feed (JSON representation of a feed)
</p>

The sample below emphasizes the strength and flexibility of the Flexible Feed. Leveraging XSLT, it is possible to completely transform the format of the feed, and even generate non-XML output. In this case, the feed is outputted as JSON to be easily parsed by Javascript applications.

<pre class="brush: xml;collapse: true; fontsize: 100; first-line: 1; ">&lt;xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform"&gt;
    &lt;xsl:output method="text" omit-xml-declaration="yes"/&gt;
	&lt;xsl:param name="KalturaHasNextItem" /&gt;
	
    &lt;xsl:template name="rss" match="/"&gt;{&lt;xsl:for-each select="rss"&gt;
		&lt;xsl:variable name="indent"&gt;&lt;xsl:text&gt;			&lt;/xsl:text&gt;&lt;/xsl:variable&gt;
		&lt;xsl:variable name="channel-title"&gt;&lt;xsl:call-template name="safe-json-string"&gt;&lt;xsl:with-param name="text" select="string(channel/title)" /&gt;&lt;/xsl:call-template&gt;&lt;/xsl:variable&gt;
		&lt;xsl:variable name="channel-link"&gt;&lt;xsl:call-template name="safe-json-string"&gt;&lt;xsl:with-param name="text" select="string(channel/link)" /&gt;&lt;/xsl:call-template&gt;&lt;/xsl:variable&gt;
		&lt;xsl:variable name="channel-description"&gt;&lt;xsl:call-template name="safe-json-string"&gt;&lt;xsl:with-param name="text" select="string(channel/description)" /&gt;&lt;/xsl:call-template&gt;&lt;/xsl:variable&gt;
        
		&lt;xsl:attribute name="version"&gt;
          &lt;xsl:value-of select="string(@version)"/&gt;
        &lt;/xsl:attribute&gt;
	   "channel":{
			"title":"&lt;xsl:value-of select="$channel-title"/&gt;",
			"link":"&lt;xsl:value-of select="$channel-link"/&gt;",
			"description":"&lt;xsl:value-of select="$channel-description"/&gt;",
			"items": {&lt;xsl:apply-templates name="item" select="channel/items/item"/&gt;
			}
        }
      &lt;/xsl:for-each&gt;		
	}&lt;/xsl:template&gt;
   		
	&lt;!-- Item Property--&gt;
	&lt;xsl:template name="item" match="item"&gt;
				"&lt;xsl:value-of select="string(entryId)"/&gt;":{
		&lt;xsl:apply-templates select="*"&gt;&lt;xsl:with-param name="indent"&gt;&lt;xsl:text&gt;			&lt;/xsl:text&gt;&lt;/xsl:with-param&gt;&lt;/xsl:apply-templates&gt;
				}&lt;xsl:if test="($KalturaHasNextItem = '1') or (count(/rss/channel/items/item) &gt; 1 and position() &lt; last())"&gt;,&lt;/xsl:if&gt;
    &lt;/xsl:template&gt;	
	

	
    &lt;!-- Object or Element Property--&gt;
    &lt;xsl:template match="*"&gt;
    	&lt;xsl:param name="indent"/&gt;
    	&lt;xsl:value-of select="$indent"/&gt;
    	&lt;xsl:text&gt;"&lt;/xsl:text&gt;
        &lt;xsl:value-of select="name()"/&gt;" : &lt;xsl:call-template name="Properties"&gt;&lt;xsl:with-param name="indent" select="$indent"/&gt;&lt;/xsl:call-template&gt;
    &lt;/xsl:template&gt;

    &lt;!-- Array Element --&gt;
    &lt;xsl:template match="*" mode="ArrayElement"&gt;
    	&lt;xsl:param name="indent"/&gt;
    	&lt;xsl:value-of select="$indent"/&gt;
        &lt;xsl:call-template name="Properties"&gt;&lt;xsl:with-param name="indent" select="$indent"/&gt;&lt;/xsl:call-template&gt;
    &lt;/xsl:template&gt;

    &lt;!-- Object Properties --&gt;
    &lt;xsl:template name="Properties"&gt;
    	&lt;xsl:param name="indent"/&gt;
        &lt;xsl:variable name="childName" select="name(*[1])"/&gt;
        &lt;xsl:choose&gt;
            &lt;xsl:when test="not(*|@*)"&gt;
				&lt;xsl:variable name="myVar1"&gt;
					&lt;xsl:text&gt;"&lt;/xsl:text&gt;
					&lt;xsl:call-template name="safe-json-string"&gt;
						&lt;xsl:with-param name="text" select="." /&gt;
					&lt;/xsl:call-template&gt;
					&lt;xsl:text&gt;"&lt;/xsl:text&gt;
				&lt;/xsl:variable&gt;
				&lt;xsl:value-of select="$myVar1" disable-output-escaping="yes"/&gt;
			&lt;/xsl:when&gt;
            &lt;xsl:when test="count(*[name()=$childName]) &gt; 1"&gt;
            	&lt;xsl:text&gt;{
			&lt;/xsl:text&gt;
				&lt;xsl:value-of select="$indent"/&gt;
				&lt;xsl:text&gt;"&lt;/xsl:text&gt;
				&lt;xsl:value-of select="$childName"/&gt;
				&lt;xsl:text&gt;" : [
		&lt;/xsl:text&gt;
				&lt;xsl:apply-templates select="*" mode="ArrayElement"&gt;
					&lt;xsl:with-param name="indent"&gt;&lt;xsl:value-of select="$indent"/&gt;&lt;xsl:text&gt;		&lt;/xsl:text&gt;&lt;/xsl:with-param&gt;
				&lt;/xsl:apply-templates&gt;
				&lt;xsl:text&gt;
			&lt;/xsl:text&gt;
				&lt;xsl:value-of select="$indent"/&gt;
				&lt;xsl:text&gt;]
		&lt;/xsl:text&gt;
				&lt;xsl:value-of select="$indent"/&gt;}
            &lt;/xsl:when&gt;
            &lt;xsl:otherwise&gt;
            	&lt;xsl:text&gt;{
		&lt;/xsl:text&gt;
				&lt;xsl:apply-templates select="@*"&gt;
					&lt;xsl:with-param name="indent"&gt;&lt;xsl:value-of select="$indent"/&gt;&lt;xsl:text&gt;	&lt;/xsl:text&gt;&lt;/xsl:with-param&gt;
				&lt;/xsl:apply-templates&gt;
				&lt;xsl:if test="(count(@*) &gt; 0) and (count(*[name()=$childName]) &gt; 0)"&gt;&lt;xsl:text&gt;,
		&lt;/xsl:text&gt;
				&lt;/xsl:if&gt;
				&lt;xsl:apply-templates select="*"&gt;&lt;xsl:with-param name="indent"&gt;&lt;xsl:value-of select="$indent"/&gt;&lt;xsl:text&gt;	&lt;/xsl:text&gt;&lt;/xsl:with-param&gt;&lt;/xsl:apply-templates&gt;
				&lt;xsl:text&gt;
		&lt;/xsl:text&gt;
				&lt;xsl:value-of select="$indent"/&gt;
				&lt;xsl:text&gt;}&lt;/xsl:text&gt;
			&lt;/xsl:otherwise&gt;
        &lt;/xsl:choose&gt;
        &lt;xsl:if test="following-sibling::*"&gt;,
        &lt;/xsl:if&gt;
    &lt;/xsl:template&gt;

    &lt;!-- Attribute Property --&gt;
    &lt;xsl:template match="@*"&gt;
    	&lt;xsl:param name="indent"/&gt;
		&lt;xsl:variable name="myVar"&gt;
			&lt;xsl:call-template name="safe-json-string"&gt;
				&lt;xsl:with-param name="text" select="." /&gt;
			&lt;/xsl:call-template&gt;
		&lt;/xsl:variable&gt;
		&lt;xsl:value-of select="$indent"/&gt;
		&lt;xsl:text&gt;"&lt;/xsl:text&gt;
		&lt;xsl:value-of select="name()"/&gt;" : "&lt;xsl:value-of select="$myVar"/&gt;
		&lt;xsl:text&gt;"&lt;/xsl:text&gt;		
		&lt;xsl:if test="position() != last()"&gt;,
		&lt;/xsl:if&gt;
    &lt;/xsl:template&gt;
	
	
	&lt;!-- replace string --&gt;
	&lt;xsl:template name="string-replace-all"&gt;
    &lt;xsl:param name="text" /&gt;
    &lt;xsl:param name="replace" /&gt;
    &lt;xsl:param name="by" /&gt;
    &lt;xsl:choose&gt;
      &lt;xsl:when test="contains($text, $replace)"&gt;
        &lt;xsl:value-of select="substring-before($text,$replace)" /&gt;
        &lt;xsl:value-of select="$by" /&gt;
        &lt;xsl:call-template name="string-replace-all"&gt;
          &lt;xsl:with-param name="text" select="substring-after($text,$replace)" /&gt;
          &lt;xsl:with-param name="replace" select="$replace" /&gt;
          &lt;xsl:with-param name="by" select="$by" /&gt;
        &lt;/xsl:call-template&gt;
      &lt;/xsl:when&gt;
      &lt;xsl:otherwise&gt;
        &lt;xsl:value-of select="$text" /&gt;
      &lt;/xsl:otherwise&gt;
    &lt;/xsl:choose&gt;
  &lt;/xsl:template&gt;

	&lt;xsl:template name="safe-json-string"&gt;
		&lt;xsl:param name="text" /&gt;
		&lt;xsl:variable name="myVar1Temp"&gt;
			&lt;xsl:call-template name="string-replace-all"&gt;
				  &lt;xsl:with-param name="text" select="$text" /&gt;
				  &lt;xsl:with-param name="replace" select="'\'" /&gt;
				  &lt;xsl:with-param name="by" select="'\\'" /&gt;
			&lt;/xsl:call-template&gt;				
		&lt;/xsl:variable&gt;
		&lt;xsl:variable name="myVar1"&gt;
			&lt;xsl:call-template name="string-replace-all"&gt;
				  &lt;xsl:with-param name="text" select="$myVar1Temp" /&gt;
				  &lt;xsl:with-param name="replace" select="'&quot;'" /&gt;
				  &lt;xsl:with-param name="by" select="'\&quot;'" /&gt;
			&lt;/xsl:call-template&gt;
		&lt;/xsl:variable&gt;
		&lt;xsl:value-of select="$myVar1"/&gt;
	&lt;/xsl:template&gt;
  
&lt;/xsl:stylesheet&gt;
</pre>
