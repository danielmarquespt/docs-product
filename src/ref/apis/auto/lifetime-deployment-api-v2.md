---
summary: >-
  Allows you to manage applications, modules, environments and deployments of
  your OutSystems infrastructure. Version 2 of the API adds support for
  deployment zones.
tags: >-
  support-application_development; support-Application_Lifecycle;
  support-devOps; support-Integrations_Extensions
---

# lifetime-deployment-api-v2

## LifeTime Deployment API v2

### Summary

| API | Base URL | Security |
| :--- | :--- | :--- |
| [v2](lifetime-deployment-api-v2.md#v2%3E) | /lifetimeapi/rest/v2 | SSL/TLS |

### v2

| API Method | Description |
| :--- | :--- |
| [GET /applications/](lifetime-deployment-api-v2.md#Applications_List%3E) | Returns a list of applications that exist in the infrastructure. |
| [GET /applications/{ApplicationKey}/](lifetime-deployment-api-v2.md#Applications_Get%3E) | Returns the details of a given application. |
| [GET /applications/{ApplicationKey}/versions/](lifetime-deployment-api-v2.md#Applications_Versions_List%3E) | Returns a list of versions of a given application. |
| [GET /applications/{ApplicationKey}/versions/{VersionKey}/](lifetime-deployment-api-v2.md#Applications_Versions_Get%3E) | Returns the details of a given version of the specified application. |
| [DELETE /applications/{ApplicationKey}/versions/{VersionKey}/](lifetime-deployment-api-v2.md#Applications_Versions_Delete%3E) | Discards a given application version if not "InUse". |
| [GET /applications/{ApplicationKey}/versions/{VersionKey}/content/](lifetime-deployment-api-v2.md#Applications_DownloadVersion%3E) | Returns a link where the binary file for a given application version can be downloaded. The link will expire in 60 minutes. |
| [GET /deployments/](lifetime-deployment-api-v2.md#Deployments_List%3E) | Returns a list of deployments ordered by creation date, from newest to oldest. You can filter the list of results by MinDate, MaxDate and TargetEnvironmentKey. |
| [POST /deployments/](lifetime-deployment-api-v2.md#Deployments_Create%3E) | Creates a deployment to a target environment. An optional list of applications to include in the deployment can be specified. The input is a subset of deployment object. |
| [GET /deployments/{DeploymentKey}/](lifetime-deployment-api-v2.md#Deployments_Get%3E) | Returns the details of a given deployment, validating if there are any conflicts. The returned information contains the applications included in the deployment plan and the possible conflicts that can arise from the deployment of the selected applications. |
| [PUT /deployments/{DeploymentKey}/](lifetime-deployment-api-v2.md#Deployments_Update%3E) | Updates a given deployment. An optional list of applications to include in the deployment can be specified. The input is a subset of deployment object. |
| [DELETE /deployments/{DeploymentKey}/](lifetime-deployment-api-v2.md#Deployments_Delete%3E) | Discards a deployment, if possible. Only deployments whose state is “saved” can be deleted. |
| [POST /deployments/{DeploymentKey}/{Command}/](lifetime-deployment-api-v2.md#Deployments_ExecuteCommand%3E) | Executes the given command in a specified deployment. The initiation of a deployment plan will check if it's valid. The applications to redeploy, if applicable, will also be included in the deployment plan. |
| [GET /deployments/{DeploymentKey}/status/](lifetime-deployment-api-v2.md#Deployments_GetStatus%3E) | Returns the details of a given deployment execution, including the deployment status and messages. |
| [GET /environments/](lifetime-deployment-api-v2.md#Environments_List%3E) | Lists all the environments in the infrastructure. |
| [GET /environments/{EnvironmentKey}/](lifetime-deployment-api-v2.md#Environments_Get%3E) | Returns the details of a given environment. |
| [GET /environments/{EnvironmentKey}/applications/](lifetime-deployment-api-v2.md#Environments_GetRunningApps%3E) | Returns information about the running versions of all applications in a given environment. |
| [GET /environments/{EnvironmentKey}/applications/{ApplicationKey}/](lifetime-deployment-api-v2.md#Environments_GetRunningApp%3E) | Returns information about the running version of the specified application in a given environment. |
| [GET /environments/{EnvironmentKey}/applications/{ApplicationKey}/content/](lifetime-deployment-api-v2.md#Environments_DownloadRunningApp%3E) | Returns a link where the binary file for a given application can be downloaded. The link will expire in 60 minutes. |
| [POST /environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/](lifetime-deployment-api-v2.md#Environments_Applications_Versions_Create%3E) | Creates a new version of the application based on the current running application. |
| [GET /environments/{EnvironmentKey}/deploymentzones/](lifetime-deployment-api-v2.md#Environments_GetDeploymentZones%3E) | Returns information about the deployment zones available in a given environment. |
| [GET /modules/](lifetime-deployment-api-v2.md#Modules_List%3E) | Returns a list of modules that exist in the infrastructure. |
| [GET /modules/{ModuleKey}/](lifetime-deployment-api-v2.md#Modules_Get%3E) | Returns the details of a given module. |
| [GET /modules/{ModuleKey}/versions/](lifetime-deployment-api-v2.md#ModuleVersions_List%3E) | Returns a list of versions of a given module. |
| [GET /modules/{ModuleKey}/versions/{ModuleVersionKey}/](lifetime-deployment-api-v2.md#ModuleVersion_Get%3E) | Returns the details of a given module version. |

## Actions

### /applications

#### GET /applications/ { \#Applications\_List }

Returns a list of applications that exist in the infrastructure.

_Full URL_

`GET /lifetimeapi/rest/v2/applications/`

_Inputs_

IncludeModules : Type: optional, Boolean  
Located in: URL.  
When set to true, the modules are also returned. The default value is false.

IncludeEnvStatus : Type: optional, Boolean  
Located in: URL.  
When set to true, the application status per environment is also returned. The default value is false.

_Outputs_

Applications : Type: [Application](lifetime-deployment-api-v2.md#Structure_Application%3E) List  
Located in: Body.  
A list of Application records including AppStatusInEnv sub-lists, if requested.

_Return Codes_

200 : Application list successfully retrieved.

204 : No applications available in the infrastructure.

400 : Failed to retrieve applications because IncludeModules was requested but IncludeEnvStatus was not, or invalid request when listing all applications.

500 : Failed to list the applications.

#### GET /applications/{ApplicationKey}/ { \#Applications\_Get }

Returns the details of a given application.

_Full URL_

`GET /lifetimeapi/rest/v2/applications/{ApplicationKey}/`

_Inputs_

ApplicationKey : Type: mandatory, Text  
Located in: URL.  
The key of the desired application.

IncludeModules : Type: optional, Boolean  
Located in: URL.  
When set to true, the modules details are also retrieved. The default value is false.

IncludeEnvStatus : Type: optional, Boolean  
Located in: URL.  
When set to true, the application status per environment is also returned. The default value is false.

_Outputs_

Application : Type: [Application](lifetime-deployment-api-v2.md#Structure_Application%3E)  
Located in: Body.  
An Application record including an AppStatusInEnv sub-list, if requested.

_Return Codes_

200 : Application details successfully retrieved.

400 : Failed to retrieve applications because IncludeModules and IncludeEnvStatus parameters were incorrect.

403 : Failed listing all applications because user has insufficient permissions.

404 : Failed getting running applications because one of the environments was not found.

#### GET /applications/{ApplicationKey}/versions/ { \#Applications\_Versions\_List }

Returns a list of versions of a given application.

_Full URL_

`GET /lifetimeapi/rest/v2/applications/{ApplicationKey}/versions/`

_Inputs_

ApplicationKey : Type: mandatory, Text  
Located in: URL.  
The key of the desired application.

MaximumVersionsToReturn : Type: optional, Integer  
Located in: URL.  
The maximum number of versions to return. The default value is 5.

ChangeLogFilter : Type: optional, Text  
Located in: URL.  
Returns versions with change logs containing the required keyword. If left empty, all versions are returned.

_Outputs_

ApplicationVersions : Type: [ApplicationVersion](lifetime-deployment-api-v2.md#Structure_ApplicationVersion%3E) List  
Located in: Body.  
A list of ApplicationVersion records.

_Return Codes_

200 : List of application versions successfully retrieved.

400 : Invalid request due to invalid max versions to return \(less than 0\).

403 : Failed to retrieve the application with key `<ApplicationKey>`. The user does not have the required permissions.

404 : Failed to retrieve the application with key `<ApplicationKey>`.

500 : Failed to list the application versions.

#### GET /applications/{ApplicationKey}/versions/{VersionKey}/ { \#Applications\_Versions\_Get }

Returns the details of a given version of the specified application.

_Full URL_

`GET /lifetimeapi/rest/v2/applications/{ApplicationKey}/versions/{VersionKey}/`

_Inputs_

ApplicationKey : Type: mandatory, Text  
Located in: URL.  
The key of the application whose version is being requested.

IncludeModules : Type: mandatory, Boolean  
Located in: URL.  
When set to true, the modules details are also retrieved. The default value is false.

VersionKey : Type: mandatory, Text  
Located in: URL.  
The key of the desired application version.

_Outputs_

ApplicationVersions : Type: [ApplicationVersion](lifetime-deployment-api-v2.md#Structure_ApplicationVersion%3E)  
Located in: Body.  
An ApplicationVersion record.

_Return Codes_

200 : Application version details successfully retrieved.

403 : Failed to retrieve the application with key `<ApplicationKey>`. The user does not have the required permissions.

404 : Failed to retrieve the application with key `<ApplicationKey>`.

500 : Failed to retrieve the application version.

#### DELETE /applications/{ApplicationKey}/versions/{VersionKey}/ { \#Applications\_Versions\_Delete }

Discards a given application version if not "InUse".

_Full URL_

`DELETE /lifetimeapi/rest/v2/applications/{ApplicationKey}/versions/{VersionKey}/`

_Inputs_

ApplicationKey : Type: mandatory, Text  
Located in: URL.  
The key of the application whose version is to be deleted.

VersionKey : Type: mandatory, Text  
Located in: URL.  
The key of the application version to be deleted.

_Return Codes_

204 : Application version successfully deleted.

403 : Service Account doesn't have permissions to delete the specified application version.

404 : Application or application version not found.

500 : Failed to delete application version `<VersionKey>`.

#### GET /applications/{ApplicationKey}/versions/{VersionKey}/content/ { \#Applications\_DownloadVersion }

Returns a link where the binary file for a given application version can be downloaded. The link will expire in 60 minutes.

_Full URL_

`GET /lifetimeapi/rest/v2/applications/{ApplicationKey}/versions/{VersionKey}/content/`

_Inputs_

ApplicationKey : Type: mandatory, Text  
Located in: URL.  
The key of the application for which to get the binary file link.

VersionKey : Type: mandatory, Text Located in: URL.  
The key of the application version for which to get the binary file link.

_Outputs_

DownloadLink : Type: DownloadLink  
Located in: Body.  
The link for the application version binary file.

Expires : Type: Date Time Located in: Header.  
The expiration date and time of the returned link.

_Return Codes_

200 : Binary file download link successfully retrieved.

204 : No binary available for given keys.

400 : The request is invalid for the given keys \(Application:`<ApplicationKey>`; ApplicationVersionKey `<ApplicationVersionKey>`\).

403 : User doesn’t have permissions for the given keys \(Application:`<ApplicationKey>`; ApplicationVersionKey `<ApplicationVersionKey>`\).

404 : Failed to retrieve the application with key `<ApplicationKey>` or the application version with key `<ApplicationVersionKey>`.

500 : Failed to download the oap of the application version.

### /deployments

#### GET /deployments/ { \#Deployments\_List }

Returns a list of deployments ordered by creation date, from newest to oldest. You can filter the list of results by MinDate, MaxDate and TargetEnvironmentKey.

_Full URL_

`GET /lifetimeapi/rest/v2/deployments/`

_Inputs_

MinDate : Type: optional, Date  
Located in: URL.  
The minimum creation date of the deployments to return. The default value is 1 week before the current date.

MaxDate : Type: optional, Date  
Located in: URL.  
The maximum creation date of the deployments to return. The default value is the current date.

TargetEnvironmentKey  
: Type: optional, Text  
Located in: URL.  
Target environment unique identifier. If the user does not have access to the environment, the list returned will be empty. If no environment key is passed, the list will not be filtered by any target environment.

_Outputs_

Deployments : Type: [Deployment](lifetime-deployment-api-v2.md#Structure_Deployment%3E) List  
Located in: Body.  
A list of Deployment records.

_Return Codes_

200 : Deployments list successfully retrieved.

204 : There are no deployments created between `<MinDate>` and `<MaxDate>` for environment key `<TargetEnvironmentKey>`.

400 : Invalid request for list of deployments created between `<MinDate>` and `<MaxDate>` for environment key `<TargetEnvironmentKey>`.

403 : User doesn't have access to any environment.

500 : Failed to list the deployments.

#### POST /deployments/ { \#Deployments\_Create }

Creates a deployment to a target environment. An optional list of applications to include in the deployment can be specified. The input is a subset of deployment object.

_Full URL_

`POST /lifetimeapi/rest/v2/deployments/`

_Inputs_

ApplicationOperations : Type: [ApplicationOperation](lifetime-deployment-api-v2.md#Structure_ApplicationOperation%3E) List  
Located in: Body.  
List of Application Operations included in the deployment.  
You should only supply the ApplicationVersionKey and DeploymentZoneKey structure attributes of the ApplicationOperation structure. To deploy an application to the default deployment zone, provide an empty string in the DeploymentZoneKey attribute.

Notes : Type: optional, Text  
Located in: Body.  
Deployment notes.

SourceEnvironmentKey : Type: mandatory, Text  
Located in: Body.  
Source environment unique identifier.

TargetEnvironmentKey : Type: mandatory, Text  
Located in: Body.  
Target environment unique identifier.

_Outputs_

DeploymentKey : Type: Text  
Located in: Body.  
The key of the newly created deployment.

_Return Codes_

201 : Deployment successfully created.

400 : Invalid request.

403 : Invalid user permissions.

404 : Source or target environment not found.

500 : Failed to create deployment from environment `<SourceEnvironmentKey>` to environment `<TargetEnvironmentKey>`.

**Example Request Body**

```javascript
{
  "ApplicationOperations": [
    {
      "ApplicationVersionKey": "702df59d-3700-41b8-907e-a629e05a68f1",
      "DeploymentZoneKey": "d91a7e60-dea3-4150-8da2-39593a780507"
    }
  ],
  "Notes": "WebPortal 1.1 - QA to PRD Deployment",
  "SourceEnvironmentKey": "10061715-16bb-491a-86bc-595b465eaffb",
  "TargetEnvironmentKey": "55c430ee-4783-43e6-a2d4-6eecfed1d90f"
}
```

#### GET /deployments/{DeploymentKey}/ { \#Deployments\_Get }

Returns the details of a given deployment, validating if there are any conflicts. The returned information contains the applications included in the deployment plan and the possible conflicts that can arise from the deployment of the selected applications.

_Full URL_

`GET /lifetimeapi/rest/v2/deployments/{DeploymentKey}/`

_Inputs_

DeploymentKey : Type: mandatory, Text  
Located in: URL.  
The key of the desired deployment.

_Outputs_

ApplicationConflicts : Type: [ApplicationConflict](lifetime-deployment-api-v2.md#Structure_ApplicationConflict%3E) List  
Located in: Body.  
List of conflicts between applications in the deployment.

ApplicationsToRedeploy : Type: Text List  
Located in: Body.  
List of applications that will be redeployed.

Deployment : Type: [Deployment](lifetime-deployment-api-v2.md#Structure_Deployment%3E)  
Located in: Body.  
The deployment details.

_Return Codes_

200 : Deployment details successfully retrieved.

403 : User doesn't have permissions to the deployment with key `<DeploymentKey>`.

404 : Deployment with key `<DeploymentKey>` not found.

500 : Failed to access the details of deployment with key `<DeploymentKey>`.

#### PUT /deployments/{DeploymentKey}/ { \#Deployments\_Update }

Updates a given deployment. An optional list of applications to include in the deployment can be specified. The input is a subset of deployment object.

_Full URL_

`PUT /lifetimeapi/rest/v2/deployments/{DeploymentKey}/`

_Inputs_

DeploymentKey : Type: mandatory, Text  
Located in: URL.  
The key of the deployment to update.

ApplicationOperations : Type: optional, [ApplicationOperation](lifetime-deployment-api-v2.md#Structure_ApplicationOperation%3E) List.  
Located in: Body.  
List of Application Operations included in the deployment.  
You should only supply the ApplicationVersionKey and DeploymentZoneKey structure attributes of the ApplicationOperation structure. To deploy an application to the default deployment zone, provide an empty string in the DeploymentZoneKey attribute.

Notes : Type: optional, Text  
Located in: Body.  
Deployment notes.

SourceEnvironmentKey : Type: optional, Text  
Located in: Body.  
Source environment unique identifier.

TargetEnvironmentKey : Type: optional, Text  
Located in: Body.  
Target environment unique identifier.

_Outputs_

Deployment : Type: [DeploymentData](lifetime-deployment-api-v2.md#Structure_DeploymentData%3E)  
Located in: Body.  
A DeploymentData record containing the updated information.

_Return Codes_

200 : Deployment successfully updated.

400 : Invalid request.

403 : Invalid user permissions.

404 : Deployment plan not found.

500 : Failed to update deployment with key `<DeploymentKey>`.

**Example Request Body**

```javascript
{
  "ApplicationOperations": [
    {
      "ApplicationVersionKey": "702df59d-3700-41b8-907e-a629e05a68f1",
      "DeploymentZoneKey": "d91a7e60-dea3-4150-8da2-39593a780507"
    }
  ],
  "Notes": "WebPortal 1.1 - QA to PRD Deployment",
  "SourceEnvironmentKey": "10061715-16bb-491a-86bc-595b465eaffb",
  "TargetEnvironmentKey": "55c430ee-4783-43e6-a2d4-6eecfed1d90f"
}
```

#### DELETE /deployments/{DeploymentKey}/ { \#Deployments\_Delete }

Discards a deployment, if possible. Only deployments whose state is “saved” can be deleted.

_Full URL_

`DELETE /lifetimeapi/rest/v2/deployments/{DeploymentKey}/`

_Inputs_

DeploymentKey : Type: mandatory, Text  
Located in: URL.  
The key of the deployment to delete.

_Return Codes_

204 : Deployment successfully deleted.

400 : Deployment with key `<DeploymentKey>` cannot be deleted

403 : Service Account doesn't have permissions to the deployment with key `<DeploymentKey>`.

404 : Deployment with key `<DeploymentKey>` not found.

500 : Failed to delete deployment `<DeploymentKey>`.

#### POST /deployments/{DeploymentKey}/{Command}/ { \#Deployments\_ExecuteCommand }

Executes the given command in a specified deployment. The initiation of a deployment plan will check if it's valid. The applications to redeploy, if applicable, will also be included in the deployment plan.

_Full URL_

`POST /lifetimeapi/rest/v2/deployments/{DeploymentKey}/{Command}/`

_Inputs_

DeploymentKey : Type: mandatory, Text  
Located in: URL.  
The key of the deployment where the command will be executed.

Command : Type: mandatory, Text  
Located in: URL.  
The command to execute. One of “start”, “continue” or “abort”.

RedeployOutdated : Type: optional, Boolean  
Located in: URL.  
If True, outdated applications in the target environment will be redeployed.

_Return Codes_

202 : Command `<Command>` executed successfully for deployment `<DeploymentKey>`.

400 : Command `<Command>` can't be executed for deployment `<DeploymentKey>`.

403 : Service Account doesn't have permissions to the deployment with key `<DeploymentKey>`.

404 : Deployment with key `<DeploymentKey>` not found, or command not found.

500 : Failed to execute command `<Command>` for deployment with key `<DeploymentKey>`.

#### GET /deployments/{DeploymentKey}/status/ { \#Deployments\_GetStatus }

Returns the details of a given deployment execution, including the deployment status and messages.

_Full URL_

`GET /lifetimeapi/rest/v2/deployments/{DeploymentKey}/status/`

_Inputs_

DeploymentKey : Type: mandatory, Text  
Located in: URL.  
The key of the deployment whose status is being requested.

_Outputs_

DeploymentLog : Type: [DeploymentMessage](lifetime-deployment-api-v2.md#Structure_DeploymentMessage%3E) List  
Located in: Body.  
List of deployment messages.

DeploymentStatus : Type: Text  
Located in: Body.  
Status of the deployment. \[saved \| running \| needs\_user\_intervention \| aborted \| aborting \| finished\_successful \| finished\_with\_warnings \| finished\_with\_errors\]

Info : Type: Text  
Located in: Body.  
Contains more information on the kind of user intervention needed when the DeploymentStatus value is "needs\_user\_intervention". For every other status, Info will contain an empty string \(""\). \[business\_process\_impact \| deploy\_prepared \| needs\_configuration\_or\_confirmation \| deployment\_suspended\].

_Return Codes_

200 : Deployment status successfully retrieved.

403 : User doesn't have permissions to the deployment with key `<DeploymentKey>`.

404 : Deployment with key `<DeploymentKey>` not found.

500 : Failed to retrieve the status of the deployment with key `<DeploymentKey>`.

### /environments

#### GET /environments/ { \#Environments\_List }

Lists all the environments in the infrastructure.

_Full URL_

`GET /lifetimeapi/rest/v2/environments/`

_Outputs_

Environments : Type: [Environment](lifetime-deployment-api-v2.md#Structure_Environment%3E) List  
Located in: Body.  
A list of Environment records.

_Return Codes_

200 : Environments list successfully retrieved.

204 : No environments found.

500 : Failed to list the environments.

#### GET /environments/{EnvironmentKey}/ { \#Environments\_Get }

Returns the details of a given environment.

_Full URL_

`GET /lifetimeapi/rest/v2/environments/{EnvironmentKey}/`

_Inputs_

EnvironmentKey : Type: mandatory, Text  
Located in: URL.  
The key of the desired environment.

_Outputs_

Environment : Type: [Environment](lifetime-deployment-api-v2.md#Structure_Environment%3E)  
Located in: Body.  
An Environment record.

_Return Codes_

200 : Environment details successfully retrieved.

403 : Failed to retrieve the environment with key: `<EnvironmentKey>`. The user does not have the required permissions.

404 : Failed to retrieve the environment with key: `<EnvironmentKey>`.

500 : Failed to access the details of environment.

#### GET /environments/{EnvironmentKey}/applications/ { \#Environments\_GetRunningApps }

Returns information about the running versions of all applications in a given environment.

_Full URL_

`GET /lifetimeapi/rest/v2/environments/{EnvironmentKey}/applications/`

_Inputs_

EnvironmentKey : Type: mandatory, Text  
Located in: URL.  
The key of the environment whose list of running applications is being requested.

IncludeModules : Type: optional, Boolean  
Located in: URL.  
When set to true, the modules details are also retrieved. The default value is false.

IncludeEnvStatus : Type: optional, Boolean  
Located in: URL.  
When set to true, the applications’ status information in the environment is included in the result. The default value is false.

_Outputs_

Applications : Type: [Application](lifetime-deployment-api-v2.md#Structure_Application%3E) List  
Located in: Body.  
A list of Application records.

_Return Codes_

200 : Applications list for the given environment successfully retrieved

204 : No applications found in environment with key `<EnvironmentKey>`.

400 : Failed to retrieve applications published in environment because IncludeModules and IncludeEnvStatus parameters were incorrect, or Invalid request when getting running applications for environment with key `<EnvironmentKey>`.

403 : Failed to retrieve the running applications for environment with key `<EnvironmentKey>` because user has insufficient permissions.

404 : Failed to retrieve running applications for environment with key `<EnvironmentKey>` because it was not found.

#### GET /environments/{EnvironmentKey}/applications/{ApplicationKey}/ { \#Environments\_GetRunningApp }

Returns information about the running version of the specified application in a given environment.

_Full URL_

`GET /lifetimeapi/rest/v2/environments/{EnvironmentKey}/applications/{ApplicationKey}/`

_Inputs_

EnvironmentKey : Type: mandatory, Text  
Located in: URL.  
The key of the environment from which to get the running application details.

ApplicationKey : Type: mandatory, Text  
Located in: URL.  
The key of the application whose details are being requested.

IncludeEnvStatus : Type: optional, Boolean  
Located in: URL.  
When set to true, the applications’ status information in the environment is included in the result. The default value is false.

IncludeModules : Type: optional, Boolean  
Located in: URL.  
When set to true, the modules details are also retrieved. The default value is false.

_Outputs_

Application : Type: [Application](lifetime-deployment-api-v2.md#Structure_Application%3E)  
Located in: Body.  
An Application record.

_Return Codes_

200 : Application information successfully retrieved.

400 : Request asked for Modules but not for Status.

403 : User doesn’t have permissions for the given keys \(EnvironmentKey:`<EnvironmentKey>`; Application:`<ApplicationKey>`\).

404 : Failed to retrieve the environment with key `<EnvironmentKey>` or the application with key `<ApplicationKey>`.

500 : Failed to access the running version of an application.

#### GET /environments/{EnvironmentKey}/applications/{ApplicationKey}/content/ { \#Environments\_DownloadRunningApp }

Returns a link where the binary file for a given application can be downloaded. The link will expire in 60 minutes.

_Full URL_

`GET /lifetimeapi/rest/v2/environments/{EnvironmentKey}/applications/{ApplicationKey}/content/`

_Inputs_

EnvironmentKey : Type: mandatory, Text  
Located in: URL.  
The key of the environment from which to get the application binary file link.

ApplicationKey : Type: mandatory, Text  
Located in: URL.  
The key of the application for which to get the binary file link.

Type : Type: optional, Text  
Located in: URL.  
The type of binary file to return, when applicable. One of “oap”, “apk” or “ipa”.

_Outputs_

DownloadLink : Type: [DownloadLink](lifetime-deployment-api-v2.md#Structure_DownloadLink%3E)  
Located in: Body.  
The link for the application binary file.

Expires : Type: Date Time  
Located in: Header.  
The expiration date and time of the returned link.

_Return Codes_

200 : Binary file download link successfully retrieved.

204 : No binary available for given type and keys.

400 : The required type `<Type>` is invalid for given keys \(EnvironmentKey:`<EnvironmentKey>`; Application:`<ApplicationKey>`\).

403 : User doesn’t have permissions for the given keys \(EnvironmentKey:`<EnvironmentKey>`; Application:`<ApplicationKey>`\).

404 : Failed to retrieve the environment with key `<EnvironmentKey>` or the application with key `<ApplicationKey>`.

500 : Failed to download `<Type>` of an application.

#### POST /environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/ { \#Environments\_Applications\_Versions\_Create }

Creates a new version of the application based on the current running application.

_Full URL_

`POST /lifetimeapi/rest/v2/environments/{EnvironmentKey}/applications/{ApplicationKey}/versions/`

_Inputs_

EnvironmentKey : Type: mandatory, Text  
Located in: URL.  
The key of the environment from which to get the application.

ApplicationKey : Type: mandatory, Text  
Located in: URL.  
The key of the application for which to generate a new version.

ApplicationVersionCreate : Type: mandatory, [ApplicationVersionCreate](lifetime-deployment-api-v2.md#Structure_ApplicationVersionCreate%3E)  
Located in: Body.  
A structure holding the new version name for the application and for its native applications, if applicable.

_Outputs_

ApplicationVersionKey : Type: Text  
Located in: Body.  
The key of the newly created application version.

_Return Codes_

201 : Application version successfully created.

400 : Invalid request.

403 : Invalid user permissions.

404 : Environment or application not found.

500 : Failed to tag an application, or Failed to create a new version for application `<ApplicationName>`.

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
  ]
}
```

#### GET /environments/{EnvironmentKey}/deploymentzones/ { \#Environments\_GetDeploymentZones }

Returns information about the deployment zones available in a given environment.

_Full URL_

`GET /lifetimeapi/rest/v2/environments/{EnvironmentKey}/deploymentzones/`

_Inputs_

EnvironmentKey : Type: mandatory, Text  
Located in: URL.  
The key of the environment from which to get the running application details.

_Outputs_

DeploymentZones : Type: [DeploymentZone](lifetime-deployment-api-v2.md#Structure_DeploymentZone%3E) List  
Located in: Body.  
A list of Deployment Zones.

_Return Codes_

200 : Deployment zone information successfully retrieved.

400 : Failed to access the deployment zones of environment.

403 : Failed to retrieve the deployment zones of environment `<EnvironmentName>` \(key: `<EnvironmentKey>`\). Error: The user does not have the required permissions, or Feature not Licensed.

404 : Failed to retrieve the deployment zones of environment with key: `<EnvironmentKey>`.

500 : Failed to access the deployment zones of environment.

### /modules

#### GET /modules/ { \#Modules\_List }

Returns a list of modules that exist in the infrastructure.

_Full URL_

`GET /lifetimeapi/rest/v2/modules/`

_Inputs_

IncludeEnvStatus : Type: optional, Boolean  
Located in: URL.  
When set to true, the module status per environment is also returned. The default value is false.

_Outputs_

ModuleList : Type: [Module](lifetime-deployment-api-v2.md#Structure_Module%3E) List  
Located in: Body.  
List of Module records.

_Return Codes_

200 : Modules list successfully retrieved.

204 : No modules found in the infrastructure.

500 : Failed to list modules.

#### GET /modules/{ModuleKey}/ { \#Modules\_Get }

Returns the details of a given module.

_Full URL_

`GET /lifetimeapi/rest/v2/modules/{ModuleKey}/`

_Inputs_

ModuleKey : Type: mandatory, Text  
Located in: URL.  
Key of the module to list the details from.

IncludeEnvStatus : Type: optional, Boolean  
Located in: URL.  
Boolean to indicate if status per env should be returned. Default is false.

_Outputs_

Module : Type: [Module](lifetime-deployment-api-v2.md#Structure_Module%3E)  
Located in: Body.  
Module record.

_Return Codes_

200 : Module details successfully retrieved.

403 : Failed to retrieve the module with key: `<ModuleKey>`. The user does not have the required permissions.

404 : Failed to retrieve the module with key: `<ModuleKey>`.

500 : Failed to retrieve the module with key `<ModuleKey>`.

#### GET /modules/{ModuleKey}/versions/ { \#ModuleVersions\_List }

Returns a list of versions of a given module.

_Full URL_

`GET /lifetimeapi/rest/v2/modules/{ModuleKey}/versions/`

_Inputs_

ModuleKey : Type: mandatory, Text  
Located in: URL.  
The module from where to retrieve the versions from.

MaximumVersionsToReturn : Type: optional, Integer  
Located in: URL.  
Maximum number of versions to return. Default is 5.

_Outputs_

ModuleVersionList : Type: [ModuleVersion](lifetime-deployment-api-v2.md#Structure_ModuleVersion%3E) List  
Located in: Body.  
List of ModuleVersion records.

_Return Codes_

200 : List of module versions successfully retrieved.

400 : Invalid request due to invalid max versions to return \(less than 0\).

403 : Failed to retrieve the module with key: `<ModuleKey>`. The user does not have the required permissions.

404 : Failed to retrieve the module with key: `<ModuleKey>`.

500 : Failed to list module versions.

#### GET /modules/{ModuleKey}/versions/{ModuleVersionKey}/ { \#ModuleVersion\_Get }

Returns the details of a given module version.

_Full URL_

`GET /lifetimeapi/rest/v2/modules/{ModuleKey}/versions/{ModuleVersionKey}/`

_Inputs_

ModuleKey : Type: mandatory, Text  
Located in: URL.  
The module from where to retrieve the versions from.

ModuleVersionKey : Type: mandatory, Text  
Located in: URL.  
Key of the module version to return.

_Outputs_

ModuleVersion : Type: [ModuleVersion](lifetime-deployment-api-v2.md#Structure_ModuleVersion%3E)  
Located in: Body.  
Record of ModuleVersion.

_Return Codes_

200 : Module version details successfully retrieved.

403 : Failed to retrieve the module with key: `<ModuleKey>`. The user does not have the required permissions.

404 : Failed to retrieve the module with key: `<ModuleKey>`, or Failed to retrieve the module version with key: `<ModuleKey>`.

500 : Failed to access the details of a module version.

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
Indicates if the application is a built-in component of the OutSystems platform \(e.g. ServiceCenter, LifeTime, ...\).

AppStatusInEnvs : Type: [AppStatusInEnv](lifetime-deployment-api-v2.md#Structure_AppStatusInEnv%3E) List.  
Information about the status of the application in each environment it is running.

#### ApplicationConflict { \#Structure\_ApplicationConflict }

A deployment conflict.

_Attributes_

Message : Type: Text.  
Description of the conflict.

ProducerApplicationOperation : Type: [ApplicationOperation](lifetime-deployment-api-v2.md#Structure_ApplicationOperation%3E).  
Operation executed over producer application.

ConsumerApplicationOperation : Type: [ApplicationOperation](lifetime-deployment-api-v2.md#Structure_ApplicationOperation%3E).  
Operation executed over consumed application.

ModuleConflict : Type: [ModuleConflict](lifetime-deployment-api-v2.md#Structure_ModuleConflict%3E).  
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

DeploymentZoneKey : Type: Text.  
Deployment Zone unique identifier.

#### ApplicationVersion { \#Structure\_ApplicationVersion }

Information about a specific version of an application and the versions of its modules.

_Attributes_

Key : Type: Text.  
Application version unique identifier.

ApplicationKey : Type: Text.  
Application unique identifier.

Version : Type: Text \(50\).  
Version of the application.

ChangeLog : Type: Text.  
ChangeLog of the Application Version. It is the log message created by the user for that Application Version.

CreatedOn : Type: Date Time.  
When was the Application Version created.

InUse : Type: Boolean.  
Defines if the Application Version is being used, i.e. a running version or a version in a Deployment.

MobileVersions : Type: [MobileVersion](lifetime-deployment-api-v2.md#Structure_MobileVersion%3E) List.  
List of mobile versions.

PrimaryColor : Type: Text \(50\).  
The primary color of the application interface.

NativeHash : Type: Text \(50\).  
The native hash relative to the mobile platform.

ModuleVersions : Type: [ModuleVersion](lifetime-deployment-api-v2.md#Structure_ModuleVersion%3E) List.  
List of module versions.

#### ApplicationVersionCreate { \#Structure\_ApplicationVersionCreate }

A structure holding the new version name for the application and for its native applications, if applicable.

_Attributes_

ChangeLog : Type: Text.  
Change log of the version to be created.

Version : Type: Text \(50\).  
Version of the application.

MobileVersions : Type: [MobileVersion](lifetime-deployment-api-v2.md#Structure_MobileVersion%3E) List.  
List of mobile versions.

ModuleVersionKeys : Type: optional, Text List.  
\(DEPRECATED\) List of module version keys to validate if the current state of the application is still the expected one. If you provide module version keys, they will still be validated.

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

MobileAppsStatus : Type: [MobileAppStatusInEnv](lifetime-deployment-api-v2.md#Structure_MobileAppStatusInEnv%3E) List.  
Status of mobile apps in environment.

ModuleStatusInEnvs : Type: [ModuleStatusInEnv](lifetime-deployment-api-v2.md#Structure_ModuleStatusInEnv%3E) List.  
Status of modules in environment.

DeploymentZoneKey : Type: Text.  
Deployment Zone unique identifier

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

ApplicationOperations : Type: [ApplicationOperation](lifetime-deployment-api-v2.md#Structure_ApplicationOperation%3E) List.  
List of Application Operations included in the deployment.

#### DeploymentData { \#Structure\_DeploymentData }

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

ApplicationOperations : Type: [ApplicationOperation](lifetime-deployment-api-v2.md#Structure_ApplicationOperation%3E) List.  
List of Application Operations included in the deployment.  
Note: Only the ApplicationVersionKey and DeploymentZoneKey attributes are used.

#### DeploymentMessage { \#Structure\_DeploymentMessage }

Message from a deployment operation log.

_Attributes_

Instant : Type: Date Time.  
Date and time when the message was logged.

Message : Type: Text.  
Details of the message.

#### DeploymentTechnology { \#Structure\_DeploymentTechnology }

Deployment Hosting technology of the Deployment Zone.

_Attributes_

Key : Type: Text.  
Deployment Technology unique identifier.

Name : Type: Text.  
Name of deployment technology

#### DeploymentZone { \#Structure\_DeploymentZone }

Deployment Zone of an environment.

_Attributes_

Key : Type: Text.  
Deployment Zone unique identifier.

Name : Type: Text.  
Name of deployment zone

IsDefault : Type: Boolean.  
True if the deployment zone is the default one in the environment

DeploymentTechnology : Type: [DeploymentTechnology](lifetime-deployment-api-v2.md#Structure_DeploymentTechnology%3E).  
The deployment techonology of the current deployment zone.

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

ModuleStatusInEnv : Type: [ModuleStatusInEnv](lifetime-deployment-api-v2.md#Structure_ModuleStatusInEnv%3E) List.  
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

ApplicationKey : Type: Text.  
Application unique identifier.

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

CreatedOn : Type: Date Time.  
Date and time of the module version creation.

CreatedBy : Type: Text \(50\).  
Name of the user that created the version.

CreatedByUsername : Type: Text \(50\).  
Username of the user that created the version.

GeneralHash : Type: Text \(100\).  
Non-unique hash of the module version. Can be used to validate if two module versions have semantic differences.

DirectUpgradeFromHash : Type: Text \(100\).  
If this module version is the result of a direct upgrade of another version, then this field contains the key of that version

