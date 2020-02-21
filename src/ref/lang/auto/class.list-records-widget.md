---
kinds: >-
  ServiceStudio.Model.WebWidgets+ListRecords+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceListRecords+Kind
helpids: 4023
---

# List Records Widget

Displays multiple records in a list layout.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Source Record List | Current list of records displayed by the widget. | Yes |  | The expression used in this property \(if present\) is evaluated when a widget runtime property is first used \(e.g. an expression using the list Length runtime property\) or when the widget is rendered. |
| Empty Message | Text displayed in the first row of the widget when there are no records to show. |  | "No items to show..." |  |
| Line Separator | Type of separator to display between records. | Yes | New Line | Possible values are: None, New Line and Bullets. |
| Line Count | Maximum number of rows to display in this widget. | Yes | 50 |  |
| Start Index | Index of the first List item to iterate. Can be an expression. | Yes | 0 | The expression used in this property \(if present\) is evaluated before the web screen preparation. |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  | "ListRecords" |  |
| Empty Message Style | Style applied to the text defined in the Empty Message property. |  |  |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |
| List | Collection of records returned by the performed query. |  | Record List |  |
| LineCount | Maximum number of rows displayed in the widget as defined in the Line Count property. | Yes | Integer |  |
| StartIndex | Index of the first record displayed in the widget as defined in the Start Index property. | Yes | Integer |  |

