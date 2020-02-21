---
kinds: ServiceStudio.Plugin.SAP.SapStructureAttributeDescriptor
helpids: 30073
---

# Structure Attribute \(SAP Remote Function\)

Attribute of structure used in input and output arguments of SAP remote functions.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Label | Text literal or expression used as a tooltip when hovering the image or displayed when the image cannot be displayed. |  |  |  |
| Data Type | The attribute data type. | Yes |  |  |
| Length | Maximum size of the attribute in characters. |  |  |  |
| Decimals | Number of decimal places. |  |  | Only available when data type is Decimal \(mandatory\). |
| Is Mandatory | Set to Yes to require for a value to be set. | Yes |  |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |
| Advanced |  |  |  |  |
| Original Type | Original data type. |  |  |  |
| Original ABAP DataType | Original ABAP data type in the SAP system. | Yes | Integer |  |

