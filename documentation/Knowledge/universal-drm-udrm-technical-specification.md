---
layout: page
title: "Universal DRM (uDRM)  Technical Specification"
date: 2016-03-31 20:21:06
---

<div class="WordSection1">
    [collapsed title="Overview of Universal DRM"]
  </div>
  
  <h1>
    1  Overview
  </h1>
  
  <p>
     
  </p>
  
  <h2>
    1.1            About This Document
  </h2>
  
  <p>
    This document provides the technical specifications for the Kaltura uDRM module that enables integration with the uDRM API interface.
  </p>
  
  <h2>
    1.2            Intended Audience
  </h2>
  
  <p>
    This document is intended for technical architects and developers who are involved in integrating with the Kaltura uDRM encryption and license server APIs.
  </p>
  
  <h2>
    1.3            Abbreviations
  </h2>
  
  <p>
    The following abbreviations are used throughout this document.
  </p>
  
  <p class="NoSpace">
     
  </p>
  
  <table style="width: 698px;" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="198">
          <p class="TableHeading">
            Abbreviation
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableHeading">
            Meaning
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            API
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Application Programming Interface
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            BE
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Backend
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            CAS
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Conditional Access System
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            CDN
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Content Delivery Network
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            CENC
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Common Encryption
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            CRUD
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Create, Read, Update, and Delete
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            DB
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Database
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            DRM
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Digital Rights Management
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            HDCP
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            High Bandwidth Digital Content Protection
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            HTTP
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Hypertext Transfer Protocol
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            JSON
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            JavaScript Object Notation
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            OTT
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Over The Top
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            OVP
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Open Video Platform
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            REST
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Representational State Transfer
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            SDK
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Software Development Kit
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            TBD
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            To Be Defined
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            uDRM
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Universal DRM
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            URL
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Uniform Resource Locator
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
            XDCR
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            Cross Data Center Replication
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <h2>
    1.4            Referenced Documents
  </h2>
  
  <p>
    The following documents are referenced throughout this document.
  </p>
  
  <p class="NoSpace">
     
  </p>
  
  <table style="width: 698px;" border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="198">
          <p class="TableHeading">
            Doc Number
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableHeading">
            Doc Title
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
             
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            <a href="http://www.ssae16guide.com/ssae-16-compliance/">SAE16 Qualification Report</a>
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="198">
          <p class="TableBodyText">
             
          </p>
        </td>
        
        <td valign="top" width="500">
          <p class="TableBodyText">
            <a href="http://docs.couchbase.com/admin/admin/XDCR/xdcr-dataEncryption.html">Couchbase XDCR Data Encryption</a>
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="uDRM Module Specifications"]
  </p>
  
  <h1>
    2  uDRM Module Specifications
  </h1>
  
  <h2>
    2.1            Architecture Diagram
  </h2>
  
  <p>
    Figure 1 presents the uDRM architecture.
  </p>
  
  <p class="Figure">
     <img src="{{site.url}}/assets/3085">
  </p>
  
  <p>
    Figure 1: uDRM Architecture
  </p>
  
  <p>
    The components in the uDRM module include the following:
  </p>
  
  <ul>
    <li>
      <strong>Encryption Modules – </strong>internal Kaltura encryption modules (whether as part of the on-the-fly packager or pre-encryption jobs) or external encryption modules (also can be pre-encryption processes or part of the on-the-fly packaging modules)
    </li>
    <li>
      <strong>Secure Players –</strong> Kaltura Secure Player or external players integrating with the uDRM license interface
    </li>
    <li>
      <strong>API Interface – </strong>uDRM API interface
    </li>
    <li>
      <strong>DRM Module Implementations –</strong> business logic layer of the uDRM module
    </li>
    <li>
      <strong>DRM Provider Logic – </strong>DRM servers and SDK hosted or proxied by the Kaltura uDRM server for generating DRM specific licenses and keys
    </li>
    <li>
      <strong>Key/License Store –</strong> uDRM DB (Couchbase) for key storage
    </li>
  </ul>
  
  <h2>
    2.2            Supported DRM Providers
  </h2>
  
  <p>
    The Kaltura uDRM module currently supports the following DRM formats and DRM providers:
  </p>
  
  <ul>
    <li>
      CENC<ul>
        <li>
          Playready
        </li>
        <li>
          Widevine (Widevine Modular)
        </li>
      </ul>
    </li>
    
    <li>
      Playready (Smooth Stream)
    </li>
    <li>
      Widevine (Classic)
    </li>
    <li>
      Apple Fairplay
    </li>
    <li>
      Adobe Primetime (TBD)
    </li>
  </ul>
  
  <h2>
    2.3             uDRM APIs
  </h2>
  
  <p>
    The Kaltura uDRM module exposes a REST API interface supporting the following operations:
  </p>
  
  <ul>
    <li>
      Encrypt – generating an encryption key for the relevant encryption module
    </li>
    <li>
      License – generating a license for the relevant DRM client
    </li>
    <li>
      Policy – CRUD (create/read/update/delete) operations on DRM policies
    </li>
  </ul>
  
  <h3>
    2.3.1       Authentication
  </h3>
  
  <p>
    Each request to the uDRM interface includes a signature authenticating the request to the relevant provider.
  </p>
  
  <p>
    The signature is constructed in the following manner
  </p>
  
  <p>
    Signature = Base64(SHA1(private_key + data))
  </p>
  
  <p>
    Where:
  </p>
  
  <ul>
    <li>
      private_key – a private key used by the specific DRM client (whether encryption process or DRM client)
    </li>
    <li>
      data – the data passed in the API request (can be the POST data or the query string data, excluding the signature, depending on the request type)
    </li>
  </ul>
  
  <h3>
    2.3.2       Custom Data
  </h3>
  
  <p>
    All requests to uDRM endpoints contain a custom data object. The custom data is passed as part of the query parameters, or as part of the JSON post data (see specific API tables for details) in Base64.
  </p>
  
  <p>
    The custom data is of the following format:
  </p>
  
  <p>
    {
  </p>
  
  <p>
        "ca_system": "OTT",
  </p>
  
  <p>
        "account_id": "167",
  </p>
  
  <p>
        "content_id": "file_name.ism",
  </p>
  
  <p>
        "files": "",
  </p>
  
  <p>
        “user_token” :”12345”,(optional)
  </p>
  
  <p>
        “key”: “CsjUtytiiiieee”, (optional)
  </p>
  
  <p>
        “key_id”: “file_external_id” (optional),
  </p>
  
  <p>
        “udid”, :”12345678” (optional)
  </p>
  
  <p>
    }
  </p>
  
  <p>
    Where:
  </p>
  
  <ul>
    <li>
      ca_system: OTT/OVP – static parameter (configured as part of the client onboarding)
    </li>
    <li>
      account_id: the account identifier (provisions as part of the account onboarding)
    </li>
    <li>
      content_id: the content external ID
    </li>
    <li>
      files: empty (future use)
    </li>
    <li>
      user_token:the user ID (optional)
    </li>
    <li>
      key:  for external encryption processes (see section ‎2.3.3) supplying a pre-generated key. Base64 encoded.
    </li>
    <li>
      key_id: for external encryption processes (see section ‎2.3.3) supplying a pre-generated key ID. Base64 encoded.
    </li>
    <li>
      Udid : the device udid
    </li>
  </ul>
  
  <h3>
    2.3.3       HTTP Methods and Samples
  </h3>
  
  <p>
    <a href="https://kaltura.sharepoint.com/product/Shared%20Documents/PaaS/DRM/DRM%20specifications.docx#get">GET</a>, <a href="https://kaltura.sharepoint.com/product/Shared%20Documents/PaaS/DRM/DRM%20specifications.docx#post">POST</a>, <a href="https://kaltura.sharepoint.com/product/Shared%20Documents/PaaS/DRM/DRM%20specifications.docx#put">PUT</a>, <a href="https://kaltura.sharepoint.com/product/Shared%20Documents/PaaS/DRM/DRM%20specifications.docx#delete">DELETE</a>
  </p>
  
  <p>
    <strong><a name="get"></a>HTTP Method  - GET</strong>
  </p>
  
  <p>
    <strong>Description</strong> - Returns content data, if it exists.
  </p>
  
  <p>
    <strong>Data</strong> - In query string:
  </p>
  
  <p class="CodeList">
    ?custom_data={custom_data}
  </p>
  
  <p>
    <strong>Sample Request</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
        "ca_system": "OTT",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "account_id": "167",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "content_id": "file_name.ism",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "files": ""
  </p>
  
  <p class="CodeListCxSpLast">
    }
  </p>
  
  <p>
    <strong>Sample Response</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
      "pssh": [
  </p>
  
  <p class="CodeListCxSpMiddle">
        {
  </p>
  
  <p class="CodeListCxSpMiddle">
          "data": "pssh data”,
  </p>
  
  <p class="CodeListCxSpMiddle">
          "uuid": "<uuid>
  </p>
  
  <p class="CodeListCxSpMiddle">
        }
  </p>
  
  <p class="CodeListCxSpMiddle">
      ],
  </p>
  
  <p class="CodeListCxSpMiddle">
      "file": null,
  </p>
  
  <p class="CodeListCxSpMiddle">
      "license_url": "<base64 la_url>
  </p>
  
  <p class="CodeListCxSpMiddle">
      "key": "<key>
  </p>
  
  <p class="CodeListCxSpMiddle">
      "key_id": "<base 64 of key ID=",
  </p>
  
  <p class="CodeListCxSpMiddle">
      "content_id": “<content id>
  </p>
  
  <p class="CodeListCxSpLast">
    }
  </p>
  
  <p>
    <strong><a name="post"></a>HTTP Method - POST</strong>
  </p>
  
  <p>
    <strong>Description - </strong>Creates a new key (if content exists, returns existing content)<strong>            </strong>
  </p>
  
  <p>
    <strong>Data -  </strong>As JSON In POST data<strong>        </strong>
  </p>
  
  <p>
    <strong>Sample Request</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
        "ca_system": "OTT",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "account_id": "167",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "content_id": "file_name.ism",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "files": ""
  </p>
  
  <p class="CodeListCxSpLast">
    }<strong>  </strong>
  </p>
  
  <p>
    <strong>Sample Response</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
      "pssh": [
  </p>
  
  <p class="CodeListCxSpMiddle">
        {
  </p>
  
  <p class="CodeListCxSpMiddle">
          "data": "pssh data”,
  </p>
  
  <p class="CodeListCxSpMiddle">
          "uuid": "<uuid>
  </p>
  
  <p class="CodeListCxSpMiddle">
        }
  </p>
  
  <p class="CodeListCxSpMiddle">
      ],
  </p>
  
  <p class="CodeListCxSpMiddle">
      "file": null,
  </p>
  
  <p class="CodeListCxSpMiddle">
      "license_url": "<base64 la_url>
  </p>
  
  <p class="CodeListCxSpMiddle">
      "key": "<key>
  </p>
  
  <p class="CodeListCxSpMiddle">
      "key_id": "<base 64 of key ID=",
  </p>
  
  <p class="CodeListCxSpMiddle">
      "content_id": “<content id>
  </p>
  
  <p class="CodeListCxSpLast">
    }
  </p>
  
  <p>
    <strong><a name="put"></a>HTTP Method - PUT</strong><strong>       </strong>
  </p>
  
  <p>
    <strong>Description - </strong>Creates a new key, overrides if exists<strong>            </strong>
  </p>
  
  <p>
    <strong>Data -  </strong>As JSON in post data
  </p>
  
  <p>
    If data contains the fields key and key_id, it creates a new entry using these parameters. If not, it generates independently (as in the case with POST) and overrides it if the key already exists.<strong>    </strong>
  </p>
  
  <p>
    <strong>Sample Request</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
        "ca_system": "OTT",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "account_id": "167",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "content_id": "file_name.ism",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "files": "",
  </p>
  
  <p class="CodeListCxSpMiddle">
         “key” : “CsjUtytiiiieee”,
  </p>
  
  <p class="CodeListCxSpMiddle">
         “key_id” : “file_external_id”
  </p>
  
  <p class="CodeListCxSpLast">
    }
  </p>
  
  <p>
    <strong>Sample Response</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
      "pssh": [
  </p>
  
  <p class="CodeListCxSpMiddle">
        {
  </p>
  
  <p class="CodeListCxSpMiddle">
          "data": "pssh data”,
  </p>
  
  <p class="CodeListCxSpMiddle">
          "uuid": "<uuid>
  </p>
  
  <p class="CodeListCxSpMiddle">
        }
  </p>
  
  <p class="CodeListCxSpMiddle">
      ],
  </p>
  
  <p class="CodeListCxSpMiddle">
      "file": null,
  </p>
  
  <p class="CodeListCxSpMiddle">
      "license_url": "<base64 la_url>
  </p>
  
  <p class="CodeListCxSpMiddle">
      "key": "<key>
  </p>
  
  <p class="CodeListCxSpMiddle">
      "key_id": "<base 64 of key ID=",
  </p>
  
  <p class="CodeListCxSpMiddle">
      "content_id": “<content id>
  </p>
  
  <p class="CodeListCxSpLast">
    }
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong><a name="delete"></a>HTTP Method - DELETE</strong>
  </p>
  
  <p>
    <strong>Description - </strong>Deletes a key entry if it exists<strong>           </strong>
  </p>
  
  <p>
    <strong>Data - </strong>JSON as part of the POST data<strong>          </strong>
  </p>
  
  <p>
    <strong>Sample Request</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
        "ca_system": "OTT",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "account_id": "167",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "content_id": "file_name.ism",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "files": "",
  </p>
  
  <p class="CodeListCxSpMiddle">
         “key” : “CsjUtytiiiieee”,
  </p>
  
  <p class="CodeListCxSpMiddle">
         “key_id” : “file_external_id”
  </p>
  
  <p class="CodeListCxSpLast">
    }<strong>  </strong>
  </p>
  
  <p>
     
  </p>
  
  <p>
    Figure 2 illustrates a typical encryption flow.
  </p>
  
  <p class="Figure">
     <img src="{{site.url}}/assets/3086">
  </p>
  
  <p>
    Figure 2: Typical Encryption Flow
  </p>
  
  <p>
     
  </p>
  
  <ol>
    <li>
      The encryption component initializes the encryption flow by requesting encryption data from the uDRM encryption interface. This component can be the Kaltura encryption process, or an external one integrating with the uDRM module.
    </li>
    <li>
      The uDRM module checks if encryption data exists for this asset.
    </li>
    <ol style="list-style-type: lower-alpha;">
      <li>
        If it exists, the uDRM module returns the data.
      </li>
      <li>
        If it does not exist:
      </li>
    </ol>
    
    <ul>
      <li>
        The uDRM module calls BE_DRM implementation (e.g. Playready/Widevine) to generate the encryption data.
      </li>
      <li>
        The uDRM module stores the data in an internal data store (Couchbase).
      </li>
      <li>
        The uDRM module returns the data to the encryption component.
      </li>
    </ul>
  </ol>
  
  <p>
    The response format for encryption key requests have the format defined in<a href="#license"> section ‎2.3.4</a>.
  </p>
  
  <h3>
    <a name="license"></a>2.3.4       License
  </h3>
  
  <p>
    The flow for requesting a license is as pictured in Figure 3.
  </p>
  
  <p class="Figure">
     <img src="{{site.url}}/assets/3087">
  </p>
  
  <p>
    Figure 3: License Generation Flow Diagram
  </p>
  
  <p>
     
  </p>
  
  <ol>
    <li>
      The player downloads content from relevant the CDN.
    </li>
    <li>
      The player generates the license URL with the relevant signature and data, and requests a license from the uDRM license acquisition API.
    </li>
    <li>
      The uDRM module retrieves the asset from the internal data store (Couchbase data store).
    </li>
    <li>
      The uDRM retrieves entitlements from the relevant entitlements BE (CAS).
    </li>
    <li>
      Once the entitlement is received, a license is generated by the relevant underlying DRM backend (for instance, Playready server, Widevine SDK).
    </li>
    <li>
      The uDRM module returns the license to the relevant player.
    </li>
  </ol>
  
  <p>
     
  </p>
  
  <p>
    All requests to the license endpoints are with the following URL scheme:
  </p>
  
  <p>
    HTTP(S)://{BASE_UDRM_LOCATION}/{DRM_PROVIDER}/LICENSE?SIGNATURE={SIGNATURE}
  </p>
  
  <p>
    Where:
  </p>
  
  <ul>
    <li>
      BASE_UDRM_LOCATION: constant uDRM prefix
    </li>
    <li>
      DRM_PROVIDER: a DRM provider for license acquisition
    </li>
    <li>
      SIGNATURE: authentication signature
    </li>
  </ul>
  
  <p class="BodyBold">
    Sample Request
  </p>
  
  <p>
    https://udrm.kaltura.com/cenc/widevine/license?signature={signature}
  </p>
  
  <p>
    The uDRM license endpoint supports the operations defined in the following table.
  </p>
  
  <p>
    <strong>HTTP Method - POST</strong>
  </p>
  
  <p>
    <strong>Description - HTTP Method - POST</strong>
  </p>
  
  <p>
    <strong>Description - </strong>Creates a new key (if content exists, returns existing content)<strong>            </strong>
  </p>
  
  <p>
    <strong>Data -  </strong>As JSON In POST data<strong>        </strong>
  </p>
  
  <p>
    <strong>Sample Request</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
        "ca_system": "OTT",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "account_id": "167",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "content_id": "file_name.ism",
  </p>
  
  <p class="CodeListCxSpMiddle">
        "files": ""
  </p>
  
  <p class="CodeListCxSpLast">
    }<strong>  </strong>
  </p>
  
  <p>
    <strong>Sample Response</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
      "pssh": [
  </p>
  
  <p class="CodeListCxSpMiddle">
        {
  </p>
  
  <p class="CodeListCxSpMiddle">
          "data": "pssh data”,
  </p>
  
  <p class="CodeListCxSpMiddle">
          "uuid": "<uuid>
  </p>
  
  <p class="CodeListCxSpMiddle">
        }
  </p>
  
  <p class="CodeListCxSpMiddle">
      ],
  </p>
  
  <p class="CodeListCxSpMiddle">
      "file": null,
  </p>
  
  <p class="CodeListCxSpMiddle">
      "license_url": "<base64 la_url>
  </p>
  
  <p class="CodeListCxSpMiddle">
      "key": "<key>
  </p>
  
  <p class="CodeListCxSpMiddle">
      "key_id": "<base 64 of key ID=",
  </p>
  
  <p class="CodeListCxSpMiddle">
      "content_id": “<content id>
  </p>
  
  <p class="CodeListCxSpLast">
    }
  </p>
  
  <p>
    <strong>Description -  </strong>As JSON In POST data<strong>         </strong>
  </p>
  
  <p>
    <strong>Data</strong>
  </p>
  
  <p>
    In query string
  </p>
  
  <p class="CodeList">
    ?custom_data={custom_data}
  </p>
  
  <p>
    <strong>Sample Request</strong>
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
       "ca_system": "OTT",
  </p>
  
  <p class="CodeListCxSpMiddle">
       "account_id": "167",
  </p>
  
  <p class="CodeListCxSpMiddle">
       "content_id": "file_name.ism",
  </p>
  
  <p class="CodeListCxSpMiddle">
       "files": "",
  </p>
  
  <p class="CodeListCxSpMiddle">
       “user_id” : “123456”
  </p>
  
  <p class="CodeListCxSpLast">
    }
  </p>
  
  <h3>
    2.3.5       Encrypt
  </h3>
  
  <p>
    All requests to the encrypt use the following URL scheme:
  </p>
  
  <p>
    HTTP(S)://{BASE_UDRM_LOCATION}/{ENCRYPTION_PROVIDER}/ENCRYPTION?SIGNATURE=<br /> {SIGNATURE}
  </p>
  
  <p>
    Where:
  </p>
  
  <ul>
    <li>
      BASE_UDRM_LOCATION: Constant uDRM prefix
    </li>
    <li>
      ENCRYPTION_PROVIDER: A DRM provider for encryption.
    </li>
    <li>
      SIGNATURE: Authentication signature
    </li>
  </ul>
  
  <p class="BodyBold">
    Sample Request
  </p>
  
  <p>
    https://udrm.kaltura.com/cenc/widevine/encryption?signature={signature}
  </p>
  
  <p>
    The following operations are supported on the encryption endpoint.
  </p>
  
  <p>
    (Responses are for the CENC flow. Playready Smooth Stream responses are similar – without the pssh section,)
  </p>
  
  <h2>
    2.4             Supported Policies
  </h2>
  
  <p>
    Policies are defined in the uDRM interface in advance. Upon content ingestion, the specific pre-defined policies can be attached to the ingested content by using the policy interface.
  </p>
  
  <h3>
    2.4.1       Playready
  </h3>
  
  <p>
    Kaltura supports all defined policy controls specified in the Microsoft product compliancy guidelines for the output protection settings defined in the following table.
  </p>
  
  <table border="1" cellspacing="0" cellpadding="0">
    <thead>
      <tr>
        <td valign="top" width="346">
          <p class="TableHeading">
            Field
          </p>
        </td>
        
        <td valign="top" width="346">
          <p class="TableHeading">
            Allowed Values
          </p>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td valign="top" width="346">
          <p class="TableBodyText">
            Minimum Compressed Digital Audio Output Protection Level
          </p>
        </td>
        
        <td valign="top" width="346">
          <p class="TableBodyText">
            100, 150, 200, 250, 300
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="346">
          <p class="TableBodyText">
            Minimum Uncompressed Digital Audio Output Protection Level
          </p>
        </td>
        
        <td valign="top" width="346">
          <p class="TableBodyText">
            100, 150, 200, 250, 300
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="346">
          <p class="TableBodyText">
            Minimum Compressed Digital Video Output Protection Level
          </p>
        </td>
        
        <td valign="top" width="346">
          <p class="TableBodyText">
            400, 500
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="346">
          <p class="TableBodyText">
            Minimum Uncompressed Digital Video Output Protection Level
          </p>
        </td>
        
        <td valign="top" width="346">
          <p class="TableBodyText">
            100, 250, 270, 300
          </p>
        </td>
      </tr>
      
      <tr>
        <td valign="top" width="346">
          <p class="TableBodyText">
            Minimum Analog Television Output Protection Level
          </p>
        </td>
        
        <td valign="top" width="346">
          <p class="TableBodyText">
            100, 150, 200
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <h3>
    2.4.2       Widevine
  </h3>
  
  <p>
    Kaltura uDRM supports adding Widevine policies based on the Widevine compliancy standards for the following outputs:
  </p>
  
  <ul>
    <li>
      EMI (CGMS-A)
    </li>
    <li>
      APS (Macrovision)
    </li>
    <li>
      CIT (Constrained Image Trigger)
    </li>
    <li>
      HDCP (High Bandwidth Digital Content Protection)
    </li>
  </ul>
  
  <p>
     
  </p>
  
  <h3>
    2.4.3       Apple Fairplay
  </h3>
  
  <p>
    Kaltura uDRM supports the following policies in the Fairplay CKC response, as defined in the Apple Fairplay development guidelines:
  </p>
  
  <ul>
    <li>
      Video Rental – the FPS implementation will not decrypt the response if the rental has expired
    </li>
    <li>
      Video Lease – allocating a lease period per device slot, to control simultaneous playback across multiple FPS enabled devices
    </li>
  </ul>
  
  <p>
     
  </p>
  
  <h2>
    2.5            Security and Fault Tolerance
  </h2>
  
  <h3>
    2.5.1       IP Protection
  </h3>
  
  <p>
    The encryption endpoints are only accessible by whitelisted encryption components verified by Kaltura. These include the internal Kaltura encryption modules and external modules integrating with the uDRM interface.
  </p>
  
  <h3>
    2.5.2       Key Obfuscation
  </h3>
  
  <p>
    All encryption keys are encrypted before storing them in the internal uDRM database. The encryption/decryption keys are stored separately in configuration files.
  </p>
  
  <p>
    When using the Kaltura encryption modules that perform on-the-fly encryption, in the case of compromise of encrypted content, a key rotation can be performed on-the-fly to change the content encryption keys.
  </p>
  
  <h3>
    2.5.3       MPAA Auditing
  </h3>
  
  <p>
    Kaltura is undergoing auditing by the MPAA for the <a href="http://ssae16.com/SSAE16_overview.html">SAE16</a> qualification report (<a href="http://ssae16.com/SSAE16_overview.html">http://ssae16.com/SSAE16_overview.html</a>) in all of the Kaltura data centers and facilities.
  </p>
  
  <h3>
    2.5.4       Fault Tolerance
  </h3>
  
  <p>
    The uDRM module is structured as an <em>n+m</em> structure, with DB on-the-fly scalability (using Couchbase clustering).
  </p>
  
  <p>
    Data is replicated between all Kaltura data centers using encrypted XDCR (Cross Data Center Replication) as detailed in the Couchbase XDCR data encryption documentation (<a href="http://docs.couchbase.com/admin/admin/XDCR/xdcr-dataEncryption.html">http://docs.couchbase.com/admin/admin/XDCR/xdcr-dataEncryption.html</a>).
  </p>
  
  <h2>
    2.6            Error Codes
  </h2>
  
  <h3>
    2.6.1       Format
  </h3>
  
  <p>
    In the case of an error , the following data format is returned:
  </p>
  
  <p class="NoSpace">
     
  </p>
  
  <p class="CodeListCxSpFirst">
    {
  </p>
  
  <p class="CodeListCxSpMiddle">
       ‘message’ : “Missing custom data file_id”,
  </p>
  
  <p class="CodeListCxSpMiddle">
       “status_code” : “400”,
  </p>
  
  <p class="CodeListCxSpMiddle">
       “reference” : 12345
  </p>
  
  <p class="CodeListCxSpLast">
    }
  </p>
  
  <p>
    Where :
  </p>
  
  <ul>
    <li>
      message: a string message depicting the error
    </li>
    <li>
      status_code: the status code of the error
    </li>
    <li>
      reference: an internal reference ID to track the error stack
    </li>
  </ul>
  
  <h3>
    2.6.2       Supported Response Codes
  </h3>
  
  <p>
    The following response codes can be returned by the Kaltura uDRM module:
  </p>
  
  <ul>
    <li>
      200 – successful action
    </li>
    <li>
      400 – invalid call (missing parameter)
    </li>
    <li>
      401 – unauthorized call (error in signature)
    </li>
    <li>
      404 – missing module
    </li>
    <li>
      500 – internal server error
    </li>
  </ul>
  
  <p>
    The above codes are returned as status codes in the error code response, along with the HTTP response code.
  </p>
  
  <p>
     [/collapsed]
  </p>
  
  <p>
    [collapsed title="Use Cases"]
  </p>
  
  <h1>
    3  Use Cases
  </h1>
  
  <p>
     
  </p>
  
  <h2>
    3.1            Kaltura MediaPrep
  </h2>
  
  <p>
     
  </p>
  
  <p>
    The most straight forward use case for usage of the Kaltura uDRM module is by leveraging the Kaltura end to end content preparation workflow – MediaPrep. The Kaltura MediaPrep solution is seamlessly integrated with the uDRM encryption process, generating encryption keys for both pre encrypted and on the fly encrypted files, to be used by the Kaltura pre encryption module or the <a href="https://github.com/kaltura/nginx-vod-module/tree/master/vod">Kaltura on the fly packager</a> respectively
  </p>
  
  <p>
    In addition, the <a href="http://knowledge.kaltura.com/node/1148#drm" target="_blank">Kaltura Universal Studio Player</a> is integrated with the uDRM module for license generation for all uDRM supported DRM providers.
  </p>
  
  <p>
    When using external players, license requests can be generated according to section <a href="#license">2.3.4</a>
  </p>
  
  <p>
     
  </p>
  
  <h2>
    3.2            External Encryption Modules
  </h2>
  
  <p>
     
  </p>
  
  <p>
    When using external encryption providers (pre-encryption or on the fly packagers), the integration with the Kaltura uDRM module is with the respective encryption end point (with the exact end point dependant on the DRM provider) – see section 2.3.3
  </p>
  
  <p>
    The encryption data returned by the Kaltura uDRM encryption service can then be used by the  external encryption module to encrypt the respective asset
  </p>
  
  <p>
    As in the use case above, the license generation flow is handled by the uDRM license endpoint, and is integrated within the <a href="http://knowledge.kaltura.com/node/1148#drm" target="_blank">Kaltura Universal Studio Player</a>.
  </p>
  
  <p>
    When using external players, license requests can be generated according to section<a href="#license"> ‎2.3.4</a>.
  </p>
  
  <p>
     [/collapsed]
  </p>