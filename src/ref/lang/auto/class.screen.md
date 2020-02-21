---
kinds: >-
  ServiceStudio.Model.NRNodes+WebScreen+Kind,
  ServiceStudio.Model.NewRuntime.ReferenceWebScreen+Kind
helpids: '4011, 0'
---

# Screen

User interface with which end-users interact.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Title | Text literal or expression displayed in the title bar of the browser. |  |  | When this property is empty, the title bar has the name of the element. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Advanced |  |  |  |  |
| Style Sheet | Style sheet associated with this element. |  |  | Click on "..." to edit the property value. |
| \(Theme Editor\) |  |  |  |  |
| Events |  |  |  |  |
| On Initialize | Action executed before rendering the screen or block and before fetching data. |  |  |  |
| On Ready | Action to be executed after the static content of this element is rendered. The data may not be available at this moment. |  |  |  |
| On Render | Action to be executed when this screen/element is completely rendered and after a change in a variable, aggregate or data action of the screen/element. |  |  |  |
| On Destroy | Action to be executed when this element will be removed from the DOM. |  |  |  |
| Required Scripts |  |  |  |  |
| Required Script | Script\(s\) required by the element. |  |  |  |
| Roles |  |  |  |  |
| Roles | List of the Roles available in your module. Allows selection of the roles that have grants to display the screen. |  | Anonymous \(unselected\) Registered |  |

