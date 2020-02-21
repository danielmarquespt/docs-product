---
kinds: ServiceStudio.Plugin.Widgets.EditableTableDescriptor
helpids: 17196
---

# Editable Table Widget

Displays content in a tabular layout and allows users to edit and create records.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Source Record List | Specifies a list with records to populate the widget. | Yes |  |  |
| Width | Width of the widget in columns. Other accepted units are pixels\(px\), points\(pt\), or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Margin Left | Left margin of the widget in columns. Other accepted units are pixels\(px\), points\(pt\), or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Margin Top | Top margin of the widget in pixels. Other accepted units are points\(pt\) or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Line Count | Maximum number of rows to display in the widget. | Yes | 50 |  |
| Show Header | Set as Yes to display the header row of the table. |  | Yes |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  | EditableTable |  |
| Enabled | Boolean literal or expression that defines if the widget is editable. | Yes | True |  |
| Delete Confirmation Message | Text literal or expression to be displayed to users to confirm the delete record action. |  |  |  |
| Add Record Message | Text to display in the link to add a new record. |  |  |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Events

| Name | Description | Mandatory | Observations |
| :--- | :--- | :--- | :--- |
| On Row Save | Screen action to be executed to persist new records or record updates. |  |  |
| On Row Delete | Screen action to be executed when a record is removed. |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |
| List | Collection of records returned by the performed query. | Yes | List |  |
| LineCount | Maximum number of rows displayed in the widget as defined in the Line Count property. | Yes | Integer |  |

