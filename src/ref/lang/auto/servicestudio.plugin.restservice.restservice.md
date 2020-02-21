---
kinds: ServiceStudio.Plugin.RESTService.RestServiceDescriptor
helpids: 17225
---

# REST API

API exposing methods to allow other systems to retrieve or manipulate information through REST.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Icon | Picture to be displayed to help identify this element. | Yes |  |  |
| URL | Base URL of all REST API methods. |  |  |  |
| Security |  |  |  |  |
| HTTP Security | Security level required for HTTP requests. Can be overridden by the security level set in the environment or infrastructure. | Yes | SSL/TLS |  |
| Authentication | Required authentication in HTTP requests. The callback action OnAuthentication is made available to implement Basic or Custom authentication. | Yes | None |  |
| Internal Access Only | Only users with access to the internal network can access the Web Service. | Yes | No |  |
| Advanced |  |  |  |  |
| Documentation | Set to Yes to automatically generate a documentation page at the REST API base URL. | Yes | Yes |  |
| Send Default Values | Send the input parameter value in the response payload if it is holding its default value. | Yes | No |  |
| On Request | The action to customize the request before it reaches the REST API methods. |  |  |  |
| On Response | The action to customize the response before sending it. |  |  |  |

