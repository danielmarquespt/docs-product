---
kinds: >-
  ServiceStudio.Model.WebWidgets+RadioButton+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceRadioButton+Kind
helpids: 4045
---

# Radio Button Widget

Two-state toggle control allowing users to select between two options.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Variable | Holds the value entered by the user. | Yes |  |  |
| Validation Parent | Specifies an Edit Record widget. Widgets with the same Validation Parent are validated as a group. |  |  |  |
| Value | Value assigned to the defined variable when this widget is selected. | Yes |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Visible | Boolean literal or expression that defines if the widget is displayed. |  | Yes |  |
| Enabled | Boolean literal or expression that defines if the widget is editable. |  | Yes |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |
| On Change |  |  |  |  |
| Destination | Screen action to be executed or a screen to navigate to when the value of the element changes. |  |  | It might be necessary to specify additional input arguments. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

