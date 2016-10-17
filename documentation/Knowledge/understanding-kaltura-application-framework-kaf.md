---
layout: page
title: "Understanding the Kaltura Application Framework (KAF)"
date: 2013-11-20 18:09:06
---

<div class="WordSection1">
  The Kaltura Application Framework (KAF) is an extensible, feature rich, UI based configurable framework that streamlines the integration of Kaltura’s rich media capabilities into different publishing applications.
</div>

<div class="WordSection4">
  <p>
    The framework is constructed of modules that provide a packaged workflow and functionalities that can be easily embedded in another application as an iFrame, instead of integrating directly with the Kaltura APIs. The framework can decrease the integration time with your application dramatically and allow you to always get up to date new functionality by decoupling the added features from the integration itself.
  </p>
  
  <p>
    The embedded iFrames are all based on a responsive design to ensure that the integrated pages are displayed properly on any given area.
  </p>
  
  <h2 class="mce-heading-2 mce-sub-heading">
    High Level Component Diagram
  </h2>
  
  <p>
    The following diagram illustrates a high level description of the different components in a typical application integration and how they interact.The extension, within an application, loads an iFrame of a specific KAF module through a single-sign-on (SSO) authentication.
  </p>
  
  <p>
    <img src="../../assets/1239.img">
  </p>
  
  <p>
    The KAF module uses Kaltura API’s to display, add, or change content depending on the module available and configured functionality. The display is rendered in HTML that can be directly used by the user in the integrated application.
  </p>
</div>

<p class="mce-heading-2">
  Integrating Kaltura’s Media Capabilities Into Different Publishing Applications
</p>

This section describes the following topics:

*   [Authentication and Authorization][1]
*   [Framework Modules][2]

 [1]: #auth
 [2]: #framework

<p class="mce-heading-3">
  <a name="auth"></a>Authentication and Authorization
</p>

To load a KAF module in an iFrame, an authentication process must occur so that the KAF module can identify the user and determine the user’s privileges.

KAF provides two methods of authentication: KS-based SSO and LTI.

<p class="mce-heading-4">
  KS-Based Single Sign-On Implementation
</p>

In KS-Based SSO, the KAF end-point (URL of a specific module) must include a security token.

The security token expected by KAF is a KS (Kaltura Session) that includes, in its list of privileges, relevant user information, session information and other security-oriented or functionality-related privileges.

A KS can be constructed using any of the <a href="http://www.kaltura.com/api_v3/testme/client-libs.php" target="_blank">Kaltura API Client libraries</a>, with the internal method that is called generateSession (or a similarly named function).

The following is an example for generating a session in PHP using the client library:

<pre class="brush: php;fontsize: 100; first-line: 1; ">$client-&gt;generateSessionV2(

   $adminSecret,

   $userId,

   $sessionType,

   $partnerId,

   $expiration,     

   $privileges

);</pre>

The following table explains the parameters expected by the generateSession method.

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="308">
        <p>
          Admin Secret
        </p>
      </td>
      
      <td valign="top" width="308">
        <p>
          The admin secret of the Kaltura account.
        </p>
        
        <p>
          Can be retrieved from the KMC, under “Settings” tab, in “Integration Settings”.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="308">
        <p>
          User ID
        </p>
      </td>
      
      <td valign="top" width="308">
        <p>
          The unique ID of the user that is being presented with the KAF module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="308">
        <p>
          <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaSessionType" target="_blank">Session Type</a>
        </p>
      </td>
      
      <td valign="top" width="308">
        <p>
          Type of Kaltura Session.
        </p>
        
        <p>
          For KAF integration, the Session Type  must be USER session.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="308">
        <p>
          Partner Id
        </p>
      </td>
      
      <td valign="top" width="308">
        <p>
          The Kaltura account ID.
        </p>
        
        <p>
          Can be retrieved from the KMC, under “Settings” tab, in “Integration Settings”.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="308">
        <p>
          Expiration
        </p>
      </td>
      
      <td valign="top" width="308">
        <p>
          Expiration length of the KS <strong>in seconds.</strong>
        </p>
        
        <p>
          For KAF integration, the Expiration valueshould be up to 60 seconds.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="308">
        <p>
          Privileges
        </p>
      </td>
      
      <td valign="top" width="308">
        <p>
          Comma-separated list of privileges.
        </p>
        
        <p>
          Some privileges are of type key-value pair, in which case they are represented as key:value.
        </p>
        
        <p>
          For the maximum security, the  required privilege is “actionslimit:-1” to make the KS useless for any API calls.
        </p>
      </td>
    </tr>
  </tbody>
</table>

The following is a practical example for generating a KS for loading a KAF module:

<pre class="brush: php;fontsize: 100; first-line: 1; ">// prepare privileges

$privileges= array();

$privileges[] = "actionslimit:-1";

$privileges[] = "firstName:John";

$privileges[] = "lastName:Doe";

$privileges[] = "role:viewerOnly";

 

// transform array privileges to string

$privilegesStr = implode(",", $privileges);

 

// prepare additional parameters

$adminSecret = "-the-string-you-copied-from-kmc-";

$userId = "john.doe";

$partnerId = 12345;

 

// generate the KS using all the above parameters

$ks = $client-&gt;generateSessionV2(

   $adminSecret,

   $userId,

   KalturaSessionType::USER,

   $partnerId,

   20,

   $privilegesStr

);

 

// build iFrame URL with KS

$iframeUrl = 'https://url.to.kaf.com/hosted/index/my-media/ks/' . $ks;

 

// render iFrame to page

echo '&lt;iframe src="' . $iframeUrl . '"&gt;&lt;/iframe&gt;';</pre>

The list of KAF privileges, that are required, depends on the KAF widget you want to use. 

To understand the privileges that are required or optional, visit <http://kaf-integration-demo.kaf.kaltura.com/kaftestme/index/index> . You can choose between the available KAF widgets (End Point) and see a detailed list of required and optional privileges per widget. After submitting your information you can simulate the KAF widget's behavior according to the values passed.

#### Roles and Permissions for KS-Based SSO

KAF has two types of roles:

*   Applicative role – a role that determines the list of allowed actions that the user is allowed to perform in the KAF application.
*   Contextual role – a role that determines a user’s capabilities within a specific given context.

When loading a KAF module, the KS must specify the user’s applicative role.

Depending on the KAF module loaded, the KS might be required to also specify the user’s contextual role in the loaded context.

In the example below:

*   The applicative role of the user is “adminRole” . The adminRole user can upload content as well as publish content in different contexts (galleries).
*   The contextual role of the user is “manager”.. In the loaded context, the user should be considered a manager of that gallery, and is given some capabilities that are only allowed for this role.

<p class="mce-note-graphic">
  Contextual role values are the available constants of <a href="http://www.kaltura.com/api_v3/testmeDoc/index.php?object=KalturaCategoryUserPermissionLevel">KalturaCategoryUserPermissionLevel</a>
</p>

<pre class="brush: php;fontsize: 100; first-line: 1; ">$privileges= array();

$privileges[] = "actionslimit:-1";

$privileges[] = "firstName:John";

$privileges[] = "lastName:Doe";

$privileges[] = "role:adminRole";

$privileges[] = "userContextualRole:0";

 

...

 

// build iFrame URL with KS

$iframeUrl = 'https://url.to.kaf.com/hosted/index/course-gallery/ks/' . $ks;

 

...</pre>

<p class="mce-note-graphic">
  The list of applicative roles can be seen in the “kaftestme” module.
</p>

### LTI-Based Authentication and Authorization

If your application supports LTI (administrator capabilities for configuring tools, or internal code-based API for rendering LTI tools) you can choose to integrate your system to KAF based on LTI.

<p class="mce-note-graphic">
  At this time,  the “kaftestme” module does not show how LTI integration should be constructed. 
</p>

The following lists the mandatory parameters expected in an LTI launch, including comments on relevancy for a specific KAF module. The entire set of required LTI parameters is not listed. The table contains the specific parameters required for KAF integration.

<table style="width: 615px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="187">
        <p class="TableHeading">
          <strong>Parameter</strong>
        </p>
      </td>
      
      <td valign="top" width="141">
        <p class="TableHeading">
          <strong>Use/Scope</strong>
        </p>
      </td>
      
      <td valign="top" width="287">
        <p class="TableHeading">
          <strong>Comments</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          context_id
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p class="TableBodyText">
          Currently required for all KAF modules, even if some modules are not loaded in a specific context (course).
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          context_title
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
          Used in the “Gallery Module” to display the name of the gallery,
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p class="TableBodyText">
          Recommended.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          user_id
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p>
          Should contain a unique identifier of the user, preferably one that the user, or you as an organization, would recognize
        </p>
        
        <p class="TableBodyText">
          An alternative attribute name can be configured in the “hosted” module.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          lis_outcome_service_url
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
          Used by the “browse and embed” module to return data of the selected content to this URL.
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p>
          An alternative attribute name can be configured in the “hosted” module of your KAF instance.
        </p>
        
        <p>
          Refer to <a href="http://www.edu-apps.org/extensions/content.html" target="_blank">content-extension</a> for the structure of the returned data.
        </p>
        
        <p class="TableBodyText">
          You can also use the “kaftestme” module to see the return data structure. There is no difference between KS-based and LTI-based SSO.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          lis_person_contact_email_primary
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          lis_person_name_family
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          lis_person_name_given
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          roles
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
          See <a href="#roles_permissions">Roles and Permissions for LTI-Based SSO.</a>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p class="TableBodyText">
          Should contain LIS roles as mentioned in the LTI specification appendix.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
          launch_presentation_locale
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="187">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="141">
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="287">
        <p class="TableBodyText">
           
        </p>
      </td>
    </tr>
  </tbody>
</table>

Additionally, you can choose to pass custom parameters in the LTI launch, if you have your own dedicated KAF module to use those parameters.

#### <a name="roles_permissions"></a>Roles and Permissions for LTI-Based SSO

Since the roles passed to the KAF application in LTI-based authentication are LIS roles, and not the expected KAF roles, KAF provides the ability to map LIS roles to KAF roles.

The mapping may be done in the configuration of the “hosted” module.

<img src="../../assets/1245.img">

For each LIS role you can configure the applicative role in KAF that the user will be assigned.

For each LIS role you can also configure a contextual role that the user will be assigned.

KAF includes a default mapping that can be modified and/or extended to map additional LIS roles.

<p class="mce-note-graphic">
  The role that the user is granted is the highest one of all matches. 
</p>

<p class="mce-heading-3">
  <a name="framework"></a>Framework Modules
</p>

This section describes the following KAF modules:

*   [Gallery Module][3]
*   [My Media Module][4]

 [3]: #Gallery_Module
 [4]: #My_Media_Module

<a name="Gallery_Module"></a><span class="mce-heading-4">Gallery Module</span>

The Gallery Module is used to create, display and contribute to a dedicated media gallery that can be associated with a group in your application. For example, a media gallery for a specific forum, a course, a community, or other context.

The Gallery Module includes the following functionality:

*   Display of media that is published in the gallery.
*   Viewing and engaging with the published media. According to the configuration, a user may: Play the media, search in-video, comment, like, add to playlist, and other actions that are configured.
*   Search metadata and transcription / closed caption files
*   Contribute to a gallery (according to user’s role)
*   Upload new content and publish to the gallery (according to user’s role)
*   Moderate content in gallery (optional)

The following diagram describes the user flow between the different available pages and functionality within this module:<img src="../../assets/1242.img">

<span style="font-size: 1em;"><img src="../../assets/1243.img">

<a name="My_Media_Module"></a><span class="mce-heading-4">My Media Module</span>

The My Media Module displays the personal media library of a authenticated user.

Specific functionality in this module includes:

*   Displaying media that the user owns (contributed by the logged user).
*   Viewing / Editing media
*   Search on metadata and transcription/closed caption files
*   Upload new content and publish to the gallery (according to user’s role)
*   Bulk publishing to a specific gallery or playlist

The following diagram describes the user flow between the different available pages and functionality within the My Media Module: 

<img src="../../assets/1284.img">

<img src="../../assets/1286.img">