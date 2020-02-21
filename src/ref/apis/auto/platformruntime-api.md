# PlatformRuntime API

For Platform Version 10.0.0.0. Allows manipulating runtime configurations for the environment.

## Summary

| Action | Description |
| :--- | :--- |
| [Audit\_CreateAuditLog](platformruntime-api.md#Audit_CreateAuditLog%3E) | Creates an audit log record in a secure auditing storage. This action waits until the audit log is successfully stored, otherwise an exception is raised.%%If the secure auditing storage is unsupported or not configured in the current environment, the creation of the audit log record is skipped. |
| [Database\_WriteInParallelTransaction](platformruntime-api.md#Database_WriteInParallelTransaction%3E) | Write a record converted to an object using other transaction besides the main transaction of the request. |
| [DatabaseConnection\_SetConnectionStringForSession](platformruntime-api.md#DatabaseConnection_SetConnectionStringForSession%3E) | Switches a Database Connection from one database to another at runtime and in the current Session.%%There are some conditions to which you have to pay attention to when using this action:%%- If there is a single query that uses the Database Connection with the old database before this action is executed, the switch to the new database will not happen until the end of the current request. Only in a next request the database switch becomes effective.%%- The Connection String must connect to a database with the same type \(e.g. Oracle, SQL Server, MySQL\) as the one configured in Service Center for the Database Connection.%%- Your license must include the Platform Extensibility APIs feature. |
| [Request\_GetKey](platformruntime-api.md#Request_GetKey%3E) | Provides the RequestKey that uniquely identifies the current request.%%If there is no RequestKey available in the current context, an empty string is returned. |
| [Session\_GetMobileAppLoginId](platformruntime-api.md#Session_GetMobileAppLoginId%3E) | Gets the token that uniquely identifies the authenticated session for a Mobile Application.%%This method can be used in when managing server side session stores where you need to uniquely identify a user authenticated session. |
| [Session\_GetMobileAppLoginInfo](platformruntime-api.md#Session_GetMobileAppLoginInfo%3E) | Gets User information of the authenticated user for a Mobile Application.%%This method is designed for interoperability scenarios where you need to embed a Responsive screen in your mobile application. |
| [Session\_GetWebAppLoginInfo](platformruntime-api.md#Session_GetWebAppLoginInfo%3E) | Gets User information of the authenticated user for a Web Application.%%This method is designed for interoperability scenarios where you need to access session information in sessionless endpoints like REST methods. |

## Actions

### Audit\_CreateAuditLog { \#Audit\_CreateAuditLog }

Creates an audit log record in a secure auditing storage. This action waits until the audit log is successfully stored, otherwise an exception is raised.  
If the secure auditing storage is unsupported or not configured in the current environment, the creation of the audit log record is skipped.

_Inputs_

Operation : Type: Text. Mandatory.  
Name of the operation being logged.

Message : Type: Text. Mandatory.  
Message of the audit log.

Extra : Type: Text.  
String in JSON format including extra information relevant to the audit log.

### Database\_WriteInParallelTransaction { \#Database\_WriteInParallelTransaction }

Write a record converted to an object using other transaction besides the main transaction of the request.

_Inputs_

Record : Type: Object. Mandatory.  
Record to write using the a parallel transaction

### DatabaseConnection\_SetConnectionStringForSession { \#DatabaseConnection\_SetConnectionStringForSession }

Switches a Database Connection from one database to another at runtime and in the current Session.  
There are some conditions to which you have to pay attention to when using this action:  
- If there is a single query that uses the Database Connection with the old database before this action is executed, the switch to the new database will not happen until the end of the current request. Only in a next request the database switch becomes effective.  
- The Connection String must connect to a database with the same type \(e.g. Oracle, SQL Server, MySQL\) as the one configured in Service Center for the Database Connection.  
- Your license must include the Platform Extensibility APIs feature.

_Inputs_

connectionName : Type: Text. Mandatory.  
Name of the Database Connection, as defined in Service Center.

connectionString : Type: Text. Mandatory.  
The Connection String to be used by the Database Connection to connect to the new database.

databaseIdentifier : Type: Text.  
The initial database to use \(effective only for Oracle databases, indicating the schema to be initialy used\).

### Request\_GetKey { \#Request\_GetKey }

Provides the RequestKey that uniquely identifies the current request.  
If there is no RequestKey available in the current context, an empty string is returned.

_Outputs_

RequestKey : Type: Text.

### Session\_GetMobileAppLoginId { \#Session\_GetMobileAppLoginId }

Gets the token that uniquely identifies the authenticated session for a Mobile Application.  
This method can be used in when managing server side session stores where you need to uniquely identify a user authenticated session.

_Outputs_

loginId : Type: Text.  
Returns the session identifier or NullTextIdentifier\(\) if no user is logged in.

### Session\_GetMobileAppLoginInfo { \#Session\_GetMobileAppLoginInfo }

Gets User information of the authenticated user for a Mobile Application.  
This method is designed for interoperability scenarios where you need to embed a Responsive screen in your mobile application.

_Outputs_

userId : Type: Integer.  
Returns the user identifier, or NullIdentifier\(\) \(userId = 0\) if user is not logged in.

isPersistent : Type: Boolean.  
True if the login is persistent.

### Session\_GetWebAppLoginInfo { \#Session\_GetWebAppLoginInfo }

Gets User information of the authenticated user for a Web Application.  
This method is designed for interoperability scenarios where you need to access session information in sessionless endpoints like REST methods.

_Outputs_

userId : Type: Integer.  
Returns the user identifier, or NullIdentifier\(\) \(userId = 0\) if user is not logged in.

