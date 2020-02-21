---
kinds: >-
  ServiceStudio.Model.WebWidgets+Image+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceImage+Kind
helpids: 4044
---

# Image Widget

Displays an image from a defined source.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Label | Text literal or expression used as a tooltip when hovering the image or displayed when the image cannot be displayed. |  |  |  |
| Image | Defines the image to be displayed when the Type property is set to Static. |  |  | The semantics of this property depends on the Type property value:  **Static**: Defines the image to be displayed both at development time and at runtime;  **Database**: Defines the image to be displayed at development time. At runtime, the Image property is ignored;  **External**: The Image property is ignored. |
| Type | Specifies the source type of the image: Static, External or Database. | Yes | Static |  |
| URL | Text literal or expression defining the URL of the image when Type property is set to External. |  |  | Mandatory when Type has the value External. |
| Filename | Text literal or expression with the name of the file, including the extension. |  |  | Mandatory when Type has the value Database. |
| Cache | Maximum time the image is stored in cache when Type property is set to Database. | Yes | 1 Week | Mandatory when Type has the value Database. |
| Attribute | Entity attribute that contains the image when Type property is set to Database. |  |  | Mandatory when Type has the value Database. |
| Entity Identifier | Entity Identifier \(literal or expression\) of the image you want to display when Type property is set to Database. |  |  | Mandatory when Type has the value Database. |
| Width | Expression that defines the width of the image in pixels. Other accepted units are points\(pt\) or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Height | Height of the widget in pixels. Other accepted units are points\(pt\) or percentage\(%\). Overrides the style sheet definition. |  |  |  |
| Style Classes | Specifies one or more style classes to apply to the widget. Separate multiple values with spaces. |  |  |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

