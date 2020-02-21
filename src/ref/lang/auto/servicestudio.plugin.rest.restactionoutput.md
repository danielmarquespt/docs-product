---
kinds: ServiceStudio.Plugin.REST.RestActionOutputDescriptor
helpids: 30081
---

# Output Parameter \(REST API Method\)

Output parameter of a consumed REST API Method.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data Type | The data type of the output parameter. | Yes |  |  |
| Advanced |  |  |  |  |
| Receive In | Indicates whether the output parameter is found in the HTTP Header or Body. | Yes | Body |  |
| Name in Response | Original name of the output parameter that is used in the HTTP response. If not specified, it has the same value as the Name. |  |  |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |

