# lifetime-deployment-api-v1

## LifeTime Deployment API v1

### Summary

| API | Base URL | Security |
| :--- | :--- | :--- |
| [v1](lifetime-deployment-api-v1.md#v1%3E) | /lifetimeapi/rest/v1 | SSL/TLS |

### v1

| API Method | Description |
| :--- | :--- |
| [GET /applications/](lifetime-deployment-api-v1.md#Applications_List%3E) | Returns a list of applications that exist in the infrastructure. |
| [GET /applications/{ApplicationKey}/](lifetime-deployment-api-v1.md#Applications_Get%3E) | Returns the details of a given application. |
| [GET /applications/{ApplicationKey}/versions/](lifetime-deployment-api-v1.md#Applications_Versions_List%3E) | Returns a list of versions of a given application. |
| [GET /applications/{ApplicationKey}/versions/{VersionKey}/](lifetime-deployment-api-v1.md#Applications_Versions_Get%3E) | Returns the details of a given version of the specified application. |
| [GET /deployments/](lifetime-deployment-api-v1.md#Deployments_List%3E) | Returns a list of deployments ordered by creation date, from newest to oldest. |
| [POST /deployments/](lifetime-deployment-api-v1.md#Deployments_Create%3E) | Creates a deployment to a target environment. An optional list of applications to include in the deployment can be specified. The input is a subset of a Deployment object. |
| [GET /deployments/{DeploymentKey}/](lifetime-deployment-api-v1.md#Deployments_Get%3E) | Returns the details of a given deployment. The returned information contains the included applications and the possible conflicts that can arise from the deployment of the current applications. |
| [PUT /deployments/{DeploymentKey}/](lifetime-deployment-api-v1.md#Deployments_Update%3E) | Updates a given deployment. An optional list of applications to include in the deployment can be specified. The input is a subset of a Deployment object. |
| [DELETE /deployments/{DeploymentKey}/](lifetime-deployment-api-v1.md#Deployments_Delete%3E) | Discards a deployment, if possible. Only deployments whose state is “saved” can be deleted. |
| [POST /deployments/{DeploymentKey}/{Command}/](lifetime-deployment-api-v1.md#Deployments_ExecuteCommand%3E) | Executes the given command in a specified deployment. The allowed commands are “start”, “continue” and “abort”. |
| [GET /deployments/{DeploymentKey}/status/](lifetime-deployment-api-v1.md#Deployments_GetStatus%3E) | Returns the details of a given deployment execution, including the deployment status and messages. |
| [GET /environments/](lifetime-deployment-api-v1.md#Environments_List%3E) | Lists all the environments in the infrastructure. |
| [GET /environments/{EnvironmentKey}/](lifetime-deployment-api-v1.md#Environments_Get%3E) | Returns the details of a given environment. |
| [GET /environments/{EnvironmentKey}/applications/](lifetime-deployment-api-v1.md#Environments_GetRunningApps%3E) | Returns information about the running versions of all applications in a given environment. |
| [GET /environments/{EnvironmentKey}/applications/{ApplicationKey}/](lifetime-deployment-api-v1.md#Environments_GetRunningApp%3E) | Returns information about the running version of the specified application in a given environment. |
| [GET /environments/{EnvironmentKey}/applications/{ApplicationKey}/content/](lifetime-deployment-api-v1.md#Environments_DownloadRunningApp%3E) | Returns a link where the binary file for a given application can be downloaded. The link will expire in 60 minutes. |
| [POST /environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/](lifetime-deployment-api-v1.md#Environments_Applications_Versions_Create%3E) | Creates a new version of the application based on the current running application. |
| [GET /modules/](lifetime-deployment-api-v1.md#Modules_List%3E) | Returns a list of modules that exist in the infrastructure. |
| [GET /modules/{ModuleKey}/](lifetime-deployment-api-v1.md#Modules_Get%3E) | Returns the details of a given module. |
| [GET /modules/{ModuleKey}/versions/](lifetime-deployment-api-v1.md#ModuleVersions_List%3E) | Returns a list of versions of a given module. |
| [GET /modules/{ModuleKey}/versions/{ModuleVersionKey}/](lifetime-deployment-api-v1.md#ModuleVersion_Get%3E) | Returns the details of a given module version. |

## Actions

### /applications

#### GET /applications/ { \#Applications\_List }

Returns a list of applications that exist in the infrastructure.

_Full URL_

`GET /lifetimeapi/rest/v1/applications/`

_Inputs_

IncludeModules : Type: optional, Boolean.  
Located in: URL.  
When set to true, the modules are also returned. The default value is false.

IncludeEnvStatus : Type: optional, Boolean.  
Located in: URL.  
When set to true, the application status per environment is also returned. The default value is false.

_Outputs_

Applications : Type: [Application](lifetime-deployment-api-v1.md#Structure_Application%3E) List.  
Located in: Body.  
A list of Application records including AppStatusInEnv sub-lists, if requested.

_Return Codes_

200 : Application list successfully retrieved.

204 : No applications available in the infrastructure. In the Java stack, code 200 is returned instead of 204.

400 : Failed to retrieve applications because IncludeModules was requested but IncludeEnvStatus was not, or invalid request when listing all applications.

#### GET /applications/{ApplicationKey}/ { \#Applications\_Get }

Returns the details of a given application.

_Full URL_

`GET /lifetimeapi/rest/v1/applications/{ApplicationKey}/`

_Inputs_

ApplicationKey : Type: mandatory, Text.  
Located in: URL.  
The key of the desired application.

IncludeModules : Type: optional, Boolean.  
Located in: URL.  
When set to true, the modules details are also retrieved. The default value is false.

IncludeEnvStatus : Type: optional, Boolean.  
Located in: URL.  
When set to true, the application status per environment is also returned. The default value is false.

_Outputs_

Application : Type: [Application](lifetime-deployment-api-v1.md#Structure_Application%3E).  
Located in: Body.  
An Application record including an AppStatusInEnv sub-list, if requested.

_Return Codes_

200 : Application details successfully retrieved.

400 : Failed to retrieve applications because IncludeModules and IncludeEnvStatus parameters were incorrect.

403 : Failed listing all applications because the user has insufficient permissions.

404 : Failed getting running applications because one of the environments was not found.

#### GET /applications/{ApplicationKey}/versions/ { \#Applications\_Versions\_List }

Returns a list of versions of a given application.

_Full URL_

`GET /lifetimeapi/rest/v1/applications/{ApplicationKey}/versions/`

_Inputs_

ApplicationKey : Type: mandatory, Text.  
Located in: URL.  
The key of the desired application.

MaximumVersionsToReturn : Type: optional, Integer.  
Located in: URL.  
The maximum number of versions to return. The default value is 5.

_Outputs_

ApplicationVersions : Type: [ApplicationVersion](lifetime-deployment-api-v1.md#Structure_ApplicationVersion%3E) List.  
Located in: Body.  
A list of ApplicationVersion records.

_Return Codes_

200 : List of application versions successfully retrieved.

400 : Invalid request due to invalid max versions to return \(less than 0\).

403 : Failed to retrieve the application with key `<ApplicationKey>`. The user does not have the required permissions.

404 : Failed to retrieve the application with key `<ApplicationKey>`.

#### GET /applications/{ApplicationKey}/versions/{VersionKey}/ { \#Applications\_Versions\_Get }

Returns the details of a given version of the specified application.

_Full URL_

`GET /lifetimeapi/rest/v1/applications/{ApplicationKey}/versions/{VersionKey}/`

_Inputs_

ApplicationKey : Type: mandatory, Text.  
Located in: URL.  
The key of the application whose version is being requested.

VersionKey : Type: mandatory, Text.  
Located in: URL.  
The key of the desired application version.

IncludeModules : Type: mandatory, Boolean.  
Located in: URL.  
When set to true, the modules details are also retrieved. The default value is false.

_Outputs_

ApplicationVersion : Type: [ApplicationVersion](lifetime-deployment-api-v1.md#Structure_ApplicationVersion%3E).  
Located in: Body.  
An ApplicationVersion record.

_Return Codes_

200 : Application version details successfully retrieved.

403 : Failed to retrieve the application with key `<ApplicationKey>`. The user does not have the required permissions.

404 : Failed to retrieve the application with key `<ApplicationKey>`.

### /deployments

#### GET /deployments/ { \#Deployments\_List }

Returns a list of deployments ordered by creation date, from newest to oldest.

_Full URL_

`GET /lifetimeapi/rest/v1/deployments/`

_Inputs_

MinDate : Type: optional, Date.  
Located in: URL.  
The minimum creation date of the deployments to return. The default value is 1 week before the current date.

MaxDate : Type: optional, Date.  
Located in: URL.  
The maximum creation date of the deployments to return. The default value is the current date.

_Outputs_

Deployments : Type: [Deployment](lifetime-deployment-api-v1.md#Structure_Deployment%3E) List.  
Located in: Body.  
A list of Deployment records.

_Return Codes_

200 : Deployments list successfully retrieved.

204 : There are no deployments created between `<MinDate>` and `<MaxDate>`. In the Java stack, code 200 is returned instead of 204.

400 : Invalid request for list of deployments created between `<MinDate>` and `<MaxDate>`.

403 : User doesn't have access to any application or environment involved in the deployments created between `<MinDate>` and `<MaxDate>`.

#### POST /deployments/ { \#Deployments\_Create }

Creates a deployment to a target environment. An optional list of applications to include in the deployment can be specified. The input is a subset of a Deployment object.

_Full URL_

`POST /lifetimeapi/rest/v1/deployments/`

_Inputs_

ApplicationVersionKeys : Type: Optional, Text List.  
Located in: Body.  
List of keys of the application versions included in the deployment.

Notes : Type: optional, Text.  
Located in: Body.  
Deployment notes.

SourceEnvironmentKey : Type: optional, Text.  
Located in: Body.  
Source environment unique identifier.

TargetEnvironmentKey : Type: optional, Text.  
Located in: Body.  
Target environment unique identifier.

_Outputs_

DeploymentKey : Type: Text.  
Located in: Body.  
The key of the newly created deployment.

_Return Codes_

201 : Deployment successfully created.

400 : Invalid request.

403 : Invalid user permissions.

404 : Source or target environment not found.

**Example Request Body**

```javascript
{
  "ApplicationVersionKeys": [
    "22dcc061-8767-46dd-8a6e-7991ee8112c7"
  ],
  "Notes": "WebPortal 1.1 - QA to PRD Deployment",
  "SourceEnvironmentKey": "10061715-16bb-491a-86bc-595b465eaffb",
  "TargetEnvironmentKey": "55c430ee-4783-43e6-a2d4-6eecfed1d90f"
}
```

#### GET /deployments/{DeploymentKey}/ { \#Deployments\_Get }

Returns the details of a given deployment. The returned information contains the included applications and the possible conflicts that can arise from the deployment of the current applications.

_Full URL_

`GET /lifetimeapi/rest/v1/deployments/{DeploymentKey}/`

_Inputs_

DeploymentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the desired deployment.

_Outputs_

ApplicationConflicts : Type: [ApplicationConflict](lifetime-deployment-api-v1.md#Structure_ApplicationConflict%3E) List.  
Located in: Body.  
List of conflicts between applications in the deployment.

Deployment : Type: [Deployment](lifetime-deployment-api-v1.md#Structure_Deployment%3E).  
Located in: Body.  
The deployment details.

_Return Codes_

200 : Deployment details successfully retrieved.

403 : User doesn't have permissions to the deployment with key `<DeploymentKey>`.

404 : Deployment with key `<DeploymentKey>` not found.

#### PUT /deployments/{DeploymentKey}/ { \#Deployments\_Update }

Updates a given deployment. An optional list of applications to include in the deployment can be specified. The input is a subset of a Deployment object.

_Full URL_

`PUT /lifetimeapi/rest/v1/deployments/{DeploymentKey}/`

_Inputs_

DeploymentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the deployment to update.

ApplicationVersionKeys : Type: optional, Text List.  
Located in: Body.  
List of keys of the application versions to include in the deployment.

Notes : Type: optional, Text.  
Located in: Body.  
Deployment notes.

SourceEnvironmentKey : Type: optional, Text.  
Located in: Body.  
Source environment unique identifier.

TargetEnvironmentKey : Type: optional, Text.  
Located in: Body.  
Target environment unique identifier.

_Outputs_

Deployment : Type: [Deployment](lifetime-deployment-api-v1.md#Structure_Deployment%3E).  
Located in: Body.  
A Deployment record containing the updated information.

_Return Codes_

200 : Deployment successfully updated.

400 : Invalid request.

403 : Invalid user permissions.

404 : Deployment plan not found.

**Example Request Body**

```javascript
{
  "ApplicationVersionKeys": [
    "73b2a7a6-d893-42de-bd94-90276eac8374"
  ],
  "Notes": "WebPortal 1.1 - QA to PRD Deployment",
  "SourceEnvironmentKey": "10061715-16bb-491a-86bc-595b465eaffb",
  "TargetEnvironmentKey": "55c430ee-4783-43e6-a2d4-6eecfed1d90f"
}
```

#### DELETE /deployments/{DeploymentKey}/ { \#Deployments\_Delete }

Discards a deployment, if possible. Only deployments whose state is “saved” can be deleted.

_Full URL_

`DELETE /lifetimeapi/rest/v1/deployments/{DeploymentKey}/`

_Inputs_

DeploymentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the deployment to delete.

_Return Codes_

204 : Deployment successfully deleted. In the Java stack, code 200 is returned instead of 204.

400 : Deployment with key `<DeploymentKey>` cannot be deleted.

403 : Could not access the deployment with key `<DeploymentKey>`. The user does not have the required permissions.

404 : Deployment with key `<DeploymentKey>` not found.

#### POST /deployments/{DeploymentKey}/{Command}/ { \#Deployments\_ExecuteCommand }

Executes the given command in a specified deployment. The allowed commands are "start", "continue" and "abort".

_Full URL_

`POST /lifetimeapi/rest/v1/deployments/{DeploymentKey}/{Command}/`

_Inputs_

DeploymentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the deployment where the command will be executed.

Command : Type: mandatory, Text.  
Located in: URL.  
The command to execute. One of “start”, “continue” or “abort”.

_Return Codes_

202 : Command `<Command>` executed successfully for deployment `<DeploymentKey>`.

400 : Command `<Command>` can't be executed for deployment `<DeploymentKey>`.

403 : User doesn't have permissions to access the deployment with key `<DeploymentKey>`.

404 : Deployment with key `<DeploymentKey>` not found, or command not found.

#### GET /deployments/{DeploymentKey}/status/ { \#Deployments\_GetStatus }

Returns the details of a given deployment execution, including the deployment status and messages.

_Full URL_

`GET /lifetimeapi/rest/v1/deployments/{DeploymentKey}/status/`

_Inputs_

DeploymentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the deployment whose status is being requested.

_Outputs_

DeploymentLog : Type: [DeploymentMessage](lifetime-deployment-api-v1.md#Structure_DeploymentMessage%3E) List.  
Located in: Body.  
List of deployment messages.

DeploymentStatus : Type: Text.  
Located in: Body.  
Status of the deployment. \[saved \| running \| needs\_user\_intervention \| aborted \| aborting \| finished\_successful \| finished\_with\_warnings \| finished\_with\_errors\]

_Return Codes_

200 : Deployment status successfully retrieved.

403 : User doesn't have permissions to the deployment with key `<DeploymentKey>`.

404 : Deployment with key `<DeploymentKey>` not found.

### /environments

#### GET /environments/ { \#Environments\_List }

Lists all the environments in the infrastructure.

_Full URL_

`GET /lifetimeapi/rest/v1/environments/`

_Outputs_

Environments : Type: [Environment](lifetime-deployment-api-v1.md#Structure_Environment%3E) List.  
Located in: Body.  
A list of Environment records.

_Return Codes_

200 : Environments list successfully retrieved.

204 : No environments found. In the Java stack, code 200 is returned instead of 204.

#### GET /environments/{EnvironmentKey}/ { \#Environments\_Get }

Returns the details of a given environment.

_Full URL_

`GET /lifetimeapi/rest/v1/environments/{EnvironmentKey}/`

_Inputs_

EnvironmentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the desired environment.

_Outputs_

Environment : Type: [Environment](lifetime-deployment-api-v1.md#Structure_Environment%3E).  
Located in: Body.  
An Environment record.

_Return Codes_

200 : Environment details successfully retrieved.

403 : Failed to retrieve the environment with key: `<EnvironmentKey>`. The user does not have the required permissions.

404 : An environment with key `<EnvironmentKey>` was not found.

#### GET /environments/{EnvironmentKey}/applications/ { \#Environments\_GetRunningApps }

Returns information about the running versions of all applications in a given environment.

_Full URL_

`GET /lifetimeapi/rest/v1/environments/{EnvironmentKey}/applications/`

_Inputs_

EnvironmentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the environment whose list of running applications is being requested.

IncludeModules : Type: optional, Boolean.  
Located in: URL.  
When set to true, the modules details are also retrieved. The default value is false.

IncludeEnvStatus : Type: optional, Boolean.  
Located in: URL.  
When set to true, the applications’ status information in the environment is included in the result. The default value is false.

_Outputs_

Applications : Type: [Application](lifetime-deployment-api-v1.md#Structure_Application%3E) List.  
Located in: Body.  
A list of Application records.

_Return Codes_

200 : Applications list for the given environment successfully retrieved

204 : No applications found in environment with key `<EnvironmentKey>`. In the Java stack, code 200 is returned instead of 204. 400 : Failed to retrieve applications published in environment because IncludeModules and IncludeEnvStatus parameters were incorrect, or invalid request when getting running applications for environment with key `<EnvironmentKey>`.

403 : Failed to retrieve the running applications for environment with key `<EnvironmentKey>` because user has insufficient permissions.

404 : Failed to retrieve running applications for environment with key `<EnvironmentKey>` because it was not found.

#### GET /environments/{EnvironmentKey}/applications/{ApplicationKey}/ { \#Environments\_GetRunningApp }

Returns information about the running version of the specified application in a given environment.

_Full URL_

`GET /lifetimeapi/rest/v1/environments/{EnvironmentKey}/applications/{ApplicationKey}/`

_Inputs_

EnvironmentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the environment from which to get the running application details.

ApplicationKey : Type: mandatory, Text.  
Located in: URL.  
The key of the application whose details are being requested.

IncludeEnvStatus : Type: optional, Boolean.  
Located in: URL.  
When set to true, the applications’ status information in the environment is included in the result. The default value is false.

IncludeModules : Type: optional, Boolean.  
Located in: URL.  
When set to true, the modules details are also retrieved. The default value is false.

_Outputs_

Application : Type: [Application](lifetime-deployment-api-v1.md#Structure_Application%3E).  
Located in: Body.  
An Application record.

_Return Codes_

200 : Application information successfully retrieved.

400 : Request asked for Modules but not for Status.

403 : User doesn’t have permissions for the given keys \(EnvironmentKey:`<EnvironmentKey>`; Application:`<ApplicationKey>`\).

404 : Failed to retrieve the environment with key `<EnvironmentKey>` or the application with key `<ApplicationKey>`.

#### GET /environments/{EnvironmentKey}/applications/{ApplicationKey}/content/ { \#Environments\_DownloadRunningApp }

Returns a link where the binary file for a given application can be downloaded. The link will expire in 60 minutes.

_Full URL_

`GET /lifetimeapi/rest/v1/environments/{EnvironmentKey}/applications/{ApplicationKey}/content/`

_Inputs_

EnvironmentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the environment from which to get the application binary file link.

ApplicationKey : Type: mandatory, Text.  
Located in: URL.  
The key of the application for which to get the binary file link.

Type : Type: optional, Text.  
Located in: URL.  
The type of binary file to return, when applicable. \[oap \| apk \| ipa\]

_Outputs_

DownloadLink : Type: [DownloadLink](lifetime-deployment-api-v1.md#Structure_DownloadLink%3E).  
Located in: Body.  
The link for the application binary file.

Expires : Type: Date Time.  
Located in: Header.  
The expiration date and time of the returned link.

_Return Codes_

200 : Binary file download link successfully retrieved.

204 : No binary available for given type and keys. In the Java stack, code 200 is returned instead of 204.

400 : The required type `<Type>` is invalid for the given keys \(EnvironmentKey:`<EnvironmentKey>`; Application:`<ApplicationKey>`\).

403 : User doesn’t have permissions for the given keys \(EnvironmentKey:`<EnvironmentKey>`; Application:`<ApplicationKey>`\).

404 : Failed to retrieve the environment with key `<EnvironmentKey>` or the application with key `<ApplicationKey>`.

#### POST /environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/ { \#Environments\_Applications\_Versions\_Create }

Creates a new version of the application based on the current running application.

_Full URL_

`POST /lifetimeapi/rest/v1/environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/`

_Inputs_

EnvironmentKey : Type: mandatory, Text.  
Located in: URL.  
The key of the environment from which to get the application.

ApplicationKey : Type: mandatory, Text.  
Located in: URL.  
The key of the application for which to generate a new version.

ApplicationVersionCreate : Type: mandatory, [ApplicationVersionCreate](lifetime-deployment-api-v1.md#Structure_ApplicationVersionCreate%3E).  
Located in: Body.  
A structure holding the new version name for the application and for its native applications, if applicable.

_Outputs_

ApplicationVersionKey : Type: Text.  
Located in: Body.  
The key of the newly created application version.

_Return Codes_

201 : Application version successfully created.

400 : Invalid request.

403 : Invalid user permissions.

404 : Environment or application not found.

**Example Request Body**

```javascript
{
  "ChangeLog": "First release of iOS mobile app",
  "Version": "1.0.0",
  "MobileVersions": [
    {
      "NativePlatform": "iOS",
      "VersionNumber": "1.0.0",
      "VersionDescription": "First release"
    }
  ],
  "ModuleVersionKeys": [
    "63146a06-06d3-4f9e-a4ca-abc7bb6950e5"
  ]
}
```

### /modules

#### GET /modules/ { \#Modules\_List }

Returns a list of modules that exist in the infrastructure.

_Full URL_

`GET /lifetimeapi/rest/v1/modules/`

_Inputs_

IncludeEnvStatus : Type: optional, Boolean.  
Located in: URL.  
When set to true, the module status per environment is also returned. The default value is false.

_Outputs_

ModuleList : Type: [Module](lifetime-deployment-api-v1.md#Structure_Module%3E) List.  
Located in: Body.  
List of Module records.

_Return Codes_

200 : Modules list successfully retrieved.

204 : No modules found in the infrastructure. In the Java stack, code 200 is returned instead of 204.

#### GET /modules/{ModuleKey}/ { \#Modules\_Get }

Returns the details of a given module.

_Full URL_

`GET /lifetimeapi/rest/v1/modules/{ModuleKey}/`

_Inputs_

ModuleKey : Type: mandatory, Text.  
Located in: URL.  
Key of the module to list the details from.

IncludeEnvStatus : Type: optional, Boolean.  
Located in: URL.  
When set to true, the module status per environment is also returned. The default value is false.

_Outputs_

Module : Type: [Module](lifetime-deployment-api-v1.md#Structure_Module%3E).  
Located in: Body.  
Module record.

_Return Codes_

200 : Module details successfully retrieved.

403 : Failed to retrieve the module with key: `<ModuleKey>`. The user does not have the required permissions.

404 : Failed to retrieve the module with key: `<ModuleKey>`.

#### GET /modules/{ModuleKey}/versions/ { \#ModuleVersions\_List }

Returns a list of versions of a given module.

_Full URL_

`GET /lifetimeapi/rest/v1/modules/{ModuleKey}/versions/`

_Inputs_

ModuleKey : Type: mandatory, Text.  
Located in: URL.  
The module from where to retrieve the versions from.

IncludePublicElements : Type: optional, Boolean.  
Located in: URL.  
Boolean to indicate if public elements should be returned. Default is false.

IncludeConsumedElements : Type: optional, Boolean.  
Located in: URL.  
Boolean to indicate if consumed elements should be returned. Default is false.

MaximumVersionsToReturn : Type: optional, Integer.  
Located in: URL.  
Maximum number of versions to return. Default is 5.

_Outputs_

ModuleVersionList : Type: [ModuleVersion](lifetime-deployment-api-v1.md#Structure_ModuleVersion%3E) List.  
Located in: Body.  
List of ModuleVersion records.

_Return Codes_

200 : List of module versions successfully retrieved.

400 : Invalid request due to invalid max versions to return \(less than 0\).

403 : Failed to retrieve the module with key: `<ModuleKey>`. The user does not have the required permissions.

404 : Failed to retrieve the module with key: `<ModuleKey>`.

#### GET /modules/{ModuleKey}/versions/{ModuleVersionKey}/ { \#ModuleVersion\_Get }

Returns the details of a given module version.

_Full URL_

`GET /lifetimeapi/rest/v1/modules/{ModuleKey}/versions/{ModuleVersionKey}/`

_Inputs_

ModuleKey : Type: mandatory, Text.  
Located in: URL.  
The module from where to retrieve the versions from.

ModuleVersionKey : Type: mandatory, Text.  
Located in: URL.  
Key of the module version to return.

IncludePublicElements : Type: optional, Boolean.  
Located in: URL.  
Boolean to indicate if public elements should be returned. Default is false.

IncludeConsumedElements : Type: optional, Boolean.  
Located in: URL.  
Boolean to indicate if consumed elements should be returned. Default is false.

_Outputs_

ModuleVersion : Type: [ModuleVersion](lifetime-deployment-api-v1.md#Structure_ModuleVersion%3E)  
Located in: Body.  
Record of ModuleVersion.

_Return Codes_

200 : Module version details successfully retrieved.

403 : Failed to retrieve the module with key: `<ModuleKey>`. The user does not have the required permissions.

404 : Failed to retrieve the module with key: `<ModuleKey>`, or failed to retrieve the module version with key: `<ModuleKey>`.

### Structures

#### Application { \#Structure\_Application }

An application with its details and its status in the environments were it is running.

_Attributes_

Key : Type: Text.  
Application unique identifier.

Name : Type: Text \(50\).  
Name of the application.

Kind : Type: RuntimeKind Identifier.  
Identifies the kind of application. \[Mobile \| WebResponsive\]

Team : Type: Text \(50\).  
The team that owns the application.

Description : Type: Text \(50\).  
Description of the application.

URLPath : Type: Text \(50\).  
Relative URL path of the application, starting from the hostname.

IconHash : Type: Text \(50\).  
Hash of the application icon. Can be used to detect changes in the application icon.

IconURL : Type: Text \(50\).  
The URL for the application icon.

IsSystem : Type: Boolean.  
Indicates if the application is a built-in component of the OutSystems platform \(e.g. Service Center, LifeTime, ...\).

AppStatusInEnvs : Type: [AppStatusInEnv](lifetime-deployment-api-v1.md#Structure_AppStatusInEnv%3E) List.  
Information about the status of the application in each environment it is running.

#### ApplicationConflict { \#Structure\_ApplicationConflict }

A deployment conflict.

_Attributes_

Message : Type: Text.  
Description of the conflict.

ProducerApplicationOperation : Type: [ApplicationOperation](lifetime-deployment-api-v1.md#Structure_ApplicationOperation%3E).  
Operation executed over producer application.

ConsumerApplicationOperation : Type: [ApplicationOperation](lifetime-deployment-api-v1.md#Structure_ApplicationOperation%3E).  
Operation executed over consumed application.

ModuleConflict : Type: [ModuleConflict](lifetime-deployment-api-v1.md#Structure_ModuleConflict%3E).  
Details of the module conflict.

#### ApplicationOperation { \#Structure\_ApplicationOperation }

Operation executed in the deployment over the application.

_Attributes_

ApplicationKey : Type: Text.  
Application unique identifier.

ApplicationVersionKey : Type: Text.  
Application Version unique identifier.

DeploymentOperation : Type: Text.  
Label of the operation to be performed. Example: Deploy 1.5.

#### ApplicationVersion { \#Structure\_ApplicationVersion }

Information about a specific version of an application and the versions of its modules.

_Attributes_

Key : Type: Text.  
Application version unique identifier.

ApplicationKey : Type: Text.  
Application unique identifier.

Version : Type: Text \(50\).  
Version of the application.

MobileVersions : Type: [MobileVersion](lifetime-deployment-api-v1.md#Structure_MobileVersion%3E) List.  
List of mobile versions.

PrimaryColor : Type: Text \(50\).  
The primary color of the application interface.

NativeHash : Type: Text \(50\).  
The native hash relative to the mobile platform.

ModuleVersions : Type: [ModuleVersion](lifetime-deployment-api-v1.md#Structure_ModuleVersion%3E) List.  
List of module versions.

#### ApplicationVersionCreate { \#Structure\_ApplicationVersionCreate }

A structure holding the new version name for the application and for its native applications, if applicable.

_Attributes_

ChangeLog : Type: Text.  
Change log of the version to be created.

Version : Type: Text \(50\).  
Version of the application.

MobileVersions : Type: [MobileVersion](lifetime-deployment-api-v1.md#Structure_MobileVersion%3E) List.  
List of mobile versions.

ModuleVersionKeys : Type: Text List.  
List of module version keys to validate if the current state of the application is still the expected one.

#### AppStatusInEnv { \#Structure\_AppStatusInEnv }

Status of application in a given environment.

_Attributes_

EnvironmentKey : Type: Text.  
Environment unique identifier.

BaseApplicationVersionKey : Type: Text.  
Base application version unique identifier. If app is not modified in environment, this is the application version deployed.

IsModified : Type: Boolean.  
True if the application has been changed since the last tag, false otherwise.

IsModifiedReason : Type: Text.  
Indicates the application status.

IsModifiedMessage : Type: Text.  
Indicates the application status.

ConsistencyStatus : Type: Text \(50\).  
Indicates the application consistency status.

ConsistencyStatusMessages : Type: Text \(2000\).  
Messages regarding the consistency status of the application.

MobileAppsStatus : Type: [MobileAppStatusInEnv](lifetime-deployment-api-v1.md#Structure_MobileAppStatusInEnv%3E) List.  
Status of mobile apps in environment.

ModuleStatusInEnvs : Type: [ModuleStatusInEnv](lifetime-deployment-api-v1.md#Structure_ModuleStatusInEnv%3E) List.  
Status of modules in environment.

#### Deployment { \#Structure\_Deployment }

Deployment information with the operations executed.

_Attributes_

Key : Type: Text.  
Deployment unique identifier.

SourceEnvironmentKey : Type: Text.  
Source environment unique identifier.

TargetEnvironmentKey : Type: Text.  
Target environment unique identifier.

Notes : Type: Text.  
Deployment notes.

CreatedOn : Type: Date Time.  
Date and time when the deployment plan was created.

CreatedBy : Type: Text.  
Name of the user who created the deployment plan.

CreatedByUsername : Type: Text.  
Username of the user who created the deployment plan.

SavedOn : Type: Date Time.  
The date and time when the deployment plan was saved.

SavedBy : Type: Text.  
Name of the user who last saved the deployment plan.

SavedByUsername : Type: Text.  
Username of the user who last saved the deployment plan.

StartedOn : Type: Date Time.  
The date and time when the deployment started.

StartedBy : Type: Text.  
Name of the user who started the deployment.

StartedByUsername : Type: Text.  
Username of the user who started the deployment.

AbortedOn : Type: Date Time.  
The date and time when the deployment was aborted.

AbortedBy : Type: Text.  
Name of the user who aborted the deployment.

AbortedByUsername : Type: Text.  
Username of the user who aborted the deployment.

ApplicationsVersionKeys : Type: Text List.  
List of Application Versions included in the deployment.

#### DeploymentMessage { \#Structure\_DeploymentMessage }

Message from a deployment operation log.

_Attributes_

Instant : Type: Date Time.  
Date and time when the message was logged.

Message : Type: Text.  
Details of the message.

#### DownloadLink { \#Structure\_DownloadLink }

The link for the application binary file.

_Attributes_

url : Type: Text.  
The link for the application binary file.

expires : Type: Date Time.  
The expiration date and time of the returned link.

#### Environment { \#Structure\_Environment }

An environment and its information.

_Attributes_

Key : Type: Text.  
Unique identifier of the environment.

Name : Type: Text \(50\).  
Name of the environment.

OSVersion : Type: Text \(50\).  
Platform Server version. \[X.X.X.X\]

Order : Type: Integer.  
The order of the environment as registered in Lifetime.

HostName : Type: Text \(50\).  
Hostname of the environment as registered.

UseHTTPS : Type: Boolean.  
Indicates if connections to the environment are made using HTTPS.

EnvironmentType : Type: Text.  
Indicates the type of the environment. \[Development \| Test \| Production\]

NumberOfFrontEnds : Type: Integer.  
Number of front-end servers in the environment.

ApplicationServerType : Type: Text \(50\).  
Stack of the application server. \[.NET \| JAVA\]

ApplicationServer : Type: Text \(50\).  
Application server in use. \[IIS \| JBoss \| WebLogic\]

DatabaseProvider : Type: Text \(50\).  
Type of database provider. \[SqlServer \| Oracle\]

IsCloudEnvironment : Type: Boolean.  
Indicates if the environment is running on a cloud service.

#### MobileAppStatusInEnv { \#Structure\_MobileAppStatusInEnv }

Status of mobile application in a given environment.

_Attributes_

EnvironmentKey : Type: Text.  
Environment unique identifier.

NativePlatform : Type: Text.  
Name of native platform. \[Android \| iOS\]

VersionNumber : Type: Text.  
The version number, like for example 1.5.4, of the native build. It is used to be able to map the version to the version in the Android or iOS store.

HasBinaryAvailable : Type: Boolean.  
True if the binary of the application is available for the current configuration.

IsConfigured : Type: Boolean.  
True if the application is configured.

IsConfigurationChanged : Type: Boolean.  
True if the configuration of the Mobile Application has changed in the environment.

IsModified : Type: Boolean.  
True if the Native Hash of the Mobile Application does not match the one in the AppVersionNativeBuild baseline.

#### MobileVersion { \#Structure\_MobileVersion }

A mobile version and its information.

_Attributes_

NativePlatform : Type: Text.  
Name of native platform. \[Android \| iOS\]

VersionNumber : Type: Text \(50\).  
The version number, like for example 1.5.4, of the native build. It is used to be able to map the version to the version in the Android or iOS store.

VersionDescription : Type: Text.  
The description of the mobile version.

#### Module { \#Structure\_Module }

Module information and the status in the environments where the modules are running.

_Attributes_

Key : Type: Text.  
Module unique identifier.

Name : Type: Text \(50\).  
Name of the module.

Description : Type: Text \(50\).  
Description of the module.

Kind : Type: Text \(50\).  
Module type \(eSpace or Extension\).

ModuleStatusInEnv : Type: [ModuleStatusInEnv](lifetime-deployment-api-v1.md#Structure_ModuleStatusInEnv%3E) List.  
Status of the module in environments.

#### ModuleConflict { \#Structure\_ModuleConflict }

A module conflict.

_Attributes_

ProducerModuleKey : Type: Text.  
Producer Module unique identifier.

ConsumerModuleKey : Type: Text.  
Consumer Module unique identifier.

TotalRequiredElements : Type: Integer.  
Total number of required elements.

ConflictType : Type: Text.  
Type of conflict. \[Producer Module Missing \| Producer Element Missing \| Producer Element Incompatible \| Consumer Module Outdated \| Newer Producer Module Available \| IncompatiblePlatformServer \| ConsumerModuleMoved \| ProducerModuleMoved \| NameColision\]

#### ModuleElement { \#Structure\_ModuleElement }

Element version information, such as action, entity, structure, among others.

_Attributes_

Key : Type: Text.  
Module element unique identifier.

Name : Type: Text \(50\).  
Name of the element as specified by the developer.

ElementType : Type: Text.  
Type of the element, such as action, entity, structure.

CompatibilitySignatureHash : Type: Text \(50\).  
Hash of the element signature. Can be used to validate if the element version is compatible with another version, not producing a broken reference.

FullSignatureHash : Type: Text \(50\).  
Hash of the element. Can be used to uniquely identify an element version.

ModuleKey : Type: Text.  
Unique identifier of the module where the element is publicly supplied, among others.

#### ModuleStatusInEnv { \#Structure\_ModuleStatusInEnv }

Status of module in a given environment.

_Attributes_

EnvironmentKey : Type: Text.  
Environment unique identifier.

ModuleVersionKey : Type: Text.  
Module version unique identifier.

ConsistencyStatus : Type: Text \(50\).  
Indicates the module consistency status.

ConsistencyStatusMessages : Type: Text \(2000\).  
Messages regarding the consistency status of the module.

#### ModuleVersion { \#Structure\_ModuleVersion }

A module version and its information.

_Attributes_

Key : Type: Text.  
Module version unique identifier.

ModuleKey : Type: Text.  
Module unique identifier.

PublicElements : Type: [ModuleElement](lifetime-deployment-api-v1.md#Structure_ModuleElement%3E) List.  
List of module elements exposed by module version.

ConsumedElements : Type: [ModuleElement](lifetime-deployment-api-v1.md#Structure_ModuleElement%3E) List.  
List of module elements consumed by module version.

