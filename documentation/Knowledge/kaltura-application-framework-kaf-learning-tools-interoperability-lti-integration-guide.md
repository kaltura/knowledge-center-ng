---
layout: page
title: "Kaltura Application Framework (KAF) Learning Tools Interoperability (LTI) Integration Guide"
date: 2015-11-30 21:47:28
---

<div class="WordSection1">
    <h1>
      Kaltura Application Framework for LTI Supported LMS Integration
    </h1>
    
    <p>
       The Kaltura Application Framework(KAF) for Learning Tools Interoperability LTI supported LMSs adds several modules and course tools to your LMS environment.
    </p>
    
    <h2>
      Prerequisites
    </h2>
    
    <ul>
      <li>
        A Kaltura account:
      </li>
      <li>
        Partner id (“pid”), e.g., <em>12345678</em>
      </li>
      <li>
        Admin secret, e.g., <em>f79359d3227f45be73c181489888afc5</em>
      </li>
      <li>
        A Kaltura Application Framework instance URL, for example, <em>12345678.kaf.kaltura.com</em>
      </li>
      <li>
        LTI compliant LMS (1.x)
      </li>
    </ul>
    
    <h2>
      External Tool Integration
    </h2>
    
    <p>
      Please refer to your LMS knowledge base for information on how to configure an external tool on your LMS environment. It is commonly required to provide the tool URL, consumer key and secret.
    </p>
    
    <p>
      The consumer key for KAF, is your partner ID (e.g. 12345678) . The secret is your Kaltura account Admin Secret (e.g.<em> f79359d3227f45be73c181489888afc5).</em>
    </p>
    
    <p>
      The URL depends on the specific tool you want to set up.
    </p>
    
    <h3>
      My Media
    </h3>
    
    <p>
      The Tool URL for My Media is your KAF instance URL with URI of /hosted/index/my-media.
    </p>
    
    <p>
      For example: http(s)://12345678.kaf.kaltura.com/hosted/index/my-media
    </p>
    
    <p>
      Use HTTP or HTTPS to match the protocol your users are browsing to your LMS.
    </p>
    
    <h3>
      Media Gallery
    </h3>
    
    <p>
      The Tool URL for the Media Gallery is your KAF instance URL with URI of /hosted/index/course-gallery.
    </p>
    
    <p>
      For example: http(s)://12345678.kaf.kaltura.com/hosted/index/course-gallery
    </p>
    
    <p>
      Use HTTP or HTTPS to match the protocol your users are browsing to your LMS.
    </p>
    
    <h2>
      Rich Text Editor Integration
    </h2>
    
    <p>
      The Browse, Search and Embed module is a KAF module that integrates with the Rich-text editor and allows you to embed Kaltura content in various areas of your LMS.
    </p>
    
    <p>
      To integrate with the Browse, Search and Embed (BSE) module, the LMS needs to store a unique reference for the selected item.
    </p>
    
    <h2>
      Content-Item-Message
    </h2>
    
    <p>
      If your LMS supports <a href="http://www.imsglobal.org/specs/lticiv1p0" target="_blank">content-item-message</a> (or you choose to develop the support for it in favor of the KAF integration) all you have to do is configure the external tool that is launched with a message type of ContentItemSelectionRequest.
    </p>
    
    <p>
      The URL for the tool is your KAF instance URL with URI of /browseandembed/index/index.
    </p>
    
    <p>
      For example: http(s)://<em>12345678.kaf.kaltura.com/browseandembed/index/</em><em>index</em>
    </p>
    
    <p>
      The consumer key for KAF, is your partner ID (e.g. 12345678) . The secret is your Kaltura account Admin Secret (e.g.<em> f79359d3227f45be73c181489888afc5).</em>.
    </p>
    
    <p>
      After you select the content-item, KAF performs a POST form submit to the return URL that is specified in the LTI launch with a content-item-message data structure. The LMS is expected to use that data to update the content (in rich text editor, for example).
    </p>
    
    <p>
      The “return_type” of the content-item-message is configurable in the “Hosted” module which basically should be one of the return types defined by the <a href="http://www.imsglobal.org/lti/ltiv1p2pd/ltiCIMv1p0pd.html" target="_blank">content-item-message</a> specification, In fact, the correct value for KAF should be LtiLink as the returned content must be viewed via an LTI launch.
    </p>
    
    <h2>
      Custom Integration
    </h2>
    
    <p>
      If your LMS does not support <a href="http://www.imsglobal.org/specs/lticiv1p0">content-item-message</a>, please contact <a href="mailto:customercare@kaltura.com" target="_blank">Kaltura Customer Care</a> to assist you with the KAF LTI Integration.
    </p>
    
    <h2>
      Publish Plugin (Optional)
    </h2>
    
    <p>
      The Publish Plugin enables users to publish items directly from My Media to Course Galleries they have access to. If you do not integrate the Publish Plugin, you can  alternatively use the Add Media option to publish items to course gallery you are in.
    </p>
    
    <p>
      Since passing the Publish Plugin information is not part of LTI specification, Kaltura has defined a generic process where KAF can get this information from an LMS.
    </p>
    
    <p>
      The LMS should expose a web service that KAF calls in HTTP.
    </p>
    
    <h3>
      Web Service Definition
    </h3>
    
    <p>
      You must create a web service that is called by KAF to integrate with the publish plugin, The following table describes the Web service components that should be exposed by the LMS.
    </p>
  </div>
  
  <table style="width: 796px;" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="150">
          <p class="TableHeading">
            Component
          </p>
        </td>
        
        <td valign="top" width="646">
          <p class="TableHeading">
            Description
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            URL
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="646">
          <p class="TableBodyText">
            Should be configured in the ‘ltigeneric’ tab. The configured URL is appended to the user ID value.
          </p>
          
          <p>
            For example, if you configured the URL to https://mylms.univ.edu/custom/kaltura-service/ and the user ID is “student1”, the actual URL that will be requested would be: https://mylms.univ.edu/custom/kaltura-service/student1<br /> Or, if you configured the URL to: https://mylms.univ.edu/custom/kaltura/service?userId<a href="https://mylms.univ.edu/custom/kaltura/service?userId=">=</a> and the user ID is “student1”, the actual URL that will be requested would be: https://mylms.univ.edu/custom/kaltura/service?userId=student1<a href="https://mylms.univ.edu/custom/kaltura/service?userId=student1"></a>
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            Authentication
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="646">
          <p class="TableBodyText">
            The Web service should expect an access token in a custom HTTP header named “auth_code”.
          </p>
          
          <p class="TableBodyText">
            The value of the custom HTTP header is a value generated by the LMS, which is sent in every LTI launch to KAF in a custom LTI parameter named “custom_auth_code”.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            Output
          </p>
        </td>
        
        <td valign="top" width="646">
          <p style="text-align: left;">
            The web service should return the membership data of the user in the following JSON format:
          </p>
          
          <p class="TableCodeCxSpFirst" style="text-align: left;">
            "id":"admin", // internal user ID
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
               "eid":"admin", // external user ID, if applicable
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
              
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
               // array of memberships
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
               "memberships":[ 
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                  { 
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                     "context_id":"873b4b81-09b5-46ed-a14e-14dd6f6ec8e1",
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                     "context_title":"Biology 101",
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                     "ltiRoles":"Instructor,"
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                  },
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                  { 
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                     "context_id":"873b4b81-09b5-46ed-a14e-14dd6f6ec8e2",
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                     "context_title":"Advanced Physics",
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                     "ltiRoles":"Instructor,Learner"
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
                  }
          </p>
          
          <p class="TableCodeCxSpMiddle" style="text-align: left;">
               ]
          </p>
          
          <p class="TableCodeCxSpLast" style="text-align: left;">
            }
          </p>
          
          <p style="text-align: left;">
            See <a href="#user_membership">User Membership Data Parameters</a> for a description of these fields.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <h4>
    <a name="user_membership"></a>User Membership Data Parameters
  </h4>
  
  <p>
    The following table describes the user membership properties in JSON and their LTI Launch equivalents. 
  </p>
  
  <table class="TableCentered" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="243">
          <p class="TableHeading" align="center">
            Property in JSON
          </p>
        </td>
        
        <td valign="top" width="241">
          <p class="TableHeading" align="center">
            Value Description
          </p>
        </td>
        
        <td valign="top" width="240">
          <p class="TableHeading" align="center">
            LTI Launch Equivalent Parameter
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td valign="top" width="243">
          <p class="TableBodyText" align="left">
            Id
          </p>
        </td>
        
        <td valign="top" width="241">
          <p class="TableBodyText" align="left">
            Internal user ID in the LMS
          </p>
        </td>
        
        <td valign="top" width="240">
          <p class="TableBodyText" align="left">
            user_id
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="243">
          <p class="TableBodyText" align="left">
            Eid
          </p>
        </td>
        
        <td valign="top" width="241">
          <p class="TableBodyText" align="left">
            External user ID in the LMS, if such is applicable.
          </p>
        </td>
        
        <td valign="top" width="240">
          <p class="TableBodyText" align="left">
            -
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="243">
          <p class="TableBodyText" align="left">
            memberships
          </p>
        </td>
        
        <td valign="top" width="241">
          <p class="TableBodyText" align="left">
            Array of course enrolments
          </p>
        </td>
        
        <td valign="top" width="240">
          <p class="TableBodyText" align="left">
            -
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="243">
          <p class="TableBodyText" align="left">
            context_id
          </p>
        </td>
        
        <td valign="top" width="241">
          <p class="TableBodyText" align="left">
            course ID
          </p>
        </td>
        
        <td valign="top" width="240">
          <p class="TableBodyText" align="left">
            context_id
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="243">
          <p class="TableBodyText" align="left">
            context_title
          </p>
        </td>
        
        <td valign="top" width="241">
          <p class="TableBodyText" align="left">
            course title/name
          </p>
        </td>
        
        <td valign="top" width="240">
          <p class="TableBodyText" align="left">
            context_title
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="243">
          <p class="TableBodyText" align="left">
            ltiRoles
          </p>
        </td>
        
        <td valign="top" width="241">
          <p class="TableBodyText" align="left">
            comma separated values of the user’s LTI roles
          </p>
        </td>
        
        <td valign="top" width="240">
          <p class="TableBodyText" align="left">
            roles
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    If you have a web-service that already answers these specifications,  or have the ability to develop one, you can configure KAF accordingly, to allow KAF to pull this information and use and enable the user to publish into different Course Galleries from My-Media.
  </p>
  
  <p>
     
  </p>