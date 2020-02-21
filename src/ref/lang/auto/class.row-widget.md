---
kinds: >-
  ServiceStudio.Model.WebWidgets+EditRecordRow+Kind,
  ServiceStudio.Model.WebWidgets+ShowRecordRow+Kind,
  ServiceStudio.Model.WebWidgets+TableRecordsDataRow+Kind,
  ServiceStudio.Model.WebWidgets+TableRow+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceEditRecordRow+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceShowRecordRow+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceTableRecordsDataRow+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceTableRow+Kind
helpids: 0
---

# Row Widget

Row of a table.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

