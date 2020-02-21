---
kinds: >-
  ServiceStudio.Model.WebWidgets+ListBox+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceListBox+Kind
helpids: 4041
---

# List Box Widget

Allows the selection of one or more values from a dropdown list of possible values.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Validation Parent | Specifies an Edit Record widget. Widgets with the same Validation Parent are validated as a group. |  |  |  |
| Source Record List | Current list of records displayed by the widget. | Yes |  |  |
| Source Attribute | Specifies the attribute of the records in the list to populate the widget. | Yes |  |  |
| Selection Mode | Specifies if the user can select only a single item or multiple items from the list. | Yes | Multiple | The possible values are: Multiple and Single. |
| Selection Attribute | Boolean attribute of the records in the list that holds if a value is selected or not. If using a list from an Aggregate, you can add a new Boolean attribute in the Aggregate. | Yes |  |  |
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
| List | Collection of records returned by the performed query. |  | Record List |  |
| Valid | Always True for List Boxes. You can override this property value when performing custom validation. |  | Boolean |  |
| ValidationMessage | Message describing the built-in validation constraints not satisfied when 'Valid' is False. You can override this property value when performing custom validations. |  | Text |  |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

