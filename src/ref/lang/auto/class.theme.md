---
kinds: >-
  ServiceStudio.Model.NewRuntime.Theme+Kind, ServiceStudio.Model.Theme+Kind,
  ServiceStudio.Model.NewRuntime.ReferenceTheme+Kind,
  ServiceStudio.Model.ReferenceTheme+Kind
helpids: '0, 17140'
---

# Theme

A Theme defines the look and feel of the application, including what layouts are used for the screens, the global stylesheet used, and also the grid definitions used to position and size elements on the screen.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Base Theme | Specifies a theme from which this theme inherits its definitions by default. |  |  |  |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Mobile | Set to Yes to optimize screen rendering for small devices. | Yes | No |  |
| OnException Handler | Specifies the 'OnException' handler to be called by all the flows using this theme. This option can only be used when the 'Global Exception Handler' property of the module is set to '\(Theme Exception Handler\)'. |  | Common\OnException |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Has Exception Handling | Read-only property informing if the referenced theme includes support for exception handling. | Yes | No | This property is only visible for referenced elements. |
| Style Sheet | The theme's style sheet. |  |  | Click on "..." to edit the property value. |
| Grid |  |  |  |  |
| Grid Type | Specifies the grid behavior when sizing and aligning widgets. If undefined, it is inherited from the Base Theme. | Yes |  |  |
| Columns | Size of each column in the grid \(in 'px'\). | Yes | 12 |  |
| Column Width | Size of the grid columns \(in 'px'\) | Yes | 60 |  |
| Gutter Width | Space between columns in the grid \(in 'px'\). | Yes | 20 |  |
| Total Width | Total grid width calculated from the previous properties \(in 'px'\). | Yes |  | This property is read-only. |
| Min. Width | Minimum size of the fluid grid \(in 'px'\) |  |  |  |
| Max. Width | Maximum size of the fluid grid \(in 'px'\) |  |  |  |
| Web Blocks |  |  |  |  |
| Layout | Specifies the web block used as layout for screens. If undefined, it is inherited from the Base Theme. |  |  |  |
| Header | Specifies the web block used as layout for the header. |  | Common\Header |  |
| Menu | Specifies the web block used as layout for the menu. |  | Common\Menu |  |
| Footer | Specifies the web block used as layout for the footer. |  | Common\Footer |  |
| Info Balloon | Specifies the web block used as layout used for info balloons. |  |  |  |
| Pop-up Editor | The Web Block to be used for the layout of popup editor pages. If empty it will inherit from Base Theme. |  |  |  |
| Email | Specifies the web block used as layout for emails. If undefined, it is inherited from the Base Theme. |  |  |  |
| Images |  |  |  |  |
| True Image | The Image for the True condition of If Widgets in TableRecords or ListRecords. |  |  |  |
| False Image | The Image for the False condition of If Widgets in TableRecords or ListRecords. |  |  |  |
| Info Balloon Image | The Image for the widget that links to a Info Balloon page. |  |  |  |

