---
layout: page
title: "How to configure VOD and Live Streaming using a BitGravity account on the Kaltura SaaS Platform?"
date: 2014-03-26 00:00:39
---

# <span style="color: #484848; font-size: 18pt;"></span>

Ensure that the following features/options are configured in the account on the Kaltura Admin Console:

# <span style="color: #484848; font-size: 18pt;"></span>

1.  Configure the account to support Live Streaming.
2.  Configure the account as a sub account of TCL main account, so that TCL can control the new account via the Management Console.

# <span style="color: #484848; font-size: 18pt;">Partner’s Parameters for VOD Streaming</span>

You will need to supply us with the Partner’s Parameters for VOD Streaming from your BitGravity account.

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          <strong>Information</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          <strong>Value</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          Partner Name
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          TCL-{company id} See <a href="#network-settings">Network Settings Parameters</a>.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          Enable Remote Storage
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          Yes/No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          Enable Origin Pull
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          Yes/No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          VOD Origin Pull Hostname
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          {company id}.pc.cdn.bitgravity.com
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          VOD Remote Storage Hostname
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          {company id}.bc.cdn.bitgravity.com
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          Multiscreen-WSA Origin Pull Hostname
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          {company id}.pc-s.cdn.bitgravity.com
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          Multiscreen-WSA Remote Storage Hostname
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          {company id}.bc-s.cdn.bitgravity.com
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          Enable SecureAccess
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          Yes/No
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          URL Secret (If SecureAccess enabled)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="362">
        <p>
          Token expiring
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="437">
        <p>
          Default - 300
        </p>
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <a name="network-settings"></a>Network Settings Parameters
</p>

The Company Id should be taken from “Network Settings” > “Network Overview” tab.

<img src="../../assets/1402.img">

<p class="mce-procedure">
  To configure the Origin Pull ONLY
</p>

<p style="padding-left: 30px;">
  The following setting should be used in BitGravity configuration:
</p>

*   The Origin pull should be set to: {company id}.tcl.origin.kaltura.com

<p class="mce-heading-2">
  Partner’s Parameters for Remote Storage
</p>

<p class="Procedure mce-procedure">
  To configure the Partner’s Parameters for Remote Storage
</p>

Please supply the following parameters from your BitGravity remote storage account.

<table border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="309">
        <strong>Information</strong>
      </td>
      
      <td style="text-align: left;" valign="top" width="489">
        <strong>Value</strong>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="309">
        BitGravity FTP username
      </td>
      
      <td style="text-align: left;" valign="top" width="489">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="309">
        BitGravity FTP password
      </td>
      
      <td style="text-align: left;" valign="top" width="489">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="309">
        BitGravity FTP Host name
      </td>
      
      <td style="text-align: left;" valign="top" width="489">
         
      </td>
    </tr>
  </tbody>
</table>

<p class="mce-heading-3">
  <span style="font-size: 1.5em;">SecureAccess Configuration</span>
</p>

Secured access should be configured on the ‘/s’ URL in BitGravity’s dashboard.

<img src="../../assets/1416.img">

<p class="Figure">
   
</p>

 