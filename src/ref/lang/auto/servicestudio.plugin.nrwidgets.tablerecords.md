---
kinds: ServiceStudio.Plugin.NRWidgets.TableRecordsDescriptor
helpids: 30198
---

# Table

Displays a list in a tabular layout.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Source | Specifies a list with records to populate the widget. | Yes |  |  |
| Show Header | Set as Yes to display the header row of the table. |  | Yes |  |
| Style Classes | Specifies one or more style classes to apply to the table. Separate multiple values with spaces. |  | "table" |  |
| Style Header | Specifies one or more style classes to apply to the table header. Separate multiple values with spaces. |  | "table-header" |  |
| Style Row | Specifies one or more style classes to apply to the table row. Separate multiple values with spaces. |  | "table-row" |  |
| Attributes |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Events

| Name | Description | Mandatory | Observations |
| :--- | :--- | :--- | :--- |
| On Sort | Screen action to be executed to sort the table. |  |  |
| Transition | Transition effect applied when navigating to another screen. |  | By default defined at module level. |
| Event | JavaScript or custom event to be handled. |  |  |
| Handler | JavaScript event handler. |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

