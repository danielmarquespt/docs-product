---
kinds: 'ServiceStudio.Model.WebReference+Kind, ServiceStudio.Model.WebService+Kind'
helpids: '11003, 11001'
---

# SOAP Web Service \(Deprecated\)

Consumed Web Service based on the SOAP protocol.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| URL | The URL where the WSDL is obtained. | Yes |  |  |
| Advanced |  |  |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. |  |  | This property is only visible for referenced elements. |
| Integrated Authentication | Set to Yes to use Integrated Authentication to validate user access. | Yes | No |  |
| WSDL | WSDL with the definition of the functionality provided by this SOAP Web Service. | Yes |  |  |
| Endpoint | Endpoint of the SOAP Web Service. |  |  |  |
| Original Description | Description of the Web Service as provided in the WSDL. |  |  |  |

