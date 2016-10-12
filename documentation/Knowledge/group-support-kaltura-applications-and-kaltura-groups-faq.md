---
layout: page
title: "Group Support in Kaltura Applications and Kaltura Groups FAQ"
date: 2016-03-03 17:00:51
---

<h2>
    Kaltura Applications - Support for Groups
  </h2>
  
  <p>
    Kaltura has created an new entity called<em> <strong>group </strong></em>that can be used<em> to manag</em>e entitlements and category assignments for a large number of users in Kaltura applications.
  </p>
  
  <h3>
    What is a Group?<span style="text-decoration: underline;"><em><br /></em></span>
  </h3>
  
  <p>
    A<em> group </em>is a single manageable entity that represents a collection of users. Technically, a group is a unique type of user that can have individual users as part of it.
  </p>
  
  <p>
    Groups can be assigned to a category/channel just like users can.
  </p>
  
  <p>
    Once a group is assigned to a category, all the individual users in the group inherit the permission of the group in the category. For example, if the group is assigned as contributor,  then all users will be contributors as well.
  </p>
  
  <h3>
    Why Use Groups?
  </h3>
  
  <ol>
    <li>
      You most probably already manage groups in the Identity Provider (SAML/SSO/LDAP/AD) and may want to use the same virtual groups in Kaltura applications (MediaSpace for example)<em>.</em>
    </li>
    <li>
      In case you have (or expect to have) more than 5000 individual users assigned to a category (technical limitation).
    </li>
  </ol>
  
  <h3>
    How to Create and Assign Groups
  </h3>
  
  <p>
    You can create groups and add users to them by either:
  </p>
  
  <ol>
    <ol>
      <li>
        Running an external periodic <strong>script</strong> on customer servers in sync with their IdP. This method will create new groups and add/remove users from groups. This script uses Kaltura APIs (groupUser) and can be written by the customer or delivered by Kaltura Professional Services. Kaltura already has a general AD script in place for use and can create additional module for other methods.
      </li>
      <li>
        Using a custom KMS <strong>module</strong> – This method is based on the user's metadata with a specific custom data schema per customer that adds users to groups dynamically according to SAML response on login. This method should be delivered by Kaltura Professional Services. Kaltura has a general SAML module in place for use and can create additional module for other methods.
      </li>
    </ol>
  </ol>
  
  <p>
    Support exists in KMS and KMC for assigning groups to channels/categories. 
  </p>
  
  <h3>
    What Happens when a New User or Group is Created on the IdP?
  </h3>
  
  <p>
    If the implementation is done by the periodic script, then when the script is run next, the new group or user is added (or updated).
  </p>
  
  <p>
    If the implementation is done by the module, when new users log into KMS for the first time, they will dynamically be added to the assigned groups, or, the groups will be created if they do not exist. Changing is users's groups are will also be updated.
  </p>
  
  <h3>
    Additional Information
  </h3>
  
  <ul>
    <li>
      An individual user can be both directly assigned to a category/channel and via a group.
    </li>
    <li>
      If an individual user is directly assigned to a category/channel and via a group, the permission of the direct assignment will overrule the group inheritance (even if it is lower permission).
    </li>
    <li>
      In case the user is a member of 2 groups and the 2 groups are assigned to a category, the higher permission of the user will be counted in this category.
    </li>
    <li>
      A user can’t be part of more than 100 groups.
    </li>
    <li>
      No more than 5000 groups can be assigned to a category.
    </li>
    <li>
      There is no limit to the number of users inside a group.
    </li>
    <li>
      In KMS – members of a channel will not include the users in the group breakdown, but only direct users and groups.
    </li>
    <li>
      Analytics are displayed for an individual user (and not the group).
    </li>
    <li>
      There is currently no interface in Kaltura applications to create groups and to add users to the group.
    </li>
    <li>
      The use of a KMS module to assign users to groups during login is limited up to 100 groups and up to 3 groups per user (due to performance consideration).
    </li>
    <li>
      Group support may be enabled for ‘Media Collaboration’ features. When enabled, you can select groups that may be assigned as co-editors/publishers for an entry.
    </li>
  </ul>