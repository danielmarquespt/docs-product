---
kinds: >-
  ServiceStudio.Model.WebWidgets+Container+Kind,
  ServiceStudio.Model.WebWidgets+EmailContainer+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceContainer+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceEmailContainer+Kind
helpids: 4047
---

# Container Widget

Groups widgets and apply styles to them. Translates into an HTML div element.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Display | Boolean literal or expression that defines if the widget is displayed. |  | True | Be aware that this property does not have the same behavior as the "Visible" property of other widgets. When set to false, the HTML for the widget is still generated, and can be accessed and manipulated, for example, using JavaScript. |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |
| On Click |  |  |  |  |
| Destination | Screen to which to navigate. |  |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

