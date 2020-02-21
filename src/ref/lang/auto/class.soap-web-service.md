---
kinds: 'ServiceStudio.Model.WebReference+Kind, ServiceStudio.Model.WebService+Kind'
helpids: '11003, 11001'
---

# SOAP Web Service

Exposed Web Service based on the SOAP protocol.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Advanced |  |  |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. |  |  | This property is only visible for referenced elements. |
| Integrated Authentication | Set to Yes to use Integrated Authentication to validate user access. | Yes | No |  |
| HTTP Security | Security level required for HTTP requests. Can be overridden by application security settings in Service Center or LifeTime. | Yes | None | The possible values are: None, SSL/TLS, SSL/TLS with client certificates. |
| Internal Access Only | Only users with access to the internal network can access the Web Service. | Yes | No |  |

