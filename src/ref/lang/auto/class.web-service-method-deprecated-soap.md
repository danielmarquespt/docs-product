---
kinds: >-
  ServiceStudio.Model.Flows+WebServiceMethod+Kind,
  ServiceStudio.Model.WebReferenceMethod+Kind
helpids: 0
---

# Web Service Method \(Deprecated SOAP\)

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Advanced |  |  |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. |  |  | This property is only visible for referenced elements. |
| Timeout in Seconds | Maximum time this method waits for a synchronous Web Service request to complete and after which an exception is raised. If unspecified, the timeout observed is 100 seconds. |  |  |  |
| Cache in Minutes | Maximum time content or results are stored in memory. When undefined, nothing is cached. |  |  |  |
| Original Description | Description of the Web Service as provided in the WSDL. |  |  |  |

