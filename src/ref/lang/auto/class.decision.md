---
kinds: ServiceStudio.Model.ProcessNodes+Decision+Kind
helpids: 0
---

# Decision

Branches the process flow into one of multiple paths depending on the outcome of an action flow.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Text displayed in the back-office when an instance of this Decision activity is executed. |  |  | If not defined, the displayed text will be the Decision activity name. |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| ClosedInstant | Date and time when the process activity instance was closed. | Yes | Date Time |  |
| ActivityId | Identifier of the process activity instance at runtime. | Yes |  |  |

