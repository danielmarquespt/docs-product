---
kinds: >-
  ServiceStudio.Model.Role+Kind, ServiceStudio.Model.SystemRole+Kind,
  ServiceStudio.Model.ReferenceRole+Kind
helpids: 15004
---

# Role

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Advanced |  |  |  |  |
| Is Persistent | If Yes, the association between the user and the role is stored in the database and is persistent across multiple sessions. If No, the role is only associated with the user for a single session. This property is read-only in mobile apps. | Yes | Yes |  |

