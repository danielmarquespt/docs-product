# DbCleaner API

For Platform Version 9.10.0.14. Allows freeing-up database space.

## Summary

| Action | Description |
| :--- | :--- |
| [Attribute\_DropColumn](dbcleaner-api.md#Attribute_DropColumn%3E) | Physically deletes the database table column associated with the specified entity attribute.  If the entity attribute still exists in a module’s meta model, the delete operation will not be performed.%%The logged user needs to have the 'Administrator' built-in role. |
| [Attribute\_ListDeleted](dbcleaner-api.md#Attribute_ListDeleted%3E) | Returns a list of attributes, with their information, that have been deleted from module’s meta model but are still physically present in the database.%%The logged user needs to have the 'Administrator' built-in role. |
| [Entity\_DropTable](dbcleaner-api.md#Entity_DropTable%3E) | Physically deletes the database table associated with the specified entity.  If the entity still exists in a module’s meta model, the delete operation will not be performed.%%The logged user needs to have the 'Administrator' built-in role. |
| [Entity\_ListDeleted](dbcleaner-api.md#Entity_ListDeleted%3E) | Returns a list of entities, with their information, that have been deleted from module’s meta model but are still physically present in the database.%%The logged user needs to have the 'Administrator' built-in role. |
| [ModuleVersion\_Delete](dbcleaner-api.md#ModuleVersion_Delete%3E) | Deletes the specified module version of the specified module from the database.%%The logged user needs to have 'Change & Deploy' permissions. |
| [ModuleVersion\_DeleteAll](dbcleaner-api.md#ModuleVersion_DeleteAll%3E) | Deletes module versions that were published before the specified date and time. This action does not delete the module version that is currently published or module versions used in tagged versions of applications or solutions.%%The logged user needs to have 'Change & Deploy' permissions. |
| [ModuleVersion\_ListOldest](dbcleaner-api.md#ModuleVersion_ListOldest%3E) | Returns a list of module versions that are stored in the database and that were published before the specified date and time. This action does not return the module version that is currently published or module versions used in tagged versions of applications or solutions.%%The logged user needs to have 'Change & Deploy' permissions. |

| Structure | Description |
| :--- | :--- |
| [AttributeInfo](dbcleaner-api.md#Structure_AttributeInfo%3E) | Information about a specific entity attribute. |
| [EntityInfo](dbcleaner-api.md#Structure_EntityInfo%3E) | Information about a specific entity. |
| [ModuleInfo](dbcleaner-api.md#Structure_ModuleInfo%3E) | Information about a specific module. |
| [ModuleVersionInfo](dbcleaner-api.md#Structure_ModuleVersionInfo%3E) | Information about a specific module version. |

| Static Entity | Description |
| :--- | :--- |
| [ModuleType](dbcleaner-api.md#StaticEntity_ModuleType%3E) | Types of modules. |

## Actions

### Attribute\_DropColumn { \#Attribute\_DropColumn }

Physically deletes the database table column associated with the specified entity attribute. If the entity attribute still exists in a module’s meta model, the delete operation will not be performed.  
The logged user needs to have the 'Administrator' built-in role.

_Inputs_

AttributeId : Type: mandatory, Integer.  
The attribute identifier.

### Attribute\_ListDeleted { \#Attribute\_ListDeleted }

Returns a list of attributes, with their information, that have been deleted from module’s meta model but are still physically present in the database.  
The logged user needs to have the 'Administrator' built-in role.

_Outputs_

DeletedAttributes : Type: [AttributeInfo](dbcleaner-api.md#Structure_AttributeInfo%3E) List.  
List of attributes, with their information, that have been deleted from module’s meta model.

### Entity\_DropTable { \#Entity\_DropTable }

Physically deletes the database table associated with the specified entity. If the entity still exists in a module’s meta model, the delete operation will not be performed.  
The logged user needs to have the 'Administrator' built-in role.

_Inputs_

EntityId : Type: mandatory, Integer.  
The entity identifier.

### Entity\_ListDeleted { \#Entity\_ListDeleted }

Returns a list of entities, with their information, that have been deleted from module’s meta model but are still physically present in the database.  
The logged user needs to have the 'Administrator' built-in role.

_Outputs_

DeletedEntities : Type: [EntityInfo](dbcleaner-api.md#Structure_EntityInfo%3E) List.  
List of entities, with their information, that have been deleted from module’s meta model.

### ModuleVersion\_Delete { \#ModuleVersion\_Delete }

Deletes the specified module version of the specified module from the database.  
The logged user needs to have 'Change & Deploy' permissions.

_Inputs_

ModuleVersionId : Type: mandatory, Integer.  
The module version identifier.

ModuleId : Type: mandatory, Integer.  
The module identifier.

### ModuleVersion\_DeleteAll { \#ModuleVersion\_DeleteAll }

Deletes module versions that were published before the specified date and time. This action does not delete the module version that is currently published or module versions used in tagged versions of applications or solutions.  
The logged user needs to have 'Change & Deploy' permissions.

_Inputs_

OlderThan : Type: mandatory, Date Time.  
Date and time that indicates the most recent point in time from which onward module versions are not to be deleted from the database.

ModuleId : Type: optional, Integer.  
The module identifier. If not specified, returns module versions of all modules.

MaxNumberOfVersions : Type: optional, Integer.  
The maximum number of versions to get. If not specified, returns the oldest 100 module versions. Set to 0 \(zero\) to get all the module versions.

_Outputs_

HasMoreVersions : Type: Boolean.  
Returns True if there are still module versions to delete.

### ModuleVersion\_ListOldest { \#ModuleVersion\_ListOldest }

Returns a list of module versions that are stored in the database and that were published before the specified date and time. This action does not return the module version that is currently published or module versions used in tagged versions of applications or solutions.  
The logged user needs to have 'Change & Deploy' permissions.

_Inputs_

OlderThan : Type: mandatory, Date Time.  
Date and time that indicates the most recent point in time from which onward module versions are not to be deleted from the database.

ModuleName : Type: optional, Text.  
The name of the module. If not specified, returns module versions of modules with any name.

ModuleTypeId : Type: optional, ModuleType Identifier.  
The type of the module. If not specified, returns module versions of modules of any type.

MaxNumberOfVersions : Type: optional, Integer.  
The maximum number of versions to get. If not specified, returns the oldest 100 module versions. Set to 0 \(zero\) to get all the module versions

_Outputs_

ModuleVersions : Type: [ModuleVersionInfo](dbcleaner-api.md#Structure_ModuleVersionInfo%3E) List.  
List of module versions, with their information, that have been published in the past and are kept stored in the database.

HasMoreVersions : Type: Boolean.  
Returns True if there are more module versions than the ones listed.

## Structures

### AttributeInfo { \#Structure\_AttributeInfo }

Information about a specific entity attribute.

_Attributes_

Id : Type: Integer.  
Attribute unique identifier

Name : Type: Text.  
Name of the attribute

IsDeleted : Type: Boolean.  
Indicates if the attribute was deleted

EntityInfo : Type: [EntityInfo](dbcleaner-api.md#Structure_EntityInfo%3E).  
Information about the entity to which the attribute belongs

### EntityInfo { \#Structure\_EntityInfo }

Information about a specific entity.

_Attributes_

Id : Type: Integer.  
Entity unique identifier

Name : Type: Text.  
Name of the entity

IsDeleted : Type: Boolean.  
Indicates if the entity was deleted

ModuleInfo : Type: [ModuleInfo](dbcleaner-api.md#Structure_ModuleInfo%3E).  
Information about the module to which the entity belongs

### ModuleInfo { \#Structure\_ModuleInfo }

Information about a specific module.

_Attributes_

Id : Type: Integer.  
Module unique identifier

Name : Type: Text.  
Name of the module

IsDeleted : Type: Boolean.  
Indicates if the module was deleted

ModuleTypeId : Type: ModuleType Identifier.  
Module type identifier

### ModuleVersionInfo { \#Structure\_ModuleVersionInfo }

Information about a specific module version.

_Attributes_

Id : Type: Integer.  
Module version unique identifier

Version : Type: Text.  
Version number

UploadedDate : Type: Date Time.  
Date and time when the version was uploaded to the server

LastPublishedDate : Type: Date Time.  
Date and time of the last publish of the module version

ModuleInfo : Type: [ModuleInfo](dbcleaner-api.md#Structure_ModuleInfo%3E).  
Information about the module to which the module version belongs

## Static Entities

### ModuleType { \#StaticEntity\_ModuleType }

Types of modules.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

_Records_

* Extension
* Espace

