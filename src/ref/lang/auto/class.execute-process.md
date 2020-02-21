---
kinds: ServiceStudio.Model.ProcessNodes+ExecuteProcess+Kind
helpids: 0
---

# Execute Process

Executes another process as an activity of the current process.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Text displayed in the back-office when an instance of this Execute Process activity is executed. |  |  | If not defined, the displayed text will be the Execute Process activity name. |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Process | Process that is executed by the process activity. | Yes |  | Read-only. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| ClosedInstant | Date and time when the process activity instance was closed. | Yes | Date Time |  |
| ActivityId | Identifier of the process activity instance at runtime. | Yes |  |  |

