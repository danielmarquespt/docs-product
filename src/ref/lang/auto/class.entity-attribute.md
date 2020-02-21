---
kinds: >-
  ServiceStudio.Model.EntityAttribute+Kind,
  ServiceStudio.Model.ReferenceEntityAttribute+Kind
helpids: 0
---

# Entity Attribute

An Entity Attribute represents a column in a database table.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Text used when the attribute is displayed in widgets. |  |  | This property is also used as the column header when exporting entity data to Excel. |
| Data Type | The attribute data type. | Yes |  | The attribute data type must be a basic data type or an Entity Identifier. |
| Length | Maximum size of the attribute in characters. |  |  |  |
| Decimals | Number of decimal places. |  |  | Only available when data type is Decimal \(mandatory\). |
| Is AutoNumber | Set to Yes to generate and set Number values automatically at runtime. | Yes | No |  |
| Is Mandatory | Set to Yes to require for a value to be set. | Yes | No |  |
| Delete Rule | Specifies the action to take when the record that the foreign key references is deleted. | Yes | Protect | Only available when data type is an Entity Identifier \(the attribute is a foreign key\).  Possible values are **Protect**, **Delete** and **Ignore**.  If the foreign key references an external Entity exposed by an Extension, the only possible value is **Ignore**, as the referential integrity can't be guaranteed. |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |
| Advanced |  |  |  |  |
| Original Name | The attribute column name as defined in the external database. |  |  | This property is only available in external entities' attributes. |
| Original Type | The attribute column data type as defined in the external database. |  |  | This property is only available in external entities' attributes. |

