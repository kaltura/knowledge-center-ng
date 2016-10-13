---
layout: page
title: "Kaltura MediaSpace Authentication and Authorization Solutions – Overview"
date: 2016-07-10 11:53:57
---

<p>
    This article provides an introduction to generic solutions for authenticating and authorizing Kaltura MediaSpace users.
  </p>
  
  <p>
    This document is intended for Kaltura partners, community members, and customers who wish to understand and deploy out-of-the-box authentication and authorization methods for MediaSpace.
  </p>
  
  <p>
    To understand this document, you need to be familiar with authentication and authorization terminology.
  </p>
  
  <p class="mce-heading-2">
    Kaltura MediaSpace Authentication and Authorization Methods – Overview
  </p>
  
  <p>
    Kaltura offers the following solutions for permitting user access to MediaSpace (authentication), and for enabling user actions within MediaSpace (authorization).
  </p>
  
  <p>
    A user's application role determines the MediaSpace actions that the user is authorized to do. To learn more, refer to Understanding Application Roles in the <a href="http://knowledge.kaltura.com/node/559/attachment/field_media">Kaltura MediaSpace Setup Guide</a>.
  </p>
  
  <table border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="104">
          <p>
            Method
          </p>
        </td>
        
        <td valign="top" width="180">
          <p>
            Authentication
          </p>
        </td>
        
        <td valign="top" width="167">
          <p>
            Authorization
          </p>
        </td>
        
        <td valign="top" width="123">
          <p>
            Integration Scope
          </p>
        </td>
        
        <td valign="top" width="120">
          <p>
            Advantages
          </p>
        </td>
        
        <td valign="top" width="121">
          <p>
            Limitations
          </p>
        </td>
        
        <td valign="top" width="124">
          <p>
            Licensing
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td valign="top" width="104">
          <p>
            <a href="http://knowledge.kaltura.com/node/677#Single_Sign-on_Gateway">Single Sign-on (SSO) Gateway</a>
          </p>
        </td>
        
        <td valign="top" width="180">
          <p>
            Enables end users to access both the customer site and MediaSpace when they log in. Uses existing customer user management systems and authentication methodologies (for example, LDAP, CAS, and local DB).
          </p>
        </td>
        
        <td valign="top" width="167">
          <p>
            The user’s application role is passed to MediaSpace as part of the customer-specific login and authentication implementation, which is set through the Kaltura SSO gateway interface.
          </p>
        </td>
        
        <td valign="top" width="123">
          <p>
            Select configuration settings in the MediaSpace Configuration Manager.
          </p>
          
          <p>
            Make minor modifications to the customer-side login code.
          </p>
        </td>
        
        <td valign="top" width="120">
          <p>
            Enables a <a href="http://en.wikipedia.org/wiki/Single_sign-on">single sign-on</a> user experience.
          </p>
          
          <p>
            Utilizes existing customer systems.
          </p>
          
          <p>
            Integrates easily with MediaSpace.
          </p>
          
          <p>
            Allows the login page to appear in the customer site.
          </p>
          
          <p>
            Allows flexibility in the user information passed to MediaSpace.
          </p>
          
          <p>
            Avoids costly login customization.
          </p>
          
          <p>
            SSO Gateway authentication can be used with any generic authorization method.
          </p>
        </td>
        
        <td valign="top" width="121">
          <p>
            Requires minor login page coding.
          </p>
          
          <p>
            SSO Gateway authorization can be used only with SSO Gateway authentication.
          </p>
        </td>
        
        <td valign="top" width="124">
          <p>
            Free with user-based licensing. Professional Service support available for a fee.
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="104">
          <p>
            <a href="http://knowledge.kaltura.com/node/677#Kaltura_AuthenticationAuthorizatio">Kaltura Authentication/Authorization </a>
          </p>
        </td>
        
        <td valign="top" width="180">
          <p>
            Enables end users to log into MediaSpace using credentials stored in Kaltura.
          </p>
        </td>
        
        <td valign="top" width="167">
          <p>
            The user’s application role is stored in Kaltura.
          </p>
        </td>
        
        <td valign="top" width="123">
          <p>
            Select configuration settings in the MediaSpace Configuration Manager.
          </p>
        </td>
        
        <td valign="top" width="120">
          <p>
            Built-in user management screen.
          </p>
          
          <p>
            Requires no integration effort and only minimal configuration.
          </p>
          
          <p>
            Kaltura authorization can be used with any generic authentication method.
          </p>
        </td>
        
        <td valign="top" width="121">
          <p>
            Requires a separate user management system. Organizations with an existing user management system are required to manage users in two places.
          </p>
          
          <p>
            Requires creating MediaSpace user accounts that include a MediaSpace Application Role.
          </p>
        </td>
        
        <td valign="top" width="124">
          <p>
            Free with user-based licensing. Ask your Kaltura Project Manager about costs for other licensing models.
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="104">
          <p>
            <a href="http://knowledge.kaltura.com/node/677#Generic_LDAP">Generic Lightweight Directory Access Protocol (LDAP</a>)
          </p>
        </td>
        
        <td valign="top" width="180">
          <p>
            Enables end users to log into the MediaSpace login screen using credentials from the organizational <a href="http://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol">LDAP</a> or <a href="http://en.wikipedia.org/wiki/Active_Directory">Active Directory (AD)</a> server.
          </p>
        </td>
        
        <td valign="top" width="167">
          <p>
            The user’s application role is based on membership in organizational groups, which are managed in the organization’s LDAP server.
          </p>
        </td>
        
        <td valign="top" width="123">
          <p>
            Select configuration settings in the MediaSpace Configuration Manager.
          </p>
        </td>
        
        <td valign="top" width="120">
          <p>
            Enables using organizational system credentials for MediaSpace login.
          </p>
          
          <p>
            Utilizes existing customer systems.
          </p>
          
          <p>
            Integrates easily with MediaSpace.
          </p>
          
          <p>
            Allows flexibility in the user information passed to MediaSpace.
          </p>
          
          <p>
            Avoids costly login customization.
          </p>
          
          <p>
            LDAP authentication and authorization methods work well together.
          </p>
          
          <p>
            LDAP authentication can be used with any generic authorization method except SSO Gateway authorization.
          </p>
          
          <p>
            LDAP authorization can be used with any generic authentication method.
          </p>
        </td>
        
        <td valign="top" width="121">
          <p>
            Does not enable a single sign-on user experience.
          </p>
          
          <p>
            Configuration settings depend on LDAP server capabilities. Before configuring authentication, determine your LDAP bind method (search before bind or direct bind). Before configuring authorization, determine your LDAP method for user groups searches (get user from groups or get groups from user).
          </p>
        </td>
        
        <td valign="top" width="124">
          <p>
            Free with user-based licensing. Available for a fee for other licensing models. Designed to work “out of the box” with generic LDAP installs.
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="104">
          <p>
            <a href="http://knowledge.kaltura.com/node/677#Header_Authentication">Header Authentication</a>
          </p>
        </td>
        
        <td valign="top" width="180">
          <p>
            Enables end-users to log into MediaSpace seamlessly (SSO user experience) based on network/software components (for example, load balancer) that automatically add a custom HTTP header when the user opens MediaSpace in the browser.
          </p>
        </td>
        
        <td valign="top" width="167">
          <p>
            N/A (Authentication method only)
          </p>
        </td>
        
        <td valign="top" width="123">
          <p>
            Select configuration settings in the MediaSpace Configuration Manager.
          </p>
        </td>
        
        <td valign="top" width="120">
          <p>
            Enables a single sign-on user experience.
          </p>
          
          <p>
            Utilizes existing customer systems.
          </p>
          
          <p>
            Requires no integration effort and only minimal configuration.
          </p>
          
          <p>
            Header authentication can be used with generic LDAP and Kaltura authorization methods.
          </p>
        </td>
        
        <td valign="top" width="121">
          <p>
            Requires a separate authorization method.
          </p>
        </td>
        
        <td valign="top" width="124">
          <p>
            Free with user-based licensing.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p class="mce-note-graphic">
    NOTE: To learn about common authentication and authorization scenarios and how to configure them, refer to <a href="{{site.url}}/documentation/Knowledge/authenticating-and-authorizing-mediaspace-users.html">Authenticating and Authorizing Users</a>.
  </p>