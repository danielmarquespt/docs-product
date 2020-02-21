---
kinds: >-
  ServiceStudio.Model.StructureAttribute+Kind,
  ServiceStudio.Model.SystemActionStructureAttribute+Kind,
  ServiceStudio.Model.WebReferenceStructureAttribute+Kind,
  ServiceStudio.Model.ReferenceStructureAttribute+Kind
helpids: 0
---

# Structure Attribute \(Deprecated SOAP\)

Attribute of structure used in input or output parameters of consumed SOAP Web Service Methods.

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
| Name in JSON | Attribute name used when serializing or deserializing JSON. If not specified, the value of the Name property will be used. |  |  |  |
| Advanced |  |  |  |  |
| Original Name | Name of the attribute as defined in the WSDL. |  |  |  |
| Send Default Value | Send the input parameter value in the response payload if it is holding its default value. | Yes | Yes |  |
| Original Description | Description of the Web Service as provided in the WSDL. |  |  |  |
| Original Default Value | Default value of the attribute defined in the WSDL. |  |  |  |
| Min. Occurrences | Minimum number of times this element can appear as defined in the WSDL. |  | 1 |  |
| Max. Occurrences | Maximum number of times this element can appear as defined in the WSDL. |  | 1 |  |
| Nillable | Set to Yes to allow elements to accept nil values. | Yes | No |  |

