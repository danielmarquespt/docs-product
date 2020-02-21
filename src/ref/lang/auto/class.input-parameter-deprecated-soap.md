---
kinds: >-
  ServiceStudio.Model.Variables+ConstantDBInputParameter+Kind,
  ServiceStudio.Model.Variables+GenericInputParameter+Kind,
  ServiceStudio.Model.Variables+JSInputParameter+Kind,
  ServiceStudio.Model.Variables+ProcessInput+Kind,
  ServiceStudio.Model.Variables+SerializableInputParameter+Kind,
  ServiceStudio.Model.Variables+SyntheticInputParameter+Kind,
  ServiceStudio.Model.Variables+URLSerializableInputParameter+Kind,
  ServiceStudio.Model.Variables+WebReferenceGenericInputParameter+Kind,
  ServiceStudio.Model.Variables+ReferenceGenericInputParameter+Kind,
  ServiceStudio.Model.Variables+ReferenceProcessInput+Kind,
  ServiceStudio.Model.Variables+ReferenceSerializableInputParameter+Kind
helpids: '7011, 30100'
---

# Input Parameter \(Deprecated SOAP\)

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Is Mandatory | Set to Yes to require for a value to be set. | Yes | Yes |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data Type |  | Yes |  |  |
| Advanced |  |  |  |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |
| Original Name | Name of the input parameter as defined in the WSDL. |  |  |  |
| Send Default Value | Send the input parameter value in the response payload if it is holding its default value. | Yes | Yes |  |
| Original Description | Description of the input parameter as provided in the WSDL. |  |  |  |
| Original Default Value | Default value of the attribute defined in the WSDL. |  |  |  |
| Min. Occurrences | Minimum number of times this element can appear as defined in the WSDL. |  | 1 |  |
| Max. Occurrences | Maximum number of times this element can appear as defined in the WSDL. |  | 1 |  |
| Nillable | Set to Yes to allow elements to accept nil values. | Yes | No |  |
| Original Namespace | Namespace as defined in the WSDL. |  |  |  |

