---
layout: page
title: "Kaltura’s Digital Rights Management (DRM) Service with Widevine Setup and Workflow Guide"
date: 2013-04-03 18:48:29
---

<div class="WordSection1">
  <a name="top"></a><h1>
    <span class="mce-heading-2"><a name="intro"></a><span class="mce-heading-1">Introduction to Kaltura’s Digital Rights Management Integration with Widevine</span></span>
  </h1>
  
  <p>
    This article provides workflow and setup related information about Kaltura’s Digital Rights Management (DRM) services offered through Kaltura’s integration with Google’s Widevine DRM technology. The article is targeted to answer questions a content administrator working with Kaltura may have with respect to enabling and using Kaltura’s DRM services through their KMC account and integrated website/application. 
  </p>The following questions are answered:
  
  <p>
    <a href="#whatisdrm">What is DRM and How Does it Work?</a>
  </p>
  
  <p>
    <a href="#whyusedrm">Why Use DRM?</a>
  </p>
  
  <p>
    <a href="#howisdrmintegrated">How is Kaltura integrated with Google Widevine's DRM Technology?</a>
  </p>
  
  <p>
    <a href="#processing_ingestion">How is Widevine DRM Processing Integrated in Kaltura’s Ingestion Flows?</a>
  </p>
  
  <p>
    <a href="#integration_KDP">How are DRM Protected Playback Flows Integrated in the Kaltura Dynamic Player (KDP)?</a>
  </p>
  
  <p>
    <a href="#enable_drm">How to Enable and Setup DRM in Your KMC Account?</a>
  </p>
  
  <p>
    <a href="#howto_managedrm">How to Manage DRM Encrypted Content in the KMC?</a>
  </p>
  
  <p>
    <a href="#considerations">What End-User Experience Considerations Should be Taken into Account for DRM</a>?
  </p>
  
  <h2>
    <a name="whatisdrm"></a><span class="mce-heading-3" style="color: #828a8c; font-size: 14pt;">What is DRM and How Does it Work?</span>
  </h2>
  
  <p>
    Digital Rights Management is a set of technologies that enables content-rights owners and content providers to set and enforce terms by which people use their intellectual property. Using DRM for protecting media assets is commonly achieved by implementing an integrated flow which includes the following: 
  </p>
  
  <ul>
    <li>
      On-disk encryption of media assets.
    </li>
    <li>
      Policies and access rules defined for each encrypted content package on a central licensing authority.
    </li>
    <li>
      License Protected Playback - Playback of encrypted content is possible only via DRM enabled applications/devices and only when a content-specific license is granted by the license authority.
    </li>
  </ul>
  
  <h2>
    <a name="whyusedrm"></a><span class="mce-heading-2 mce-heading-3">Why Use DRM?</span>
  </h2>DRM encryption and controlled licensing is commonly in use for preventing cases of unauthorized distribution and piracy of content.  When relating to media assets - DRM may be suitable on the following cases:
</div>

<div class="WordSection1">
  <ul>
    <li>
      Meeting studios and content-rights owners’ mandatory requirements for DRM protection on premium content
    </li>
    <li>
      Unprotected nature of content origin (CDN or downloaded copy available on end-user device) requires that content will be encrypted on-disk.
    </li>
    <li>
      Ability to revoke access to content.
    </li>
    <li>
      Built-in policies and enforcement for different content monetization models.
    </li>
  </ul>
  
  <h1 class="mce-heading-1">
    <a name="howisdrmintegrated"></a>Kaltura DRM Service with Google Widevine
  </h1>Kaltura is a 
  
  <a href="http://www.widevine.com/cwip/index.html">Certified Widevine Implementation Partner</a> that is authorized to provide Widevine DRM services.  Kaltura offers an out-of-the-box DRM solution integrated with Kaltura’s Dynamic (Flash) Player (KDP) while also enabling its customer to integrate their device specific applications with Widevine’s DRM packaging and license services according to the application specific workflow. <h3 class="mce-heading-3">
    Integrated Components
  </h3>Kaltura’s DRM service is offered through the integration with the following components:
</div>

<div class="WordSection1">
  <strong><a name="widevinelicenseserver"></a>Widevine License Server</strong> – A cloud service, hosted and managed by Google, holding records of encrypted assets and policies, each defined per specific DRM service provider, such as Kaltura.  The license server accepts licensing authorization requests for enabling the playback of encrypted content. 
</div>

<div class="WordSection1">
  <strong>Widevine VOD Packager </strong>- Deployed in the Kaltura Data Center. This component is responsible for:
</div>

<div class="WordSection1">
  <ul>
    <li>
      Encryption/packaging of original video assets
    </li>
    <li>
      Registration of encrypted packages on the Widevine License Server.
    </li>
    <li>
      Providing a set of service provider admin tools for managing policies and assets on the Widevine license server.
    </li>
  </ul>
  
  <strong>Kaltura’s Widevine License Proxy</strong> – A Kaltura API based service responsible for proxying DRM license requests from the DRM client to the <a href="#widevinelicenseserver">Widevine License Server</a>. The license proxy applies preliminary authorization logic based on the respective entry’s access control settings prior to passing the request to the <a href="#widevinelicenseserver">Widevine License Server</a>.
</div>

<div class="WordSection1">
  <strong>Widevine DRM Device Client</strong> – Responsible for managing the DRM license flow, receiving content from its origin location and decrypting it for enabling playback in a DRM enabled player application.  With web browsing DRM flow, the DRM is managed through a widevine browser plugin.
</div>

<p class="WordSection1">
  <strong>DRM Enabled Player/Application</strong>– The actual player/application on which video playback occurs. DRM enablement is achieved by integrating the player/application with the DRM client through Widevine standard SDKs. Kaltura offers out-of-the-box integration of its Flash player with Widevine DRM.
</p>

<span class="mce-heading-2">How is Widevine DRM Processing Integrated in Kaltura’s Ingestion Flows?</span>

<p class="WordSection1">
  The following <a name="ingestion_flow"></a>ingestion flow diagram illustrates the processing flow for DRM encryption and packaging of content ingested to Kaltura as part of Kaltura’s content ingestion flow:<img src="{{site.url}}/assets/1018">
</p>

<p class="WordSection1">
   
</p>

<span class="mce-heading-2">How are DRM Protected Playback Flows Integrated in the Kaltura Dynamic Player (KDP)?</span>

The following <a name="playback_flow_diagram"></a>playblack flow diagram illustrates a simple browser based playback flow for DRM encrypted content in Kaltura’s Dynamic Player (KDP). DRM license requests may also be triggered outside of the playback flow, supporting different license authorization scenarios by utilizing Widevine JavaScript APIs.

<img src="{{site.url}}/assets/1103">

<h1 class="mce-heading-1">
  <span><span><a name="enable_drm"></a>How to Enable and Setup DRM in Your KMC Account?</span></span>
</h1>

<div class="WordSection1">
  Kaltura provides the Widevine DRM service as a premium feature that requires account activation and setup. After the DRM service is added to your business order, the Widevine DRM option is enabled in your KMC account by Kaltura’s integration services teams.
</div>

<div class="WordSection1">
  The following settings are defined according to your specific needs.
</div>

*   [DRM License Policies and Access Control Settings][1]
*   [Widevine Enabled Transcoding Flavors Settings][2]
*   [Adding the Widevine Plugin to the KDP ][3]

 [1]: #drm_license_policies
 [2]: #widevine_enable_trans
 [3]: #adding_to_kdp

## <a name="drm_license_policies"></a>DRM License Policies and Access Control Settings

DRM License authorization is granted based on the following settings associated with a specific content item.

*   A specific DRM policy defined on Widevine License Server– a Widevine DRM policy is associated with the encrypted content as part of its packaging process and can also be overridden dynamically to support different website/application flows and needs.  From the Widevine policy, it is possible to define specific rules –such as limiting rental duration for a specific video, with or without also limiting actual playback license duration. In addition, Widevine enables the definition of cases where playback should stop due to the expiration of license duration or detection of copy attempts.  The Widevine policy used as a Kaltura default limits the license duration and is set to stop playback in case copy attempt is detected – The default policy is suitable for generic restriction rules such as limiting playback to specific countries and to specific schedule. More detailed information related to policy customization options is provided by Kaltura as part of the DRM discovery and setup process.
*   The Kaltura access control profile rules associated with the entry. The same rules defined on the access control profile for playback authorization are also applicable for DRM license request authorization. With access control settings,  it is possible to restrict license requests for specific content to specific countries, specific publishing domains, and specific IP ranges, and also with requiring KS based authorization as a way to enforce application user specific authorization flows. In addition to Kaltura’s access control rules, the entry scheduling is validated by Kaltura’s DRM licensing proxy to ensure that license distribution is possible only within the entry scheduling window.

As illustrated in the[ playback flow diagram][4], Kaltura’s Widevine DRM license proxy first applies validation of access control rules and scheduling conditions defined on the entry, and only when these conditions are met, the license request is passed to Widevine’s Licensing Server for validating the rules defined on the Widevine policy associated to the specific asset. 

 [4]: #playback_flow_diagram

<h3 class="mce-heading-3">
  Creating Custom Widevine Policies for Your Account
</h3>

Kaltura sets up and maintains the Widevine policies. Kaltura provides a **default policy** that is available out-of-the-box and can be used as-is for cases where no time-based license limits are required. Customer specific **custom policies** may be created according to solution needs by Kaltura’s integration services teams.

<h3 class="mce-heading-3">
  Creating Access Control Profiles in Your Account
</h3>

Access control profiles may be configured from your KMC account. For DRM encrypted entries, the access control settings defined for content delivery/playback also apply on DRM licensing authorization.

<p class="mce-heading-2">
  <a name="widevine_enable_trans"></a>Widevine Enabled Transcoding Flavor's Settings
</p>

To add DRM encryption and packaging as an integral part of the Kaltura ingestion process, the transcoding profile in use should include the H264 flavors as well as DRM enabled flavor/s that will hold the packaged/encrypted asset. The DRM flavors are flavors that were set to include a DRM encryption/packaging operation that starts immediately after the transcoding operation of the expected H264 flavors has completed. In addition to DRM processing enablement, each DRM enabled flavor is connected to a specific Widevine policy that defines license terms to which DRM license authorization should be granted. The Widevine policy is then applicable to the DRM encrprypted asset connected to the Widevine flavor. It is possible to override this initial policy selection as part of the website/application integration.

<p class="mce-heading-3">
  <a name="using_the_default"></a>Using the Default Set of DRM Enabled Transcoding Flavors in Your KMC Account
</p>

When you activate the DRM service in your KMC account, a default set of DRM enabled flavors becomes available in the KMC. The default set of DRM enabled flavors can be used to create transcoding profiles either for multi-bitrate DRM packaging or for single bitrate DRM packaging.

*   **Multi-bitrate DRM Packaging**<span style="color: #000000;"> - You can create a transcoding profile dedicated for enabling adaptive bitrate playback of DRM protected content. The default Widevine-multi-bitrate flavor is set to package the six H264 flavors in Kaltura's default flavor set. Select the Widevine-multi-bitrate flavor, and the six H264 flavors to be included in your Kaltura transcoding profile.  You may choose to delete the intermediate H264 flavors after the DRM packaging is complete.  We recommend that you set the Widevine-multi-bitrate flavor as required, so that the entry will not become "ready" before the DRM processing completes. </span>

<img src="{{site.url}}/assets/1041">

 

*   **Single-bitrate DRM Packaging** <span style="color: #000000;">- You can create a transcoding profile dedicated for enabling single bitrate playback in a specific quality, which may be useful when playback is targeted to a specific device or for offline playback. The six default Widevine-single-bitrate flavors are each set to encrypt their respective H264 flavors into a DRM package that contains only one bitrate. A transcoding profile dedicated to content targeted for single bitrate playback will include one H264 flavor with the required bitrate and the respective Widevine-single-bitrate flavor. You may choose to delete the intermediate H264 flavors after the DRM packaging is complete.  We recommend that you set the Widevine-multi-bitrate flavor as required, so that the entry will not become "ready" before the DRM processing completes. <img src="{{site.url}}/assets/1042">

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;"><img src="{{site.url}}/assets/1043">

<span style="color: #828a8c; font-size: 14pt; font-weight: bold;">Creating Custom DRM Enabled Transcoding Flavors in Your KMC Account</span>

As part of the DRM enablement process, Kaltura’s integration services teams and transcoding experts set your transcoding profiles to include DRM enabled flavors according to your specific transcoding needs and Widevine’s specifications. The custom flavor set is associated with a DRM policy according to your needs.

<h3 class="mce-heading-3">
  Creating Transcoding Profiles with DRM Enabled Flavors
</h3>

After your KMC account is set with an applicable set of DRM enabled flavors, you can create transcoding profiles that include the DRM flavors for[ automated encryption of content as part your content ingestion flow][5][.][6]

 [5]: #ingestion_flow
 [6]: file:///C:/Users/Debbie/Documents/drm/Kalturas_DRM_Service_with_Widevine_Setup_and_Workflow_Guideapril3.docx#_Content_Ingestion,_encryption

[][6]You can set transcoding profiles that include both encrypted and non-encrypted flavors. The following options and constraints are related to transcoding profiles with DRM enabled flavors.

*   <span style="color: #000000;">For enabling work with KMC’s Clipping/Trimming/Ad cue point setting tools - the source flavor <span style="text-decoration: underline;">must</span> be included (checked) in the transcoding profile.</span>
*   <span style="color: #000000;">Preview of encrypted content in the KMC is only possible from the entry preview and embed window when selecting a Widevine enabled player and delivery method of either Kaltura Auto or Progressive Download.</span>
*   <span style="color: #000000;">If the entry does not have any non-encrypted flavors, the entry cannot be played back using the KMC standard players (which are not Widevine enabled).</span>
*   <span style="color: #000000;">It is possible to maintain both non-encrypted and encrypted flavors for a single entry. This can be useful  for releasing the content in separate scenarios such as:</span>
*   <span style="color: #000000;">Enabling playback of low-quality flavors without DRM protection</span>
*   <span style="color: #000000;">Enabling playback of high quality flavors with DRM protection  </span>

*   <span style="color: #000000;">It is possible to maintain source and non-encrypted flavors in a secure manner by setting flavor authorization in the access control settings to allow delivery and download only of encrypted flavors.</span>
*   <span style="color: #ff0000;"><span style="color: #000000;">Manual DRM packaging/repackaging from the Entry Edit's Flavors tab requires that the H264 flavors that are included in the DRM package will be present or manualy converted/reconverted as well</span>. </span>

<h2 class="mce-heading-2">
  <a name="adding_to_kdp"></a>Adding the Widevine Plugin to the KDP
</h2>

Kaltura provides out-of-the-box enablement of the Widevine plugin into the Kaltura Dynamic Player (KDP) in DRM enabled KMC accounts. After the KDP is enabled with the Widevine plugin, the player can be used to embed encrypted content in your website. The same DRM enabled player may be used in your website for playing both encrypted as well as non-encrypted entries. The default selection of flavors <span style="text-decoration: underline;">within a DRM enabled player</span> is as follows:

*   Whenever the entry includes a Widevine multi-bitrate flavor - this will be the flavor loaded by the player.
*   Whenever the entry includes more than one Widevine multi-bitrate flavor - only a single multi-bitrate flavor will be loaded to the player. 
*   Multiple single-bitrate flavors can be used in a single player but without automated adaptive bitrate playback. A manual switch between the flavors can be provided in this case.
*   Whenever the entry includes one or more encrypted flavors: <span style="text-decoration: underline;">only</span> the encrypted flavor(s) will be used for playback. If non-encrypted flavors are available on the entry as well, they will not be used together with the set of encrypted flavors in the same playback.
*   Whenever an entry does not include encrypted flavors: the non-encrypted flavors available on the entry will be used for playback as in any non-DRM enabled player.

<h3 class="mce-heading-3">
  Adding the Widevine DRM Player Plugin to a New Player
</h3>

<p class="mce-procedure">
  To add the Widevine DRM Player plugin to a new player:
</p>

1.  In the Studio tab, create a player.
2.  In the Features tab, check the DRM-Widevine option under the security feature band.<img src="{{site.url}}/assets/1008">

<h3 class="mce-heading-3">
  Adding the Widevine DRM Player Plugin to an existing player
</h3>

<p class="Procedure mce-procedure">
  To add the Widevine DRM player plugin to an Existing Player (KDP 3.8.3 and lower<span style="font-size: 12pt;">):</span>
</p>

1.  In the Studio tab, select a player.
2.  In the Features tab, select the Additional Parameters and Plugin section.
3.  Add the following plug-in line:

<pre>widevine.plugin=true&widevine.width=0%&widevine.height=0%&widevine.includeInLayout=false&widevine.relativeTo=PlayerHolder&widevine.position=before&widevine.onPageJs1={onPagePluginPath}/widevineMediaOptimizer/widevineMediaOptimizer.js&widevine.asyncInit=true&widevine.loadInIframe=true&widevine.flavorTags=widevine_mbr,widevine,mbr,web&widevine.loadingPolicy=preInitialize</pre>

<p class="mce-procedure">
  To add the Widevine DRM player plugin to an Existing Player that was previsouly set with DRM (KDP v3.8.4):
</p>

1.  In the Studio tab, select a player.
2.  In the Features tab, select the Additional Parameters and Plugin section.
3.  Add the following plug-in line to enable adaptive bitrate playback:

<pre>widevine.flavorTags=widevine_mbr,widevine,mbr,web</pre>

<p class="mce-heading-2">
  <a name="howto_managedrm"></a>How to Manage DRM Encrypted Content in the KMC?
</p>

The on-going management of DRM encrypted content may be managed in your KMC account along-side with any non-encrypted content you manage in your account 

The following are recommendations and best practices related to management of DRM encrypted content in your KMC account:

*   **Use a DRM Custom Data Schema** - Use a custom data schema dedicated to DRM settings and indications. Using a custom data field for indicating that the entry includes encrypted assets may be useful for convenient filtering of encrypted entries in the KMC, and/or in your application.  Additional metadata fields such as policy name, rental duration and license duration may be useful as part of your solution implementation for dynamic overriding of these settings via a specific KS syntax or for managing specific applicative logic related to license rules associated with the content.<img src="{{site.url}}/assets/1011">

**Use a Default Metadata Template with DRM Indication** - Set the transcoding profile used for content encryption with metadata default entry that includes the custom data value indicating that the entry is encrypted.When using this type of setting, every entry processed for DRM encryption is automatically set with the appropriate DRM metadata.<img src="{{site.url}}/assets/1044">

 

<img src="{{site.url}}/assets/1045">

 

 

*   **DRM Processing Indication in KMC**- Entry and flavor status in the KMC during the DRM encryption/packaging is marked as Converting.
*   **Export to CDN / Remote Storage** - When a CDN or remote storage is defined for the KMC account, flavors set to include DRM encryption will automatically be exported to the remote storage only following DRM encryption and packaging.
*   **Preview of Encrypted Content in KMC** - Encrypted content may be previewed in the KMC only from the preview and embed window when selecting a Widevine enabled player and when using either Kaltura Auto or Progressive Download video delivery options. There are no restrictions on the selected embed type.<img src="{{site.url}}/assets/1014">
*   **Grabbing Embed Codes of Entries with Encrypted Content** – Embed codes grabbed from the KMC for entries with encrypted content should be set with a selection of a Widevine enabled player, and when using either Kaltura Auto or Progressive Download video delivery options. There are no restrictions on the selected embed type.
*   **Keep the Source Flavor in the Transcoding Profile Used for DRM Encryption **– This recommendation is to enable automated thumbnail creation for using media interactive tools available from the KMC such as Clipping / Trimming and Advertising Cue point settings and for possible future conversion to additional flavors. To secure non-encrypted flavors outside of the KMC, you may define the specific set of flavors authorized for delivery and download via the Access Control settings in the KMC.
*   **Distribution Window and Content/License Revocation** - Use the entry scheduling option for defining the schedule window in which content is available for distribution. The entry scheduling is one of the conditions enforced by the Kaltura Widevine license proxy, thus license to view content will not be granted when outside of the defined schedule. You may set the entry scheduling information to a past time to revoke license granting and refreshing of existing licenses for a specific DRM protected content.

<p class="mce-heading-2">
  <a name="considerations"></a><span class="mce-heading-1">What End-User Experience Considerations Should be taken into Account for DRM?</span>
</p>

The following considerations should be taken into account when launching a browser based website or VOD portal containing DRM encrypted content and a Flash Player.

<h2 class="mce-heading-2">
  First-Time DRM
</h2>

<span style="color: #000000;">Playback of encrypted content via a DRM enabled Flash player is enabled through an integrated flow, in which a Widevine browser plugin manages the DRM licensing flow and on-the-fly decryption of content for enabling playback.</span>

To enable playback of encrypted content in a browser environment, the Widevine browser plugin must be installed on the end-user desktop. The KDP is integrated with a Widevine Java script responsible for:

*   The detection of the browser plugin availability
*   A prompt to trigger a direct download of the browser plugin when it is not available yet for the specific browser used by the end-user.

<span style="color: #ff0000;"><span style="color: #000000;">Kaltura implemented a “first-time DRM” experience where an end-user is notified about the need to install the Widevine browser plugin to be able to playback encrypted content.</span> <span style="color: #000000;">A prompt with a link that triggers the download process is displayed. </span><span style="color: #000000;">This prompt is triggered automatically from an on-page plugin included in the Flash player configuration and does not require any additional integration of the website page. The install prompt becomes available from any page where a Widevine enabled KDP is embedded, and only when embedded content is encrypted. An option to direct end-users to a customer specific "Learn More" page, for providing detailed installation instructions in possible through player configuration.</span> </span>

<h2 class="mce-heading-2">
  HTML5 Based Playback and DRM
</h2>

<span style="color: #000000;">As DRM has not been integrated with HTML5 based playback technology, end-users browsing to a website that includes DRM encrypted content from a device/browser that does not support Flash, will not be able to play the encrypted content, and will be prompted with an appropriate message suggesting to view content from other devices.</span>