---
kinds: ServiceStudio.Plugin.SOAP.SOAPStructureAttributeDescriptor
helpids: -1
---

# Structure Attribute \(Consumed SOAP\)

## Properties

| Name | Description | Mandatory | Default value | Observations |  |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |  |
| Label | Text literal or expression used as a tooltip when hovering the image or displayed when the image cannot be displayed. |  |  |  |  |
| Data Type |  | Yes |  |  |  |
| Length | Maximum size of the attribute in characters. |  |  |  |  |
| Decimals | Number of decimal places. |  |  | Only available when data type is Decimal \(mandatory\). |  |
| Is Mandatory | Set to Yes to require for a value to be set. | Yes |  |  |  |
| Advanced |  |  |  |  |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |  |
| Send Default Value | Send the attribute value in the response payload if it is holding its default value. | Yes |  |  |  |
| Original Name | Name of the attribute as defined in the WSDL. | Yes |  |  |  |
| Original Description | Description of the attribute as provided in the WSDL. |  |  |  |  |
| Original Type | Type of the attribute as defined in the WSDL. |  |  |  |  |
| Original Default Value | Default value of the attribute defined in the WSDL. |  |  |  |  |
| Min. Occurrences | Minimum number of times this element can appear as defined in the WSDL. | Yes |  |  |  |
| Max. Occurrences | Maximum number of times this element can appear as defined in the WSDL. | Yes |  |  |  |
| Nillable | Set to Yes to allow elements to accept nil values. | Yes |  |  |  |

