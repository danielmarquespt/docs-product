---
kinds: >-
  ServiceStudio.Model.NRNodes+WebBlock+Kind,
  ServiceStudio.Model.NewRuntime.ReferenceWebBlock+Kind
helpids: 1006
---

# Block

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
| Style Sheet | Style sheet associated with this element. |  |  | Click on "..." to edit the property value. |
| Events |  |  |  |  |
| On Initialize | Action to be executed before the block is rendered. |  |  |  |
| On Ready | Action to be executed after the static content of this element is rendered. The data may not be available at this moment. |  |  |  |
| On Render | Action to be executed when this screen/element is completely rendered and after a change in a variable, aggregate or data action of the screen/element. |  |  |  |
| On Destroy | Action to be executed when this element will be removed from the DOM. |  |  |  |
| On Parameters Changed | Action to be executed when the value of an input parameter of this element changes. |  |  |  |
| Required Scripts |  |  |  |  |
| Required Script | Script\(s\) required by the element. |  |  |  |

