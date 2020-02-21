---
kinds: ServiceStudio.Plugin.SOAP.SOAPClientDescriptor
helpids: -1
---

# SOAP Web Service \(Consumed\)

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Icon | Picture to be displayed to help identify this element. | Yes |  |  |
| Authentication |  |  |  |  |
| Authentication Type | Authentication type for each request. | Yes | \(None\) |  |
| Username | Username sent for authenticating requests. Can be customized at runtime using Dynamic Authentication or in the environment console. |  |  |  |
| Password | Password sent for authenticating requests. Can be customized at runtime using Dynamic Authentication or in the environment console. |  |  |  |
| Advanced |  |  |  |  |
| On Before Request | Action to modify the connection, request and/or response message by using extension actions that use the SOAP Extensibility API. |  |  |  |
| WSDL Location | Location where the WSDL is obtained. |  |  |  |
| WSDL | WSDL with the definition of the functionality provided by this SOAP Web Service. |  |  |  |
| Binding | Binding of the SOAP Web Service. |  |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. |  |  | This property is only visible for referenced elements. |
| Original Description | Description of the Web Service as provided in the WSDL. |  |  |  |

