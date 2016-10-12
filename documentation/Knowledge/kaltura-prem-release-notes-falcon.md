---
layout: page
title: "Kaltura On-Prem Release Notes Falcon"
date: 2012-11-12 15:02:45
---

<span><span>Falcon Version: 6.0.1 </span><span>build 148</span></span>

<span>These release notes are intended for content managers and Kaltura Admin Console users and also contain the latest information for developers, integrators, and operations and site administrators using the Kaltura platform. </span>

#### Known Issues

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="bottom" width="118">
        <p class="TableHeading">
          <strong>Defect ID</strong>
        </p>
      </td>
      
      <td valign="bottom" width="119">
        <p class="TableHeading">
          <strong>Component</strong>
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p class="TableHeading">
          <strong>Summary</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="118">
        <p>
          4985
        </p>
      </td>
      
      <td valign="top" width="119">
        <p>
           Core
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p>
          Default categories are not created for new partners. Entries that are created use the templates from the previous version. 
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="118">
        <p>
          5033
        </p>
      </td>
      
      <td valign="top" width="119">
        <p>
          Licensing / Admin Console
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p>
          When trying to access the Kaltura Admin Console before supplying an activation key, an application error is displayed.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="118">
        <p>
          5403
        </p>
      </td>
      
      <td valign="top" width="119">
        <p>
           KMC
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p>
          When a Name for a live stream entry is 4 characters or less, the live-stream-entry is rejected.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="118">
        <p>
          5416
        </p>
      </td>
      
      <td valign="top" width="119">
        <p>
           KMS4/3
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p>
          When using On-Prem with Red5, Krecord v1.5.2 does not save the record. Krecord v1.5.12 is required to work with Red5.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="118">
        <p>
          5427
        </p>
      </td>
      
      <td valign="top" width="119">
        <p>
          KMS 4 or previous
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p>
          Auto generation of flavor params by KMS for doc-conversion use, creates an incorrect flavor type.  
        </p>
        
        <p>
          Work around: Change the type of the flavor type in the database to be of type swfFalvorParam.
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="118">
        <p>
          5450
        </p>
      </td>
      
      <td valign="top" width="119">
        <p>
           Analytics
        </p>
      </td>
      
      <td valign="bottom" width="525">
        <p>
          Playlists are calculated in Publisher Bandwidth & Storage Report.
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### Limitations

The Multi-account Management Console is included in the On-Prem package was not fully tested. For more information see [Kaltura's Multi-Account Management Console User Manual][1].

 [1]: http://knowledge.kaltura.com/node/572/attachment/field_media

The UI Confs tab in the Kaltura Admin Console was not fully tested.

#### Third Party Software Components

<table style="width: 633px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          Component
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableHeading">
          Version
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          Operating system
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          CentOS 6.3
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          Web server
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          Apache 2.2.15
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          PHP
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          PHP 5.3.3
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          Database
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          MySQL 5.1.61
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          Java
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          JRE 1.6.0_24
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          BI Suite
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          Pentaho 4.2.1
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          Transcoding engine
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          ffmpeg 0.10
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          Search server
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          Sphinx 2.0.4
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="198">
        <p class="TableBodyText">
          Media server
        </p>
      </td>
      
      <td valign="top" width="435">
        <p class="TableBodyText">
          Red5 1.0.0
        </p>
      </td>
    </tr>
  </tbody>
</table>