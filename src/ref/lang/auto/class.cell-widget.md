---
kinds: >-
  ServiceStudio.Model.WebWidgets+EditRecordCell+Kind,
  ServiceStudio.Model.WebWidgets+ShowRecordCell+Kind,
  ServiceStudio.Model.WebWidgets+TableCell+Kind,
  ServiceStudio.Model.WebWidgets+TableRecordsDataCell+Kind,
  ServiceStudio.Model.WebWidgets+TableRecordsHeaderCell+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceEditRecordCell+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceShowRecordCell+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceTableCell+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceTableRecordsDataCell+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceTableRecordsHeaderCell+Kind
helpids: 0
---

# Cell Widget

Cell of a table.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Height | Height of the widget in pixels. Other accepted units are points\(pt\) or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Vertical Alignment | Specifies the relative vertical alignment of the widgets inside the cell. | Yes |  | The possible values are: "" \(use default alignment\), "Top", "Middle", "Bottom". |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Column Span | Indicates the number of columns that the cell spans across. Merge or split cells using the right-click contextual menu. |  |  |  |
| Row Span | Indicates the number of rows that the cell spans across. Merge or split cells using the right-click contextual menu. |  |  |  |
| Width | Width of the widget in columns. Other accepted units are pixels\(px\), points\(pt\), or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

