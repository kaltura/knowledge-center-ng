---
layout: page
title: "How to Create Custom Roles in the Kaltura Management Console"
date: 2012-10-22 13:44:57
---

### Creating Custom Roles

When you add a KMC admin user role to a specific publisher account, you should add the relevant set of permissions in the **Add Role** window. You can select which KMC functionalities are available to users with the defined role. Clicking the checkmark next to each permission group name will toggle the permission level for the specific KMC functionality to the following modes:

*   **Full Permission ****(checked)** – Grants access to all KMC functionalities listed under the permission group.
*   **View-Only Permission**** (partially checked)** –Only part of the functionality listed in the group is selected.
*   **No Permission ****(unchecked)** – No access to the KMC pages that are relevant to the KMC functionalities listed under the permission group.

<p class="mce-procedure">
  To create custom roles
</p>

1.  Go to the Administration tab and select the Roles tab.
2.  Click Add Role to create a custom role.
3.  Enter the Role Name and provide a description.  
    <img src="../../assets/756.img">
    After naming the role and providing a description you will be able to select the specific permissions required.
4.  Most of the permissions are organized under KMC high-level functionalities. For granular permissions within each category click Expand All. Or click Advanced to open a more detailed list of the specific KMC functionalities related to the group.
5.  Click Save.

You can edit, duplicate or delete any existing role via the using the Select action drop-down menu.

### Role Management

After you create roles you can:

*   Edit a role
*   Duplicate a role.
*   Delete a role.

<p class="mce-procedure">
  To modify roles
</p>

1.  Go to the Administration tab and select the Roles tab.
2.  Click on a role.
3.  Select an option from the Actions menu.

*   **Edit a role**

<p style="padding-left: 30px;">
  Editing a user role affects the access level of the KMC user associated with this role only after the user logs in to the KMC. We recommend that you edit an “in-use” role when users associated with this role are not logged into the KMC.
</p>

*   **Duplicate a role**

<p style="padding-left: 30px;">
  Duplicating a role is a quick way to create a new KMC user role with a similar, but not identical, set of permissions as an existing user role. The duplicated role is populated with the permission set of the duplication source role, so minor changes to this permission set can be easily made. After you duplicate a role, use the Edit option to modify the permissions.
</p>

*   **Delete Role**

<p style="padding-left: 30px;">
  Deleting a role is a permanent action. It is not possible to delete a user role record as long as KMC admin users are associated with the role. In such cases, make sure to update the relevant KMC user accounts with another user role before attempting to delete their existing role. 
</p>