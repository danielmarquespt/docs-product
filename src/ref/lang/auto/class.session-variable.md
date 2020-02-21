---
kinds: ServiceStudio.Model.Variables+SessionVariable+Kind
helpids: 15001
---

# Session Variable

Holds data that is persisted during the session and can be used to save information during the end-user interaction. Only available in web apps.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data Type | The variable data type. | Yes |  |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  | The default value of a session variable must be a literal. |

