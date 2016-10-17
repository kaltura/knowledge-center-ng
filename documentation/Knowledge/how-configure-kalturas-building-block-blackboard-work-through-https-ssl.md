---
layout: page
title: "How to configure Kaltura's Building Block for Blackboard to work through HTTPs / SSL"
date: 2013-11-14 14:09:05
---

**Instructions:.**

**Step 1 for OnPrem accounts:**

Change partner's CDN Host ("Service Host Name") configuration in Admin Console to: *http://cdnsecakmi.kaltura.com*

 **<img src="../../assets/1247.img">

**Note** - this should be configured with http prefix and NOT https.

If the OnPrem CDN host (for example cdn.mykaltuasystem.com) has a valid SSL certificate, this step is not necessary.

If the OnPrem CDN host does not have a valid HTTPs certificate, the CDN host should be changed to a host with a valid SSL certificate.

**Step 2**

1.  Go to 'System Admin' tab.
2.  Go to 'Building Block' in the 'Building Block' window.
3.  Go to 'Installed Tools'.
4.  Find 'Kaltura Integration' click on the row and on 'Setting'.
5.  Go to 'Kaltura Server Connection Configuration'.
6.  Change the End point to [https://www.kaltura.com][1]. (For OnPrem, it should be the server host address.)
7.  Add ‘s’ to the “Report end point” as well.

 [1]: https://www.kaltura.com/

<img src="../../assets/1248.img">

**Step 3**

1. Go back to “Kaltura Video Building Block Configuration”.

2. Under "Widget Settings" you will find a list of UiConf. Please provide <a href="mailto:customercare@kaltura.com" target="_blank">Kaltura Customer Care</a> with that list.

In addition, please confirm that your Blackboard supports SSL:

System admin> Security tab> SSL choice> 1.

System-wide -> mark the: “SSL system-wide” option.

**Notes for OnPrem Customers:**

SSL is usually configured in the machine that holds the Application (for example MediaSpace) since it is 'customer facing'.  
However, SSL should also be configured on the API machines the application communicates with.

SSL can also be configured in the KMC machine if needed, which is typically accessed by staff members.