---
layout: page
title: "Kaltura MediaSpace SSO Integration Guide"
date: 2012-10-21 12:23:12
---

This article describes how to implement [single sign-on (SSO)][1] in Kaltura MediaSpace™ Version 5.0.

 [1]: http://en.wikipedia.org/wiki/Single_sign-on

This article is intended for Kaltura partners, community members, and customers who want to understand and deploy SSO authentication and authorization in MediaSpace.

To understand this document, you need to be familiar with authentication and authorization terminology.

<p class="mce-heading-2">
  Understanding MediaSpace Authentication and Authorization
</p>

MediaSpace includes a low-level authentication mechanism. When a user attempts to access MediaSpace, MediaSpace checks whether the user is logged in. If the user is not logged in or the login is expired, the user is redirected to another URL.+

As part of the authentication mechanism, MediaSpace determines the user's application role following a successful login. The application role determines the MediaSpace actions that the user is authorized to do. To learn more about the MediaSpace application role, refer to [Understanding Application Roles][2].

 [2]: http://knowledge.kaltura.com/node/615#Application_Roles

<p class="mce-heading-3 mce-heading-2">
  <a name="The_SSO_Gateway"></a>Understanding the SSO Gateway
</p>

In the SSO Gateway, an expired login causes the user to be redirected to the SSO Gateway’s login page.

On the login page, the user logs into *your* user management system using your methodologies (you are responsible for writing the login code).

When a user logs in successfully, the login page generates a unique session key using a *secret* shared between the login page and MediaSpace (which you define for MediaSpace on the Configuration Management panel of the Kaltura MediaSpace Administration Area. Refer to [Configuring SSO Gateway Authentication and Authorization][3]). The session key also securely encapsulates user information that is passed to MediaSpace.

 [3]: http://knowledge.kaltura.com/node/621#SSOGatewayAuth

After successfully logging into your system, the user is redirected to the [MediaSpace authentication URL][4]. The session key is passed as a URL parameter.

 [4]: #MediaSpace_Authentication_URL

The MediaSpace authentication URL uses the secret to validate the session key. If the session key is valid, the MediaSpace authentication URL logs the user into MediaSpace. If the session key is not valid, the MediaSpace authentication URL redirects the user back to your login page.

<p class="mce-note-graphic">
  NOTE: A sample login page (and related files) is available from your project manager upon request.
</p>

<p class="mce-heading-2">
  <a name="MediaSpace_Authentication_URL"></a>Constructing the MediaSpace Authentication URL
</p>

In [the SSO Gateway][5], the MediaSpace authentication URL logs in a user based on the customer user management's session key. The following is the URL structure:

 [5]: #The_SSO_Gateway

http://*mediaspace\_domain/mediaspace\_path*/user/authenticate/sessionKey/{secure hash string}

The URL consists of the following elements:

*   **mediaspace_domain** – the host name of the server that hosts your MediaSpace. Replace *mediaspace_domain* with the actual value in your environment.
*   **mediaspace_path** – the URI of MediaSpace, when MediaSpace is installed under a subfolder. Replace *mediaspace_path* with the actual value in your environment.
*   **user** – the controller that handles all user-related actions in MediaSpace. This element is hardcoded.
*   **authenticate** – the action within the user controller that handles the authentication. This element is hardcoded.
*   **sessionKey** – the parameter name in the URI for the secure hash string. This element is hardcoded.
*   **[secure hash string][6]** – the token that your login page creates and then passes to MediaSpace in the redirect URL.

 [6]: #SecureHashString

<p class="mce-heading-3">
  Retaining User Context (Returning to the Referring Page)
</p>

In case a user followed a link to a specific page in MediaSpace but needs to authenticate in order to reach this resource, MediaSpace SSO will pass a GET parameter, named "ref" to the configured SSO login page. 

For example, if the SSO login URL is configured to:

http://*company.domain.com/path*/to/mediaspace\_sso\_page.ext

The user will be redirected to:

http://*company.domain.com/path*/to/mediaspace\_sso\_page.ext?ref={relative URL in MediaSpace requested by the user}

The value of the "ref" parameter can be added to the authentication URL that was constructed, so when the user is redirected back to MediaSpace (with the session key), MediaSpace will redirect the user to the originally requested resource.

The "ref" parameter should be added as a GET parameter to the URL.

For example:

http://*mediaspace\_domain/mediaspace\_path*/user/authenticate/sessionKey/{secure hash string}?ref={original ref value}

We recommend that you support this use case in your SSO implementation.

<p class="mce-heading-3">
  <a name="SecureHashString"></a>Generating and Validating a Secure Hash String
</p>

A secure hash string is [generated][7] in your login page and is passed to MediaSpace in the redirect URL.

 [7]: #GeneratingCodeSecureHashString

As part of the MediaSpace authentication process, MediaSpace [validates][8] the secure hash string received from the login page.

 [8]: #ValidatingCodeSecureHashString

<p class="mce-heading-4">
  <a name="GeneratingCodeSecureHashString"></a>Sample Code for Generating a Secure Hash String
</p>

The following pseudo code demonstrates how to generate a secure hash string. 

<pre class="brush: php;fontsize: 100; first-line: 1; ">info = “userId;userRole;extraUserInfo;expiry;random”
	salt = {MEDIA_SPACE_LOGIN_SECRET}
	signature = sha1(salt+info)
	stringToHash = signature+”|”+info
	hashedString = base64_encode(stringToHash)</pre>

*   **userId** – the ID of the user in your system as you use want it to be identified in Kaltura.
*   **userRole** – the application role that you assign the user in MediaSpace.
*   **extraUserInfo** – a key-value string in which pairing is specified using colons (:) and pairs are separated by commas (,). For example: extraUserInfo = "firstName:John,lastName:Doe,email:JohnDoe@mail.com"
*   **expiry** – a Unix-timestamp after which the hashed string is no longer valid.
*   **random** – a randomly generated number from 0-32000.
*   **MEDIA\_SPACE\_LOGIN_SECRET** – the secret string shared by MediaSpace and the login page.

<p class="mce-heading-4">
  <a name="ValidatingCodeSecureHashString"></a>Sample Code for Validating a Secure Hash String
</p>

The following pseudo code demonstrates how the secure hash string passed in the sessionKey URL parameter is validated.

<pre class="brush: php;fontsize: 100; first-line: 1; ">decodedString = base64_decode(hashedString)
	separate decoded string by |, first part is signature second is info
	salt = {MEDIA_SPACE_LOGIN_SECRET}
	validateSignature = sha1(salt, info)
	IF validateSignature = signature AND expiry &lt; current unix time
		hash is valid
	ELSE
		hash is not valid</pre>

The validation code mirrors the [token generation][7] actions in reverse order:

1.  The secure hash string is decoded from its base64 encoding.
2.  The decoded string is separated into two parts: the signature and the information.
3.  The code creates a signature using the information provided and the SSO secret, which is defined in the MediaSpace configuration.

If the signature created by the code matches the signature provided by the redirect URL and the expiration date did not pass, the secure hash string is valid and the user is successfully authenticated.

<p class="mce-heading-2">
  Configuring the SSO Gateway in MediaSpace
</p>

To learn how to configure the SSO Gateway for authentication and authorization in MediaSpace, refer to [Configuring SSO Gateway Authentication and Authorization][3].