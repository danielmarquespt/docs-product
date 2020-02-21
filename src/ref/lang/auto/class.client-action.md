---
kinds: >-
  ServiceStudio.Model.NRFlows+ClientActionFlow+Kind,
  ServiceStudio.Model.NRFlows+ClientScreenActionFlow+Kind,
  ServiceStudio.Model.ReferenceClientAction+Kind
helpids: 30098
---

# Client Action

Action that runs logic on the client side.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Function | Set to Yes to define the action as a function. Functions must return a value and can be used in expressions. | Yes | No | This property is only available in global scope actions. Client actions set as functions can only be used in client action expressions. |
| Icon | Picture to be displayed to help identify this element. | Yes |  | The recommended dimensions for the icon are 32 × 32 pixels. |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |

