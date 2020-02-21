---
kinds: >-
  ServiceStudio.Model.WebWidgets+ComboBox+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceComboBox+Kind
helpids: 4027
---

# Combo Box Widget

Dropdown allowing the user to select a value from a list.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Variable | Holds the value entered by the user. |  |  | Mandatory if Source Entity/Structure is specified. |
| Validation Parent | Specifies an Edit Record widget. Widgets with the same Validation Parent are validated as a group. |  |  |  |
| Mandatory | Boolean literal or expression that defines if the user input is required. | Yes | No |  |
| Source Record List | Current list of records displayed by the widget. |  |  |  |
| Source Entity | Data entity to populate the widget. |  |  |  |
| Source Attribute | Specifies the attribute of the records in the list to populate the widget. |  |  |  |
| Source Identifier Attribute | Attribute of the structure to be used as the identifier of the selected value. |  |  |  |
| Special Variable | Holds the value selected by the user if this value belongs to the defined Special List. |  |  | The variable must be of type Text, Phone Number, Email, Boolean, Integer, or Long Integer. At runtime, if the user selects a value among the Source Entity/Structure list of values, this property will have the value "". |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Visible | Boolean literal or expression that defines if the widget is displayed. |  | Yes |  |
| Enabled | Boolean literal or expression that defines if the widget is editable. |  | Yes |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |
| On Change |  |  |  |  |
| Destination | Screen action to be executed or a screen to navigate to when the value of the element changes. |  |  | It might be necessary to specify additional input arguments. |
| Special List |  |  |  |  |
| Value | Value assigned to the Special Variable. |  |  |  |
| Option | Text displayed in the widget. |  |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| SpecialListValue | SpecialListValue runtime property is deprecated. Consider using the Special Variable property instead. |  | Text |  |
| Valid | Always True for Combo Boxes. You can override this property value when performing custom validation. |  | Boolean |  |
| ValidationMessage | Message describing the built-in validation constraints not satisfied when 'Valid' is False. You can override this property value when performing custom validations. |  | Text |  |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

