---
kinds: ServiceStudio.Plugin.NRWidgets.ListDescriptor
helpids: 30030
---

# List

Presents a list of records.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Source | Specifies a list with records to populate the widget. | Yes |  |  |
| Animate Items | Set to Yes to Animate Items on append, insert or remove. |  | Yes |  |
| Mode | Set to Custom to define a custom HTML tag to be used by the widget in runtime. Default mode sets tag as div. | Yes | Default |  |
| Tag | Wrapper HTML tag to be used by this widget in runtime. | Yes | div | Only available when Mode is set to Custom. |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  | "list list-group" |  |
| Attributes |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Events

| Name | Description | Mandatory | Observations |
| :--- | :--- | :--- | :--- |
| On Scroll Ending | Screen action to be executed or a screen to navigate to when the user scrolling is nearing the end of the loaded list. |  |  |
| Transition | Transition effect applied when navigating to another screen. |  | By default defined at module level. |
| Event | JavaScript or custom event to be handled. |  |  |
| Handler | JavaScript event handler. |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

