---
layout: page
title: "Kaltura Online Video Security Capabilities"
date: 2016-06-30 16:30:07
---

<h1>
    Overview of Kaltura Online Video Security Capabilities
  </h1>
  
  <p>
    Kaltura’s online video platform offers advanced video publishing, management, syndication and monetization solutions suitable for many verticals, including education, enterprise, government, media and entertainment, advertising, and many others. Kaltura’s flexible platform and APIs allow publishers and organizations to rapidly, and cost-effectively, build video applications, widgets and plug-ins, as well as add core video services to their existing offerings.
  </p>
  
  <p>
    Whether you publish video on the web or use it only for internal audiences, it is important for you to address the security aspects of your online video strategy. Kaltura offers various effective ways to implement the right level of security for your needs and has built in physical, architectural and applicative security measures that provide end-to-end protection for your assets and information.
  </p>
  
  <p>
    Whether you choose a Software as a Service (SaaS) implementation using our scalable infrastructure and trusted CDN partner, or opt for a self-hosted and self-operated platform on your own premises (Kaltura On-Prem™), Kaltura will help you implement the security measures you need to have in place, while assuring an intuitive and smooth experience for your end users.
  </p>
  
  <p>
    This guide provides an overview of the security capabilities that Kaltura offers and includes a high level description of the Kaltura security capabilities for video based content – including ingestion, storage and delivery.  The methods that Kaltura uses to protect user information are described, in addition to Kaltura’s business continuity and disaster recovery policies, Kaltura’s secure platform architecture, and the physical security Kaltura maintains in its hosting facilities. If you require a more in depth description of Kaltura’s security capabilities, please contact a Kaltura representative.
  </p>
  
  <p>
    The options can be used as standalone capabilities – or used together to provide a full security package.
  </p>
  
  <p>
    The following topics are described:
  </p>
  
  <p>
    [collapsed title="Forensic Watermarking"]
  </p>
  
  <h2>
    Forensic Watermarking
  </h2>
  
  <p>
    Forensic watermarking is a process where a unique indivisible mark is added to the content. This mark indicates the originator of the video content (e.g. the studio, aggregator, content owner) and also the authorized user accessing the content. This makes it easy for the content owners to track down any acts of illegal use of the content, such as piracy, illegal recordings and distributions.
  </p>
  
  <p>
    Kaltura adds the forensic watermark to the content on the fly, minimizing the storage footprint and making sure the watermark can be added to any supported delivery profile.
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Kaltura Access Control"]
  </p>
  
  <h2>
    <a name="KAC"></a>Kaltura Access Control
  </h2>
  
  <p>
    In many cases, organizations are interested in restricting access to content. You may want or need to employ broad controls such as allowing access only from a specific geographic location, domains, or you may want to restrict access to specific assets to certain authorized individuals only.
  </p>
  
  <p>
    Kaltura offers several features that are designed to help you achieve the right level of access control to your media.
  </p>
  
  <p>
    The options are summarized in the following table:
  </p>
  
  <table border="0" cellspacing="0" cellpadding="0">
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableHeading">
            <strong>Feature</strong>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableHeading">
            <strong>Description</strong>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableHeading">
            <strong>When to use it?</strong>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableHeading">
            <strong>How to apply it?</strong>
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableBodyText">
            Authentication on entry to the web page
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableBodyText">
            Restricts access to the web page in which the media is hosted. Only authorized users will be able to access the web page using a password or any other secret.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableBodyText">
            In case access needs to be granted to specific people.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableBodyText">
            For Kaltura’s Video Portal, MediaSpace, Kaltura offers multiple authorization options – manage users through our system or integrate with external authorization systems (LDAP, Shibboleth, CAS) as well as custom databases for single sign-on (SSO), or use a hybrid approach where authentication is done by your organization and authorization is handled by Kaltura.
          </p>
          
          <p class="TableBodyText">
            For more information about the MediaSpace permissions, refer to the article <a href="{{site.url}}/documentation/Knowledge/introduction-kaltura-entitlement-infrastructure.html" target="_blank">Kaltura Entitlement Infrastructure</a>.
          </p>
          
          <p class="TableBodyText">
            For integrations with LMSs (Learning Management Systems) and CMSs (Content Management Systems), Kaltura operates within the context of the LMS or CMS. The authentication method used in the organization for access to the LMS or CMS is in effect and the media file can only be viewed by those with access permissions to the page that hosts it per the LMS/CMS  configuration.
          </p>
          
          <p class="TableBodyText">
            If the video is embedded in the customer’s website, password protection needs to be set up by the customer. on their web page.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableBodyText">
            Geo Restriction
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableBodyText">
            Restricts access to media based on the viewer’s IP address geo location. This is set using the browser IP address received within the HTTP requests and the use of IP to location lookup services. For example, a Spanish client can deny access to their media to all users outside of Spain, allowing users with Spanish IPs only to access the site’s media.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableBodyText">
            Geo restriction is a good way to help enforce licensing agreements, which often limit viewership to a list of approved countries.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableBodyText">
            Geo restriction can be applied using the Kaltura Management Console (KMC) on each entry or in bulk. For more information about creation of access profiles via the KMC, refer to the article <a href="{{site.url}}/documentation/Knowledge/how-create-access-profile.html">How to create an access profile. </a> 
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableBodyText">
            Authorized domains
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableBodyText">
            Restricts access to media based on a predefined list of approved domains.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableBodyText">
            Domain restriction is useful, for example, in case you want to make sure content can only be viewed from within your domains. For example – an internal training video can only be viewed from within the enterprise domain, or a course video can only be viewed from within the university domain.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableBodyText">
            Domain restriction can be applied using the Kaltura Management Console (KMC) on each entry or in bulk. For more information about creation of access profiles via the KMC refer to the article <a href="{{site.url}}/documentation/Knowledge/how-create-access-profile.html">How to create an access profile. </a>
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableBodyText">
            Authorized IP addresses
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableBodyText">
            Restricts access to media based on a predefined list of approved IP addresses
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableBodyText">
            In case domain authorization is not granular enough (for example if there is a large organization comprising several networks serving different divisions, and there is a desire to limit access to a specific division only).
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableBodyText">
            IP address restriction can be applied using the Kaltura Management Console (KMC) on each entry or in bulk. For more information about creation of access profiles via the KMC, refer to the article <a href="{{site.url}}/documentation/Knowledge/how-create-access-profile.html" target="_blank">How to create an access profile</a><a href="{{site.url}}/documentation/Knowledge/how-create-access-profile.html">. </a>
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableBodyText">
            Make your content playable only within your Kaltura account and by your player
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableBodyText">
            Restrict content playback to Kaltura players from your account only
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableBodyText">
            To prevent video theft, this feature also enhances brand awareness by showing your videos only on your branded player.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableBodyText">
            This setting can be turned on from within the Kaltura Management Console (KMC). If you already have content that was not secured this way, Kaltura support can assist in applying this security measure to existing entries as well.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableBodyText">
            Make your content available only in specific time windows
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableBodyText">
            Configure a schedule for media entries, defining a start and end date.
          </p>
          
          <p class="TableBodyText">
            Playback will be allowed only within the defined schedule.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableBodyText">
            When you want to limit the time in which a media entry is available for viewing.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableBodyText">
            Scheduling can be applied using the Kaltura Management Console (KMC) on each entry or in bulk. For more information about scheduling, refer to the article  <a href="{{site.url}}/documentation/Knowledge/how-configure-content-scheduling.html" target="_blank">How to configure content scheduling?</a>
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableBodyText">
            Kaltura Session Authentication for embed codes
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableBodyText">
            Any published embed code of media requires a valid Kaltura Session to be passed to the embed code before the content is played. A Kaltura Session has a time expiration.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableBodyText">
            If you would like to restrict embed codes to play in authorized applications only.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableBodyText">
            Kaltura Session authentication for embed codes can be applied using the Kaltura Management Console (KMC) on each entry or in bulk. For more information about creation of access profiles via the KMC, refer to the article <a href="{{site.url}}/documentation/Knowledge/how-create-access-profile.html" target="_blank">How to create an access profile. </a>
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="124">
          <p class="TableBodyText">
            URL
          </p>
          
          <p class="TableBodyText">
            tokenization
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="204">
          <p class="TableBodyText">
            URL tokenization is a content protection offered at the CDN level. The token includes a TTL (time-to-live), so that if an end user tampers with the URL, their request for CDN content is denied. If a URL has an expired TTL, end-user requests for CDN content are denied.
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="161">
          <p class="TableBodyText">
            All the access control solutions described in this table are enforced on the Kaltura Player level. If a sophisticated user spoofs the content URL, these solutions will not be effective. URL tokenization helps prevent attempts to play the content outside of the Kaltura player. It is best to combine this feature with one of the other described access control features
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="229">
          <p class="TableBodyText">
            URL tokenization is enabled on the CDN level, Kaltura’s support team is available to set this up on your behalf.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    Note: This form of protection does not encrypt the content itself, but only restricts access to the content – according to the specifications listed.
  </p>
  
  <p>
    <a href="#KAC">Back</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Protecting Content in Transit"]
  </p>
  
  <h2>
    Protecting Content in Transit
  </h2>
  
  <p>
    Some organizations are concerned about the security of their media as it is being streamed. Content can be hijacked using man-in-the-middle attacks or other stream capture methods, and then the content can be stored locally or published illegally.
  </p>
  
  <p>
    To protect your content in transit, you can use a secured streaming protocol. You can configure the CDN to stream over an encrypted protocol (HTTPS/RTPME) to prevent exposure of the content in transit. The Kaltura platform allows you to easily implement secured streaming.
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="AES Encryption"]
  </p>
  
  <h2>
    <span>AES Encryption</span>
  </h2>
  
  <p>
    To support content protection on delivery, Kaltura supports AES standard encryption of content delivery for HLS delivery. Content is encrypted on the fly utilizing the Kaltura on the fly packager, and the Kaltura player can access the decryption key on the Kaltura servers to decrypt content as it is being played back.
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Encryption at Rest"]
  </p>
  
  <h2>
    <span>Encryption at Rest</span>
  </h2>
  
  <p>
    To support secure storage of content on the Kaltura servers, Kaltura employs encryption at rest of content. Encryption is on a per rendition level, with the encryption done as part of the transcoding process. Content is securely transitioned and stored thought the whole ingest/transcoding process.
  </p>
  
  <p>
    Encryption at rest is especially beneficial for customers utilizing the Kaltura uDRM module. Since Kaltura utilizes on the fly packaging and encryption for DRM content, customers can enjoy the benefits of storing only the original content renditions – without the need of storing pre encrypted DRM flavors, and still make sure content is stored securely utilizing encryption at rest.
  </p>
  
  <p>
    See <a href="#DRM">Digital Rights Management</a> for more information.
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Digital Rights Management"]
  </p>
  
  <h2>
    <span><a name="DRM"></a>Digital Rights Management</span>
  </h2>
  
  <p>
    DRM offers another layer of content protection, by adding a license policy to the content encryption.
  </p>
  
  <p>
    By adding a license, content owners can make sure that only authorized users can have access to decryption keys – and can tie their content to their business modules and protection policies.
  </p>
  
  <p>
    The Kaltura uDRM module is fully integrated with Kaltura business modules definitions, making it possible for content owners to define complex business scenarios – supporting AVOD, TVOD and SVOD configurations.
  </p>
  
  <p>
    Kaltura offers a full multi DRM solution – supporting all major DRM schemas including
  </p>
  
  <ul>
    <li>
      Microsoft PlayReady
    </li>
    <li>
      Google Widevine
    </li>
    <li>
      Apple Fairplay
    </li>
  </ul>
  
  <p>
    By supporting all DRM schemas – content owners can ensure their content is fully DRM protected across all devices, browsers and OS, as Kaltura delivers the most natively supported and security enhanced schema on playback – utilizing the Kaltura on the fly packager. This also ensures a minimal storage foot-print, by enabling the content owners to store only the original transcoded renditions – instead of pre encrypted renditions for all DRM schemas.
  </p>
  
  <p>
    DRM protection is usually required when using premium content on a monetized service and is usually a content owner/studio requirement.
  </p>
  
  <p>
    The Kaltura uDRM module is integrated with the Kaltura player and the Kaltura on the fly packager, to offer a complete, easy to setup DRM eco system. In addition, since the uDRM module is API-driven – it is easily integrated with external video head ends and players is needed.
  </p>
  
  <p>
    For additional information about the Kaltura uDRM solution, see <a href="{{site.url}}/documentation/Knowledge/universal-drm-udrm-technical-specification.html">here</a>.
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Supported Desktop Browsers for UDRM"]
  </p>
  
  <h2>
    Supported Desktop Browsers for DRM
  </h2>
  
  <table border="0" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="136">
          <p class="TableHeading">
            <strong>Browser</strong>
          </p>
        </td>
        
        <td valign="top" width="171">
          <p class="TableHeading">
            <strong>Delivery Format</strong>
          </p>
        </td>
        
        <td valign="top" width="143">
          <p class="TableHeading">
            <strong>DRM</strong>
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          <p class="TableBodyText">
            IE < 11
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="171">
          <p class="TableBodyText">
            Smooth Stream
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="143">
          <p class="TableBodyText">
            PlayReady
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          <p class="TableBodyText">
            IE >= 11, Edge
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="171">
          <p class="TableBodyText">
            Dash
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="143">
          <p class="TableBodyText">
            PlayReady
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          <p class="TableBodyText">
            Chrome
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="171">
          <p class="TableBodyText">
            Dash
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="143">
          <p class="TableBodyText">
            Widevine
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          <p class="TableBodyText">
            Safari
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="171">
          <p class="TableBodyText">
            HLS
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="143">
          <p class="TableBodyText">
            Fairplay
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="136">
          <p class="TableBodyText">
            Firefox
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="171">
          <p class="TableBodyText">
            Smooth Stream
          </p>
          
          <p class="TableBodyText">
            Dash
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="143">
          <p class="TableBodyText">
            PlayReady
          </p>
          
          <p class="TableBodyText">
            Widevine
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Mobile Device Support for DRM"]
  </p>
  
  <h2>
    Mobile Device Support for DRM
  </h2>
  
  <table border="0" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top">
          <p class="TableHeading">
            <strong>Mobile Device/OS </strong>
          </p>
        </td>
        
        <td valign="top">
          <p class="TableHeading">
            <strong>Delivery Format </strong>
          </p>
        </td>
        
        <td valign="top">
          <strong>DRM</strong>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Android 4.1
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            WVM
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Widevine Classic
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Android >= 4.2
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Dash
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Widevine Modular
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            iOS
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            HLS
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Fairplay
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Connected Devices Support for DRM"]
  </p>
  
  <h2>
    Connected Devices Support for DRM
  </h2>
  
  <p>
    Note: <strong>*</strong> marks devices that are not supported by Kaltura player SDK and DRM plugin. Support is in the form of uDRM licensing API with integration to external players.
  </p>
  
  <table border="0" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top">
          <p>
            <strong>Device</strong>
          </p>
        </td>
        
        <td valign="top">
          <p>
            <strong>Delivery Type</strong>
          </p>
        </td>
        
        <td valign="top">
          <p>
            <strong>DRM</strong>
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Chromecast
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Dash
          </p>
          
          <p class="TableBodyText">
            Dash
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Widevine
          </p>
          
          <p class="TableBodyText">
            PlayReady
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            XBox*
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Smooth Stream
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            PlayReady
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            AppleTV*
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            HLS
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Fairplay
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            GoogleTV*
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            WVM
          </p>
          
          <p class="TableBodyText">
            Smooth Stream
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Widevine Classic
          </p>
          
          <p class="TableBodyText">
            PlayReady
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            FireTV*
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Smooth Stream
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            PlayReady
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            SmartTV Alliance (LG, Phillips, Panasonic, Toshiba)*
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Smooth Stream
          </p>
          
          <p class="TableBodyText">
            WVM
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            PlayReady
          </p>
          
          <p class="TableBodyText">
            Widevine Classic
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Samsung TV*
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            Smooth Stream
          </p>
          
          <p class="TableBodyText">
            WVM
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            PlayReady
          </p>
          
          <p class="TableBodyText">
            Widevine Classic
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            HBBTV (1.5+)*
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            DVB Dash
          </p>
        </td>
        
        <td style="text-align: left;" valign="top">
          <p class="TableBodyText">
            PlayReady
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    [/collapsed]
  </p>