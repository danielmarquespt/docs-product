---
kinds: >-
  ServiceStudio.Model.WebWidgets+InputFilename+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceInputFilename+Kind
helpids: 4040
---

# Upload Widget

Field to select a file to be uploaded to the server when the user submits the form.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Validation Parent | Specifies an Edit Record widget. Widgets with the same Validation Parent are validated as a group. |  |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Visible | Boolean literal or expression that defines if the widget is displayed. |  | Yes |  |
| Enabled | Boolean literal or expression that defines if the widget is editable. |  | Yes |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Content | Binary content of the file specified in the widget. |  | Binary Data |  |
| Type | Content-type provided by the browser. |  | Text |  |
| Filename | Name of the file specified in the widget. Does not include the path of the file. |  | Text |  |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

