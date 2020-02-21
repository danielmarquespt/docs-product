---
kinds: ServiceStudio.Plugin.RESTService.RestServiceActionInputDescriptor
helpids: 30059
---

# Input Parameter \(REST API Method\)

Input parameter of an exposed REST API Method.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data Type | The data type of the input parameter. | Yes |  |  |
| Is Mandatory | Set to Yes to require for a value to be set. | Yes | Yes |  |
| Advanced |  |  |  |  |
| Receive In | Specifies if the value of the input parameter is to be received in the URL, the Header or Body of the HTTP request. | Yes | URL |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |
| Name in Request | The parameter name received in the request, for example: Content-Language. |  |  |  |

