---
layout: page
title: "Kaltura MediaSpace LDAP Integration Guide"
date: 2012-10-21 15:33:12
---

This article describes how to implement [Lightweight Directory Access Protocol (LDAP)][1] in Kaltura MediaSpace™ Version 4.0.

 [1]: http://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol

This article is intended for Kaltura partners, community members, and customers who wish to understand and deploy LDAP authentication and authorization in MediaSpace.

To understand this document, you need to be familiar with authentication and authorization terminology.

<p class="mce-heading-2">
  Understanding LDAP Authentication in MediaSpace
</p>

LDAP authentication in MediaSpace enables users to log into MediaSpace using their credentials from an organizational LDAP or Active Directory (AD) server. A user does not require an additional set of credentials for MediaSpace. LDAP authentication for MediaSpace uses the MediaSpace login window.

When MediaSpace is configured to authenticate using LDAP, other authentication methods are disabled.

<p class="mce-heading-2">
  Understanding LDAP Authorization in MediaSpace
</p>

A user's *application role* determines the MediaSpace actions that the user is authorized to do. When LDAP is used for authorization in MediaSpace, the user’s application role is based on membership in organizational groups. The organizational groups are managed in the organization’s LDAP server.

To learn more about the MediaSpace application role, refer to [Understanding Application Roles][2].

 [2]: http://knowledge.kaltura.com/node/615#Application_Roles

<p class="mce-heading-2">
  Understanding the LDAP Authentication Flow
</p>

The LDAP authentication method implements the following authentication flow:

<img src="{{site.url}}/assets/752">

<p class="mce-note-graphic">
  NOTES:<br />1. LDAP server capabilities and <a href="#MediaSpaceLDAPconfiguration">MediaSpace LDAP configuration</a> determine whether search for user Distinguished Name (DN) or direct binding is used.<br />2. MediaSpace can connect with only one LDAP server.
</p>

<span class="mce-heading-3">Understanding LDAP Authentication Flow Details</span>  
Depending on your [MediaSpace LDAP configuration][3], MediaSpace uses one of the following workflows:Understanding LDAP Authentication Flow Details

 [3]: #MediaSpaceLDAPconfiguration

*   Search before bind
*   Direct bind

<p class="mce-sub-heading">
   <span>“Search before bind” Workflow:</span>
</p>

1.  MediaSpace connects to the configured LDAP server and binds with a privileged user.
2.  MediaSpace queries the LDAP server to find the user’s record using a configurable query and the user name entered in the login window.
3.  If a record is found, MediaSpace tries to bind the user using the DN that was found and the password entered in the login window.
4.  When a user is successfully bound, the user is logged into MediaSpace.

<p class="mce-sub-heading">
  <span>“Direct bind” Workflow:</span>
</p>

1.  MediaSpace constructs the expected DN of the user using the user name entered in the login window and a configurable pattern of the DN.
2.  MediaSpace tries to bind the user using the constructed DN and the password entered in the login window.
3.  When a user is successfully bound, the user is logged into MediaSpace. 

<span class="mce-heading-2">Understanding the LDAP Authorization Flow</span>

The LDAP authentication method implements the following authorization flow:

 <img src="{{site.url}}/assets/753">

<p class="mce-note-graphic">
  NOTES:<br />1. LDAP server capabilities and <a href="#MediaSpaceLDAPconfiguration">MediaSpace LDAP configuration</a> determine whether group membership is queried based on user or group records.<br />2. When an AD server is used and primaryGroupIdAttribute is configured in the MediaSpace Configuration Management panel, the primary group ID is searched for a matching role if no other group matches a role.<br />3. Authorization based on nested groups is not supported.<br />4. When querying group membership from group objects, using large groups is not recommended since MediaSpace does not support paging when querying LDAP.
</p>

<p class="mce-heading-3">
  Understanding LDAP Authorization Flow Details
</p>

Depending on your [MediaSpace LDAP configuration][3], MediaSpace queries group membership using one of the following workflows:

*   **Get users from groups** – Fetch group records with their member attribute

*   **Get groups from user** – Fetch the user record with its memberOf attribute 

<p class="mce-sub-heading">
  “Get users from groups” Workflow:
</p>

1.  Using a single LDAP query, the LDAP authentication method searches for all groups that are preconfigured in a group→role mapping setup of MediaSpace and retrieves the configurable membership attribute for the groups that are found.
2.  For each group found, the LDAP authentication method:
<ol style="list-style-type: lower-alpha;">
  <li>
    Loops through all members of the group
  </li>
  <ol style="list-style-type: lower-roman;">
    <li>
      Tries to match the authenticated user DN with the member DN.<br />If a match is found, the role mapped to the current group is taken, and the loop ends.
    </li>
  </ol>
</ol>

The LDAP query used to search for the groups can be one of the following:

*   A preconfigured query defined by the LDAP administrator in your organization
*   A preconfigured combination of query patterns that constitutes one query

<p class="mce-sub-heading">
  “Get groups from user” Workflow:
</p>

1.  Using a single LDAP query, the LDAP authentication method fetches the user record including its “memberOf” attribute. The name of the attribute is configurable.
2.  For each group found, the LDAP authentication method:
<ol style="list-style-type: lower-alpha;">
  <li>
    Tries to match the group name with one of the groups that are preconfigured in a group→role mapping setup of MediaSpace.<br />If a match is found, the role mapped to the current group is taken, and the loop ends.
  </li>
</ol>

<p class="mce-heading-2">
  <a name="MediaSpaceLDAPconfiguration"></a>Configuring LDAP in MediaSpace
</p>

Configuration settings depend on LDAP server capabilities. Before configuring authentication, determine your LDAP bind method (search before bind or direct bind). Before configuring authorization, determine your LDAP method for user groups searches (get user from groups or get groups from user).

To learn how to configure LDAP for authentication and authorization in MediaSpace, refer to [Configuring LDAP Authentication and Authorization][4].

 [4]: http://knowledge.kaltura.com/node/621#LDAPAuth