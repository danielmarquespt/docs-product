---
kinds: >-
  ServiceStudio.Model.WebWidgets+TableRecords+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceTableRecords+Kind
helpids: 4042
---

# Table Records Widget

Displays a list in a tabular layout.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Source Record List | Current list of records displayed by the widget. | Yes |  | The expression used in this property \(if present\) is evaluated when a widget runtime property is first used \(e.g. an expression using the list Length runtime property\) or when the widget is rendered. |
| Empty Message | Text displayed in the first row of the widget when there are no records to show. |  | "No items to show..." |  |
| Line Count | Maximum number of rows to display in this widget. | Yes | 50 |  |
| Start Index | Index of the first List item to iterate. Can be an expression. | Yes | 0 | The expression used in this property \(if present\) is evaluated before the web screen preparation. |
| Cell Height | Height of cells in the table in pixels. Other accepted units are points\(pt\) or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Cell Spacing | Space between cells in pixels. Overrides the style sheet definition. |  |  |  |
| Show Header | Set as Yes to display the header row of the table. | Yes | Yes |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  | "TableRecords" |  |
| Header Style | Specifies one or more style classes to apply to the header of the widget. Separate multiple values with spaces. |  | "TableRecords\_Header" |  |
| Odd Line Style | Specifies one or more style classes to apply to the odd lines of the widget \(excluding the header\). Separate multiple values with spaces. |  | "TableRecords\_OddLine" |  |
| Even Line Style | Specifies one or more style classes to apply to the even lines of the widget \(excluding the header\). Separate multiple values with spaces. |  | "TableRecords\_EvenLine" |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| List | Collection of records returned by the performed query. |  | Record List |  |
| LineCount | Maximum number of rows displayed in the widget as defined in the Line Count property. | Yes | Integer |  |
| StartIndex | Index of the first record displayed in the widget as defined in the Start Index property. | Yes | Integer |  |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

