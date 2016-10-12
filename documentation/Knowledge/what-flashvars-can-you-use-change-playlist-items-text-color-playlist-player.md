---
layout: page
title: "What flashvars can you use to change the playlist items text color in a playlist player"
date: 2013-02-06 15:11:13
---

In general, two flashvars are required:

*   [labelId].dynamicColor=true
*   [labelId].color1=[your color]

[labelId] should be replaced with the id of the label you would like to change.

For example (relevant for the “new” templates, not “basic”):

If you would like to change the name text color to red , add:

*   nameLabel.dynamicColor=true
*   nameLabel.color1=0xFF0000
*   hoverNameLabel.dynamicColor=true
*   hoverNameLabel.color1=0xFF0000

*Notice: In this example both nameLabel and hoverNameLabel were changed. In the new templates, each item is represented by two labels, one is used in regular state, and the other is used on mouse over.

In the “basic” player, only one item needs to be  changed. In this example it would be " irLinkIrScreen" label.

There’s a difference between the IDs of labels in the ”new” templates and in the “basic” templates.

Here is a complete list of playlist item renderer labels and their matching IDs:

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>Playlist Item</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          <strong>ID in “new” template:</strong>
        </p>
        
        <p>
          <strong>regular / hover</strong>
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          <strong>ID in “basic” template</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>Name</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          nameLabel / hoverNameLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irLinkIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>Description</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          descriptionLabel / hoverDescriptionLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irDescriptionIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>Duration</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          durationLabel / hoverDurationLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irDurationIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>plays</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          playsLabel / hoverPlaysLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irPlaysIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>rank</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          rankLabel / hoverRankLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irRankIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>votes</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          votesLabel / hoverVotesLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irVotesIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>tags</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          tagsLabel / hoverTagsLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irTagsIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>categories</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          adminTagsLabel / hoverAdminTagsLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irAdminTagsIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>Created At</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          createdAtLabel / hoverCreatedAtLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irCreatedAtIrScreen
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="213">
        <p>
          <strong>Created By</strong>
        </p>
      </td>
      
      <td valign="top" width="283">
        <p>
          createdByLabel/ hoverCreatedByLabel
        </p>
      </td>
      
      <td valign="top" width="142">
        <p>
          irCreatedByIrScreen
        </p>
      </td>
    </tr>
  </tbody>
</table>

 