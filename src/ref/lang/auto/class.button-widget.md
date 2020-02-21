---
kinds: >-
  ServiceStudio.Model.WebWidgets+Button+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceButton+Kind
helpids: 4009
---

# Button Widget

Provides a button that users can click or tap to trigger an action.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Label | Text literal or expression to be displayed in this widget. |  | "Ok" |  |
| Example | Text to display in Preview and Design modes. |  |  |  |
| Validation Parent | Specifies an Edit Record widget. Widgets with the same Validation Parent are validated as a group. |  |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Visible | Boolean literal or expression that defines if the widget is displayed. |  | Yes |  |
| Enabled | Boolean literal or expression that defines if the widget is editable. |  | Yes |  |
| Is Default | Set to Yes to define this widget as the screen or block default target when the user presses Enter. | Yes | No | In your web screens or web blocks you can define one default button or link. When you define a Button or Link widget as default, it means that pressing the `ENTER` key in an Input, Input Password, Select or Check Box widget has the same effect as pressing the button or the link. |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |
| On Click |  |  |  |  |
| Destination | Screen to which to navigate. | Yes |  |  |
| Method | Specifies how the inputs are to be submitted. | Yes | Submit | The possible values are:  **Submit**: the inputs are submitted. Uses the `POST` HTTP method;  **Ajax Submit**: all the inputs you use in the Destination logic are asynchronously submitted \(using Ajax techniques\) while keeping the state of the screen;  **Navigate**: the inputs are ignored. Uses the `GET` HTTP method. |
| Validation | Specifies input validation to be used. | Yes | Server | The possible values are:  **Client & Server**: built-in validations are performed before submitting to the server;  **Server**: validation is performed server-side;  **None**. |
| Confirmation Message | Text literal or expression to define the confirmation message displayed after clicking the button. |  |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

