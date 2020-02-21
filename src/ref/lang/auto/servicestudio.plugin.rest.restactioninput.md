---
kinds: ServiceStudio.Plugin.REST.RestActionInputDescriptor
helpids: 30080
---

# Input Parameter \(REST API Method\)

Input parameter of a consumed REST API Method.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data Type | The data type of the input parameter. | Yes |  |  |
| Is Mandatory | Set to Yes to require for a value to be set. | Yes | Yes |  |
| Advanced |  |  |  |  |
| Send In | Name to use for the parameter in the request. Only available when parameter is sent in the header of the request. | Yes | URL |  |
| Name in Request | Original name of the input parameter that is used in the HTTP request. If not specified, it has the same value as the Name. |  |  |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |

