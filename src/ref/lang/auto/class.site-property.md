---
kinds: ServiceStudio.Model.Variables+SiteProperty+Kind
helpids: 15003
---

# Site Property

Global variable that has a constant value, or a value that does not change often.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data Type | The data type of the site property. | Yes |  |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |
| Advanced |  |  |  |  |
| Is Multi-tenant | Set to Yes to enable muti-tenancy for this specific element. Overrides the multi-tenancy definitions inherited from the module. | Yes |  |  |

