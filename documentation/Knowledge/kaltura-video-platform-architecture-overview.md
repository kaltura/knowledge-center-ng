---
layout: page
title: "The Kaltura Video Platform Architecture Overview"
date: 2011-12-28 01:50:00
---

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="bottom">
        <p style="text-align: left;">
          <span style="font-family: verdana, geneva;">This article describes the Kaltura Video Platform Architecture.</span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-family: verdana, geneva;">To learn more about The Kaltura Architecture Framework that is part of the Kaltura Video Platform Architecture, see <a href="http://knowledge.kaltura.com/node/986">Understanding the Kaltura Application Framework</a>.</span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-family: verdana, geneva;">If you are unable to find the information that you are looking for here, please use the search bar above to search for the information you seek, or report a missing information: "<a href="http://knowledge.kaltura.com/node/86">Couldn't find what you were looking for</a>?” form.</span>
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-2">
  <span style="font-family: verdana, geneva;">Introduction to Kaltura’s Video Platform</span>
</p>

<span style="font-family: verdana, geneva;">Kaltura’s video platform is a modular system that exposes different web-services and that may be deployed in several deployment modes to support different levels of scale. Kaltura’s platform comes in different editions, including the Kaltura-hosted SaaS edition, managed by Kaltura for single publishers and Value Added Resellers (VARs), as well as in several licensing modes of the, self-hosted, Kaltura On-Prem™ edition: Kaltura Community Edition, Kaltura On-Prem™ for Publishers and Kaltura OnPrem™ for OEMs. </span>

<span style="font-family: verdana, geneva;">This article provides a description of Kaltura’s main service layers, system components and their recommended setup based on several scales of deployments. The article also recommends Kaltura’s ‘best practices’ for system architecture design, to be considered when planning self-hosted deployments of Kaltura’s platform.</span>

<p class="mce-heading-2">
  <span style="font-family: verdana, geneva;">Overview of Logical Layers</span>
</p>

<span style="font-family: verdana, geneva;">Kaltura’s online video platform relies on a modular software infrastructure, designed to enable flexible usage of Kaltura’s technologies and features. There are 5 main layers in Kaltura’s platform:</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Kaltura Core Technologies</span>
</p>

<span style="font-family: verdana, geneva;">The following diagram illustrates the logical layout of Kaltura’s Online Video Platform layers. </span>

  
<span style="font-family: verdana, geneva;"><img src="{{site.url}}/assets/1448">

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"> [collapsed title="Layer 1 - Kaltura Core Technology"] </span>

<span style="font-family: verdana, geneva;"><img src="{{site.url}}/assets/2134">

<span style="font-family: verdana, geneva;">The following list includes the main features of the Kaltura server-side implementation.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Storage and Hosting Services</span>
</p>

<span style="font-family: verdana, geneva;">Kaltura's hosted SaaS Edition offers robust storage and hosting services. Kaltura's servers operate out of state-of-the-art data centers with the highest levels of stability, redundancy and security. Kaltura’s, self-hosted, On-Prem™ edition allows service providers and publishers to set-up their own hosting and storage infrastructure (see below "best practices for self-hosting and hardware considerations").</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Content Delivery and Streaming Services</span>
</p>

<span style="font-family: verdana, geneva;">Kaltura's content delivery and streaming is based on optimizing and reselling tier-1 CDN services, including those of Akamai, Limelight Networks, and Level3 Communications. The streaming infrastructure ensures the best media delivery performance possible, even when working with high volumes of content and audience and when utilizing different streaming methods (e.g. progressive download, RTMP, HTTP Streaming). Optionally, Kaltura's platform can be integrated with other CDNs and delivery components, so self-hosting service providers and publishers can customize their Kaltura setup for integrating their system to work with their CDN of choice or to utilize their local streaming facilities.</span>

<span style="font-family: verdana, geneva;">Kaltura supports 2 alternative content delivery paths via CDN:</span>

1.  <span style="font-family: verdana, geneva;">Using Kaltura's platform local storage as the CDN origin  - this is the standard delivery mode for publisher accounts hosted on Kaltura's  SaaS platform.</span>
2.  <span style="font-family: verdana, geneva;">Utilizing publishers' storage accounts on their CDN (e.g. Akamai NetStorage) to be used as the CDN storage origin, while still managing their content on Kaltura.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Media Ingestion and Transcoding Services</span>
</p>

<span style="font-family: verdana, geneva;">The Kaltura platform applies a transcoding process after media upload. Per the account's transcoding settings, video files are transcoded into the required format and codecs to enable web publishing in adaptive qualities and on multiple devices (including different mobile and iOS devices), while supporting all popular media codecs. Each media file is handled according to its type based on a set of pre-defined adjustable parameters, such as transcoder type, quality (bit rate), aspect ratio, and video viewing optimization. These parameters can be set by publishers to provide the best streaming and editing capabilities required to support their media workflow needs. Each source file could be transcoded into multiple flavors – i.e. files with different bitrates, dimensions, and quality. During playback the player selects the most appropriate flavor for playback based on the viewer's available bandwidth, player dimensions, and CPU usage.  Kaltura's unique technology combines several transcoding components with in-house utilities and shell scripts. In addition, Kaltura's platform comes pre-integrated with commercial transcoders. Advanced ingestion options are also available to support the ingestion of multiple flavors, that were generated on the publisher's local transcoding engine into the Kaltura system as well as further automated ingestion workflows utilizing an ingestion drop folders mechanism.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Media Manipulation Services</span>
</p>

<span style="font-family: verdana, geneva;">The platform provides core capabilities of media manipulation, including: thumbnail generation, image cropping and resizing, video trimming, video transitions, video overlaying (annotations), video effects, audio and voice control, video speed control and more. In addition, the platform supports conversion of Office documents (PPT, DOC, XLS, PDF) into SWF files that are playable in the Kaltura player, as well as synchronization and playback of the converted documents with a selected video, creating a  single user interface for a synchronized view of video and document content.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Media Management Services</span>
</p>

<span style="font-family: verdana, geneva;">The platform provides a comprehensive set of media management capabilities and tools. Publishers can easily upload their media, manage and populate a comprehensive set of metadata fields, and organize their media within playlists and gallery widgets while applying filtering criteria and paging options. In addition, Kaltura's system includes media moderation tools enabling publishers to implement safe and controlled UGC functionalities within their web sites.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Account Management Services</span>
</p>

<span style="font-family: verdana, geneva;">The platform provides publisher administration capabilities and tools. Publishers are able to fully manage their accounts, to ensure publisher-level web security while relying on their unique identifiers and secret keys, to configure their specific server settings and more. Administrators of self-hosted deployments of the Kaltura platform can manage multiple accounts for publishers registered to their Kaltura deployments. </span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">User Management Services</span>
</p>

<span style="font-family: verdana, geneva;">The platform provides user administration capabilities allowing publishers to provision multiple user accounts and assign each user to a pre-defined or custom role. Publisher admins can define specific user roles for providing different levels of permissions to content management and administration functionalities according to their specific organizational needs. In addition publishers are able to relate their internal user identifiers to the media uploaded to the system and, by doing so, to enable user specific media functionality, as well as media related social networking activities on their web sites.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Advertising & Monetization Services</span>
</p>

<span style="font-family: verdana, geneva;">Kaltura's media players come with built-in support for in-stream and companion rich-media advertising. This enables publishers to implement an advertising solution supporting a wide variety of ad formats and ad sources. Kaltura's media players may include the following advertising modes: Simple advertising deployment, Overlay ads, Ad timing configuration, Companion ads, Ad frequency configuration, and Ad reporting and analytics. Kaltura also supports pay-per-view functionalities, like blocking unauthorized access using increased security hashed URL's and Server Secrets. A ‘free preview' feature enables publisher to configure the occurrence and duration of free previews before a fee is charged.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Web Video Analytics Services</span>
</p>

<span style="font-family: verdana, geneva;">Kaltura provides a built-in web video analytics infrastructure combined with a state-of-the-art reporting tool. These technologies provide publishers the ability to track and understand their end-users' video related behavior, and to better monetize their web media services. Kaltura's reporting tool includes user-specific as well as aggregated indicators for media analytics and audience measurement, including: number of contributors, number of syndications, top played content, number of plays, media plays latency, media play drop-offs, number of user interactions with media, media indicators per media type and more.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Media Syndication and Distribution Services</span>
</p>

<span style="font-family: verdana, geneva;">Kaltura provides integrated social syndication technologies within its players, allowing end-users to easily distribute videos to their own web sites, to the most popular social networks sites and blogging platforms, to simply distribute videos to their friends via emails or to locally download videos for their personal use. In addition to social syndication Kaltura's platform provides capabilities and tools for enabling automated multi-destination syndication and distribution of content. Publishers are able to create playlist based syndication feeds for maximizing their content's reach and generate traffic back to their site.  Access Control can be set for each content item/group to limit the access to specific countries, domains or times (scheduling).</span>

<span style="font-family: verdana, geneva;">Kaltura's content distribution infrastructure enables media companies and content creators to create and automate customized video packages to send to distribution partners directly from within the KMC. Administrators are able to control the destinations for each video package, and for each distribution destination admins can control the video qualities, multiple thumbnails in different sizes, metadata, scheduling data, and more. </span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Styling & Branding Services</span>
</p>

<span style="font-family: verdana, geneva;">Kaltura provides tools and the API to customize the style, branding and functionality of the video player, as well as that of additional widgets (e.g. the Upload/Import widget, and the Video Editor). This allows publishes to maintain a consistent UI, and opens up monetization opportunities by way of custom skins that can be sold to advertisers. [/collapsed]</span>

<span style="font-family: verdana, geneva;"></span><span style="font-family: verdana, geneva;">[collapsed title="Layer 2 - Kaltura API Client Libraries"]</span>

<span style="font-family: verdana, geneva;"><img src="{{site.url}}/assets/2132">

<span style="font-family: verdana, geneva;">[collapsed title="Layer 3 - Kaltura Widgets"] <br /></span>

<span style="font-family: verdana, geneva;"><img src="{{site.url}}/assets/2130">

<span style="font-family: verdana, geneva;">The Kaltura platform includes self-contained, client-side components called Kaltura Widgets, which implement specific APIs in Flash or HTML. Kaltura widgets can be customized, skinned and easily embedded within publisher’s websites. Kaltura widgets rely on advanced web technologies, encapsulating graphics, media functionalities, and workflow events control along with direct access to Kaltura core technologies (via the Kaltura web services layer). Kaltura’s most commonly used widgets include: the <a href="http://knowledge.kaltura.com/kaltura-simple-uploader-ksu">Kaltura Simple Uploader</a>, <a href="http://knowledge.kaltura.com/node/416">Kaltura Contributor Wizard</a> (KCW) <a href="http://knowledge.kaltura.com/node/353#ksr">Kaltura Screen Recorder</a> and the <a href="http://html5video.org/wiki/Kaltura_HTML5_Video_Library">HTML5 Player</a>.</span>

<span style="font-family: verdana, geneva;">Some Kaltura widgets (specifically the Kaltura Dynamic Player) implement internal hooks to enable the widget’s integration with a Kaltura or a 3<sup>rd</sup> party plug-in applications. Such plug-in applications are then used to provide Kaltura widgets’ functionality with complementary media services. Examples of 3<sup>rd</sup> party services already integrated as a plug-in within Kaltura widgets are: Doubleclick for Publishers (DFP) ad services powered by Google, Ad services powered by Adap.tv, Ad services powered by Tremor Media, Ad services supporting VAST based ad servers, Media social syndication services powered by Gigya, and subtitle editing services powered by PLYmedia. [/collapsed]</span>

<span style="font-family: verdana, geneva;">[collapsed title="Layer 4 - Kaltura Application Framework"]</span>

<span style="font-family: verdana, geneva;"><img src="{{site.url}}/assets/2133">

<span style="font-family: verdana, geneva;"><br /><img src="{{site.url}}/assets/2128">

<span style="font-family: verdana, geneva;"><span class="mce-heading-3">KMC</span>The Kaltura Management Console, (KMC) is a basic Kaltura application, available to administrators of all publisher accounts, which provides a comprehensive and user friendly tool for utilizing Kaltura’s media and account management core capabilities, including content importing/uploading, sorting/filtering/moderating, creation of playlists, configuration of widgets’ features and graphic interface, management of publishers’ account and server settings, user administration and reporting and analytics.</span>

<span style="font-family: verdana, geneva;"><span class="mce-heading-3">KAC</span>The Kaltura Admin Console is a basic Kaltura application, available to Kaltura On-Prem platform administrators which provides a comprehensive and user friendly tool for utilizing Kaltura’s system and service administration capabilities including: publisher management and configuration, server batch processing control, system monitoring and developers tools.</span>

<span style="font-family: verdana, geneva;"><span class="mce-heading-3">KMS</span>The Kaltura MediaSpace application allows you to instantly launch a video-centric website, where users users can create, upload, share, search, browse, and watch live and on demand videos, video presentations, screencasts, and other rich media content. MediaSpace provides superb cross device user experience, unmatched user engagement capabilities, and powerful control and governance tools. </span>

<span style="font-family: verdana, geneva;"><span class="mce-heading-3">Kaltura MediaGo</span>The Kaltura MediaGo application is a market-leading set of end user applications for connected devices such as iOS, Android, web and TVs. The different device applications are designed to unlock Kaltura’s full offering, while offering customized experiences for different screens, capabilities and use-cases, and enabling a consistent cross-device experience.[/collapsed]</span>

<p class="mce-heading-2">
  <span style="font-family: verdana, geneva;">Overview of Functional Components</span>
</p>

<span style="font-family: verdana, geneva;">The platform's logical layers, described in the previous section, are implemented using several different functional components that are listed in this section. Some of the components must be deployed as part of the core platform (i.e. the service will not operate without them), and some are optional, whereby the decision for their deployment is derived from the applicative needs and/or from the necessary scale of the deployment. All optional components are operable as part of Kaltura SaaS edition deployment.</span>

<span style="font-family: verdana, geneva;">[collapsed title="Required Components"] </span><span style="font-family: verdana, geneva;">The following components must operate within Kaltura’s online video platform:</span>

1.  <span class="mce-sub-heading" style="font-family: verdana, geneva;">Kaltura Web Services </span>  
    <span style="font-family: verdana, geneva;">Apache server and Kaltura web services layer in the form of a set of Application Programming Interfaces (API) as a single access point for client-server applicative communication. This module should be deployed on front-end server/s (traffic distributed by load balancing equipment).</span>
2.  <span class="mce-sub-heading" style="font-family: verdana, geneva;">Kaltura Batch Jobs</span>  
    <span style="font-family: verdana, geneva;">Scalable middleware entities deployed on back-end server/s. Central orchestration of atomic batch services such as media import, media info extraction, transcoding, server notification and others. This module should be deployed on a backend server. </span>
3.  <span class="mce-sub-heading" style="font-family: verdana, geneva;">Kaltura Transcoding Engine</span>  
    <span style="font-family: verdana, geneva;">This module manages all media transcoding tasks, by utilizing open source and/or commercial transcoders. This is a CPU intensive module and could either be deployed on a backend server at a local deployment or can be distributed using independent transcoding servers deployed in a cloud solution. </span>
4.  <span class="mce-sub-heading" style="font-family: verdana, geneva;">Shared Storage</span>  
    <span style="font-family: verdana, geneva;">A dedicated disk space that is shared and accessible by all of Kaltura’s servers within a specific deployment. The Shared storage holds all content and application files, including: media assets, Kaltura flash widgets/applications, skins, thumbnails, players/playlist configuration files (UI conf) etc. The shard storage can be deployed as part of a local deployment or using independent storage within a cloud solution.</span>
5.  <span class="mce-sub-heading" style="font-family: verdana, geneva;">Operational Database</span>  
    <span style="font-family: verdana, geneva;">This is the applicative database, used for storing and managing both content related data (metadata, identifiers, URLs etc.) as well as application and business logic supporting data. The operational database should be deployed as part of a local deployment, preferably on dedicated server/s utilizing a master/slave topology. </span>
6.  <span class="mce-sub-heading" style="font-family: verdana, geneva;">Search Server</span>  
    <span style="font-family: verdana, geneva;">Full text search servers based on the <a href="http://sphinxsearch.com/" target="_blank">Sphinx</a> open source solution for fast indexing and search.</span>
7.  <span class="mce-sub-heading" style="font-family: verdana, geneva;">Site Admin Module</span>  
    <span style="font-family: verdana, geneva;">This module is responsible for operating Kaltura’s Admin Console, enabling site administrators to monitor and operate their own deployment of Kaltura’s online video platform. For full monitoring, it is important to deploy this module on a local separate server. </span>
8.  <span class="mce-sub-heading" style="font-family: verdana, geneva;">Media Analytics Module </span>  
    <span style="font-family: verdana, geneva;">This module is responsible for processing and aggregating Kaltura’s video analytics data into a dedicated Data Warehouse (DWH), and the production of video usage and behavior reports. The module includes the data Exporting, Transforming and Loading processes (ETL), a DWH database, and the reporting utilities in use. This module can be deployed as part of a local deployment or can be distributed using independent analytics servers deployed in a cloud solution.[/collapsed] </span>

<span style="font-family: verdana, geneva;">[collapsed title="Optional Components"] </span>

<div>
  <ol>
    <li>
      <span style="font-family: verdana, geneva;"><span class="mce-sub-heading"><span class="mce-sub-heading">MediaSpace (Optional)<br /></span></span>Kaltura MediaSpace is a fully customizable media destination site for the organization. MediaSpace is an out-of-the-box video-centric site that can serve as a repository for media collections across the organization or a full-featured "internal YouTube. It can be integrated into the local authentication environment for role-based authentication, or use it as a public destination site. It can be easily configured and branded, and requires minimal resources to get up and running while allowing extensive customization.</span>
    </li>
    <li>
      <span style="font-family: verdana, geneva;"><span class="mce-sub-heading"><span class="mce-sub-heading">Document Conversion Module (Optional)<br /></span></span>The Document Conversion Module converts various document formats into a Flash based swf document, later to be used within the Kaltura Dynamic Player as a synchronized slideshow alongside a video. The supported document formats include the following: MS Office documents (for example. Word, PowerPoint), Open Office documents, and Adobe PDF. The document conversion process can be distributed using independent document conversion servers deployed in a cloud solution. Each server must run Open Office and MS to perform the document conversion.</span>
    </li>
    <li>
      <span class="mce-sub-heading" style="font-family: verdana, geneva;">Video Recording Module (Optional)</span><br /><span style="font-family: verdana, geneva;">This module is responsible for recording web camera streams; it is an optional component to be deployed only when there is a need to support video recording functionalities. Kaltura operates this module using the Adobe FMIS (Flash Media Interactive Server) solution.  Using a local FMS of another provider is possible as well but may require validation.</span>
    </li>
    <li>
      <span style="font-family: verdana, geneva;"><span class="mce-sub-heading"><span class="mce-sub-heading">Lecture Capture (Optional)<br /></span></span>Kaltura CaptureSpace enables easy capture in class, at home or on-the-go with automated publishing and interactive viewing within the LMS and Kaltura’s MediaSpace video portal. CaptureSpace is a professional and all-inclusive capture solution.</span>
    </li>
    <li>
      <span style="font-family: verdana, geneva;"><span class="mce-sub-heading"><span class="mce-sub-heading">Web Conferencing<br /></span></span>Whether you’re using WebEx, Go2Meeting, Lync, Vidyo or others, Kaltura web-conferencing connectors maximize the effectiveness of your web-conferences and significantly reduce storage and other costs.</span>
    </li>
    <li>
      <span style="font-family: verdana, geneva;"><span class="mce-sub-heading"><span class="mce-sub-heading">Webcasting<br /></span></span>Kaltura Webcasting supports internal delivery, ingest from different encoders and source types, archiving of webcasts to your VOD portal and enhanced interactive features. This all makes it easy for your organization to optimize internal communication and increase return on investment for customer facing communications.</span>
    </li>
    <li>
      <span style="font-family: verdana, geneva;"><span class="mce-sub-heading"><span class="mce-sub-heading">Live Streaming<br /></span></span>The Kaltura live streaming platform enables you to broadcast live events or 24/7 broadcasts to any screen. A Kaltura live stream can be provisioned in the Kaltura Management Console (KMC) or directly from applications such as MediaSpace. Kaltura live streaming supports both passthrough and cloud encoding with multi protocol output for HLS, HDS, MPEG-DASH and Smooth Streaming.  Kaltura live streams can be delivered through a Content Delivery Network (CDN) such as Akamai, as well as support internal delivery in diverse network topologies with support for eCDNs and Multicast. Kaltura live streaming also supports Live to VOD with a single embed code, instant provisioning and live captions passthrough.  </span>
    </li>
    <li>
      <span style="font-family: verdana, geneva;"><span class="mce-sub-heading">DRM<br /></span>Kaltura is a <a href="http://www.widevine.com/cwip/index.html">Certified Widevine Implementation Partner</a> that is authorized to provide Widevine DRM services.  Kaltura offers an out-of-the-box DRM solution integrated with Kaltura’s Dynamic (Flash) Player (KDP) while also enabling its customer to integrate their device specific applications with Widevine’s DRM packaging and license services according to the application specific workflow.[/collapsed] </span>
    </li>
  </ol>
</div>

<p class="mce-heading-2">
  <span style="font-family: verdana, geneva;">Overview of Physical Setup</span>
</p>

<span style="font-family: verdana, geneva;">The physical deployment of the Kaltura platform is flexible and should be tailored according to the size and applicative needs of the specific site deployment.  For optimal resource utilization as well as security reasons, Kaltura platform deployment should be separated to a front-end layer and a back-end layer.</span>

<span style="font-family: verdana, geneva;"><span> [collapsed title="Sample Deployment Architecture"]</span> </span>

<span style="font-family: verdana, geneva;">The following diagram illustrates a sample deployment architecture:</span>

<span style="font-family: verdana, geneva;"><img src="{{site.url}}/assets/886">

<table class="kaltura-table" style="width: 100%;">
  <thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;"> Category</span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;"> Component Name</span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;"> Description</span>
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;"> </span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Load Balancers  </span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">LVS based , running on Linux server.  In a Kaltura On-Prem deployment, load balancing equipment and setup is the site administrator’s responsibility and is not part of the Kaltura platform setup. </span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">API</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Web Servers</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Kaltura API and access to shared content</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span>API</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Thumbnails Server (optional)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Dedicated servers for generating thumbnails from images or videos  - In most On-Prem deployment types thumbnail processing is  done on the front end servers.</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span>API</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Admin Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Monitoring and application administration</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Data</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">MYSQL1  - Master DB</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Primary SQL server for write operations</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Data</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">MYSQL2  - Slave DB (optional)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">SQL servers for read only operations</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Data</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Analytics (DWH DB)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Server running Analytics ETL software and data warehouse database</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Data</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Shared Storage</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">External storage contains all Kaltura media entities shared to all relevant servers over a distributed file system</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;"> </span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">FMS Server (optional)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Servers for webcam recording</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Batch</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Batch Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Kaltura dedicated batch servers</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Batch</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Document Conversion Server (optional)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Windows based server running document conversion application</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Batch</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Encoder Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Kaltura generic Linux-based encoding server</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;"> </span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Internal API  Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Internal API servers for Kaltura batch servers</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;"> </span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">FTP server (optional)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">FTP server for pushing logs from CDN to the Kaltura platform for updating delivery usage metrics into the Kaltura data warehouse</span>
      </td>
    </tr>
  </tbody>
</table>

<span style="font-family: verdana, geneva;"><span>[/collapsed] </span></span>

<span style="font-family: verdana, geneva;"><span></span></span><span style="font-family: verdana, geneva;">[collapsed title="Virtualization"]</span>

<span style="font-family: verdana, geneva;">All server components listed in this section can be set on a physical machine or run on top of a virtualization infrastructure. Kaltura provides a standard VMware image to be deployed and run on a VMware ESXi Hypervisor setup. In this case dedicated hardware should be <a href="http://partnerweb.vmware.com/comp_guide2/search.php" target="_blank">VMWare ESXi compatible</a>.[/collapsed]</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"> [collapsed title="Standard Setup Sizes"]</span>

<span style="font-family: verdana, geneva;">The following sections describe Kaltura’s recommendation for required hardware to be set for initial setup of an instance of the Kaltura platform. Specific site assessment can be made by Kaltura’s engineering and IT teams upon request.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Small - Single Server Setup</span>
</p>

<span style="font-family: verdana, geneva;">Single server setup may be suitable in the following cases, all assuming low traffic and CPU utilization:</span>

*   <span style="font-family: verdana, geneva;">Small deployment of a Kaltura Community Edition instance.</span>
*   <span style="font-family: verdana, geneva;">Platform deployment dedicated for providing limited usage video capabilities to a CMS/LMS platform while using Kaltura CMS/LMS extensions</span>
*   <span style="font-family: verdana, geneva;">Platform deployment used for development or platform evaluation purposes.</span>

<span style="font-family: verdana, geneva;">In this setup, all required components are deployed on one server. Document conversion module and workflow cannot be utilized in this topology.</span>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Medium - Distributed Site Setup</span>
</p>

<span style="font-family: verdana, geneva;">This physical setup is suitable as an initial setup for small to medium-size deployments of the Kaltura platform, that are expected to serve medium to high traffic/streaming volume and medium to high number of video uploads and transcoding operations. With growth in service utilization this initial setup can be scaled up as needed, to add the required server type (e.g. additional transcoding servers, additional database servers for replications, additional front end server etc).<span style="text-align: left;"></span></span>

<table class="kaltura-table" style="width: 100%;">
  <thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;">Server </span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;">Recommended Hardware Specs. </span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;">Operable Components </span>
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;"> Load Balancing Server/s</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Site Admin responsibility </span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Site Admin responsibility </span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Platform Shared Storage</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Can reside on one of the platform servers. Storage size to be set according to the expected volume of media assets.</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">On average - 3X size of the expected video source files (assuming source should be stored as well).</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">To be accessible by the Kaltura platform servers via NFS.</span>
        </p>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Stroage</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">2 Front-End Servers</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">64bit based Linux OS with  4-8 GB RAM and 1 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Kaltura Web Services Module, on top of an apache server</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Kaltura Video Recording Module  (if applicable)</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Back-End Batch Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">64bit based Linux OS with at least 4GB RAM and 1 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Batch Jobs Module</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Back-End Transcoding Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">64bit based Linux OS with at least 8GB RAM and 2 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Transcoding Module</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Back-End DB Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">64bit based Linux OS with at least 4GB RAM and 1 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Operational Database</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Sphinx – full text search engine</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Back-End DWH Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">64bit based Linux OS with at least 8GB RAM and 1 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Video Analytics Module</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Site Admin Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Linux based OS.</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">No minimal specifications on hardware</span>
        </p>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Site Admin Module </span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Document Conversion Server (optional)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Windows server 2008 With at least 2GB RAM. 1 CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Kaltura Document Conversion Module (if applicable)</span>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <span style="font-family: verdana, geneva;">Large - Full Distributed Site Setup</span>
</p>

<span style="font-family: verdana, geneva;">This physical setup may be suitable as an initial setup for large-size deployments of a Kaltura platform, that are expected to serve high traffic/streaming volume and high number of video uploads and transcoding needs.  With any growth in service utilization this initial setup can be scaled up as needed, to add the required server type (e.g. additional transcoding servers, additional database replication server, additional front end server etc).</span>

<span style="font-family: verdana, geneva;">This setup may include the following servers:</span>

<table class="kaltura-table" style="width: 100%;">
  <thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;">Server </span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;">Recommended Hardware Specs. </span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;">Operable Components </span>
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;"> Load Balancing Server/s</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Site Admin responsibility </span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Site Admin responsibility </span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Few Front-End Servers</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Several 64bit based Linux OS with at least 8GB RAM and 1 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Kaltura Web Services Module, on top of an apache server.</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Kaltura Video Recording Module  (if applicable)</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Few Back-End Batch Servers</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Several 64bit based Linux OS with at least 4GB RAM and 1 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Batch Jobs Module</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Few Back-End Transcoding Servers</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Several 64bit based Linux OS with at least 8GB RAM and 2 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Transcoding Module</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Few Back-End DB Server/s  (master + replications)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">64bit based Linux OS with at least 4GB RAM and 1 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Operational Database</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Back-End DWH Server/s</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">64bit based Linux OS with at least 16 GB RAM and 1 quad core CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Video Analytics Module</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Site Admin Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Linux based OS. No minimal specifications on hardware</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">Site Admin Module </span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Connected to Shared Storage (NFS)</span>
        </p>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Document Conversion Server/s (optional)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Windows server 2008. With at least 2GB RAM. 1 CPU</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Kaltura Document Conversion Module (if applicable) </span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Shared Storage Dedicated Server</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <p>
          <span style="font-family: verdana, geneva;">64bit based Linux OS with at least 4GB RAM and 1 quad core CPU</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">On average - 3X size of the expected video source files (assuming source should be stored as well)</span>
        </p>
        
        <p>
          <span style="font-family: verdana, geneva;">Storage size to be set according to the expected volume of media assets</span>
        </p>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Shared Storage</span>
      </td>
    </tr>
  </tbody>
</table>

[/collapsed] 

<span style="font-family: verdana, geneva;"> [collapsed title="Multple Data-Centers Site Setup"]</span>

<span style="font-family: verdana, geneva;">For enabling full redundancy and better performance for end users, utilization of multiple data centers may be needed. The geographic location of the data center should be chosen according to the geo-location distribution of the end users.  </span>

<span style="font-family: verdana, geneva;">The synchronization of multiple data centers should be performed on both database and storage. For database synchronization a native MySQL Master-Master replication can be utilized.</span>

<span style="font-family: verdana, geneva;">For media files synchronization, a batch process can copy media items from one datacenter to the other datacenter, in order to maintain full online redundancy.  Below is a diagram illustrating the architecture of a multi-datacenter setup of the Kaltura Platform.</span>

<span style="font-family: verdana, geneva;"><img src="{{site.url}}/assets/186">

<span style="font-family: verdana, geneva;"> [collapsed title="Self-Streaming Considerations"]</span>

<span style="font-family: verdana, geneva;">In most cases, when planning for a new deployment of the Kaltura online video platform, a use of external CDN functionality is recommended. When this is not possible and/or not required, it is recommended to add additional front-end hardware to be dedicated for playback streaming.  </span>

<span style="font-family: verdana, geneva;">Kaltura recommends the following addition to site setup in such cases:</span>

<table class="kaltura-table" style="width: 100%;">
  <thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;"> Server</span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;"> Recommended Hardware Specs.</span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 33%; text-align: center;">
        <span style="font-family: verdana, geneva;"> Operable Components</span>
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;"> Streaming proxy servers</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">2 servers with  64bit based Linux OS, at least 8GB RAM and 1 quad core CPU </span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 33%; text-align: left;">
        <span style="font-family: verdana, geneva;">Media streaming (relevant for self-streaming deployments) </span>
      </td>
    </tr>
  </tbody>
</table>

<span style="font-family: verdana, geneva;">[/collapsed]</span>

<span style="font-family: verdana, geneva;"> </span>

<span style="font-family: verdana, geneva;"> [collapsed title="Additional Scalability Considerations"];</span>

<span style="font-family: verdana, geneva;">The following table includes estimated sizing calculations that may be useful for determining the required hardware for setting up a new deployment of the Kaltura online video platform:</span>

<div>
  <table class="kaltura-table" style="width: 100%;">
    <thead>
      <tr class="kaltura-table-header">
        <th class="kaltura-table-head-item" style="width: 50%; text-align: center;">
          <span style="font-family: verdana, geneva;"> Factor</span>
        </th>
        
        <th class="kaltura-table-head-item" style="width: 50%; text-align: center;">
          <span style="font-family: verdana, geneva;"> Estimated Sizing Information</span>
        </th>
      </tr>
    </thead>
    
    <tbody>
      <tr class="kaltura-table-row">
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">Storage Resources </span>
        </td>
        
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <p>
            <span style="font-family: verdana, geneva;">As a general rule of thumb, in order to have multiple flavors generated for each video entry, including mobile flavors, - storage of 3X the size of the expected video source files should be reserved (assuming source should be stored as well).</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Example of storage calculation: </span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Original video clip at backup storage:</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Bit rate = 8000 kbps - good quality camera recording</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Storage Size = ~60 Mb for a one minute duration</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;"> </span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Normal Web Quality Flavor (transcoded files)</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Bit rate = 600 kbps</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Storage Size = 4-8 MB for a one minute duration = ~ 7.5% of Original</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;"> </span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">High Web Quality Flavor (transcoded files)</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Bit rate = 1200 kbps</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">Storage Size = 8-16 MB for a one minute duration = ~ 15% of Original</span>
          </p>
        </td>
      </tr>
      
      <tr class="kaltura-table-row">
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">Transcoding Resources</span>
        </td>
        
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <p>
            <span style="font-family: verdana, geneva;">Each CPU allows for 360-720 video hours of transcoding per month</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">One CPU can handle one transcoding task at a time. </span>
          </p>
        </td>
      </tr>
      
      <tr class="kaltura-table-row">
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">Playback Streaming</span>
        </td>
        
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <p>
            <span style="font-family: verdana, geneva;">The actual streaming volume can be deduced from the single clip storage size and site usage information. </span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">if CDN is in use - most streaming volume is handled by CDN provider (excluding cases of long tail media type) </span>
          </p>
        </td>
      </tr>
      
      <tr class="kaltura-table-row">
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">Video Recording Streaming (if applicable)</span>
        </td>
        
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <p>
            <span style="font-family: verdana, geneva;">Each FMS server can hold hundreds of concurrent recording connections</span>
          </p>
          
          <p>
            <span style="font-family: verdana, geneva;">30 days * 24 hours = 720 streaming hours a month per connection </span>
          </p>
        </td>
      </tr>
      
      <tr class="kaltura-table-row">
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">Web Services</span>
        </td>
        
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">One front-end server can support ~75,000 daily unique users (API calls and playback streaming to CDN when CDN is in use) </span>
        </td>
      </tr>
      
      <tr class="kaltura-table-row">
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">Operational Database</span>
        </td>
        
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">2 quad core DB Machines running in a master/slave topology can hold tens of millions of media items </span>
        </td>
      </tr>
      
      <tr class="kaltura-table-row">
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">Video Analytics</span>
        </td>
        
        <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
          <span style="font-family: verdana, geneva;">1 quad core DB Machine for storing 6 months of historical data for tens of millions of media items </span>
        </td>
      </tr>
    </tbody>
  </table>
</div>

<span style="font-family: verdana, geneva;">The following aspects should be taken into account as a basis for a scale-up decision:</span>

<table class="kaltura-table" style="width: 100%;">
  <thead>
    <tr class="kaltura-table-header">
      <th class="kaltura-table-head-item" style="width: 50%; text-align: center;">
        <span style="font-family: verdana, geneva;"> Scale up Reason</span>
      </th>
      
      <th class="kaltura-table-head-item" style="width: 50%; text-align: center;">
        <span style="font-family: verdana, geneva;"> Scale up Activity</span>
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;"> Back-end server/s CPU’s are repeatedly overloaded due to increase in number of transcoding operations</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">Move transcoding to a dedicated  server or add a dedicated transcoding server </span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">Apache/web services are repeatedly overloaded</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">Add a dedicated front end server (and load balancing hardware if needed)</span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">System is repeatedly slow due to db related operations, with no change after performance tuning</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">Move DB to a dedicated server or add a db server </span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">System is intolerable slow during daily ETL processes or reporting executions</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">Move ETL or DWH& ETL to a dedicated server </span>
      </td>
    </tr>
    
    <tr class="kaltura-table-row">
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">Back end server/s CPU is overloaded (no increase in number of transcoding operations)</span>
      </td>
      
      <td class="kaltura-table-row-item" style="width: 50%; text-align: left;">
        <span style="font-family: verdana, geneva;">Add a dedicated back end server for batch processes</span>
      </td>
    </tr>
  </tbody>
</table>

<span style="font-family: verdana, geneva;">[/collapsed]</span>