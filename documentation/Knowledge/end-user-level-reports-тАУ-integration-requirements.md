---
layout: page
title: "End-User Level Reports – Integration Requirements"
date: 2012-12-31 23:19:30
---

Kaltura’s End-User Level Reports provide answers to customer’s questions about end-user behavior and is primarily intended for the Education and Enterprise markets.

### Enablement

As a first step,  End-User reports should be enabled in the Kaltura Admin Console by a Kaltura admin, so that the partner account can start aggregating data for reports.

Contact your Kaltura Account Manager or Kaltura support to configure your administration settings..

### Detailed Requirements

The following parameters may be transferred from the application and from Kaltura players only, for an application to support End-User Level Reports.

*   [userId][1]
*   [applicationName][2]
*   [playbackContext][3]

 [1]: #UserId
 [2]: #ApplicationName
 [3]: #PlaybackContext

These parameters should be transferred to Kaltura for each event that the player is reporting (player load, drop, share,  and all other events).

#### <a name="UserId"></a>userId

flashVar (userId)

The userId parameter is manadatory and is the basic parameter that allows for collecting and displaying data at the user level.

The userId can be passed in the Kaltura Session or as a flashVar (userId). If the userId is passed both via KS and flashVar, the KS value is used. We recommend delivering the userId parameter on the KS.

#### applicationName<a name="ApplicationName"></a>

flashVar – applicationName

The applicationName parameter is used to filter  the different reports by application. The applicationName parameter is optional.

#### <a name="PlaybackContext"></a>playbackContext

flashvar - playbackContext.

The playbackContext value is the category ID and is used to filter content by channel/category/course in the different reports. Playback Context represents the category in which a certain action was performed from. The playbackContext parameter is optional.

For example, if an entry has 2 categories, A and B, if you filter content by category A, the returned results are the plays for the entry in both categories, namely A and B.

If you filter content by playback context on category A, the returned results are only the plays done on category A.

### Application Status For End-User Level Reports

#### Kaltura Video Building Block for Blackboard

*   Blackboard Learn 9.x v2 reports the user ID, but not report course (category) nor application.
*   Blackboard Learn v3, v4 reports all 3 parameters.

#### Kaltura Video Package for Moodle

*   Kaltura Video Package v1 for Moodle 2.x  does not report the user ID, and does not have courses reflected as categories in the KMC. The Application parameter is not relevant.
*   Moodle versions  (v2, v3) include all 3 parameters.
*   The user level reports are exposed within the application.

#### Kaltura Video Tool for Sakai

*   Kaltura Video Tool for Sakai CLE v1 reports user ID, but does not report the  course (category) or application.  
*   Kaltura Video Tool for Sakai CLE v2 reports the user ID, but  does not report the  course (category) or application.
*   The user level reports are exposed within the application.

#### MediaSpace

*   KMS 3 does not report all 3 parameters.
*   KMS 4 and up reports all 3 parameters.

#### Kaltura Sharepoint Extension

*   Kaltura Sharepoint Extension v2  does not report all 3 parameters.

### Old Version's Applications Integration

*   Kaltura Video Building Block for Blackboard v2 is based on categories.  Professional Services for Blackboard v2 are not provided by Kaltura sinceBlackboard is a java application that has little flexibility for additional modules.
*   Kaltura SharePoint extension is based on categories. Professional Services for the Kaltura  SharePoint Extension are not provided by Kaltura sincethe Sharepoint Extension is a .NET application  that has little flexibility for additional modules.
*   Other LMS and CMS extensions (Moodle v1 extension and Blackboard v1) are not based on categories.
*   Professional Services may be engaged to enable MediaSpace 3 .

### Non-Kaltura-Applications Integration

For integrations with non-Kaltura applications you will need to create a KS for passing the User ID.

*   For example:
*   Install the Kaltura PHP client library: <a href="http://www.kaltura.com/api_v3/testme/client-libs.php" target="_blank">http://www.kaltura.com/api_v3/testme/client-libs.php</a>
*   Implement a local session as described in option 3 using UserID in the variable $userId: <a href="http://knowledge.kaltura.com/faq/how-create-kaltura-session" target="_blank">http://knowledge.kaltura.com/faq/how-create-kaltura-session</a>
*   Passing the parameter also depends on the application’s integration. Most integrations into an existing system usually have some kind of internal API to query for the current user ID. For an application name, a simple string needs to be added. Adding the string  as a flashvar is a matter of modifying the embed codes, which are generated in the integration, to include the additional flashvars.

<span style="text-align: justify;">The relevant flashVars are:</span>

<pre class="brush: as3;fontsize: 100; first-line: 1; ">&lt;param name="flashVars"  value="applicationName=Application1&amp;playbackContext=86091" /&gt;</pre>

 Where:

*   applicationName - the name of the application as it will be presented in the analytics, sample: "Application1"
*   playbackContext - the category ID (e.g., 86091)

 