---
kinds: >-
  ServiceStudio.Model.Nodes+WebScreen+Kind,
  ServiceStudio.Model.ReferenceWebScreen+Kind
helpids: 4011
---

# Web Screen

User interface that end-users interact with.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Title | Text literal or expression displayed in the title bar of the browser. |  |  | When this property is empty, the title bar has the name of the element. |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Advanced |  |  |  |  |
| HTTP Security | Security level required for HTTP requests. Can be overridden by application security settings in Service Center or LifeTime. | Yes |  | The possible values are: "" \(empty\), None, SSL/TLS, SSL/TLS with client certificates. |
| Integrated Authentication | Set to Yes to use Integrated Authentication to validate user access. | Yes |  | An empty value means that the element inherits the integrated authentication specified at flow level. |
| Cache in Minutes | Maximum time content or results are stored in memory. When undefined, nothing is cached. |  |  |  |
| Is Frequent Destination | Set to Yes to make this element visible as a quick option in Destination lists. | Yes | No |  |
| Style Sheet | Style sheet associated with this element. |  |  | Click on "..." to edit the property value. |
| JavaScript | JavaScript associated with this element. |  |  | Click on "..." to edit the property value. |
| Roles |  |  |  |  |
| Roles | List of the Roles available in your module. Allows selection of the roles that have grants to display the web screen. |  | Anonymous \(unselected\) Registered ApplicationUser |  |
| Extended Properties |  |  |  |  |
| Property | Name of an attribute to add to the HTML translation for this element. |  |  | You can pick a property from the drop-down list or type a free text. The name of the property will not be validated by the platform.  Duplicated properties are not allowed. Spaces, " or ' are also not allowed. |
| Value | Value of the attribute. |  |  | You can type the value directly or write expressions using the Expression Editor.  If the Value is empty, the corresponding HTML tag is created as property="property". For example, the nowrap property does not require a value, therefore nowrap="nowrap" is added. |

