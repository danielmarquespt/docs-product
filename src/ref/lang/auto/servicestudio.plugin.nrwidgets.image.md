---
kinds: ServiceStudio.Plugin.NRWidgets.ImageDescriptor
helpids: 30043
---

# Image

Displays an image from a defined source.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Type | Specifies the source of the image: Local Image, External URL or Binary Data. | Yes | Local Image |  |
| Image | Defines the image to display when Type is set to Local Image. |  |  | Only available when Type is set as Local. |
| URL | Defines the URL of the image to display when Type is set to External URL. |  |  | Only available when Type is set as External URL. |
| Image Content | Defines the image to display when Type is set to Binary Data. |  |  | Only available when Type is set as Binary Data. |
| Default Image | Image to display when the Binary Data image cannot be fetched. |  |  | Only available when Type is set as Binary Data. |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
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

