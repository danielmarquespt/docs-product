# Users API

For version 10.0.907.100. Backoffice to manage users, groups and roles.

## Summary

| Widget | Description |
| :--- | :--- |
| [ChangePassword](users-api.md#ChangePassword%3E) | Allows changing the user password. |
| [EditMyInfo](users-api.md#EditMyInfo%3E) |  |

| Action | Description |
| :--- | :--- |
| [EncryptPassword](users-api.md#EncryptPassword%3E) | Returns the encrypted password for a specific username and password. This is the value kept in the Password attribute of the User system entity. |
| [GetEffectiveUserProviderEspaceId](users-api.md#GetEffectiveUserProviderEspaceId%3E) | Returns the eSpace identifier of the effective user provider. Normally it returns the Users eSpaceId, in upgrade scenarios it returns the EnterpriseManager eSpaceId. |
| [Group\_CreateNew](users-api.md#Group_CreateNew%3E) | Create a new system group. Requires the UserManager role to be invoked. |
| [Group\_Delete](users-api.md#Group_Delete%3E) | Delete a system group. Requires the UserManager role to be invoked. |
| [Group\_Update](users-api.md#Group_Update%3E) | Updates a system group. Requires the UserManager role to be invoked. |
| [IPAddress\_GetBlockedStatus](users-api.md#IPAddress_GetBlockedStatus%3E) | Returns the blocking state of the IP address. |
| [IPAddress\_GetBlocks](users-api.md#IPAddress_GetBlocks%3E) | Returns the blocking state of the IP address. If there are no blocks for this address, the list will be empty. If no IP address is given, information on all blocked IP addresses will be returned. |
| [IPAddress\_Unblock](users-api.md#IPAddress_Unblock%3E) | Ends the blocking period for the specified IP address, allowing any user to login in that address. |
| [UseActiveDirectoryAuthentication](users-api.md#UseActiveDirectoryAuthentication%3E) | Returns the Users configuration that determines if the Active Directory is used for authentication |
| [UseIntegratedAuthentication](users-api.md#UseIntegratedAuthentication%3E) | Returns the Users configuration that determines if the Integrated Authentication is used to login. |
| [UseLDAPAuthentication](users-api.md#UseLDAPAuthentication%3E) | Returns the Users configuration that determines if the Active Directory is used for authentication |
| [User\_CanChangePassword](users-api.md#User_CanChangePassword%3E) | Checks if the User is allowed to change a password. It is false for Active Directory users. |
| [User\_Create](users-api.md#User_Create%3E) | Create a new user. Requires UserManager role to be invoked.%%Fails when the username is repeated. |
| [User\_CreateOrUpdate](users-api.md#User_CreateOrUpdate%3E) | Create or updates a user. Requires UserManager role to be invoked. |
| [User\_DeleteIfNoRoles](users-api.md#User_DeleteIfNoRoles%3E) | Deletes the User if there are no roles assigned to it. |
| [User\_GetBlockedStatus](users-api.md#User_GetBlockedStatus%3E) | Returns information regarding the blocking state of the user and the blocking reason, in the specified IP address. If no IP address is given, checks the last IP address from where the user attempted to login. |
| [User\_GetIdByUsername](users-api.md#User_GetIdByUsername%3E) | Returns the user identifier for a specific user given the username |
| [User\_GetLastFailedLoginAttempts](users-api.md#User_GetLastFailedLoginAttempts%3E) | Returns a list of last failed login attempts \(one record for each IP address\). This information can be used to invoke User\_Unblock or IPaddress\_Unblock. |
| [User\_GetName](users-api.md#User_GetName%3E) | Returns the name of the logged user. |
| [User\_GetUnifiedLoginUrl](users-api.md#User_GetUnifiedLoginUrl%3E) | Returns the Url used for custom unified login patterns. Includes Windows Integrated Authentication pattern. |
| [User\_IsExternalUser](users-api.md#User_IsExternalUser%3E) |  |
| [User\_Login](users-api.md#User_Login%3E) | Action to login using username and password as credentials. |
| [User\_Logout](users-api.md#User_Logout%3E) | Logs out the current user. Session variables are cleared during the logout process. |
| [User\_Unblock](users-api.md#User_Unblock%3E) | Ends the blocking period for the specified user, allowing the user to login in all IP addresses where the user was blocked. |
| [User\_Update](users-api.md#User_Update%3E) | Updates a specific user. |

| Structure | Description |
| :--- | :--- |
| [LoginAttemptPublic](users-api.md#Structure_LoginAttemptPublic%3E) | Represents the Login attempt record structure that is exposed |

| Static Entity | Description |
| :--- | :--- |
| [LoginAttemptResult](users-api.md#StaticEntity_LoginAttemptResult%3E) | The alternative values that may appear in the LoginAttempt record Result column. |
| [MenuItem](users-api.md#StaticEntity_MenuItem%3E) | Menu item to be used in menu web block parameters. |

| Role | Description |
| :--- | :--- |
| UserManager |  |

## Widgets

### ChangePassword { \#ChangePassword }

Allows changing the user password.

_Inputs_

UserId : Type: optional, User Identifier.

### EditMyInfo { \#EditMyInfo }

## Actions

### EncryptPassword { \#EncryptPassword }

Returns the encrypted password for a specific username and password. This is the value kept in the Password attribute of the User system entity.

_Inputs_

Username : Type: mandatory, Text.

Password : Type: mandatory, Text.

_Outputs_

EncryptedPassword : Type: Text.

### GetEffectiveUserProviderEspaceId { \#GetEffectiveUserProviderEspaceId }

Returns the eSpace identifier of the effective user provider. Normally it returns the Users eSpaceId, in upgrade scenarios it returns the EnterpriseManager eSpaceId.

_Outputs_

EspaceId : Type: Espace Identifier.

### Group\_CreateNew { \#Group\_CreateNew }

Create a new system group. Requires the UserManager role to be invoked.

_Inputs_

Group : Type: mandatory, Group.

_Outputs_

GroupId : Type: Group Identifier.

### Group\_Delete { \#Group\_Delete }

Delete a system group. Requires the UserManager role to be invoked.

_Inputs_

GroupId : Type: mandatory, Group Identifier.

### Group\_Update { \#Group\_Update }

Updates a system group. Requires the UserManager role to be invoked.

_Inputs_

Group : Type: mandatory, Group.

### IPAddress\_GetBlockedStatus { \#IPAddress\_GetBlockedStatus }

Returns the blocking state of the IP address.

_Inputs_

IPAddress : Type: mandatory, Text.  
IP address for which the blocking state should be evaluated.

_Outputs_

LoginAttemptResult : Type: [LoginAttemptResult](users-api.md#Structure_LoginAttemptResult%3E).  
Blocking state for the given IP address.

### IPAddress\_GetBlocks { \#IPAddress\_GetBlocks }

Returns the blocking state of the IP address. If there are no blocks for this address, the list will be empty. If no IP address is given, information on all blocked IP addresses will be returned.

_Inputs_

IPAddress : Type: optional, Text.  
IP Address for which the current block information should be given.

_Outputs_

BlockedAddresses : Type: [LoginAttemptPublic](users-api.md#Structure_LoginAttemptPublic%3E) List.  
Blocked login attempts associated to the given IP address, or all IP addresses, if no input is given.

### IPAddress\_Unblock { \#IPAddress\_Unblock }

Ends the blocking period for the specified IP address, allowing any user to login in that address.

_Inputs_

IPAddress : Type: mandatory, Text.  
The IP address to be unblocked.

### UseActiveDirectoryAuthentication { \#UseActiveDirectoryAuthentication }

Returns the Users configuration that determines if the Active Directory is used for authentication

_Outputs_

IsActive : Type: Boolean.

### UseIntegratedAuthentication { \#UseIntegratedAuthentication }

Returns the Users configuration that determines if the Integrated Authentication is used to login.

_Outputs_

IsActive : Type: Boolean.

### UseLDAPAuthentication { \#UseLDAPAuthentication }

Returns the Users configuration that determines if the Active Directory is used for authentication

_Outputs_

IsActive : Type: Boolean.

### User\_CanChangePassword { \#User\_CanChangePassword }

Checks if the User is allowed to change a password. It is false for Active Directory users.

_Inputs_

UserId : Type: mandatory, User Identifier.

_Outputs_

IsAllowed : Type: Boolean.

### User\_Create { \#User\_Create }

Create a new user. Requires UserManager role to be invoked.  
Fails when the username is repeated.

_Inputs_

User : Type: mandatory, User.

_Outputs_

UserId : Type: User Identifier.

### User\_CreateOrUpdate { \#User\_CreateOrUpdate }

Create or updates a user. Requires UserManager role to be invoked.

_Inputs_

User : Type: mandatory, User.

_Outputs_

UserId : Type: User Identifier.

### User\_DeleteIfNoRoles { \#User\_DeleteIfNoRoles }

Deletes the User if there are no roles assigned to it.

_Inputs_

UserId : Type: mandatory, User Identifier.

### User\_GetBlockedStatus { \#User\_GetBlockedStatus }

Returns information regarding the blocking state of the user and the blocking reason, in the specified IP address. If no IP address is given, checks the last IP address from where the user attempted to login.

_Inputs_

Username : Type: mandatory, Text.  
The username of the user whose information regarding the blocked/unblocked state will be retrieved.

IPAddress : Type: optional, Text.  
The IP address for which the information regarding the blocked/unblocked user state will be retrieved.

_Outputs_

LoginAttemptResult : Type: [LoginAttemptResult](users-api.md#Structure_LoginAttemptResult%3E).  
Blocking state and reason for the given username.

### User\_GetIdByUsername { \#User\_GetIdByUsername }

Returns the user identifier for a specific user given the username

_Inputs_

Username : Type: mandatory, Text.

_Outputs_

UserId : Type: User Identifier.

### User\_GetLastFailedLoginAttempts { \#User\_GetLastFailedLoginAttempts }

Returns a list of last failed login attempts \(one record for each IP address\). This information can be used to invoke User\_Unblock or IPaddress\_Unblock.

_Inputs_

Username : Type: mandatory, Text.  
The username of the user whose failed login attempts are retrieved.

Since : Type: optional, Date Time.  
Only the login attempts after this datetime are retrieved.

_Outputs_

LoginAttempt : Type: [LoginAttemptPublic](users-api.md#Structure_LoginAttemptPublic%3E) List.  
List of last failed login attempts for the given username.

### User\_GetName { \#User\_GetName }

Returns the name of the logged user.

_Outputs_

Name : Type: Text.

### User\_GetUnifiedLoginUrl { \#User\_GetUnifiedLoginUrl }

Returns the Url used for custom unified login patterns. Includes Windows Integrated Authentication pattern.

_Inputs_

OriginalUrl : Type: mandatory, Text.

_Outputs_

Url : Type: Text.

### User\_IsExternalUser { \#User\_IsExternalUser }

_Inputs_

UserId : Type: mandatory, User Identifier.

_Outputs_

IsExternal : Type: Boolean.

### User\_Login { \#User\_Login }

Action to login using username and password as credentials.

_Inputs_

Username : Type: mandatory, Text.  
User's username.

Password : Type: mandatory, Text.  
User's password \(should not be encrypted\).

RememberLogin : Type: mandatory, Boolean.  
If true, the login will be persistent for 10 days.

### User\_Logout { \#User\_Logout }

Logs out the current user. Session variables are cleared during the logout process.

### User\_Unblock { \#User\_Unblock }

Ends the blocking period for the specified user, allowing the user to login in all IP addresses where the user was blocked.

_Inputs_

Username : Type: mandatory, Text.  
The username of the user that is being unblocked and that will be allowed to login again from the specified IP address.

IPAddress : Type: optional, Text.  
The IP address that is being unblocked and from where the specified user will be allowed to login again.

### User\_Update { \#User\_Update }

Updates a specific user.

_Inputs_

User : Type: mandatory, User.

## Structures

### LoginAttemptPublic { \#Structure\_LoginAttemptPublic }

Represents the Login attempt record structure that is exposed

_Attributes_

Instant : Type: Date Time.

Success : Type: Boolean.

IPAddress : Type: Text \(45\).

UsernameFailureCount : Type: Integer.

IPAddressFailureCount : Type: Integer.

RequestKey : Type: Text \(36\).

UserAgent : Type: Text \(200\).

Visitor : Type: Text \(36\).

Result : Type: Text.

## Static Entities

### LoginAttemptResult { \#StaticEntity\_LoginAttemptResult }

The alternative values that may appear in the LoginAttempt record Result column.

_Attributes_

Id : Type: Text \(50\).

_Records_

* InvalidLDAPAuthentication
* BlockedIP
* Unblocked
* LoggedIn
* BlockedUser
* InvalidADAuthentication
* InvalidUser
* InvalidPassword

### MenuItem { \#StaticEntity\_MenuItem }

Menu item to be used in menu web block parameters.

_Attributes_

Id : Type: Integer.

Order : Type: Integer.

Caption : Type: Text \(50\).

_Records_

* Applications
* Users
* Groups

