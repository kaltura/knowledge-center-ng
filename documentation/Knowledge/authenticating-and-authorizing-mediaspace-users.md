---
layout: page
title: "Authenticating and Authorizing MediaSpace Users"
date: 2012-09-06 15:37:55
---

On the Configuration Management panel Auth tab of the Kaltura MediaSpace Administration Area, you can configure the settings for the required user **authentication **method and the required method for **authorizing** a user’s access to MediaSpace with a specific [Application Role][1]. The following scenarios are supported:

 [1]: http://knowledge.kaltura.com/node/615#Application_Roles

*   [Scenario 1: Authentication and Authorization Are Managed in Organizational Systems][2]
*   [Scenario 2: Authentication and Authorization Are Managed in Kaltura][3]
*   [Scenario 3: Authentication Is Managed in an Organizational System, Authorization Is Managed in Kaltura][4]

 [2]: #Scenario1
 [3]: #Scenario2
 [4]: #Scenario3

Usually, both authentication and role authorization are set through integration with the organizational identity and group management systems (scenario 1). Kaltura’s authentication and/or authorization options may be useful in the cases described in scenarios 2 and 3.

<p class="mce-note-graphic">
  NOTE: User authorization to channel and content entitlements is handled separately.
</p>

<p class="mce-heading-2">
  Understanding MediaSpace Authentication and Authorization Scenarios
</p>

<p class="mce-heading-3">
  <a name="Scenario1"></a>Scenario 1: Authentication and Authorization Are Managed in Organizational Systems
</p>

<p class="mce-sub-heading">
  When does this scenario apply?
</p>

You can use your organizational system as your MediaSpace identity and role authorization provider when:

*   You have a large-scale MediaSpace deployment. You want all users to log into MediaSpace with their organizational credentials and to be authenticated by your centralized authentication system.
*   You can provide access from the MediaSpace application to your authentication and group management systems.
*   Authorization to access MediaSpace with a specific Application Role derive in most cases from user membership in organizational units or groups.

<p class="mce-sub-heading">
  Who can access MediaSpace?
</p>

Only users who are authenticated and authorized by your systems can access MediaSpace. Users who are not authenticated by your systems are denied access to MediaSpace and are not able to log in.

<p class="mce-sub-heading">
  What user details are stored in Kaltura?
</p>

The user’s identifier, Application Role, and first and last names (optional but recommended) must be stored in Kaltura. After the user logs into MediaSpace for the first time, administrators can view and manage the user record on the User Management panel of the Kaltura MediaSpace Administration Area. The user’s organizational password is not saved in Kaltura.

<p class="mce-sub-heading">
  Can you manually set different user details in Kaltura?
</p>

Yes, you can manually set different user details in Kaltura. After the user logs into MediaSpace for the first time, administrators can manage the user record on the User Management panel of the Kaltura MediaSpace Administration Area. An administrator can override the user details (first and last name) and the user MediaSpace Application Role. This option is useful mainly for granting a higher- or lower‑level Application Role to certain users. For example, you can set a **Viewer **Application Role to a large group of people within your organization and then manually assign the higher level MediaSpace Admin role to a few of them.

<p class="mce-procedure">
  To enable manually overriding settings
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.
2.  Set the following values and click **Save**.
<ol style="list-style-type: lower-alpha;">
  <li>
    Under <em>refreshDetailsOnLogin</em>, select <strong>No</strong>.<br />This option is displayed only when using an external authentication provider.
  </li>
  <li>
    Under <em>refreshRoleOnLogin</em>, select <strong>No</strong>.<br />This option is displayed only when using an external role authorization provider.<br /><img src="../../assets/650">
  </li>
</ol>

<p class="mce-heading-3">
  <a name="Scenario2"></a>Scenario 2: Authentication and Authorization Are Managed in Kaltura
</p>

<p class="mce-sub-heading">
  When does this scenario apply?
</p>

You can use Kaltura as your MediaSpace identity and role authorization provider when:

*   You want to launch a MediaSpace pilot in your organization without IT integration.
*   You want to quickly go live with your organizational video portal before performing IT integration with your organizational authentication and group management systems.
*   Only a few users in your organization need to work with MediaSpace, and there is no requirement or need for managing user authentication and credential validation in your organizational systems.
*   You do not have a centralized authentication system or you are not able to provide access to your authentication system from the MediaSpace application.

<p class="mce-sub-heading">
  Who can access MediaSpace?
</p>

Only users with a MediaSpace user account pre-provisioned in Kaltura can access MediaSpace. (The user account must include a MediaSpace Role and a MediaSpace password.) If you want to revoke MediaSpace access from a specific user, it is your responsibility to delete the user account in one of the following ways:

*   On the User Management panel of the Kaltura MediaSpace Administration area, select one or more users, and click **Delete **or **Delete Checked**.
*   Submit a Kaltura end-users CSV to delete MediaSpace user accounts in bulk.  To learn more, see the [submit a Kaltura end-users CSV][5] procedure step.
*   Use the Kaltura API to:
*   Delete the user record.
*   Remove the user's MediaSpace Role stored in a custom data profile.

 [5]: #SubmitaKalturaendusersCSV

<p class="mce-sub-heading">
  How do you switch from Kaltura-managed authentication and authorization to managing MediaSpace authentication and authorization in your system?
</p>

Following the completion of your pilot, or when the IT integration with your user authentication and group management systems is completed, on the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab and change the selected authentication/authorization method. In the Kaltura MediaSpace Administration Area, you may override the Kaltura‑managed Application Roles from your system on the Configuration Management panel or by manually deleting existing MediaSpace user accounts on the User Management panel.

<p class="mce-procedure">
  To override Kaltura-managed Application Roles on the Configuration Management panel
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.
2.  Set the following values and click **Save**.
<ol style="list-style-type: lower-alpha;">
  <li>
    Under <em>refreshDetailsOnLogin</em>, select <strong>Yes</strong>.<br />This option is displayed only when using an external authentication provider.
  </li>
  <li>
    Under <em>refreshRoleOnLogin</em>, select <strong>Yes</strong>.<br />This option is displayed only when using an external role authorization provider.
  </li>
</ol>

<p class="mce-heading-3">
  <a name="Scenario3"></a>Scenario 3: Authentication Is Managed in an Organizational System, Authorization Is Managed in Kaltura
</p>

<p class="mce-sub-heading">
  When does this scenario apply?
</p>

You can use Kaltura as your MediaSpace access and role authorization provider when:

*   You have a small- to large-scale MediaSpace deployment. You want all users to log into MediaSpace with their organizational credentials and to be authenticated by your centralized authentication system.
*   Authorization for users to access MediaSpace and MediaSpace Application Roles is independent of their membership in organizational units or groups. For example, users who will be granted MediaSpace access do not belong to a specific organizational unit or group.
*   You are not able to provide access to your group management system from the MediaSpace application for setting group-based role authorization. You want to set users' application roles before their first login to MediaSpace.

<p class="mce-sub-heading">
  Who can access MediaSpace?
</p>

Only users who are authenticated by your systems and have MediaSpace user accounts pre‑provisioned in Kaltura (the user account includes MediaSpace Application Roles) can access MediaSpace. Users who are not authenticated by your systems are denied access to MediaSpace, even if they are have a user account and a MediaSpace Application Role in Kaltura. These unauthenticated users will not be able to log in.

<p class="mce-heading-2">
  Configuring Authentication and Authorization for MediaSpace
</p>

<p class="mce-heading-3">
  <a name="CommonLoginOptions"></a>Enabling Common Login Configurations
</p>

On the Configuration Management panel Auth tab of the Kaltura MediaSpace Administration Area, the following MediaSpace login options are available for all authentication and authorization methods. 

<img src="../../assets/651">

<img src="../../assets/652">

<p class="mce-heading-3">
  Enabling Authentication Methods
</p>

On the Configuration Management panel Auth tab of the Kaltura MediaSpace Administration Area, the following authentication methods are supported as part of the MediaSpace standard installation. When you select an authentication adapter, a set of relevant configuration fields is displayed to fill in. 

<img src="../../assets/653">

*   **[LDAP Authentication][6]** – User authentication and credentials validation through direct access to the organizational LDAP or Active Directory server.
*   **[SSO Gateway Authentication][7] **– A Kaltura generic gateway for integrating with a customer‑ specific login and authentication implementation, while providing the user with a Single Sign-On experience.
*   **[Header Authentication][8] **– User is authenticated through a request in the organizational authentication system. The response includes the authenticated user ID in a specific HTTP header.
*   **[Kaltura Authentication][9] –** Manage MediaSpace users and their authentication in Kaltura.
*   **Custom Authentication Methods** – For any other type of authentication method, custom adapters can be developed and added to the MediaSpace installation.

 [6]: #LDAPAuth
 [7]: #SSOGatewayAuth
 [8]: #HeaderAuth
 [9]: #KalturaAuth

<p class="mce-heading-3">
  Enabling Authorization Methods
</p>

On the Configuration Management panel Auth tab of the Kaltura MediaSpace Administration Area, the following authorization methods are supported as part of the MediaSpace standard installation. When you select an authorization method, a set of relevant configuration fields is displayed to fill in.

<img src="../../assets/654">

*   **[LDAP Authorization][6] **– The user’s application role in MediaSpace is determined based on organizational groups in which the user is a member, which are managed in the organization’s LDAP server. This authorization method usually is used together with the LDAP authentication method. The method also can be selected when using other authentication methods (SSO Gateway authentication, Kaltura authentication, and Header authentication).
*   **[SSO Gateway Authorization][7] –** The user’s application role in MediaSpace is set and passed to MediaSpace as part of the customer-specific login and authentication implementation, which is set through the Kaltura SSO gateway interface. Always use this option with SSO Gateway authentication. This option cannot be used with any authentication method besides SSO Gateway authentication.
*   **[Kaltura Authorization][9] **– Manage user authorization to access MediaSpace and user MediaSpace application roles in Kaltura. This authorization option can be used with any other authentication method (SSO Gateway authentication, Kaltura authentication, and Header authentication).
*   **Custom Authentication Methods** – For any other type of access and role authorization method, custom adapters can be developed and added to the MediaSpace installation.

<p class="mce-heading-2">
  Setting up Authentication and Authorization
</p>

<p class="mce-heading-3">
  <a name="LDAPAuth"></a>Configuring LDAP Authentication and Authorization
</p>

To learn more about integrating your LDAP server for authenticating users and authorizing user access to MediaSpace with a specific application role, refer to [Kaltura MediaSpace Introduction to Authentication and Authorization Solutions][10] and [Kaltura MediaSpace LDAP Integration Guide][11].

 [10]: http://knowledge.kaltura.com/node/554/attachment/field_media
 [11]: http://knowledge.kaltura.com/node/555/attachment/field_media

<p class="mce-procedure">
  To configure user authentication through your LDAP server
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.  
    After you complete and verify the following steps, click **Save**.
2.  Under *authNAdapter*, select **LDAP AuthN**.  
    <img src="../../assets/655">
3.  Select your preferences for the [common login options][12].
4.  Under *refreshDetailsOnLogin*, select your preference.  
    This option affects the updating of the user’s first name, last name, and email address (when provided) from your LDAP system upon every login.  
    <img src="../../assets/656">
5.  Under *ldapServer*:
<ol style="list-style-type: lower-alpha;">
  <li>
    Select the LDAP Server access and bind settings.<br />Your <strong>bindMethod</strong> selection will affect the information you need to provide for authenticating the user.<br /><img src="../../assets/659">
  </li>
  <li>
    Select the LDAP attributes for first name, last name and email address.<br />Populating the user’s first and last name is used for several MediaSpace options that require the user name.<br />The email address is optional. This field is useful for user management and for future features (such as email notifications).<br /><img src="../../assets/660">
  </li>
</ol>

6.  If you are using your LDAP server to authorize user access to MediaSpace with a specific application role, continue with the next procedure. If not, select a different authorization method.

 [12]: #CommonLoginOptions

<p class="mce-procedure">
  To configure user authorization through your LDAP server
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.  
    After you complete and verify the following steps, click **Save**.
2.  Under *authZAdapter*, select **LDAP AuthZ**.  
    <img src="../../assets/661">
3.  Under *refreshRoleOnLogin*, select your preference.  
    This option affects the updating of the user’s role from your LDAP system upon every login.   
    <img src="../../assets/662">
4.  Under *ldapOptions*, select your preferences for getting the list of groups in which the user is a member.  
    This option is used to determine the user's MediaSpace Application Role.  
    Under *groupsMatchingOrder*, enter the order for matching MediaSpace roles to LDAP groups. The order determines whether the strongest or weakest role is mapped first.  
    Your **groupSearch** selection will affect the information you need to provide.  
    <img src="../../assets/663">
    LDAP Authorization Options - Get Groups from User  
      
    <img src="../../assets/664">
    LDAP Authorization Options - Get User from Groups
5.  Under *ldapGroups*, select your preferences to define the mappings between the groups defined in your LDAP server and the MediaSpace Application Roles.  
    <img src="../../assets/665">

<p class="mce-heading-3">
  <a name="SSOGatewayAuth"></a>Configuring SSO Gateway Authentication and Authorization
</p>

To learn more about integrating MediaSpace with your authentication systems using the MediaSpace SSO Gateway, refer to [Kaltura MediaSpace Introduction to Authentication and Authorization Solutions][10] and [Kaltura MediaSpace SSO Integration Guide][13].

 [13]: http://knowledge.kaltura.com/node/556/attachment/field_media

<p class="mce-procedure">
  To configure user authentication using the MediaSpace SSO gateway
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.  
    After you complete and verify the following steps, click **Save**.
2.  Under *authNAdapter*, select **SSO Gateway AuthN**.  
    <img src="../../assets/666">
3.  Select your preferences for the [common login options][12].
4.  Under *refreshDetailsOnLogin*, select your preference.  
    This option affects the updating of the user’s first name, last name and email address (when provided) from your authentication system upon every login.  
    <img src="../../assets/667">
5.  Under *sso*, select your preferences for integrating the MediaSpace SSO Gateway with your login implementation:
*   **loginUrl** – Enter the absolute URL where you host the login page.
*   **logoutUrl** – Enter the URL to which MediaSpace redirects a user after invalidating the local MediaSpace session (for example, when a user clicks **logout**).
*   On your site you may use this page to invalidate other authenticated sessions, if needed (for example, CAS login).
*   A *sessionKey* URL parameter is automatically appended to the logout URL. This parameter securely encapsulates the user information, enabling you to know which user logged out. The *sessionKey* parameter is constructed using the [secret][14] shared with the login page.<img src="../../assets/668">

6.  If you are using the MediaSpace SSO Gateway to authorize user access to MediaSpace with a specific application role, continue with the next procedure.

 [14]: #secret

<p class="mce-procedure">
  To configure user authorization using the MediaSpace SSO gateway
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.  
    After you complete and verify the following steps, click **Save**.
2.  Under *authZAdapter*, select **SSO Gateway AuthZ**.  
     <img src="../../assets/669">
3.  Under *refreshRoleOnLogin*, select your preference.  
    This option affects the updating of the user’s role upon every login.  
    <img src="../../assets/662">

<p class="mce-heading-3">
  <a name="HeaderAuth"></a>Configuring Header Authentication
</p>

<p class="mce-procedure">
  To configure header authentication through the MediaSpace SSO gateway
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.  
    After you complete and verify the following steps, click **Save**. 
2.  Under *authNAdapter*, select **Header AuthN**.  
    <img src="../../assets/670">
3.  Select your preferences for the [common login options][12].
4.  Under *refreshDetailsOnLogin*, select your preference.  
    This option affects the updating of the user’s first name, last name, and email address (when provided) from your authentication system upon every login.  
    <img src="../../assets/667">
5.  Under *headerAuth*, enter values for:
*   **headerName** – the ID of the authenticated user
*   **logoutUrl  
    <img src="../../assets/671">

<p class="mce-heading-3">
  <a name="KalturaAuth"></a>Configuring Kaltura Authentication and Authorization
</p>

Authenticating or authorizing MediaSpace users in Kaltura requires creating MediaSpace user accounts that include a MediaSpace Application Role. Only users with a MediaSpace user account and MediaSpace Application Role are able to log into MediaSpace.

Authenticating MediaSpace users in Kaltura also requires setting a password for each MediaSpace user. Follow the procedure [to create MediaSpace user accounts that include a MediaSpace Application Role][15].

 [15]: #TocreateMediaSpaceuseraccounts

<p class="mce-procedure">
  To configure Kaltura authentication
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.  
    After you complete and verify the following steps, click **Save**.
2.  Under *authNAdapter*, select **Kms_Auth AuthN**.  
    <img src="../../assets/672">
3.  Select your preferences for the [common login options][12].

<p class="mce-procedure">
  To configure Kaltura authorization
</p>

1.  On the Configuration Management panel of the Kaltura MediaSpace Administration Area, open the Auth tab.

2.  Under *authZAdapter*, select **Kms_Auth AuthZ** and click **Save**.  
    <img src="../../assets/673">

<p class="mce-procedure">
  <a name="TocreateMediaSpaceuseraccounts"></a>To create MediaSpace user accounts that include a MediaSpace Application Role
</p>

Do one of the following:

*   On the User Management panel of the Kaltura MediaSpace Administration Area, you can create and manage MediaSpace user accounts.  
    Use the list to manually manage all users in the partner account that have a MediaSpace role for the specific MediaSpace instance.  
    <img src="../../assets/674">
*   <a name="SubmitaKalturaendusersCSV"></a>Submit a Kaltura end-users CSV to create MediaSpace user accounts in bulk.    
      
    ***Note: There is a 5000 user limitation on channel and category members.** If more members are expected, please use Kaltura Groups . See* <a href="https://knowledge.kaltura.com/node/1672%20" target="_blank">Group Support in Kaltura Applications and Kaltura Groups FAQ</a> for additional information.  
      
    Use the following format:
*   <img src="../../assets/675">
*   To learn more about the end-user CSV schema, refer to [End-Users CSV – Usage and Schema Description][16].
*   The userId field must include a minimum of three characters.
*   The MediaSpace Application Role is managed within the MediaSpace user metadata schema. Adjust the schema name in the example to include your MediaSpace **instanceId**. (You can copy the MediaSpace **instanceId **from the Configuration Management panel Application tab of the Kaltura MediaSpace Administration Area.)
*   Set the role names in the CSV according to the role labels you set in the Configuration Management panel [Roles][17] tab of the Kaltura MediaSpace Administration Area.
*   When using Kaltura to authenticate users, you may populate a [sha1][18] hashed password in the CSV as part of the partnerData field, as in the example. MediaSpace administrators are responsible for managing password hashing and distribution to users. The un-hashed password must include a minimum of six characters.
*   When using Kaltura only for authorizing user access to MediaSpace with a specific application role, do not populate the password in the CSV. (You can remove the partnerData column in the example from the CSV since it is not required.)
*   You can submit the end-users CSV in the following ways:
*   On the User Management panel of the Kaltura MediaSpace Administration Area, click **Submit CSV**.
*   In the KMC, select the Upload tab and then under Submit Bulk, select **End-Users CSV**.  
    <img src="../../assets/676">

 [16]: http://knowledge.kaltura.com/node/464
 [17]: http://knowledge.kaltura.com/node/615#ModifyingApplicationRoleNames
 [18]: http://en.wikipedia.org/wiki/SHA-1

<p class="mce-procedure">
  To automate the update of the authorized MediaSpace users list
</p>

When you manage MediaSpace authorization in Kaltura, you can develop automated processes for updating the list of MediaSpace users based on changes in your organizational information system.

*   You can develop a scheduled update process to periodically add or delete multiple users to the MediaSpace users list using the [Kaltura end-users CSV][16]. In your script, you can call the [user.addfrombulkupload][19] Kaltura API action to submit the CSV.
*   Using Kaltura API actions, you can develop a trigger-based process to update the MediaSpace users list in real time when changes occur in your organizational information system. You can call the [user.add][20], [user.delete][21] and [user.update][22] Kaltura API actions to add, delete, and update specific user records. You can call the [metadata.add][23], [metadata.delete][24], and [metadata.update][25] Kaltura API actions to add, delete, and update the user's MediaSpace role. 

 [19]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=addfrombulkupload
 [20]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=add
 [21]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=delete
 [22]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=user&action=update
 [23]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=metadata_metadata&action=add
 [24]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=metadata_metadata&action=delete
 [25]: http://www.kaltura.com/api_v3/testmeDoc/index.php?service=metadata_metadata&action=update

<p class="mce-note-graphic">
  NOTE: Deleted users are also removed from all channels in which they are members. Content ownership and analytics information of the deleted user are not deleted.
</p>

<p class="mce-note-graphic">
  NOTE: Since user records are shared by all Kaltura applications running on the same account, we recommend that you delete records only of users who left the organization. In other cases, we recommend revoking the user's access to MediaSpace by using the Kaltura API to remove only the user's MediaSpace role or by using the User Management panel of the Kaltura MediaSpace Administration Area to delete the user.  
</p>