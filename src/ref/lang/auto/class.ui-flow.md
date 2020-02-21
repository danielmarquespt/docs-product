---
kinds: >-
  ServiceStudio.Model.Flows+WebFlow+Kind,
  ServiceStudio.Model.NRFlows+WebFlow+Kind,
  ServiceStudio.Model.NewRuntime.ReferenceWebFlow+Kind,
  ServiceStudio.Model.ReferenceWebFlow+Kind
helpids: '4034, 0'
---

# UI Flow

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Theme | Defines the look and feel to apply to the screens and blocks of the UI Flow. |  |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Advanced |  |  |  |  |
| HTTP Security | Security level required for HTTP requests. Can be overridden by application security settings in Service Center or LifeTime. | Yes | None | The possible values are: None, SSL/TLS, SSL/TLS with client certificates. This property is only available in web apps. |
| Integrated Authentication | Set to Yes to use Integrated Authentication to validate user access. | Yes | No | This property is only available in web apps. |
| Internal Access Only | Only users with access to the internal network can access the UI Flow elements. | Yes | No | This property is only available in web apps. |

