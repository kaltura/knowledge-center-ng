---
layout: page
title: "Kaltura Video App for Canvas - Common Use Cases of Role Configuration"
date: 2014-02-04 09:42:06
---

 

<table style="width: 897px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td rowspan="2" valign="top" width="97">
        <p class="TableHeading">
          Canvas Role
        </p>
      </td>
      
      <td rowspan="2" valign="top" width="200">
        <p class="TableHeading">
          Use case
        </p>
      </td>
      
      <td colspan="3" valign="top" width="600">
        <p class="TableHeading">
          Kaltura
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td valign="top" width="200">
        <p class="TableBodyText">
          ItiRole
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          kmsRole
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          kmsContextualRole
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="97">
        <p class="TableBodyText">
          Student
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Allow authoring new content (upload, webcam recording, screencast recording)  and allow publishing to course Media Galleries
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Learner
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          privateOnlyRole
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          CONTRIBUTOR
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="97">
        <p class="TableBodyText">
          Student
        </p>
      </td>
      
      <td valign="top" width="200">
        <p>
          Allow viewing content only. Do not allow authoring new content or publishing to course Media Galleries.
        </p>
        
        <p class="TableBodyText">
          It is recommended to hide the My Media navigation link on the course menu, so that students will not receive an “Access Denied” screen when trying to access My Media.
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Learner
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          viewerRole
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          MEMBER
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="97">
        <p class="TableBodyText">
          TA (Teaching Assistant)
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Allow to author new content, to contribute to course Media Galleries and to moderate course media galleries.
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          TeachingAssistant
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          privateOnlyRole
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          MODERATOR
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="97">
        <p class="TableBodyText">
          Teacher
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Allow authoring new content, contributing to course Media Galleries and moderating course Media Galleries.
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Instructor
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          privateOnlyRole
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          MANAGER
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="97">
        <p class="TableBodyText">
          Designer
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Allow authoring new content, contributing to course Media Galleries and moderating course Media Galleries.
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          ContentDeveloper
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          privateOnlyRole
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          MANAGER
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="97">
        <p class="TableBodyText">
          Observer
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Only allow viewing.
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          Observer
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          viewOnly
        </p>
      </td>
      
      <td valign="top" width="200">
        <p class="TableBodyText">
          MEMBER
        </p>
      </td>
    </tr>
  </tbody>
</table>

<h2 class="mce-heading-3">
  Summary of Default Canvas -> LIS -> Kaltura Roles Mapping
</h2>

<table style="width: 862px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td width="160">
        <p class="TableHeading">
          Canvas role
        </p>
      </td>
      
      <td width="207">
        <p class="TableHeading">
          LIS role
        </p>
      </td>
      
      <td width="207">
        <p class="TableHeading">
          Kaltura applicative role (kmsRole)
        </p>
      </td>
      
      <td width="288">
        <p class="TableHeading">
          Kaltura contextual role (kmsContextualRole)
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td width="160">
        <p class="TableBodyText">
          Student
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          ‘Learner’
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          privateOnlyRole
        </p>
      </td>
      
      <td width="288">
        <p class="TableBodyText">
          CONTRIBUTOR
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="160">
        <p class="TableBodyText">
          Teacher
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          ‘Instructor’
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          privateOnlyRole
        </p>
      </td>
      
      <td width="288">
        <p class="TableBodyText">
          MANAGER
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="160">
        <p class="TableBodyText">
          TA
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          ‘TeachingAssistant’
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          privateOnlyRole
        </p>
      </td>
      
      <td width="288">
        <p class="TableBodyText">
          MODERATOR
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="160">
        <p class="TableBodyText">
          Designer
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          ‘ContentDeveloper’
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          privateOnlyRole
        </p>
      </td>
      
      <td width="288">
        <p class="TableBodyText">
          MANAGER
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="160">
        <p class="TableBodyText">
          Observer
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          ‘Observer’
        </p>
      </td>
      
      <td width="207">
        <p class="TableBodyText">
          viewerRole
        </p>
      </td>
      
      <td width="288">
        <p class="TableBodyText">
          MEMBER
        </p>
      </td>
    </tr>
  </tbody>
</table>

 