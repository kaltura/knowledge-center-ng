---
layout: page
title: "Kaltura REACH Release Notes"
date: 2015-08-26 00:15:59
---

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
      <tr>
        <td valign="bottom">
          <p>
            This document contains the release notes for the Kaltura REACH suite for Video Discovery, Search, and Accessibility.
          </p>
          
          <p>
            Kaltura REACH is a video discovery, search, and accessibility suite that helps organizations deliver the best video experiences for every audience group across every device. The suite supports captioning, transcription and translation services, in-video and cross-library search and discovery, deep-linking capabilities, and metadata and keyword extraction. With Kaltura REACH, organizations can access global audiences, comply with government regulations and industry standards, and capture accurate data.
          </p>
          
          <p>
            If you are unable to find the information that you are looking for here, use the search bar located above to search for the information you seek, or report missing information using the form: "<a href="http://knowledge.kaltura.com/node/86">Couldn't find what you were looking for</a>?”.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p class="mce-title mce-heading-1">
    Version 2.0 
  </p>
  
  <p>
    These release notes are applicable for the Kaltura REACH cielo24 KMS Plugin, version 2.0 released on January <span><span>2016.</span></span>
  </p>
  
  <p>
    <span><span> <br /></span></span>
  </p>
  
  <p>
    <span><span> </span></span><span style="color: #828a8c; font-size: 14pt; font-weight: bold;">What's New in This Release</span>
  </p>
  
  <ul>
    <li>
      <strong><strong>Moderation Features and Updates:</strong><br /></strong>
    </li>
    <ul>
      <li>
        The ability to change TurnAround Time (Priority) and Fidelity (Accuracy) of requested jobs within moderation step (approval process) has been added.
      </li>
      <li>
        Captioning Approval Filters:  Ability to filter caption requests. Filtering is now available for all applicable fields (by ‘Requester’, Fidelity, TAT, Lang, Status, date range)
      </li>
      <li>
        Display aggregate minutes per service type at to the top of the Moderation plugin: summary of the minuted processed categorized by Fidelity is shown on the top the table displaying the captioning requests.
      </li>
      <li>
        The ability to control Moderation (‘Require Customer Authorization') via Admin setting has been added.
      </li>
    </ul>
    
    <li>
      <strong>Updated functionality for Caption Ordering, View, and Edit:</strong>
    </li>
    <ul>
      <li>
        The ability to allow 'role' configurable permission options to 'view' previous caption requests was added
      </li>
      <li>
        The capability to display all caption requests in KMS for editing purposes including made jobs requested via the KMC was added
      </li>
      <li>
        The capability to provide a customer specific 'Caption Ordering instructions' for the 'Caption Ordering' form was added
      </li>
    </ul>
    
    <li>
      <strong>Machine Enhancments:</strong>
    </li>
    <ul>
      <li>
        The ability to order captions in 6 languages for Machine transcription in 'Caption Ordering' form was added
      </li>
      <li>
        The ability to disable/enable Moderation for Machine transcription in the admin module (override account level moderation for Machine) was added<ul>
          <li>
            Note: With Moderation disabled and the updated integration all new videos in the account can be automatically Machine transcribed without having to request on a per-video basis
          </li>
        </ul>
      </li>
    </ul>
    
    <li>
      <strong>Speaker ID:</strong>
    </li>
    <ul>
      <li>
        The ability to control which roles can request speaker name when in 'Caption Ordering' was added
      </li>
      <li>
        The ability to request speaker name identification when ordering captions using ‘Add Speaker Names’ checkbox was added
      </li>
    </ul>
    
    <li>
      <strong>Enhanced Captions and Media Intelligence:</strong>
    </li>
    <ul>
      <li>
        The ability to disable/enable displaying Keywords and Topics extracted from the video as tags was added
      </li>
      <li>
        The default caption file format form was updated SRT to DFXP
      </li>
      <li>
        The ability to provide global notes (including glossary of terms) to be used during transcription of videos was added
      </li>
      <li>
        The ability to add a co-editor to edit captions for a video using the 'allowEdit' field was added
      </li>
    </ul>
  </ul>
  
  <div>
     
  </div>
  
  <p class="mce-heading-3">
    Resolved Issues
  </p>
  
  <table border="0">
    <thead>
      <tr>
        <td>
          <strong>ID#</strong>
        </td>
        
        <td>
          <strong>Summary</strong>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td>
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          Mechanical selections now only display options available for use with a Mechanical fidelity job
        </td>
      </tr>
      
      <tr>
        <td>
           
        </td>
        
        <td style="text-align: left;">
          The 'Admin' configuration was <span>rearranged</span> to better group like options for module
        </td>
      </tr>
      
      <tr>
        <td>
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          Foreign language copy updates were made
        </td>
      </tr>
      
      <tr>
        <td>
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          The issue causing incorrect 'complete' date for processed caption requests has been resolved
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
     
  </p>
  
  <p class="mce-heading-3">
    Limitations & Known Issues<span><br /></span>
  </p>
  
  <p class="mce-title mce-heading-1">
    Version 1.0
  </p>
  
  <p>
    These release notes are applicable for the Kaltura REACH cielo24 KMS Plugin, version 1.0 released on September <span style="color: #ff0000;"><span style="color: #000000;">07, 2015.</span></span>
  </p>
  
  <p>
    <span style="color: #ff0000;"><span style="color: #000000;"> <br /></span></span>
  </p>
  
  <p>
    <span style="color: #ff0000;"><span style="color: #000000;"> </span></span>
  </p>
  
  <p class="mce-heading-3">
    What's New in This Release
  </p>
  
  <ul>
    <li>
      <strong>Auto Provisioning -</strong> Functionality has been added to auto provision new accounts.
    </li>
    <ul>
      <li>
        A CLICK HERE option has been added so that new users are able to link to unregistered accounts.
      </li>
      <li>
        A pop-up form for customer sign-up with instructions to upload a sample video is now available.
      </li>
      <li>
        The registration form automatically creates a cielo24 account linked to a Kaltura account.
      </li>
      <li>
        The plugin is "active" after the form is submitted using the default configuration settings.
      </li>
    </ul>
    
    <li>
      <strong>KAF support: </strong>
    </li>
    <ul>
      <li>
        The Moderation menu for Pending Caption Requests has been moved to "My Media".
      </li>
    </ul>
    
    <li>
      <strong>Customer Edit Tool and Permissions Updates</strong>:
    </li>
    <ul>
      <li>
        Support has been added for configuring role-based permissions for caption editing.
      </li>
      <li>
        The Edit Captions option has been added in the  'Action' tab  for permitted users:
      </li>
      <ul>
        <li>
          Selecting Edit Captions directly launches the customer Edit Tool.
        </li>
        <li>
          Completed stage caption requests are hyperlinked to launch the customer Edit Tool. <span style="color: #ff0000;"><br /></span>
        </li>
      </ul>
      
      <li>
        The View Captions options has been added in 'Action' tab:
      </li>
      <ul>
        <li>
          Selecting View Caption Request displays the pending, processing, and completed caption requests.
        </li>
      </ul>
    </ul>
    
    <li>
      <strong>Default Configuration Selection Updates for New Users:</strong>
    </li>
    <ul>
      <li>
        Fidelity choices have been updated: the "self-caption in Amara" option has been removed.
      </li>
      <li>
        Default values for Fidelity have been set to uncheck Premium as the default.
      </li>
      <li>
        Default values for Turnaround times have been set to default available in REACH packages.
      </li>
      <li>
        Mechanical Fidelity now sets the turnaround time automatically, and removes the display for the user.
      </li>
    </ul>
  </ul>
  
  <p class="mce-heading-3">
    Resolved Issues
  </p>
  
  <table border="0">
    <thead>
      <tr>
        <td>
          <strong>ID#</strong>
        </td>
        
        <td>
          <strong>Summary</strong>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;">
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            The logo no longer needs to be enabled to edit captions and add edit permissions.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SUP-4597
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            An erroneous error is no longer displayed when waiting for KMS moderation approval following successful approval.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            The caption's label is set automatically; there is no need to set the caption label from the API.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            Columns now display correctly when only Fidelity and Turnaround time are exposed.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            Language codes for Hebrew, Japanese, Korean now render properly.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            The "owner only" role privilege setting for caption ordering is now working properly.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p class="mce-heading-3">
    Limitations & Known Issues<span style="color: #ff0000;"><br /></span>
  </p>
  
  <table border="0">
    <thead>
      <tr>
        <td>
          <strong>ID#</strong>
        </td>
        
        <td>
          <strong>Summary</strong>
        </td>
      </tr>
    </thead>
    
    <tbody>
      <tr>
        <td style="text-align: left;">
          <p>
             
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            This issue has been fixed, and will appear in te next update: Use moduleHeadLink/moduleHeadScript() instead of headLink/headScript()
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            SUP-5364 
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            This issue has been fixed, and will appear in the next update: Convert cielo24 API PST times to Kaltura server time, and display the timezone
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;">
          <p>
            KMS-8724
          </p>
        </td>
        
        <td style="text-align: left;">
          <p>
            This issue has been fixed, and will appear in the next update: Blank 'ok' box that appears after approving moderation.
          </p>
        </td>
      </tr>
    </tbody>
  </table>