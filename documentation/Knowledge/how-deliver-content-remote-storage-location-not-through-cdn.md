---
layout: page
title: "How to deliver content from a remote storage location (not through a CDN)"
date: 2012-11-05 23:37:00
---

At times, customers may prefer to have their content located on their premises, and do not have a CDN for delivering content. This may be applicable for low usage streaming inside an organizational network and customers can use their own servers for such content delivery. For delivering content in a progressive download mode an internal Apache server may be used. 

The following describes the steps for setting up remote storage configuration to deliver content from an Apache server within the customer's internal network.

<p class="mce-heading-3">
  Disclaimer
</p>

1.  The following solution is for customers that use Kaltura SaaS and would like to host and play content from their local environment. (Customers that use Kaltura On-Prem can choose to play content directly from their Kaltura server.)
2.  The proposed solution will work only for a small number of viewers that are all in close proximity (preferably on the same LAN).
3.  This process works for progressive download only (not RTMP, HDS, HLS, …). 

<p class="mce-procedure">
  To configure FTP & the Apache Server  (By The Customer)
</p>

1.  Set up a machine with an Apache server and an FTP server. 
2.  Configure the Apache server so that it can serve the files dropped in the FTP folder. (Use the document root or virtual directory, or any other applicable method.)<span></span>

<p class="mce-heading-3">
  Information Required from the Customer
</p>

The customer should send the following information to Kaltura:

1.  FTP details: host, user, password and the path of the base folder under which he wants the flavors to reside
2.  The base HTTP URL through which the FTP folder content can be downloaded (the URL to the Apache that was installed…)
3.  Recommended: Send the FTP and HTTP path of a sample file (for example, the file /a/b in the FTP folder, can be downloaded from   
    <http://www.somedomain.com/1/2/a/b>)

<p class="mce-procedure">
  To configure the Remote Storage Setup (By Kaltura)
</p>

1.  In the KAC, create a new remote storage profile under the partner account.
2.  Paste the FTP details under the "export details" section.
3.  Set 'HTTP delivery base URL'.
4.  Select all the flavors that should be exported (under advanced). 
5.  In the remote storage profiles screen, under "actions", set the profile status to automatic.

<span style="color: #ff0000;"><em> </em></span>