---
kinds: >-
  ServiceStudio.Model.NewRuntime.Theme+Kind, ServiceStudio.Model.Theme+Kind,
  ServiceStudio.Model.NewRuntime.ReferenceTheme+Kind,
  ServiceStudio.Model.ReferenceTheme+Kind
helpids: '0, 17140'
---

# Mobile Theme

A Theme defines the look and feel of the application, including what layouts are used for the screens, the global stylesheet used, and also the grid definitions used to position and size elements on the screen.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Base Theme | Specifies a theme from which this theme inherits its definitions by default. |  |  |  |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Style Sheet | The theme's style sheet. |  |  | Click on "..." to edit the property value. |
| Grid |  |  |  |  |
| Grid Type | Specifies the grid behavior when sizing and aligning widgets. If undefined, it is inherited from the Base Theme. | Yes |  |  |
| Columns | Size of each column in the grid \(in 'px'\). | Yes | 12 |  |
| Column Width | Size of the grid columns \(in 'px'\) | Yes | 60 |  |
| Gutter Width | Space between columns in the grid \(in 'px'\). | Yes |  |  |
| Total Width | Total grid width calculated from the previous properties \(in 'px'\). | Yes |  | This property is read-only. |
| Min. Width | Minimum size of the fluid grid \(in 'px'\) |  |  |  |
| Max. Width | Maximum size of the fluid grid \(in 'px'\) |  |  |  |
| Blocks |  |  |  |  |
| Layout | Specifies the web block used as layout for screens. If undefined, it is inherited from the Base Theme. |  |  |  |

