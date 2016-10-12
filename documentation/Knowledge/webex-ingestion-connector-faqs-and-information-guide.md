---
layout: page
title: "WebEx Ingestion Connector FAQs and Information Guide"
date: 2014-06-02 00:40:20
---

# What is the WebEx Ingestion Connector?

The WebEx Ingestion Connector is a connector on Kaltura server side that automatically imports content from a customer’s WebEx server and intelligently assigns the content to the content owner.

# Terminology

WebEx account – the WebEx URL in the organization, for example, kaltura.webex.com

WebEx host – a specific user in that account. There are 2 types of hosts used in organizations:

*   **Generic host** – An organization with an account/s that has hosts, where each host may have many users (employees/faculty/etc.)  For example, the way Kaltura uses WebEx. 
*   **Unique host** – Each user in the organization has their own personal host that is used to create/participate in live events.

In some of the organizations the unique host is more common, though some departments might still have a single host that has many users.

# How does the WebEx Ingestion Connector Work?

The WebEx Ingestion Connector is based on the <a href="http://knowledge.kaltura.com/node/46" target="_blank">Kaltura Drop Folder Mechanism</a>. Periodically, the connector checks the WebEx server for new content then using the WebEx APIs, it imports that content into Kaltura.

Kaltura imports the content from the entire WebEx account and not from each host individually.

The content is delivered in the form of ARF files, which are WebEx’s proprietary format. The Kaltura server, using WebEx’s NBR player tool (that is installed on the Kaltura Data-Center) transcodes the ARF file to a WMV file and then to the flavor-set chosen by the customer (by default to Kaltura MP4 set).

The entry includes:

*   The original ARF file – that can playback on a WebEx player and stored for future use (The file does not have to be hosted on a WebEx server as well.)
*   A Kaltura source file – WMV format, from which the customer can re-transcode to any flavor
*   All the customer’s flavors

<img src="{{site.url}}/assets/1443">

On top of the video content itself, Kaltura imports the content metadata as "name" and "host name".

The content on Kaltura side is assigned with this metadata as well – name (added with time to make it unique) and owner.

If the organization uses a unique host method and SSO between WebEx and KMS (for example, user mail for user name), then the user *john.doe@organization.com* will see their recordings appear in ‘My media’ in their KMS.

If an automatic assignment of the WebEx recording to a Kaltura user is not needed, or when a WebEx host ID does not match the Kaltura user ID (for example, if the WebEx host is a generic user like generichost3) then we can pre-configure that all the recordings from this host will be assigned to Kaltura user *john.doe@organization.com*.

When you import a WebEx session into Kaltura, a fixed single screen is imported and the WebEx interactivity is no longer available. Recordings imported from WebEx become video entries in Kaltura. The WebEx enabled interactivity with the ARF file on the WebEx player (for example hiding, and moving displayed panels ) is lost.

The WebEx Ingestion Connector dynamically imports the WebEx panels as they are configured in the WebEx console. If you select panels in Panels Display Options ( as shown in the following screenshot) in the recording configuration , they will be included in the created video. Unchecked panels are not included. This option is available per the API that WebEx (Cisco) supports.

<img src="{{site.url}}/assets/1445">

# Can the WebEx Ingestion Connector work in an OnPrem environment?

Technically, it is possible but we do not offer this product out of the box for OnPrem at the moment.

# Can a WebEx Ingestion Connector automatically import only a subset of the WebEx hosts?

At the moment, the connector imports the entire account content and not pre-defined hosts. In case specific users need their recording sessions, it is recommended to configure their settings on the WebEx side. For example, a customer has 100 hosts for 100 employees. If all of the 100 are recording sessions and would like to search, embed, share, etc. afterwards, the Kaltura WebEx connector will import the entire account (all the 100 employees) for their use. If, only 20 hosts need their recordings and the rest of the 80 may be using their recordings for spontaneous meetings and don’t need to record anything, the customer needs is to import only the 20 hosts and ignore the 80 hosts that have recorded sessions there. The customer can block the recording option for the 80 users. If the use-case does not require recording sessions, you can configure this on the WebEx workflow even before accessing Kaltura.

# How many WebEx Ingestion Connectors do I need if I have few WebEx accounts in my organization?

A WebEx Ingestion Connector is defined per a single WebEx account. Several Kaltura accounts can have the same WebEx Ingestion Connector configured on them.

# Can the WebEx Ingestion Connector auto-delete content from the WebEx server?

Yes, that is possible and configurable. Files will be deleted only if they were successfully imported to Kaltura. Files with errors are not be deleted from the WebEx server.

Note that files that were imported but not properly transcoded will still be deleted from the WebEx server, though Kaltura will host the ARF file so that manual re-transcoding is possible and content will not be lost.

# How long does it take for a recording to show up on Kaltura?

The turnaround time is built out of few elements:

*   Availability on WebEx server – from the second you ended your session it will take few minutes for it to appear on the server – depends on WebEx.
*   Drop folder cycle time – currently, the default is configured to scan the WebEx server every 15 minutes (900 seconds) – so it will be less than 15 minutes for this phase.
*   Import of the file from WebEx server to the Kaltura server – This is rather fast even for large files, and should take few minutes.
*   File Transcoding – since this is a proprietary file format, it usually takes times 3 of the session time to transcode the file. So for example, a 1 hour session will take ~3 hours to transcode.

it is safe to assume that after you finish recording a 1 hour session in WebEx the recording should be available for playback in KMS after 4 hours.

# Can a customer configure the Drop Folder Cycle Time?

Contact your Account Manager and Product IT representative to change the drop folder cycle time. They will create a special worker for your drop folder and setup a different drop folder cycle time.

# What do you need to provide to activate the drop folder cycle time?

You will be required to obtain info from WebEx (Cisco) for y<span>our Project Manager (on top of the configuration and test information).</span><span><br /></span>

We need to know some of the basic API IDs for the setup - siteID and partnerID . This inform<span style="font-size: 10px;">ation is free of charge to obtain from Cisco but needs to be provided by your WebEx  Account Manager.</span>

For example, the following displays the information that was provided to us for webex.kaltura.com:

<table style="width: 779px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td colspan="2" valign="top" width="779">
        <p>
          <strong><em>Welcome to the WebEx API</em></strong>
        </p>
        
        <p>
          <strong><em>Thank you for your interest in the WebEx API! We are excited to provide you with the following API related information about your site</em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Site Information:</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong> </strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>URL:</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><a href="https://kaltura.webex.com/"><em>https://kaltura.webex.com</em></a></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Site ID: </em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><em>346216</em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Partner ID:</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><em>563rt</em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Cluster:</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><em>C</em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>API Information</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong> </strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Single Sign On: </em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><em>Enabled</em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>URL:</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><em>Enabled</em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>XML:</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><em>Enabled</em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>XML URL: </em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><a href="https://kaltura.webex.com/WBXService/XMLService"><em>https://kaltura.webex.com/WBXService/XMLService</em></a></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Support Information</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong> </strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Site/Account Questions: </em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><em>Please contact your CSM </em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>API Development: </em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><a href="mailto:apidev@webex.com"><em>apidev@webex.com</em></a></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Production API Issues: </em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><em>Please reference your webex site(s) support page for technical contact information.</em></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>Other Technical/Product Questions: </em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><a href="mailto:support@webex.com"><em>support@webex.com</em></a></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="292">
        <p>
          <strong><em>General API information and FAQs:</em></strong>
        </p>
      </td>
      
      <td valign="top" width="487">
        <p>
          <strong><a href="http://developers.webex.com/"><em>http://developers.webex.com</em></a></strong>
        </p>
      </td>
    </tr>
  </tbody>
</table>

# What about migration of existing content in the WebEx server?

You can set the time you want to begin the import from for the first import to the drop folder from the WebEx server. You can import all the content from the beginning of all time or you can decide to import only 1 month back. For the 2<sup>nd</sup> import and onwards, only the new recordings added will be imported.

Migration is performed by Kaltura personnel - configurable through the TestMe Console but not the Kaltura Admin Console.

# Where can I see the drop folder files that failed imports?

Files that failed to import are displayed in the drop-folder tab.

For more information, see <span><a href="http://knowledge.kaltura.com/node/46#statuses">Drop Folder Files' Statuses</a>.</span>