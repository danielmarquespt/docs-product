---
kinds: ServiceStudio.Model.Nodes+WebEntry+Kind
helpids: 4001
---

# Entry

Defines the UI flow entry and represents a well-known URL public address.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Is Default | Set to Yes to make this entry the starting point of the module. | Yes | Yes | The entry will redirect to the screen it points to. |

