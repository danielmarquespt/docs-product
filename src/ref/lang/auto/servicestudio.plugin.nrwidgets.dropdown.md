---
kinds: ServiceStudio.Plugin.NRWidgets.DropdownDescriptor
helpids: 30036
---

# Dropdown

Dropdown list from which the user can select a value.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Variable | Holds the value entered by the user. | Yes |  |  |
| List | Specifies the list of records to show in the dropdown. | Yes |  |  |
| Options Content | 'Text \(Default\)' content provides a native experience for selecting textual values \(uses the select HTML tag\). 'Custom' provides richer content with non-textual widgets \(e.g. images\) inside the dropdown \(uses the div HTML tag\). | Yes | Custom |  |
| Options Text | Attribute of the records in the list to use as the label. |  |  |  |
| Options Value | Attribute of the records in the list to use as the identifier of the selected value. | Yes |  |  |
| Mandatory | Boolean literal or expression that defines if the widget is required. | Yes | False |  |
| Enabled | Boolean literal or expression that defines if the widget is editable. |  | True |  |
| Empty Text | Text literal or expression displayed in the Dropdown list that represents an empty selection. When this option is selected, the variable defined holds a default value. |  |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  | "dropdown" |  |
| Attributes |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Events

| Name | Description | Mandatory | Observations |
| :--- | :--- | :--- | :--- |
| On Change | Screen action to be executed or a screen to navigate to when the value of the element changes. |  |  |
| Transition | Transition effect applied when navigating to another screen. |  | By default defined at module level. |
| Event | JavaScript or custom event to be handled. |  |  |
| Handler | JavaScript event handler. |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |
| Valid | False when required inputs are not present or the input value does not comply with the defined data type. You can override this property value when performing custom validations. |  | Boolean |  |
| ValidationMessage | Message describing the built-in validation constraints not satisfied when 'Valid' is False. You can override this property value when performing custom validations. |  | Text |  |

