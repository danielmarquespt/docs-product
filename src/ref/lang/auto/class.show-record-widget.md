---
kinds: >-
  ServiceStudio.Model.WebWidgets+ShowRecord+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceShowRecord+Kind
helpids: 4022
---

# Show Record Widget

Displays a record.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Source Record | Current record being edited in the widget. | Yes |  |  |
| Display Columns | Specifies if the widget presents records in one or two columns. | Yes | 1 |  |
| Label Width | Width of the label in columns. Other accepted units are pixels\(px\), points\(pt\), or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Cell Height | Height of cells in the table in pixels. Other accepted units are points\(pt\) or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Cell Spacing | Space between cells in pixels. Overrides the style sheet definition. |  |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  | "ShowRecord" |  |
| Label Style | Specifies one or more style classes to apply to labels. Separate multiple values with spaces. |  | "ShowRecord\_Caption" |  |
| Value Style | Specifies one or more style classes to apply to values. Separate multiple values with spaces. |  | "ShowRecord\_Value" |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Record | Current record being displayed in the widget. | Yes | Record |  |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

