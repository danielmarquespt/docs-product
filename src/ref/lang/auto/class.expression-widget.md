---
kinds: >-
  ServiceStudio.Model.WebWidgets+InlineExpression+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceInlineExpression+Kind
helpids: 4020
---

# Expression Widget

Displays a text literal or an expression to be calculated at runtime.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Value | Combination of values, operands, operators and variables or the result of a function whose value is computed at runtime. | Yes |  |  |
| Example | Text to display in Preview and Design modes. |  |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Escape Content | Set as No to display directly the results of your expression in the screen content or set to Yes to perform escaping. | Yes | Yes | Escaping an expression means that all accented and other special characters are replaced by a sequence that does not interfere with the protocols being used. In mobile apps expressions are escaped by default. |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

