---
kinds: ServiceStudio.Plugin.NRWidgets.ButtonGroupItemDescriptor
helpids: 30075
---

# Button Group Item

Individual item representing an option within a ButtonGroup widget.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Value | Value assigned to the Button Group widget variable when this item is selected. | Yes |  |  |
| Enabled | Boolean literal or expression that defines if the widget is editable. |  | True |  |
| Visible | Boolean literal or expression that defines if the widget is displayed. | Yes | True |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  | "button-group-item" |  |
| Attributes |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Events

| Name | Description | Mandatory | Observations |
| :--- | :--- | :--- | :--- |
| Event | JavaScript or custom event to be handled. |  |  |
| Handler | JavaScript event handler. |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

