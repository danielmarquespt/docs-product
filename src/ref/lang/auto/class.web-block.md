---
kinds: >-
  ServiceStudio.Model.Nodes+WebBlock+Kind,
  ServiceStudio.Model.ReferenceWebBlock+Kind
helpids: 1006
---

# Web Block

Reusable screen part that can implement its own logic.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Icon | Picture to be displayed to help identify this element. | Yes |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Advanced |  |  |  |  |
| Cache in Minutes | Maximum time content or results are stored in memory. When undefined, nothing is cached. |  |  |  |
| Style Sheet | Style sheet associated with this element. |  |  | Click on "..." to edit the property value. |
| JavaScript | JavaScript associated with this element. |  |  | Click on "..." to edit the property value. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| RuntimeId | The identifier of the Web Block instance at runtime. | Yes | Text |  |

