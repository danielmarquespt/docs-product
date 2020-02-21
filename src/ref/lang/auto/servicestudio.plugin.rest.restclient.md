---
kinds: ServiceStudio.Plugin.REST.RestClientDescriptor
helpids: 17200
---

# REST API

API to consume information from another system through REST.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Icon | Picture to be displayed to help identify this element. | Yes |  |  |
| Base URL | The base URL of all methods of the REST API. This value can be customized at runtime in the environment management console. |  |  |  |
| Basic Authentication |  |  |  |  |
| Username | Username sent in the Authorization header of all methods for Basic Authentication. Can be customized at runtime in the environment console. |  |  |  |
| Password | Password sent in the Authorization header of all methods for Basic Authentication. Can be customized at runtime in the environment console. |  |  |  |
| Advanced |  |  |  |  |
| Date Format | Date format used by the Web Service. | Yes | 2014-01-01T00:00:00Z \(ISO\) |  |
| On Before Request | The action to customize the request before sending it. |  |  | This callback action is useful to debug and customize requests. |
| On After Response | The action to customize the response before it is processed. |  |  | This callback action is useful to debug and customize responses. |

