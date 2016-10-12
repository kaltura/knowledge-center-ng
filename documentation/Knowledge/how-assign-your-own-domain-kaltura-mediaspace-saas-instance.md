---
layout: page
title: "How to Assign Your Own Domain to a Kaltura MediaSpace SaaS Instance?"
date: 2013-06-05 18:08:32
---

Kaltura uses a wildcard domain name for all MediaSpace SaaS instances. By default the domain name is *[**<span style="color: #ff0000;">partner id</span>**].mediaspace.kaltura.com*.

If you want to use a more informative URL, you can request our support team to assign a more meaningful alias for your MediaSpace instance, for example: ***[<span style="color: #ff0000;">company name</span>].mediaspace.kaltura.com***.

If you want to use your own domain name, for example, ***videos.company.com***, Kaltura's MediaSpace SaaS environment supports <a href="http://en.wikipedia.org/wiki/CNAME_record" target="_blank">CNAME</a> records, allowing your end-users to browse for your domain, while behind the scenes accessing the MediaSpace instance and URL assigned in our SaaS environment.

<p class="mce-procedure">
  To use your own domain perform the following actions
</p>

1.  Have your IT department or web host provider configure a CNAME DNS record to point to your Kaltura MediaSpace SaaS instance: *****[****<span style="color: #ff0000;"><em>partner id</em></span>****]**.mediaspace.kaltura.com***.
2.  Contact our support team and provide them with your partner ID and your own URL that was configured, as we will need to assign your domain as an additional alias to your MediaSpace instance.

 

<p class="mce-procedure">
  To set your MediaSpace with SSL perform the following actions
</p>

<div style="padding-left: 60px;">
  If your MediaSpace SaaS instance is configured to use HTTPS instead of HTTP, you will need to provide our support team with the SSL certificate for your domain, <strong><em>videos.company.com</em></strong>, so we can deploy the SSL certificate on our server. 
</div>

<p style="padding-left: 60px;">
  Include the following files:
</p>

*   The private key file (.key extension) to apply to SSLCertificateKeyFile
*   The intermediate certificate file to apply to SSLCertificateChainFile 
*   The domain certificate (for example videos.customer.com.crt) to apply SSLCertificateFile

<p style="padding-left: 60px;">
  <span class="mce-note-graphic">If you cannot send us the private key due to organizational security reasons, please provide us with the following information:</span>
</p>

*   **Common Name**: The fully-qualified domain name, or URL, you are securing.
*   If you are requesting a Wildcard certificate, add an asterisk (*) to the left of the common name where you want the wildcard, for example **.coolexample.com*.
*   **Organization**: The legally-registered name for your business. If you are enrolling as an individual, enter the certificate requestor's name.
*   **Organization Unit**: If applicable, enter the DBA (doing business as) name.
*   **City or Locality**: Name of the city where your organization is registered/located. Do not abbreviate.
*   **State or Province**: Name of the state or province where your organization is located. Do not abbreviate.
*   **Country**: The two-letter International Organization for Standardization (ISO) format <a href="http://www.iso.org/iso/home/standards/country_codes/iso-3166-1_decoding_table.htm" target="_blank">country code</a> for where your organization is legally registered.

<p style="padding-left: 60px;">
  Kaltura will create and provide the CSR. 
</p>

<p style="padding-left: 60px;">
  <span class="mce-note-graphic">The PEM format is the most common format that <a href="http://www.sslshopper.com/certificate-authority-reviews.html" target="_blank">Certificate Authorities</a> issue certificates in. PEM certificates usually have extentions such as <strong>.pem, .crt, .cer, and .key</strong>. They are Base64 encoded ASCII files and contain "-----BEGIN CERTIFICATE-----" and "-----END CERTIFICATE-----" statements. </span>
</p>