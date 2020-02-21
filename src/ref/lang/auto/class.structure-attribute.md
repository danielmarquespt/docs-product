---
kinds: >-
  ServiceStudio.Model.StructureAttribute+Kind,
  ServiceStudio.Model.SystemActionStructureAttribute+Kind,
  ServiceStudio.Model.WebReferenceStructureAttribute+Kind,
  ServiceStudio.Model.ReferenceStructureAttribute+Kind
helpids: 0
---

# Structure Attribute

Stores part of the information that concerns a structure. Examples of attributes are: customer name, product id, product price.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Label | Text of the label associated with the input field of this attribute when it is the source of a widget allowing record editing. |  |  |  |
| Data Type | The attribute data type. | Yes |  |  |
| Length | Maximum size of the attribute in characters. |  |  |  |
| Decimals | Number of decimal places. |  |  | Only available when data type is Decimal \(mandatory\). |
| Is Mandatory | Set to Yes to require for a value to be set. | Yes | No |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |
| JSON Properties |  |  |  |  |
| Name in JSON | Name to use when sending this attribute in the payload of the request. |  |  |  |

