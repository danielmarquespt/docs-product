---
kinds: >-
  ServiceStudio.Model.WebWidgets+Input+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceInput+Kind
helpids: 4024
---

# Input Widget

Field allowing the user to input data.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Variable | Holds the value entered by the user. | Yes |  |  |
| Validation Parent | Specifies an Edit Record widget. Widgets with the same Validation Parent are validated as a group. |  |  |  |
| Mandatory | Boolean literal or expression that defines if the user input is required. | Yes | No |  |
| Null Value | Value assigned to the variable when no user input is provided. |  |  | If this property is not specified, the default value for the data type is used. |
| Max. Length | Maximum number of characters allowed. |  | 50 |  |
| Text Lines | Line-height of the widget. |  | 1 |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Visible | Boolean literal or expression that defines if the widget is displayed. |  | Yes |  |
| Enabled | Boolean literal or expression that defines if the widget is editable. |  | Yes |  |
| Type | HTML5 input element type. Allows a better input control and extra functionality. | Yes | Text | Available element types: Text: the input allows any text; Number: the input allows numeric values; Email: the input allows email addresses; Search: the input is used to provide search field.  The specific behavior defined by this property value varies from browser to browser.   The Date and DateTime types must follow the configurable format specified in the environment console for all the applications. When changing the format, re-publish the modules for the change to take effect.  The default format is `yyyy-mm-dd` \(e.g. 2006-03-15\). |
| Prompt | Text hint that describes the expected value of the input. Hides when the field has focus or is no longer empty. |  |  |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |
| On Change |  |  |  |  |
| Destination | Screen action to be executed or a screen to navigate to when the value of the element changes. |  |  | It might be necessary to specify additional input arguments. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| TypedValue | Value entered by the user at the time the input was submitted. | Yes | Text |  |
| Valid | False when required inputs are not present or the input value does not comply with the defined data type. You can override this property value when performing custom validations. |  | Boolean |  |
| ValidationMessage | Message describing the built-in validation constraints not satisfied when 'Valid' is False. You can override this property value when performing custom validations. |  | Text |  |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

