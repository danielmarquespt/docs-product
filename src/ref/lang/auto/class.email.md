---
kinds: ServiceStudio.Model.Nodes+EmailScreen+Kind
helpids: 0
---

# Email

Allows defining the content to send by email.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Subject | Subject of the email. | Yes |  |  |
| Advanced |  |  |  |  |
| Style Sheet | Specifies one or more style classes to apply to the email. Separate multiple values with spaces. |  |  | Click on "..." to edit the property value. |
| Extended Properties |  |  |  |  |
| Property | One or more extended properties for enhanced control of email headers \(also known as MIME headers\). |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the extended property. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

