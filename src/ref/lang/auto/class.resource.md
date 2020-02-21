---
kinds: 'ServiceStudio.Model.Resource+Kind, ServiceStudio.Model.ReferenceResource+Kind'
helpids: 17020
---

# Resource

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No | Available in Mobile modules only. |
| Deploy Action | Specifies the action to be executed when the module is deployed. | Yes | Do Nothing | The possible values are: Do Nothing, Deploy to Target Directory. |
| Target Directory | Target directory where the resource is to be deployed. Use / to separate multiple names. Only available when the selected Deploy Action is Deploy to Target Directory. |  |  |  |
| Runtime Path | Path where the resource is to be deployed. | Yes |  |  |
| Resource Content | Image content. | Yes |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| URL | The runtime URL of the resource. | Yes | Text | Only available in mobile apps. |
| Content | Binary content of the file specified in the widget. | Yes | Binary Data |  |

