---
kinds: ServiceStudio.Plugin.RESTService.RestServiceActionOutputDescriptor
helpids: 30060
---

# Output Parameter \(REST API Method\)

Output parameter of an exposed REST API Method.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data Type | The data type of the output parameter. | Yes |  |  |
| Advanced |  |  |  |  |
| Send In | Indicates whether the output parameter is sent in the HTTP Header or Body. | Yes | Body |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |
| Name in Response | The parameter name sent in the response, for example: Content-Language. |  |  |  |

