---
kinds: >-
  ServiceStudio.Model.NRWebWidgets+Placeholder+Kind,
  ServiceStudio.Model.WebWidgets+Placeholder+Kind,
  ServiceStudio.Model.NRWebWidgets+ReferencePlaceholder+Kind,
  ServiceStudio.Model.WebWidgets+ReferencePlaceholder+Kind
helpids: 17142
---

# Placeholder Widget

Reserves space to be designed later in the context where the block is used.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text documenting the widget. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Align | Specifies the horizontal alignment of the widgets inside this widget. | Yes |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Is Ajax Refreshed | Read-only property informing if the placeholder, or one of its containers, is refreshed by an Ajax Refresh. | Yes | No | This is useful to understand the placeholders design in the web block regarding refreshing their content. |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

