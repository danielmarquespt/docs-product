# LifeTime Services API

For version 10.0.708.100. Provides APIs to LifeTime functionality.

## Summary

| Web Service | Description |
| :--- | :--- |
| [RoleManagementService](lifetime-services-api.md#RoleManagementService%3E) | The Platform API to manage IT roles: roles created in the platform. The authenticated user needs to have 'Manage Infrastructure' permissions in the platform to use this API.%%To use this API you need to send an authentication argument with username/password, or use the AuthenticationService Web Service API to acquire a session token to send as argument. |
| [AuthenticationService](lifetime-services-api.md#AuthenticationService%3E) | The Platform API to acquire an authentication token to be used when invoking other OutSystems APIs. After 5 minutes, the token expires. |
| [TeamManagementService](lifetime-services-api.md#TeamManagementService%3E) | The Platform API to manage teams in the platform.%%To use this API you need to send an authentication argument with username/password, or use the AuthenticationService Web Service API to acquire a session token to send as argument. |
| [SecurityManagementService](lifetime-services-api.md#SecurityManagementService%3E) | The Platform API for getting security information about users and addresses who login to the platform.%%To use this API you need to send an authentication argument with username/password, or use the AuthenticationService Web Service API to acquire a session token to send as argument. |
| [DbConnectionManagementService](lifetime-services-api.md#DbConnectionManagementService%3E) | This API provides methods to create, change, and delete connections to external databases. It also allows managing users permissions. |
| [UserManagementService](lifetime-services-api.md#UserManagementService%3E) | The Platform API to manage IT users: users created in the platform. The authenticated user needs to have 'Manage Infrastructure' permissions in the platform to use this API.%%To use this API you need to send an authentication argument with username/password, or use the AuthenticationService Web Service API to acquire a session token to send as argument. |

## RoleManagementService

The Platform API to manage IT roles: roles created in the platform. The authenticated user needs to have 'Manage Infrastructure' permissions in the platform to use this API.  
To use this API you need to send an authentication argument with username/password, or use the AuthenticationService Web Service API to acquire a session token to send as argument.

This API is exposed as a Web Service, made available at:  
`http://<InfrastructureManagementEnvironment>/LifeTimeServices/RoleManagementService.asmx?WSDL`

| Action | Description |
| :--- | :--- |
| [Role\_ChangeName](lifetime-services-api.md#Role_ChangeName%3E) | Updates the name of a platform role. |
| [Role\_CreateOrUpdate](lifetime-services-api.md#Role_CreateOrUpdate%3E) | Creates a new platform role or updates a platform role that already exists. |
| [Role\_Delete](lifetime-services-api.md#Role_Delete%3E) | Deletes a platform role that already exists. Since the platform requires IT users to have a single platform role, you need to specify a new platform role to grant to the users that are currently set with the role you want to delete.%% |
| [Role\_GetEnvironmentPermissionsLevels](lifetime-services-api.md#Role_GetEnvironmentPermissionsLevels%3E) | Lists the permission levels that a platform user has over the environments. |
| [Role\_GetPermissions](lifetime-services-api.md#Role_GetPermissions%3E) | Returns the list of permissions a platform role has in the environments registered in the platform. |
| [Role\_List](lifetime-services-api.md#Role_List%3E) | Returns all platform roles with their information. |
| [Role\_UpdatePermission](lifetime-services-api.md#Role_UpdatePermission%3E) | Updates the permissions a platform role has in a specified environment. |

### Actions

#### Role\_ChangeName { \#Role\_ChangeName }

Updates the name of a platform role.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

OldRoleName : Type: mandatory, Text.  
The name of a platform role that is going to be renamed.

NewRoleName : Type: mandatory, Text.  
The new name of the platform role.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### Role\_CreateOrUpdate { \#Role\_CreateOrUpdate }

Creates a new platform role or updates a platform role that already exists.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

RoleName : Type: mandatory, Text.  
The name of a platform role. If this role does not exist in the platform it is created, otherwise it is updated.

CanConfigureInfrastructure : Type: mandatory, Boolean.  
Specifies whether the platform role has permissions to configure the infrastructure.

RoleDescription : Type: mandatory, Text.  
The description for the platform role.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

PlatformRole : Type: [PlatformRole](lifetime-services-api.md#Structure_PlatformRole%3E).  
A platform role with its information.

#### Role\_Delete { \#Role\_Delete }

Deletes a platform role that already exists. Since the platform requires IT users to have a single platform role, you need to specify a new platform role to grant to the users that are currently set with the role you want to delete.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

RoleName : Type: mandatory, Text.  
The name of a platform role.

UsersNewRoleName : Type: mandatory, Text.  
A platform role to grant to the users that had the platform role that is going to be deleted.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

AffectedPlatformUsers : Type: [PlatformUser](lifetime-services-api.md#Structure_PlatformUser%3E) List.  
The list of IT users that had the deleted platform role assigned to them.

#### Role\_GetEnvironmentPermissionsLevels { \#Role\_GetEnvironmentPermissionsLevels }

Lists the permission levels that a platform user has over the environments.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

RolePermissionLevels : Type: EnvironmentPermissionLevel List.  
The permissions an IT user has over an environment, as configured in the platform.

#### Role\_GetPermissions { \#Role\_GetPermissions }

Returns the list of permissions a platform role has in the environments registered in the platform.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

RoleName : Type: mandatory, Text.  
The name of a platform role.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

PlatformRolePermissions : Type: [EnvironmentPermissionForRole](lifetime-services-api.md#Structure_EnvironmentPermissionForRole%3E) List.  
The list of permissions a platform role has over the environments registered in the platform.

#### Role\_List { \#Role\_List }

Returns all platform roles with their information.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

PlatformRoles : Type: [PlatformRole](lifetime-services-api.md#Structure_PlatformRole%3E) List.  
The list of platform roles.

#### Role\_UpdatePermission { \#Role\_UpdatePermission }

Updates the permissions a platform role has in a specified environment.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

RoleName : Type: mandatory, Text.  
The name of a platform role.

EnvironmentKey : Type: mandatory, Text.  
The environment unique identifier.

NewPermissionLevelId : Type: mandatory, EnvironmentPermissionLevel Identifier.  
A reference to the new permission level the platform role will have.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

## AuthenticationService

The Platform API to acquire an authentication token to be used when invoking other OutSystems APIs. After 5 minutes, the token expires.

This API is exposed as a Web Service, made available at:  
`http://<InfrastructureManagementEnvironment>/LifeTimeServices/AuthenticationService.asmx?WSDL`

| Action | Description |
| :--- | :--- |
| [Authentication\_GetToken](lifetime-services-api.md#Authentication_GetToken%3E) | Returns an authentication token that is valid for 5 minutes. |

### Actions

#### Authentication\_GetToken { \#Authentication\_GetToken }

Returns an authentication token that is valid for 5 minutes.

_Inputs_

Username : Type: mandatory, Text.  
A platform username.

Password : Type: mandatory, Text.  
A platform password.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

Token : Type: Text.  
A session token. This token expires 5 minutes after it has been created.

## TeamManagementService

The Platform API to manage teams in the platform.  
To use this API you need to send an authentication argument with username/password, or use the AuthenticationService Web Service API to acquire a session token to send as argument.

This API is exposed as a Web Service, made available at:  
`http://<InfrastructureManagementEnvironment>/LifeTimeServices/TeamManagementService.asmx?WSDL`

| Action | Description |
| :--- | :--- |
| [Team\_AddUser](lifetime-services-api.md#Team_AddUser%3E) | Adds a user to a team with a specified role. |
| [Team\_AssignApplication](lifetime-services-api.md#Team_AssignApplication%3E) | Assigns an application to a team, replacing a previous assignment, if any. An application can only be assigned to a team a time. |
| [Team\_CreateOrUpdate](lifetime-services-api.md#Team_CreateOrUpdate%3E) | Creates a new team or updates an already existent team. |
| [Team\_Delete](lifetime-services-api.md#Team_Delete%3E) | Deletes a team. |
| [Team\_GetDetails](lifetime-services-api.md#Team_GetDetails%3E) | Returns the details of a team, with its users and applications. |
| [Team\_List](lifetime-services-api.md#Team_List%3E) | Returns a list of the teams. |
| [Team\_RemoveApplication](lifetime-services-api.md#Team_RemoveApplication%3E) | Removes an application from a team. |
| [Team\_RemoveUser](lifetime-services-api.md#Team_RemoveUser%3E) | Removes a user from a team. |

### Actions

#### Team\_AddUser { \#Team\_AddUser }

Adds a user to a team with a specified role.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid username and password, or use the AuthenticationService API to acquire a session token.

TeamName : Type: mandatory, Text.  
The name of the team.

Username : Type: mandatory, Text.  
The username of the user.

RoleName : Type: mandatory, Text.  
The name of the role to assign to the user.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

#### Team\_AssignApplication { \#Team\_AssignApplication }

Assigns an application to a team, replacing a previous assignment, if any. An application can only be assigned to a team a time.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid username and password, or use the AuthenticationService API to acquire a session token.

TeamName : Type: mandatory, Text.  
The name of the team.

ApplicationKey : Type: mandatory, Text.  
The application unique identifier.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

#### Team\_CreateOrUpdate { \#Team\_CreateOrUpdate }

Creates a new team or updates an already existent team.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid username and password, or use the AuthenticationService API to acquire a session token.

TeamName : Type: mandatory, Text.  
The name of the team.

Description : Type: mandatory, Text.  
The description of the team.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

PlatformTeam : Type: [PlatformTeam](lifetime-services-api.md#Structure_PlatformTeam%3E).  
The team created or updated.

#### Team\_Delete { \#Team\_Delete }

Deletes a team.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid username and password, or use the AuthenticationService API to acquire a session token.

TeamName : Type: mandatory, Text.  
The name of the team.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

#### Team\_GetDetails { \#Team\_GetDetails }

Returns the details of a team, with its users and applications.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid username and password, or use the AuthenticationService API to acquire a session token.

TeamName : Type: mandatory, Text.  
The name of the team.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

PlatformTeam : Type: [PlatformTeam](lifetime-services-api.md#Structure_PlatformTeam%3E).  
The team details.

#### Team\_List { \#Team\_List }

Returns a list of the teams.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid username and password, or use the AuthenticationService API to acquire a session token.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

PlatformTeams : Type: [PlatformTeam](lifetime-services-api.md#Structure_PlatformTeam%3E) List.  
The list with the teams. The returned ApplicationList and UserList attributes of each team will be empty; call the Team\_GetDetails action to obtain the application and user list of a team.

#### Team\_RemoveApplication { \#Team\_RemoveApplication }

Removes an application from a team.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid username and password, or use the AuthenticationService API to acquire a session token.

TeamName : Type: mandatory, Text.  
The name of the team.

ApplicationKey : Type: mandatory, Text.  
The application unique identifier.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

#### Team\_RemoveUser { \#Team\_RemoveUser }

Removes a user from a team.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid username and password, or use the AuthenticationService API to acquire a session token.

TeamName : Type: mandatory, Text.  
The name of the team.

Username : Type: mandatory, Text.  
The username of the user.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API action. In case of error, contains the error code and human-readable error messages.

## SecurityManagementService

The Platform API for getting security information about users and addresses who login to the platform.  
To use this API you need to send an authentication argument with username/password, or use the AuthenticationService Web Service API to acquire a session token to send as argument.

This API is exposed as a Web Service, made available at:  
`http://<InfrastructureManagementEnvironment>/LifeTimeServices/SecurityManagementService.asmx?WSDL`

| Action | Description |
| :--- | :--- |
| [IPAddress\_GetLockedStatus](lifetime-services-api.md#IPAddress_GetLockedStatus%3E) |  |
| [IPAddress\_Unlock](lifetime-services-api.md#IPAddress_Unlock%3E) |  |
| [User\_GetLockedStatus](lifetime-services-api.md#User_GetLockedStatus%3E) |  |
| [User\_Unlock](lifetime-services-api.md#User_Unlock%3E) |  |

### Actions

#### IPAddress\_GetLockedStatus { \#IPAddress\_GetLockedStatus }

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

IPAddress : Type: optional, Text.  
IP Address to which the lock information, should it exist, belongs to. If this parameter is empty, information on all IP locked addresses is returned.

EnvironmentKey : Type: optional, Text.  
The environment unique identifier in which the lock information should be searched. If the parameter is empty, it returns the pertaining information regarding all active environments.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

PlatformLoginAttempts : Type: [PlatformLoginAttempt](lifetime-services-api.md#Structure_PlatformLoginAttempt%3E) List.  
List of login attempts with respect to the given IP address \(or all IP addresses\) in the given environment \(or all active environments\).

#### IPAddress\_Unlock { \#IPAddress\_Unlock }

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

IPAddress : Type: mandatory, Text.  
IP Address to be unlocked in the given environment.

EnvironmentKey : Type: optional, Text.  
The environment unique identifier in which the IP address should be unlocked.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### User\_GetLockedStatus { \#User\_GetLockedStatus }

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
Username to which the lock information, should it exist, belongs to.

EnvironmentKey : Type: optional, Text.  
The environment unique identifier in which the lock information should be searched. If the parameter is empty, it returns the pertaining information regarding all active environments.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

PlatformLoginAttempts : Type: [PlatformLoginAttempt](lifetime-services-api.md#Structure_PlatformLoginAttempt%3E) List.  
List of login attempts with respect to the given Username in the given environment \(or all active environments\).

#### User\_Unlock { \#User\_Unlock }

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
Username to be unlocked in the given environment \(or all environments\).

IPAddress : Type: optional, Text.  
IP address from which the specified Username is to be unlocked.

EnvironmentKey : Type: optional, Text.  
The environment unique identifier in which the Username should be unlocked.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

## DbConnectionManagementService

This API provides methods to create, change, and delete connections to external databases. It also allows managing users permissions.

This API is exposed as a Web Service, made available at:  
`http://<InfrastructureManagementEnvironment>/LifeTimeServices/DbConnectionManagementService.asmx?WSDL`

| Action | Description |
| :--- | :--- |
| [DbConnection\_Create](lifetime-services-api.md#DbConnection_Create%3E) | Creates a new database connection. |
| [DbConnection\_Delete](lifetime-services-api.md#DbConnection_Delete%3E) | Deletes the database connection given by the name. |
| [DbConnection\_Edit](lifetime-services-api.md#DbConnection_Edit%3E) | Updates the configuration of the database connection. |
| [DbConnection\_Get](lifetime-services-api.md#DbConnection_Get%3E) | Returns the database connection. |
| [DbConnection\_GetRoleAccess](lifetime-services-api.md#DbConnection_GetRoleAccess%3E) | Returns the role permissions to use a database connection. |
| [DbConnection\_GetUserAccess](lifetime-services-api.md#DbConnection_GetUserAccess%3E) | Returns the user permissions to use a database connection. |
| [DbConnection\_GrantRoleAccess](lifetime-services-api.md#DbConnection_GrantRoleAccess%3E) | Grants a role with a permission level to use the database connection. |
| [DbConnection\_GrantUserAccess](lifetime-services-api.md#DbConnection_GrantUserAccess%3E) | Grants a user with a permission level to use the database connection. |
| [DbConnection\_ListAll](lifetime-services-api.md#DbConnection_ListAll%3E) | Returns a list with all database connections. |
| [DbConnection\_ListProviders](lifetime-services-api.md#DbConnection_ListProviders%3E) | The list of database providers that a user can associate to a database connection. |
| [DbConnection\_PermissionLevel\_List](lifetime-services-api.md#DbConnection_PermissionLevel_List%3E) | Returns the list of permission levels. |
| [DbConnection\_Rename](lifetime-services-api.md#DbConnection_Rename%3E) | Renames an database connection. This may have impact on all running application that use this database connection. |
| [DbConnection\_RevokeRoleAccess](lifetime-services-api.md#DbConnection_RevokeRoleAccess%3E) | Revokes the role permissions to use the database connection. |
| [DbConnection\_RevokeUserAccess](lifetime-services-api.md#DbConnection_RevokeUserAccess%3E) | Revokes the user permissions to use the database connection. |
| [DbConnection\_TestConnection](lifetime-services-api.md#DbConnection_TestConnection%3E) | Tests a database connection with the given parameters. |

### Actions

#### DbConnection\_Create { \#DbConnection\_Create }

Creates a new database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid Platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
The environment unique identifier.

Name : Type: mandatory, Text.  
The name of the new database connection.

ProviderKey : Type: mandatory, Text.  
The key of the database provider associated with the new database connection. See method DBConnection\_ListProviders.

Description : Type: mandatory, Text.  
The description of the new database connection.

DBUsername : Type: mandatory, Text.  
The username to log in to the external database.

DBPassword : Type: mandatory, Text.  
The password to log in to the external database.

DBConfigParams : Type: mandatory, Text.  
Parameters for the connection string. Separate them using ';'.

TestConnection : Type: mandatory, Boolean.  
If True, the database connection is only created after being tested with success.

_Outputs_

DbConnection : Type: .  
The database connection that was created.

Success : Type: Boolean.  
True if the database connection was created.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_Delete { \#DbConnection\_Delete }

Deletes the database connection given by the name.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection .

_Outputs_

Success : Type: Boolean.  
True if the database connection was deleted.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_Edit { \#DbConnection\_Edit }

Updates the configuration of the database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection.

ProviderKey : Type: mandatory, Text.  
The key of the database provider associated with the new database connection. See method DBConnection\_ListProviders.

Description : Type: mandatory, Text.  
The database connection description.

DBUsername : Type: mandatory, Text.  
The username to log in to the external database.

DBPassword : Type: mandatory, Text.  
The password to log in to the external database.

DBConfigParams : Type: mandatory, Text.  
Parameters for the connection string. Separate them using ';'.

TestConnection : Type: mandatory, Boolean.  
If True, the database connection is only updated after being tested with sucess.

_Outputs_

Success : Type: Boolean.  
True if the database connection was changed.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_Get { \#DbConnection\_Get }

Returns the database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection.

_Outputs_

DbConnection : Type: .  
The database connection.

Success : Type: Boolean.  
True if the database connection was got.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_GetRoleAccess { \#DbConnection\_GetRoleAccess }

Returns the role permissions to use a database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection.

RoleName : Type: mandatory, Text.  
The name of the role.

_Outputs_

PermissionLevel : Type: .  
The role's permission level.

Success : Type: Boolean.  
True if the permissions were got.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_GetUserAccess { \#DbConnection\_GetUserAccess }

Returns the user permissions to use a database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection.

Username : Type: mandatory, Text.  
The username of the user.

_Outputs_

PermissionLevel : Type: .  
The user's permission level.

Success : Type: Boolean.  
True if the permissions were got.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_GrantRoleAccess { \#DbConnection\_GrantRoleAccess }

Grants a role with a permission level to use the database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection.

RoleName : Type: mandatory, Text.  
The name of the role of users to grant permissions.

PermissionLevelId : Type: mandatory, DbConnectionPermissionLevel Identifier.  
The permission level to be granted. See method DbConnection\_PermissionLevel\_List.

_Outputs_

Success : Type: Boolean.  
True if the permissions were granted.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_GrantUserAccess { \#DbConnection\_GrantUserAccess }

Grants a user with a permission level to use the database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection.

Username : Type: mandatory, Text.  
The username of the user to grant permissions.

PermissionLevelId : Type: mandatory, DbConnectionPermissionLevel Identifier.  
The permission level to be granted. See method DbConnection\_PermissionLevel\_List.

_Outputs_

Success : Type: Boolean.  
True if the permissions were granted.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_ListAll { \#DbConnection\_ListAll }

Returns a list with all database connections.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

_Outputs_

DbConnections : Type: DatabaseConnection List.  
The list of all database connections.

Success : Type: Boolean.  
True if the list of database connections is filled.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_ListProviders { \#DbConnection\_ListProviders }

The list of database providers that a user can associate to a database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid Platform username and password, or use the LoginService API to acquire a session token.

_Outputs_

Providers : Type: DbProvider List.  
The list of allowed database providers.

Success : Type: Boolean.  
True if the authentication succeeds and a list of providers is returned.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error message.

#### DbConnection\_PermissionLevel\_List { \#DbConnection\_PermissionLevel\_List }

Returns the list of permission levels.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

_Outputs_

Success : Type: Boolean.  
True if the authentication succeeds and a list of permission levels is returned.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

DbConnectionPermissionLevels : Type: DbConnectionPermissionLevel List.  
The list of permission levels.

#### DbConnection\_Rename { \#DbConnection\_Rename }

Renames an database connection. This may have impact on all running application that use this database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

CurrentName : Type: mandatory, Text.  
The current name of the database connection.

NewName : Type: mandatory, Text.  
The new name for the database connection.

_Outputs_

Success : Type: Boolean.  
True if the database connection was renamed.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_RevokeRoleAccess { \#DbConnection\_RevokeRoleAccess }

Revokes the role permissions to use the database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection.

RoleName : Type: mandatory, Text.  
The name of the role to revoke permissions.

_Outputs_

Success : Type: Boolean.  
True if the permissions were revoked.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_RevokeUserAccess { \#DbConnection\_RevokeUserAccess }

Revokes the user permissions to use the database connection.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

DbConnectionName : Type: mandatory, Text.  
The name of the database connection.

Username : Type: mandatory, Text.  
The username of the user to revoke permissions.

_Outputs_

Success : Type: Boolean.  
True if the permissions were revoked.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### DbConnection\_TestConnection { \#DbConnection\_TestConnection }

Tests a database connection with the given parameters.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid Platform username and password, or use the LoginService API to acquire a session token.

EnvironmentKey : Type: mandatory, Text.  
An environment unique identifier.

ProviderKey : Type: mandatory, Text.  
The key of the database provider associated with the new database connection. See method DBConnection\_ListProviders.

DBUsername : Type: mandatory, Text.  
The username to log in to the external database.

DBPassword : Type: mandatory, Text.  
The password to log in to the external database.

DBConfigParams : Type: mandatory, Text.  
Parameters for the connection string. Separate them using ';'.

_Outputs_

Success : Type: Boolean.  
True if the connection was successful.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

## UserManagementService

The Platform API to manage IT users: users created in the platform. The authenticated user needs to have 'Manage Infrastructure' permissions in the platform to use this API.  
To use this API you need to send an authentication argument with username/password, or use the AuthenticationService Web Service API to acquire a session token to send as argument.

This API is exposed as a Web Service, made available at:  
`http://<InfrastructureManagementEnvironment>/LifeTimeServices/UserManagementService.asmx?WSDL`

| Action | Description |
| :--- | :--- |
| [User\_ChangePassword](lifetime-services-api.md#User_ChangePassword%3E) | Changes the password of a platform user. |
| [User\_ChangeUsername](lifetime-services-api.md#User_ChangeUsername%3E) | Changes the username of a platform user. |
| [User\_CreateOrUpdate](lifetime-services-api.md#User_CreateOrUpdate%3E) | Creates a new platform user or updates an existing one. The operation activates the user in the platform. |
| [User\_DeleteApplicationPermission](lifetime-services-api.md#User_DeleteApplicationPermission%3E) | Deletes the permission a platform user has for a specific application. After executing this operation, the user permissions for the application are defined by the platform roles the platform user has. |
| [User\_GetAllPermissions](lifetime-services-api.md#User_GetAllPermissions%3E) | Returns the permissions a platform user has over each existing application and the permissions of the platform role, in each environment of the infrastructure. |
| [User\_GetApplicationPermissions](lifetime-services-api.md#User_GetApplicationPermissions%3E) | Returns the permissions a platform user has over an application, in each environment of the infrastructure, or the permissions from the platform role in case of specific permissions for the application were not specified. |
| [User\_List](lifetime-services-api.md#User_List%3E) | Returns the list of platform users, with their information, such as username, email and platform role. |
| [User\_SetActive](lifetime-services-api.md#User_SetActive%3E) | Activates a user in the platform, restoring all permissions the platform user has associated. |
| [User\_SetApplicationRole](lifetime-services-api.md#User_SetApplicationRole%3E) | Updates the role a platform user has for an application with the given key. |
| [User\_SetInactive](lifetime-services-api.md#User_SetInactive%3E) | Deactivates a user in the platform. The user stops having access to all operations that require authentication. |

### Actions

#### User\_ChangePassword { \#User\_ChangePassword }

Changes the password of a platform user.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
The username of a platform user.

NewPassword : Type: mandatory, Text.  
The new password.

EncryptPassword : Type: mandatory, Boolean.  
Specifies if the password of the platform user will be encrypted.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### User\_ChangeUsername { \#User\_ChangeUsername }

Changes the username of a platform user.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

OldUsername : Type: mandatory, Text.  
The username of a platform user.

NewUsername : Type: mandatory, Text.  
The new username.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### User\_CreateOrUpdate { \#User\_CreateOrUpdate }

Creates a new platform user or updates an existing one. The operation activates the user in the platform.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
The username of a platform user.

Password : Type: mandatory, Text.  
The password of a platform user.

EncryptPassword : Type: mandatory, Boolean.  
Specifies if the password of the platform user will be encrypted.

Name : Type: mandatory, Text.  
The name of a platform user.

Email : Type: mandatory, Email.  
The email of a platform user.

RoleName : Type: mandatory, Text.  
The platform role to grant to a platform user.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

PlatformUser : Type: [PlatformUser](lifetime-services-api.md#Structure_PlatformUser%3E).  
A platform user.

#### User\_DeleteApplicationPermission { \#User\_DeleteApplicationPermission }

Deletes the permission a platform user has for a specific application. After executing this operation, the user permissions for the application are defined by the platform roles the platform user has.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
The username of a platform user.

ApplicationKey : Type: mandatory, Text.  
An application unique identifier.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### User\_GetAllPermissions { \#User\_GetAllPermissions }

Returns the permissions a platform user has over each existing application and the permissions of the platform role, in each environment of the infrastructure.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
The username of a platform user.

_Outputs_

Success : Type: Boolean.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

ApplicationPermissions : Type: [ApplicationPermissions](lifetime-services-api.md#Structure_ApplicationPermissions%3E), [ApplicationShortInfo](lifetime-services-api.md#Structure_ApplicationShortInfo%3E) List.  
The list of permissions a platform user has over each application in each environment registered in platform.

PlatformRolePermissions : Type: [ApplicationPermissions](lifetime-services-api.md#Structure_ApplicationPermissions%3E).  
The list of permissions a platform user has considering the platform role in each environment registered in platform.

#### User\_GetApplicationPermissions { \#User\_GetApplicationPermissions }

Returns the permissions a platform user has over an application, in each environment of the infrastructure, or the permissions from the platform role in case of specific permissions for the application were not specified.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
The username of a platform user.

ApplicationKey : Type: mandatory, Text.  
An application unique identifier.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

ArePlatformRolePermissions : Type: Boolean.  
Specifies whether the permissions are granted from the user's role or if the user has permissions configured for the application.

ApplicationPermissions : Type: [ApplicationPermissions](lifetime-services-api.md#Structure_ApplicationPermissions%3E).  
The list of permissions a platform user has over the application in each environment registered in platform.

#### User\_List { \#User\_List }

Returns the list of platform users, with their information, such as username, email and platform role.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

ShowInactive : Type: mandatory, Boolean.  
If True returns users that are set to inactive. If False, only returns active users.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

PlatformUsers : Type: [PlatformUser](lifetime-services-api.md#Structure_PlatformUser%3E) List.  
The list of platform users.

#### User\_SetActive { \#User\_SetActive }

Activates a user in the platform, restoring all permissions the platform user has associated.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
The username of a platform user.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### User\_SetApplicationRole { \#User\_SetApplicationRole }

Updates the role a platform user has for an application with the given key.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
The username of a platform user.

ApplicationKey : Type: mandatory, Text.  
An application unique identifier.

RoleName : Type: mandatory, Text.  
The role name.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

#### User\_SetInactive { \#User\_SetInactive }

Deactivates a user in the platform. The user stops having access to all operations that require authentication.

_Inputs_

Authentication : Type: mandatory, [WebServiceSimpleAuthentication](lifetime-services-api.md#Structure_WebServiceSimpleAuthentication%3E).  
The authentication required to use this API. Specify a valid platform username and password, or use the AuthenticationService API to acquire a session token.

Username : Type: mandatory, Text.  
The username of a platform user.

_Outputs_

Success : Type: Boolean.  
True if the method was successful, False otherwise.

Status : Type: APIStatus.  
The status of invoking this API. This status contains an error code and human-readable error messages.

## Structures

### ApplicationPermissions { \#Structure\_ApplicationPermissions }

Represents a set of permissions of an application with respect each one of the available environments.

_Attributes_

ApplicationPermissions : Type: [EnvironmentPermissionForApplication](lifetime-services-api.md#Structure_EnvironmentPermissionForApplication%3E) List.  
The permissions list where each permission corresponds to an environment.

### ApplicationShortInfo { \#Structure\_ApplicationShortInfo }

Few details about an application managed by the platform.

_Attributes_

Name : Type: Text \(50\).  
Name of the application.

Key : Type: Text \(50\).  
Application unique identifier.

Description : Type: Text \(50\).  
Description of the application.

### EnvironmentPermissionForApplication { \#Structure\_EnvironmentPermissionForApplication }

Permissions an IT user or role has over an application running on a specified environment.

_Attributes_

EnvironmentKey : Type: Text \(50\).  
Environment unique identifier.

EnvironmentName : Type: Text \(50\).  
Name of the environment.

EnvironmentHost : Type: Text \(50\).  
The environment host which is represented by a relative URL path, starting from the hostname.

EnvironmentType : Type: Text \(50\).  
Type of the environment. \[Development \| Test \| Production\]

ApplicationPermissionLevelId : Type: ApplicationPermissionLevel Identifier.  
The Application Permission Level ID with respect to the environment.

### EnvironmentPermissionForRole { \#Structure\_EnvironmentPermissionForRole }

Permissions an IT role has over an environment.

_Attributes_

EnvironmentKey : Type: Text \(50\).  
Environment unique identifier.

EnvironmentName : Type: Text \(50\).  
Name of the environment.

EnvironmentHost : Type: Text \(50\).  
The environment host which is represented by a relative URL path, starting from the hostname.

EnvironmentType : Type: Text \(50\).  
Type of the environment. \[Development \| Test \| Production\]

EnvironmentPermissionLevelId : Type: EnvironmentPermissionLevel Identifier.  
The Environment Permission Level ID with respect to the environment.

### PlatformLoginAttempt { \#Structure\_PlatformLoginAttempt }

_Attributes_

Id : Type: Long Integer.

UserId : Type: Integer.

Username : Type: Text \(250\).

Success : Type: Boolean.

Instant : Type: Date Time.

IPAddress : Type: Text \(45\).

UsernameFailureCount : Type: Integer.

OriginAddressFailureCount : Type: Integer.

UserAgent : Type: Text \(200\).

Visitor : Type: Text \(36\).

RequestKey : Type: Text \(36\).

Result : Type: Text \(50\).

EnvironmentId : Type: Environment Identifier.

EnvironmentName : Type: Text.

### PlatformRole { \#Structure\_PlatformRole }

Details about a role.

_Attributes_

Id : Type: InfrastructureRole Identifier.  
Role unique identifier.

Name : Type: Text \(50\).  
Name of the role.

Description : Type: Text \(500\).  
Description of the role.

CanManageInfrastructure : Type: Boolean.  
Specifies whether this role has permissions to configure the infrastructure or not.

IsProtected : Type: Boolean.  
True if the role is protected. False otherwise.

AllowChangePermissions : Type: Boolean.  
True if it is possible to change the role permissions. False otherwise.

PermissionsPerEnvironment : Type: [EnvironmentPermissionForRole](lifetime-services-api.md#Structure_EnvironmentPermissionForRole%3E) List.  
Role permissions information for each environment.

### PlatformTeam { \#Structure\_PlatformTeam }

The information about a platform team.

_Attributes_

Id : Type: Integer.  
The team unique identifier.

Name : Type: Text \(50\).  
The name of the team.

Description : Type: Text \(50\).  
The description of the team.

ApplicationList : Type: [ApplicationShortInfo](lifetime-services-api.md#Structure_ApplicationShortInfo%3E) List.  
The list of applications associated with the team.

UserList : Type: [PlatformUser](lifetime-services-api.md#Structure_PlatformUser%3E) List.  
The list of users associated with the team.

### PlatformUser { \#Structure\_PlatformUser }

The information about a user.

_Attributes_

Id : Type: Integer.  
User unique identifier.

Username : Type: Text \(50\).  
Username of an IT user.

Name : Type: Text \(50\).  
Name of an IT user.

Email : Type: Email.  
Email of an IT user.

RoleName : Type: Text \(50\).  
Role name the IT user has assigned.

### WebServiceSimpleAuthentication { \#Structure\_WebServiceSimpleAuthentication }

Represents the fields to authenticate an OutSystems IT user. Specify a username/password combination to authenticate, or use the AuthenticationService Web Service API to acquire a session token.

_Attributes_

Username : Type: Text \(50\).  
The username of an IT user.

Password : Type: Text.  
The password of the IT user.

Token : Type: Text \(50\).  
An authentication token.

