# IncludeJavascript API

For Platform Version 9.0.99.11. API for including scripts in Web Screens for all web apps running in the environment.

## Summary

| Action | Description |
| :--- | :--- |
| [Application\_AddExclusionRule](includejavascript-api.md#Application_AddExclusionRule%3E) | Creates exclusion rules for a script. The specified script is not included in the specified application. |
| [Application\_RemoveExclusionRule](includejavascript-api.md#Application_RemoveExclusionRule%3E) | Removes a script exclusion rule. The specified script is to be included in the specified application. |
| [Espace\_AddExclusionRule](includejavascript-api.md#Espace_AddExclusionRule%3E) | Creates exclusion rules for a script. The specified script is not included in the specified eSpace. |
| [Espace\_RemoveExclusionRule](includejavascript-api.md#Espace_RemoveExclusionRule%3E) | Removes a script exclusion rule. The specified script is to be included in the specified application. |
| [Script\_CreateOrUpdate](includejavascript-api.md#Script_CreateOrUpdate%3E) | Creates or updates a javascript. The script is inserted in the HTML of all Web Screens of all eSpace modules.%%If the script name already exists, the script is updated, otherwise a new script is created. |
| [Script\_Delete](includejavascript-api.md#Script_Delete%3E) | Deletes a script: the script is no longer included in Web Screens. |
| [Script\_Get](includejavascript-api.md#Script_Get%3E) | Returns the information of a script. |
| [Script\_List](includejavascript-api.md#Script_List%3E) | Returns a list of scripts to be included in Web Screens. |
| [Script\_SetActive](includejavascript-api.md#Script_SetActive%3E) | Activates a certain script to be included in Web Screens. |
| [Script\_SetInactive](includejavascript-api.md#Script_SetInactive%3E) | Deactivates a certain script. The script is not included in Web Screens. |

| Structure | Description |
| :--- | :--- |
| [ExcludedApplications](includejavascript-api.md#Structure_ExcludedApplications%3E) | Represents an exclusion rule for a specific application. Exclusion rules specify applications in which scripts are not to be inserted. |
| [ExcludedEspaces](includejavascript-api.md#Structure_ExcludedEspaces%3E) | Represents an exclusion rule for a specific eSpace. Exclusion rules specify eSpaces in which scripts are not to be inserted. |
| [JavaScript](includejavascript-api.md#Structure_JavaScript%3E) | Represents a script to be included in the HTML of Web Screens. |

## Actions

### Application\_AddExclusionRule { \#Application\_AddExclusionRule }

Creates exclusion rules for a script. The specified script is not included in the specified application.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script.

ApplicationKey : Type: Text. Mandatory.  
The application unique key.

### Application\_RemoveExclusionRule { \#Application\_RemoveExclusionRule }

Removes a script exclusion rule. The specified script is to be included in the specified application.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script.

ApplicationKey : Type: Text. Mandatory.  
The application unique key.

### Espace\_AddExclusionRule { \#Espace\_AddExclusionRule }

Creates exclusion rules for a script. The specified script is not included in the specified eSpace.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script.

EspaceKey : Type: Text. Mandatory.  
The eSpace unique key.

### Espace\_RemoveExclusionRule { \#Espace\_RemoveExclusionRule }

Removes a script exclusion rule. The specified script is to be included in the specified application.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script to be included.

EspaceKey : Type: Text. Mandatory.  
The eSpace unique key.

### Script\_CreateOrUpdate { \#Script\_CreateOrUpdate }

Creates or updates a javascript. The script is inserted in the HTML of all Web Screens of all eSpace modules.  
If the script name already exists, the script is updated, otherwise a new script is created.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script.

ScriptOrURL : Type: Text. Mandatory.  
The inline script or a URL specifying where the script is located. This parameter needs to comply with the isUrl parameter.

IncludeAt : Type: Text. Mandatory.  
The location in the HTML where the script is to be included. Valid locations are ‘HeadTop’, ‘HeadBottom’, ‘BodyTop’, ‘BodyBottom’.

Order : Type: Integer.  
Specifies the order in which the script is to be included in the Web Screen or Web Block.

Description : Type: Text.  
The documentation of the script.

### Script\_Delete { \#Script\_Delete }

Deletes a script: the script is no longer included in Web Screens.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script.

### Script\_Get { \#Script\_Get }

Returns the information of a script.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script.

_Outputs_

JavaScript : Type: Record of [JavaScript](includejavascript-api.md#Structure_JavaScript%3E).  
The script to be included in Web Screens.

### Script\_List { \#Script\_List }

Returns a list of scripts to be included in Web Screens.

_Inputs_

ShowInactive : Type: Boolean. Mandatory.  
If true returns all scripts, including scripts marked as inactive.

_Outputs_

JavaScriptList : Type: RecordList of [JavaScript](includejavascript-api.md#Structure_JavaScript%3E).  
List of scripts.

### Script\_SetActive { \#Script\_SetActive }

Activates a certain script to be included in Web Screens.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script.

### Script\_SetInactive { \#Script\_SetInactive }

Deactivates a certain script. The script is not included in Web Screens.

_Inputs_

ScriptName : Type: Text. Mandatory.  
The name of the script.

## Structures

### ExcludedApplications { \#Structure\_ExcludedApplications }

Represents an exclusion rule for a specific application. Exclusion rules specify applications in which scripts are not to be inserted.

_Attributes_

ApplicationKey : Type: Text \(50\). Mandatory.  
The unique key of the application.

ApplicationName : Type: Text \(50\). Mandatory.  
The name of the application.

### ExcludedEspaces { \#Structure\_ExcludedEspaces }

Represents an exclusion rule for a specific eSpace. Exclusion rules specify eSpaces in which scripts are not to be inserted.

_Attributes_

EspaceKey : Type: Text \(50\). Mandatory.  
The unique key of the eSpace.

EspaceName : Type: Text \(50\). Mandatory.  
The name of the eSpace.

### JavaScript { \#Structure\_JavaScript }

Represents a script to be included in the HTML of Web Screens.

_Attributes_

Name : Type: Text \(50\). Mandatory.  
The name of the script.

ScriptOrURL : Type: Text \(4096\). Mandatory.  
The inline script or an absolute URL specifying where the script is located.

IncludeAt : Type: Text \(50\). Mandatory.  
The location in the HTML where the script is to be included. Valid locations are ‘HeadTop’, ‘HeadBottom’, ‘BodyTop’, ‘BodyBottom’.

Order : Type: Integer.  
Specifies the order in which the script is to be included in the Web Screen or Web Block.

Description : Type: Text \(50\).  
The documentation of the script.

IsActive : Type: Boolean. Mandatory.  
Describes whether the script is globally enabled or disabled.

ExcludedApplications : Type: RecordList of [ExcludedApplications](includejavascript-api.md#Structure_ExcludedApplications%3E). Mandatory.  
The script is not inserted in the Web Screens of these applications.

ExcludedEspaces : Type: RecordList of [ExcludedEspaces](includejavascript-api.md#Structure_ExcludedEspaces%3E). Mandatory.  
The script is not inserted in the Web Screens of these eSpaces.

