---
kinds: ServiceStudio.Plugin.REST.RestActionDescriptor
helpids: 17201
---

# REST API Method

Method of a consumed REST API.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| URL Path | URL of the method relative to the Base URL of the REST API. It supports using input parameters enclosed in braces, e.g., /drive/v1/files/{id}?convert={convert} | Yes |  |  |
| HTTP Method | HTTP verb used in the request. | Yes | GET | The possible values are: GET, PUT, POST, DELETE, PATCH. |
| Request Format | Content format of the body request. Mandatory for POST, PUT and PATCH HTTP methods. | Yes |  | The possible values are: JSON: for JSON content; Form URL Encoded; for URL-encoded form data; Binary: for binary content; Plain Text: for other content like, for example, XML. |
| Response Format | Content format of the body response. | Yes |  | The possible values are: JSON: for JSON content; Binary: for binary content; Plain Text: for other content like, for example, XML. |
| Timeout in Seconds | Maximum waiting time to get a response from the Web Service. By default is 100 seconds. |  |  |  |

