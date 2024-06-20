# Management System

User decentralization management system, api access token to the system

## Basic authentication

Manage tokens used on the system.

### Basic authentication list

![List of token](/images/media-live/um-basic-auth/list.png)

Each token value will consist of the following basic information:

- Name.
- Right.

  To better understand permissions, visit the Permissions section.

---

**\* NOTE**

A token will be assigned one or more permissions.

---

### Create a token

1. Click on the ! [Add button] (/images/media-live/um-member/btn-add.png).

2. Enter the token information in the form.

   ![Add Form](/images/media-live/um-basic-auth/form-add.png)

   When assigning permissions to tokens, you can select the permissions available in the list of groups. At that time, the token will inherit all rights belonging to the selected group. Inherited permissions can be modified (added/deleted) accordingly.

   Click the ! [Add perm button] (/images/media-live/um-basic-auth/btn-add-perm.png) to display an additional list of permissions.

   ![Add Form](/images/media-live/um-basic-auth/form-add-2.png)

3. Save the token by clicking the ! [Submit button] (/images/media-live/um-member/btn-submit.png).

Token creation execution system:

- If successfully displayed the newly created token information:
  ! [Token info] (/images/media-live/um-basic-auth/info.png)

  Click on the icons ! [Icon copy password] (/images/media-live/um-member/icon-copy.png) copy the Token ID and Token Secret. The Secret Token value will be deleted shortly thereafter

- If it fails, an error message will be displayed.

### Edit tokens

Click on the ! [Edit button] (/images/media-live/um-action-btns/edit.png) to change the name and permissions of the token.

![Edit token](/images/media-live/um-basic-auth/form-edit.png)

## Group

Manage user groups

### Group list

![List of group](/images/media-live/um-group/list.png)

Each group will consist of two basic information:

- Name (column **Name** in the table above).
- List of permissions (**Permissions** column in the table above).

  To better understand permissions, visit the Permissions section.

---

**\* NOTE**

A group will include one or several permissions. Accounts in a group that inherit all permissions belong to that group

---

### Create a group

1. Click on the ! [Add button] (/images/media-live/um-member/btn-add.png).
2. Enter your account information in the form.

   ![Add Form](/images/media-live/um-group/form-add.png)

   The information to enter includes:

   - Name.
   - Password.
   - Powers.
3. Save the group by clicking the ! [Submit button] (/images/media-live/um-member/btn-submit.png).

The execution system creates a new group:

- If successful, display a success message.
- If the failure displays an error

### Edit account permissions

Click on the ! [Edit button] (/images/media-live/um-action-btns/edit.png) to edit the group's name and permission information.

## Member

Manage the list of user accounts on the system.

### Account list

![List of member](/images/media-live/um-member/list.png)

Each account will include a few basic information:

- Username (**User** column in the table above).
- The group/permissions to which the account is assigned (column **Group** in the table above).

Move your mouse to the group to display permission details.

![Permissions of group](/images/media-live/um-member/permission.png)

To better understand permissions, visit the Permissions section.

---

**\* NOTE**

An account will be a member of one and only one group.

---

### Create an account

1. Click on the ! [Add button] (/images/media-live/um-member/btn-add.png).
2. Enter your account information in the form.

   ![Add Form](/images/media-live/um-member/form-add.png)

   The information to enter includes:

   - Username.
   - Password.
   - The team will empower.

     The selected group will display a blue tick! [Selected group] (/images/media-live/um-member/group-selected.png)
3. Save the account by clicking the ! [Submit button] (/images/media-live/um-member/btn-submit.png).

The execution system creates a new account:

- If successfully displays the newly created account information including username and password:
  ! [Account info] (/images/media-live/um-member/account-info.png)

  Click on the icons ! [Icon show password] (/images/media-live/um-member/icon-eye.png), ! [Icon copy password] (/images/media-live/um-member/icon-copy.png) to display and copy the password.

- If it fails, an error message will be displayed.

### Edit account permissions

Click on the ! [Edit button] (/images/media-live/um-action-btns/edit.png) to change account permissions by assigning the account to another group.

! [Edit account] (/images/media-live/um-member/form-edit.png)

## Permission

An account is created and granted certain permissions and may only perform operations corresponding to the allowed permissions.

### Decentralization rules

The system will be divided into many different permissions, each of which will include two basic information:

- Identifier: refers to the object or entity that the right will influence.

  For example, the 'Sigma Livestream' permission denotes the object it affects as the 'Livestream'.
- Actions: represent actions that are allowed to be executed on an entity assigned with permissions. It is about answering the question _What can a user do with entity A?_

  The system defines two actions for working with permissions:

  - READ: Users can only view entity information.
  - FULL: users can view and edit entity information.

    When setting permissions, only one of these two actions can be selected.

Example interface showing a permission on the system

! [Permission] (/images/media-live/um-permission/general.png)
