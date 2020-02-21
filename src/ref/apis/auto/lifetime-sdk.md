# LifeTime SDK

For version 10.0.902.100. Core layout components and APIs used by LifeTime and its plugins.

## Summary

| Widget | Description |
| :--- | :--- |
| [Internal\_Layout\_LifeTime](lifetime-sdk.md#Internal_Layout_LifeTime%3E) | The LifeTime layout. |
| [Internal\_Layout\_Popup](lifetime-sdk.md#Internal_Layout_Popup%3E) | The Popup Layout to be used in a LifeTime plugin. Pressing the popup buttons triggers the OnNotify action containing a LayoutPopupButtonClicked identifier. |
| [Layout\_LifeTimeSDK](lifetime-sdk.md#Layout_LifeTimeSDK%3E) | The Web Block to be used as the base layout for a LifeTime plugin. The layout allows you to easily create screens with the look and feel of LifeTime, since it contains LifeTime header and footer.%%%%The layout also contains a stamp for you to customize with the developer or company name, when you register the plugin. |

| Action | Description |
| :--- | :--- |
| [Application\_Get](lifetime-sdk.md#Application_Get%3E) | Returns the information of an application in an environment.%%If the environment is not specified, information of the application across all infrastructure is returned. |
| [Application\_List](lifetime-sdk.md#Application_List%3E) | Returns a list of the applications in the specified environment that are visible within LifeTime, with their information, such as name, description, url. If no environment is specified, information of all visible applications across all environments is returned. |
| [ApplicationVersion\_Get](lifetime-sdk.md#ApplicationVersion_Get%3E) | Returns information of an application on a specified date. |
| [ApplicationVersion\_List](lifetime-sdk.md#ApplicationVersion_List%3E) | Returns the information of all tagged application versions for the specified application. |
| [Deployment\_Get](lifetime-sdk.md#Deployment_Get%3E) | Returns information of the specified deployment. |
| [Deployment\_List](lifetime-sdk.md#Deployment_List%3E) | Returns information of all deployments made between two environments. |
| [Environment\_Get](lifetime-sdk.md#Environment_Get%3E) | Returns the information of an environment, such as name, version of the Platform, Application Server. |
| [Environment\_List](lifetime-sdk.md#Environment_List%3E) | Returns a list of environments with their information, such as name, version of the Platform, Application Server. |
| [GetUserSessionToken](lifetime-sdk.md#GetUserSessionToken%3E) | Returns an authentication token that is valid for 5 minutes, for the session user. |
| [ModuleVersion\_Get](lifetime-sdk.md#ModuleVersion_Get%3E) | Returns the information of a module version for the specified module and version. |
| [ModuleVersion\_List](lifetime-sdk.md#ModuleVersion_List%3E) | Returns the information of all module versions for the specified module. |
| [Plugin\_Register](lifetime-sdk.md#Plugin_Register%3E) | Registers the caller eSpace as a LifeTime plugin: in the LifeTime 'More' menu a new link is created with the specified name that redirects to the entry point provided, or the default entry point if none is provided. All web screens of the plugin are displayed with their owner name.%%Each eSpace can only register a single plugin.%% |
| [Plugin\_Unregister](lifetime-sdk.md#Plugin_Unregister%3E) | Unregisters the caller eSpace as a LifeTime plugin: in the LifeTime 'More' menu there is no longer a link to the plugin. |
| [Security\_CheckApplicationPermission](lifetime-sdk.md#Security_CheckApplicationPermission%3E) | Checks if a user has a permission for a specific application running on an environment.%%If no user is specified, the current user is used. |
| [Security\_CheckEnvironmentPermission](lifetime-sdk.md#Security_CheckEnvironmentPermission%3E) | Checks if a user has a permission for a specific environment. If no user is specified, the current user is used. |
| [Security\_CheckInfrastructurePermission](lifetime-sdk.md#Security_CheckInfrastructurePermission%3E) | Checks if a user has the 'Configure Infrastructure' permission. If no user is specified, the current user is used. |
| [Security\_GetApplicationsPermissions](lifetime-sdk.md#Security_GetApplicationsPermissions%3E) | Returns the permissions the specified user has for each application in the environment. If no user is specified, the current user is used. |
| [Security\_GetEnvironmentsPermissions](lifetime-sdk.md#Security_GetEnvironmentsPermissions%3E) | Returns the permissions the specified user has for each environment. If no user is specified, the current user is used. |
| [SetLoginRedirectURL](lifetime-sdk.md#SetLoginRedirectURL%3E) |  |

| Structure | Description |
| :--- | :--- |
| [ApplicationInfo](lifetime-sdk.md#Structure_ApplicationInfo%3E) | Application details and environment specific information where the application is running. |
| [ApplicationVersionInfo](lifetime-sdk.md#Structure_ApplicationVersionInfo%3E) | Information of a specific version of an application, and the versions of its modules. |
| [DeploymentInfo](lifetime-sdk.md#Structure_DeploymentInfo%3E) | Deployment information with the operations executed. |
| [DeploymentMessage](lifetime-sdk.md#Structure_DeploymentMessage%3E) | Message from a deployment operation log. |
| [DeploymentOperationInfo](lifetime-sdk.md#Structure_DeploymentOperationInfo%3E) | A deployment operation as specified in the deployment plan. |
| [EnvironmentApplicationInfo](lifetime-sdk.md#Structure_EnvironmentApplicationInfo%3E) | Application information for a specific environment. |
| [EnvironmentApplicationPermission](lifetime-sdk.md#Structure_EnvironmentApplicationPermission%3E) | A user's permission to an application in an environment. |
| [EnvironmentInfo](lifetime-sdk.md#Structure_EnvironmentInfo%3E) | An environment and its information. |
| [EnvironmentModuleInfo](lifetime-sdk.md#Structure_EnvironmentModuleInfo%3E) | Information of a module in a specific environment. |
| [EnvironmentPermission](lifetime-sdk.md#Structure_EnvironmentPermission%3E) | A user's permission to an environment. |
| [ModuleInfo](lifetime-sdk.md#Structure_ModuleInfo%3E) | Module information and the status in the environments where the modules are running. |
| [ModuleVersionInfo](lifetime-sdk.md#Structure_ModuleVersionInfo%3E) | Information about a module version. |

| Static Entity | Description |
| :--- | :--- |
| [ApplicationPermissionLevel](lifetime-sdk.md#StaticEntity_ApplicationPermissionLevel%3E) | Permission level that a user has over an application. |
| [DeploymentMessageType](lifetime-sdk.md#StaticEntity_DeploymentMessageType%3E) | The type of a deployment message. |
| [DeploymentOperationType](lifetime-sdk.md#StaticEntity_DeploymentOperationType%3E) | The type of a deployment operation. |
| [DeploymentStatus](lifetime-sdk.md#StaticEntity_DeploymentStatus%3E) | The status of a deployment operation. |
| [DialogBoxIcon](lifetime-sdk.md#StaticEntity_DialogBoxIcon%3E) | Internal only. Icon of a Dialog Box. |
| [ElementType](lifetime-sdk.md#StaticEntity_ElementType%3E) | The types of elements a module references or exposes as public. |
| [EnvironmentPermissionLevel](lifetime-sdk.md#StaticEntity_EnvironmentPermissionLevel%3E) | Permission level that a user has over an epplication. |
| [LayoutPopupButtonClicked](lifetime-sdk.md#StaticEntity_LayoutPopupButtonClicked%3E) | The message of an OnNotify action when a button is pressed in a popup. |

## Widgets

### Internal\_Layout\_LifeTime { \#Internal\_Layout\_LifeTime }

The LifeTime layout.

_Inputs_

HelpURL : Type: optional, Text.

ForceFixedContentOnTop : Type: optional, Boolean.

### Internal\_Layout\_Popup { \#Internal\_Layout\_Popup }

The Popup Layout to be used in a LifeTime plugin. Pressing the popup buttons triggers the OnNotify action containing a LayoutPopupButtonClicked identifier.

_Inputs_

Title : Type: mandatory, Text.  
The Title of the Popup.

Subtitle : Type: optional, Text.  
The Subtitle of the Popup.

ConfirmButtonLabel : Type: optional, Text.  
The label of the confirmation button.

CancelButtonLabel : Type: optional, Text.  
The label of the cancel button.

HideConfirmButton : Type: optional, Boolean.  
If True, the confirmation button is hidden.

HideCancelButton : Type: optional, Boolean.  
If True, the cancel button is hidden.

AlignTitleToCenter : Type: optional, Boolean.  
If True, the Title is aligned to the center of the popup.

IgnoreNotifyOnCancel : Type: optional, Boolean.  
If True, pressing the cancel button does not trigger the OnNotify action.

WrapTitle : Type: optional, Boolean.  
If True, the Title is wrapped.

HideScrollbars : Type: optional, Boolean.  
If True, no scrollbars are shown when necessary.

JustifyContent : Type: optional, Boolean.  
If True, the content of the popup is justified.

Icon : Type: optional, DialogBoxIcon Identifier.  
The icon to appear in the Popup.

### Layout\_LifeTimeSDK { \#Layout\_LifeTimeSDK }

The Web Block to be used as the base layout for a LifeTime plugin. The layout allows you to easily create screens with the look and feel of LifeTime, since it contains LifeTime header and footer.

The layout also contains a stamp for you to customize with the developer or company name, when you register the plugin.

## Actions

### Application\_Get { \#Application\_Get }

Returns the information of an application in an environment.  
If the environment is not specified, information of the application across all infrastructure is returned.

_Inputs_

ApplicationKey : Type: mandatory, Text.  
The application unique identifier.

EnvironmentKey : Type: optional, Text.  
The environment unique identifier. If the environment is not specified, information of the application across all infrastructure is returned.

IncludeModules : Type: mandatory, Boolean.  
True returns information about the modules of the application, false only returns information of the application.

_Outputs_

Application : Type: [ApplicationInfo](lifetime-sdk.md#Structure_ApplicationInfo%3E).  
Application with its information, such as name, description, url.

Modules : Type: [ModuleInfo](lifetime-sdk.md#Structure_ModuleInfo%3E) List.  
List of modules with their information, such as name, description, status.

### Application\_List { \#Application\_List }

Returns a list of the applications in the specified environment that are visible within LifeTime, with their information, such as name, description, url. If no environment is specified, information of all visible applications across all environments is returned.

_Inputs_

EnvironmentKey : Type: optional, Text.  
The environment unique identifier. If no environment is specified, information of all visible applications across all environments is returned.

IncludeHiddenApplications : Type: optional, Boolean.  
If set to True, the result includes applications that are not visible within LifeTime.

_Outputs_

Applications : Type: [ApplicationInfo](lifetime-sdk.md#Structure_ApplicationInfo%3E) List.  
List of applications with their information, such as name, description, url.

### ApplicationVersion\_Get { \#ApplicationVersion\_Get }

Returns information of an application on a specified date.

_Inputs_

ApplicationKey : Type: mandatory, Text.  
The application unique identifier.

Version : Type: mandatory, Text.  
The version number.

_Outputs_

ApplicationVersion : Type: [ApplicationVersionInfo](lifetime-sdk.md#Structure_ApplicationVersionInfo%3E).  
Application with its information, such as version, description and modules.

### ApplicationVersion\_List { \#ApplicationVersion\_List }

Returns the information of all tagged application versions for the specified application.

_Inputs_

ApplicationKey : Type: mandatory, Text.  
The application unique identifier.

CreatedOnEnvironmentKey : Type: optional, Text.  
The environment unique identifier from where the versions are to be retrieved. If the environment is not specified, information of the application versions across all infrastructure is returned.

_Outputs_

ApplicationVersions : Type: [ApplicationVersionInfo](lifetime-sdk.md#Structure_ApplicationVersionInfo%3E) List.  
List of application versions with their information, such as version, description and its modules.

### Deployment\_Get { \#Deployment\_Get }

Returns information of the specified deployment.

_Inputs_

DeploymentKey : Type: mandatory, Text.  
The deployment unique identifier.

IncludeLog : Type: mandatory, Boolean.  
If true, returns the deployment log information.

_Outputs_

Deployment : Type: [DeploymentInfo](lifetime-sdk.md#Structure_DeploymentInfo%3E).  
The deployment with its information, such as source environment, target environment, and operations executed.

DeploymentLog : Type: [DeploymentMessage](lifetime-sdk.md#Structure_DeploymentMessage%3E) List.  
The log of the operations executed during the deployment.

### Deployment\_List { \#Deployment\_List }

Returns information of all deployments made between two environments.

_Inputs_

SourceEnvironmentKey : Type: optional, Text.  
The environment unique identifier. If not specified, returns deployments from all environments.

TargetEnvironmentKey : Type: optional, Text.  
The environment unique identifier. If not specified, returns deployments to all environments.

DeploymentStatus : Type: optional, DeploymentStatus Identifier.  
The deployment status. If not specified, returns deployments finished with any status.

IgnoreUnchangedApplications : Type: mandatory, Boolean.  
If true, ignores the applications that were not changed in the deployments.

_Outputs_

Deployments : Type: [DeploymentInfo](lifetime-sdk.md#Structure_DeploymentInfo%3E) List.  
The list of deployments with their information, such as source environment, target environment, and operations executed.

### Environment\_Get { \#Environment\_Get }

Returns the information of an environment, such as name, version of the Platform, Application Server.

_Inputs_

EnvironmentKey : Type: mandatory, Text.  
The environment unique identifier.

_Outputs_

Environment : Type: [EnvironmentInfo](lifetime-sdk.md#Structure_EnvironmentInfo%3E).  
Information of an environment, such as name, version of the Platform, Application Server.

### Environment\_List { \#Environment\_List }

Returns a list of environments with their information, such as name, version of the Platform, Application Server.

_Outputs_

Environments : Type: [EnvironmentInfo](lifetime-sdk.md#Structure_EnvironmentInfo%3E) List.  
List of environments with their information, such as name, version of the Platform, Application Server...

### GetUserSessionToken { \#GetUserSessionToken }

Returns an authentication token that is valid for 5 minutes, for the session user.

_Inputs_

Username : Type: mandatory, Text.  
A LifeTime username.

_Outputs_

Token : Type: Text.  
A session token. This token expires 5 minutes after it has been created.

ResponseMessage : Type: Text.  
A human readable message that explains why the call to the API failed.

ResponseAdditionalInfo : Type: Text.  
More information about why the call to the API failed.

### ModuleVersion\_Get { \#ModuleVersion\_Get }

Returns the information of a module version for the specified module and version.

_Inputs_

ModuleKey : Type: mandatory, Text.  
The module unique identifier.

ModuleVersionKey : Type: mandatory, Text.  
The module version unique identifier.

_Outputs_

ModuleVersion : Type: [ModuleVersionInfo](lifetime-sdk.md#Structure_ModuleVersionInfo%3E).  
Module version with its information, such as key, when it was created and by whom.

### ModuleVersion\_List { \#ModuleVersion\_List }

Returns the information of all module versions for the specified module.

_Inputs_

ModuleKey : Type: mandatory, Text.  
The module unique identifier.

_Outputs_

ModuleVersions : Type: [ModuleVersionInfo](lifetime-sdk.md#Structure_ModuleVersionInfo%3E) List.  
List of module versions with their information, such as key, when it was created and by whom.

### Plugin\_Register { \#Plugin\_Register }

Registers the caller eSpace as a LifeTime plugin: in the LifeTime 'More' menu a new link is created with the specified name that redirects to the entry point provided, or the default entry point if none is provided. All web screens of the plugin are displayed with their owner name.  
Each eSpace can only register a single plugin.

_Inputs_

PluginName : Type: mandatory, Text.  
The name of the plugin. The name provided will be displayed in LifeTime 'More' menu.

EntryPointName : Type: optional, Text.  
The entry point to use when clicking the link created in Lifetime 'More' menu. If no entry point is provided, the default is used.

DeveloperName : Type: optional, Text.  
The developers of the plugin. The name is displayed in all web screens of the plugin.

### Plugin\_Unregister { \#Plugin\_Unregister }

Unregisters the caller eSpace as a LifeTime plugin: in the LifeTime 'More' menu there is no longer a link to the plugin.

### Security\_CheckApplicationPermission { \#Security\_CheckApplicationPermission }

Checks if a user has a permission for a specific application running on an environment.  
If no user is specified, the current user is used.

_Inputs_

UserId : Type: optional, User Identifier.  
The user to check permissions for. If no user is specified, the current user is used instead.

RequiredPermissionLevel : Type: mandatory, ApplicationPermissionLevel Identifier.  
The permission level to check for.

EnvironmentKey : Type: mandatory, Text.  
The environment unique identifier.

ApplicationKey : Type: mandatory, Text.  
The application unique identifier.

_Outputs_

HasPermission : Type: Boolean.  
True if the user has the specified permission, false otherwise.

### Security\_CheckEnvironmentPermission { \#Security\_CheckEnvironmentPermission }

Checks if a user has a permission for a specific environment. If no user is specified, the current user is used.

_Inputs_

UserId : Type: optional, User Identifier.  
The user to check permissions for. Defaults to the logged in user if not specified.

RequiredPermissionLevel : Type: mandatory, EnvironmentPermissionLevel Identifier.  
The permission level to check for.

EnvironmentKey : Type: mandatory, Text.  
The environment unique identifier.

_Outputs_

HasPermission : Type: Boolean.  
True if the user has the requested permission, false otherwise.

### Security\_CheckInfrastructurePermission { \#Security\_CheckInfrastructurePermission }

Checks if a user has the 'Configure Infrastructure' permission. If no user is specified, the current user is used.

_Inputs_

UserId : Type: optional, User Identifier.  
The user to check permissions for. If no user is specified, the current user is used instead.

_Outputs_

HasPermission : Type: Boolean.  
True if the user has the requested permission, false otherwise.

### Security\_GetApplicationsPermissions { \#Security\_GetApplicationsPermissions }

Returns the permissions the specified user has for each application in the environment. If no user is specified, the current user is used.

_Inputs_

UserId : Type: optional, User Identifier.  
The user to check permissions for. If no user is specified, the current user is used instead.

EnvironmentKey : Type: mandatory, Text.  
The environment unique identifier.

_Outputs_

EnvironmentApplicationsPermissions : Type: [EnvironmentApplicationPermission](lifetime-sdk.md#Structure_EnvironmentApplicationPermission%3E) List.  
List of the application permissions for each application in the environment.

### Security\_GetEnvironmentsPermissions { \#Security\_GetEnvironmentsPermissions }

Returns the permissions the specified user has for each environment. If no user is specified, the current user is used.

_Inputs_

UserId : Type: optional, User Identifier.  
The user to check permissions for. If no user is specified, the current user is used instead.

_Outputs_

EnvironmentsPermissions : Type: [EnvironmentPermission](lifetime-sdk.md#Structure_EnvironmentPermission%3E) List.  
List of the permissions for each environment.

### SetLoginRedirectURL { \#SetLoginRedirectURL }

_Inputs_

URL : Type: mandatory, Text.

## Structures

### ApplicationInfo { \#Structure\_ApplicationInfo }

Application details and environment specific information where the application is running.

_Attributes_

Key : Type: Text \(50\).  
Application unique identifier.

Name : Type: Text \(50\).  
Name of the application.

Description : Type: Text \(50\).  
Description of the application.

URLPath : Type: Text \(50\).  
Relative URL path of the application, starting from the hostname.

IconHash : Type: Text \(50\).  
Hash of the application icon. Can be used to detect changes in the application icon.

IconURL : Type: Text \(50\).  
The URL for the application icon.

StatusInEnvironments : Type: [EnvironmentApplicationInfo](lifetime-sdk.md#Structure_EnvironmentApplicationInfo%3E) List.  
Information about the status of the application in each environment it is running.

IsSystem : Type: Boolean.  
Indicates if the application is a built-in component of the AgilePlatform \(e.g. ServiceCenter, LifeTime, ...\).

IsHidden : Type: Boolean.  
Indicates if the application is not visible within LifeTime.

ApplicationKindId : Type: RuntimeKind Identifier.

### ApplicationVersionInfo { \#Structure\_ApplicationVersionInfo }

Information of a specific version of an application, and the versions of its modules.

_Attributes_

Version : Type: Text \(50\).  
Version of the application.

Description : Type: Text \(50\).  
Description of the version.

CreatedOnEnvironmentKey : Type: Text \(50\).  
Environment unique identifier of the environment where the application was created.

CreatedOn : Type: Date Time.  
Date and time of the application creation.

CreatedBy : Type: Text \(50\).  
Username of the user that created the application version.

ModuleVersions : Type: [ModuleVersionInfo](lifetime-sdk.md#Structure_ModuleVersionInfo%3E) List.  
List of module versions that make the application version.

### DeploymentInfo { \#Structure\_DeploymentInfo }

Deployment information with the operations executed.

_Attributes_

Key : Type: Text \(50\).  
Deployment unique identifier.

SourceEnvironmentKey : Type: Text \(50\).  
Source environment unique identifier.

TargetEnvironmentKey : Type: Text \(50\).  
Target environment unique identifier.

Notes : Type: Text \(50\).  
Deployment notes.

TwoStepMode : Type: Boolean.  
True if the deployment was executed in two stages, false otherwise.

DeploymentStatusId : Type: DeploymentStatus Identifier.  
Deployment status identifier.

CreatedOn : Type: Date Time.  
Date and time when the deployment plan was created.

CreatedBy : Type: Text \(50\).  
Username of the user that created deployment plan.

SavedOn : Type: Date Time.  
The date and time when the deployment plan was saved.

StartedOn : Type: Date Time.  
The date and time when the deployment started.

StartedBy : Type: Text \(50\).  
Username of the user that started the deployment.

NeedsUserIntervention : Type: Boolean.  
True if the deployment needs the user intervention to proceed, false otherwise.

DeploymentFinishedOn : Type: Date Time.  
Date and time when the deployment was completed.

SyncFinishedOn : Type: Date Time.  
Date and time when the synchronization between the target environment and LifeTime was completed.

Operations : Type: [DeploymentOperationInfo](lifetime-sdk.md#Structure_DeploymentOperationInfo%3E) List.  
List of operations to execute, as specified in the deployment plan.

### DeploymentMessage { \#Structure\_DeploymentMessage }

Message from a deployment operation log.

_Attributes_

Instant : Type: Date Time.  
Date and time when the message was logged.

Message : Type: Text \(50\).  
Content of the message. Can be used to group messages.

Detail : Type: Text \(50\).  
Details of the message.

DeploymentMessageTypeId : Type: DeploymentMessageType Identifier.  
Type of the message. Can be used to identify errors, warnings and other events.

### DeploymentOperationInfo { \#Structure\_DeploymentOperationInfo }

A deployment operation as specified in the deployment plan.

_Attributes_

ApplicationKey : Type: Text \(50\).  
Application unique identifier.

SourceApplicationVersion : Type: Text \(50\).  
Application version in the source environment.

TargetApplicationVersion : Type: Text \(50\).  
Application version in the target environment.

DeploymentOperationTypeId : Type: DeploymentOperationType Identifier.  
Type of operation to execute, as specified in the deployment plan.

### EnvironmentApplicationInfo { \#Structure\_EnvironmentApplicationInfo }

Application information for a specific environment.

_Attributes_

EnvironmentKey : Type: Text \(50\).  
Environment unique identifier.

ExistsInEnvironment : Type: Boolean.  
True if the application exists in the environment, false otherwise.

Version : Type: Text \(50\).  
Version of the application.

IsModified : Type: Boolean.  
True if the application has been changed since the last tag, false otherwise.

LastPublishedOn : Type: Date Time.  
Date and time of the last publication.

LastPublishedBy : Type: Text \(50\).  
Username of user that performed the last publication.

### EnvironmentApplicationPermission { \#Structure\_EnvironmentApplicationPermission }

A user's permission to an application in an environment.

_Attributes_

ApplicationKey : Type: Text \(50\).  
Application unique identifier.

ApplicationPermissionLevelId : Type: ApplicationPermissionLevel Identifier.  
Application Permission Level identifier.

### EnvironmentInfo { \#Structure\_EnvironmentInfo }

An environment and its information.

_Attributes_

Key : Type: Text \(50\).  
Environment unique identifier.

Name : Type: Text \(50\).  
Name of the environment.

Version : Type: Text \(50\).  
Platform Server version. \[X.X.X.X\]

Order : Type: Integer.  
The order of the environment as displayed in Lifetime.

HostName : Type: Text \(50\).  
Hostname of the environment.

UseHTTPS : Type: Boolean.  
Indicates if connections to the environment are made using HTTPS.

InProductionMode : Type: Boolean.  
Indicates if the environment is running in production mode.

NumberOfFrontEnds : Type: Integer.  
Number of front-end servers in the environment.

ApplicationServerType : Type: Text \(50\).  
Stack of the application server.

ApplicationServer : Type: Text \(50\).  
Type of application server. \[IIS \| JBoss \| WebLogic\]

DatabaseProvider : Type: Text \(50\).  
Type of database provider. \[SqlServer \| Oracle\]

IsCloudEnvironment : Type: Boolean.  
Indicates if the environment is running on a cloud service.

### EnvironmentModuleInfo { \#Structure\_EnvironmentModuleInfo }

Information of a module in a specific environment.

_Attributes_

EnvironmentKey : Type: Text \(50\).  
Environment unique identifier.

ExistsInEnvironment : Type: Boolean.  
True if the module exists in the environment, false otherwise.

PublishedOn : Type: Date Time.  
Date and time of the publication.

PublishedBy : Type: Text \(50\).  
Username of the user that published the module.

Status : Type: Text \(50\).  
Status of the module. Is empty if the module is working correctly, and returns ‘Warning’ if the module has outdated references, or ‘Error’ if the module uses broken references.

StatusMessage : Type: Text \(50\).  
Verbose status messages. associated with the module, one message per line of text.

ModuleVersionInfoKey : Type: Text \(50\).  
Module version unique identifier.

### EnvironmentPermission { \#Structure\_EnvironmentPermission }

A user's permission to an environment.

_Attributes_

EnvironmentKey : Type: Text \(50\).  
Environment unique identifier.

EnvironmentPermissionLevelId : Type: EnvironmentPermissionLevel Identifier.  
Environment Permission Level identifier.

### ModuleInfo { \#Structure\_ModuleInfo }

Module information and the status in the environments where the modules are running.

_Attributes_

Key : Type: Text \(50\).  
Module unique identifier.

Name : Type: Text \(50\).  
Name of the module.

Kind : Type: Text \(50\).  
Module type \(eSpace or Extension\).

Description : Type: Text \(50\).  
Description of the module.

StatusInEnvironments : Type: [EnvironmentModuleInfo](lifetime-sdk.md#Structure_EnvironmentModuleInfo%3E) List.  
Status of the module for each environment where the application is running.

### ModuleVersionInfo { \#Structure\_ModuleVersionInfo }

Information about a module version.

_Attributes_

Key : Type: Text \(50\).  
Module version unique identifier.

ComparisonHash : Type: Text \(100\).  
Hash of the module version. Can be used to validate if two module versions have differences.

CreatedOn : Type: Date Time.  
Date and time of the module version creation.

CreatedBy : Type: Text \(50\).  
Username of the user that created the version.

## Static Entities

### ApplicationPermissionLevel { \#StaticEntity\_ApplicationPermissionLevel }

Permission level that a user has over an application.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

Description : Type: Text \(128\).

Level : Type: Integer.

_Records_

* NoAccess
* List
* OpenReuse
* ChangeDeploy

### DeploymentMessageType { \#StaticEntity\_DeploymentMessageType }

The type of a deployment message.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

_Records_

* StageAborted
* Info
* PublishStop
* Start
* End
* Error
* Unknown
* Warning
* Step
* StepSub
* AcceptableError

### DeploymentOperationType { \#StaticEntity\_DeploymentOperationType }

The type of a deployment operation.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

Order : Type: Integer.

_Records_

* Unchanged
* Deploy
* Republish

### DeploymentStatus { \#StaticEntity\_DeploymentStatus }

The status of a deployment operation.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

Order : Type: Integer.

_Records_

* NeedsUserIntervention
* InProgress
* Planned
* Synchronized
* Deployed
* Draft

### DialogBoxIcon { \#StaticEntity\_DialogBoxIcon }

Internal only. Icon of a Dialog Box.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

CssClass : Type: Text \(50\).

_Records_

* None
* Success
* Error
* Feedback
* Warning

### ElementType { \#StaticEntity\_ElementType }

The types of elements a module references or exposes as public.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

Order : Type: Integer.

_Records_

* HumanActivity
* Structure
* HiddenEntity
* WebBlock
* Unknown
* Image
* Action
* WebFlow
* WebScreen
* Theme
* StaticEntity
* Role
* Entity
* Process
* ServiceAPIMethod

### EnvironmentPermissionLevel { \#StaticEntity\_EnvironmentPermissionLevel }

Permission level that a user has over an epplication.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

Description : Type: Text \(128\).

Level : Type: Integer.

ApplicationLevelId : Type: ApplicationPermissionLevel Identifier.  
The application level to which this environment level corresponds.

_Records_

* NoAccess
* FullControl
* ChangeDeploy
* OpenReuse
* List

### LayoutPopupButtonClicked { \#StaticEntity\_LayoutPopupButtonClicked }

The message of an OnNotify action when a button is pressed in a popup.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

_Records_

* Cancel
* Confirm

