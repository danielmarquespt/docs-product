---
kinds: ServiceStudio.Plugin.RESTService.RestServiceActionDescriptor
helpids: 17226
---

# REST API Method

Method of an exposed REST API.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| URL | Relative URL where the method is made available. |  |  |  |
| URL Path | Customized URL for the method. Use it in order to follow RESTful principles identified by your organization. |  |  | Due to a limitation in .NET stack, the last part of the URL \(i.e. the part after the last '/' character\) cannot contain a '.' character, otherwise method calls will not work. |
| HTTP Method | HTTP verb to access this method. | Yes | GET | The possible values are: GET, PUT, POST, DELETE. |

