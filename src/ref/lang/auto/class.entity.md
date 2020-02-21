---
kinds: >-
  ServiceStudio.Model.Entity+Kind, ServiceStudio.Model.SyntheticEntity+Kind,
  ServiceStudio.Model.ReferenceEntity+Kind
helpids: 15005
---

# Entity

An Entity represents a table in a database.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies the entity in the module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Label used to describe the entity in the user interface of the application. |  |  |  |
| Label \(plural\) | Label used to described the plural of the entity in the user interface of the application. |  |  |  |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Expose Read Only | Set to Yes to expose the entity while protecting its data records from being written in a consumer module. | Yes | No |  |
| Identifier Attribute | Attribute that uniquely identifies the entity. |  |  |  |
| Label Attribute | Label used to describe the attribute. |  |  |  |
| Order By Attribute | Attribute used for the default ordering of the records of the entity. |  | \(None\) |  |
| Is Active Attribute | Specifies a Boolean attribute of the entity which defines if the record is to be fetched in a query. |  | \(None\) |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Advanced |  |  |  |  |
| Update Behavior | Set which is the way the update of entity records is performed:  - **All Attributes**: all the attributes are always updated in the database.  - **Changed Attributes**: only the attributes that were changed are updated in the database thus, improving efficiency. | Yes | Changed Attributes |  |
| Expose Process Events | If set to True, creating or updating entity records issues events to processes. | Yes | No |  |
| Is Multi-tenant | Set to Yes to isolate data per tenant or No to share data among tenants. If not set, it inherits the module setting. | Yes |  |  |
| Show Tenant Identifier | Set to Yes to show the `TenantId` entity attribute and disable automatic data isolation for this entity. | Yes | No |  |
| Original Show Tenant Identifier | Indicates the `TenantId` property value originally set in the referenced module. | Yes | No |  |
| Logical Database | The Platform's logical name for the external database where the entity is stored. |  |  |  |
| Supports Nulls | If set to Yes, mandatory attributes that are set with the default value are converted to/from null when storing/retrieving data from the external database. Otherwise no conversion is done. | Yes | No | This property is only visible for reference entities from extension modules. The value conversion only applies to mandatory attributes. |

