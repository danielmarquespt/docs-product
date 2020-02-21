---
kinds: ServiceStudio.Model.ProcessNodes+Activity+Kind
helpids: 0
---

# Automatic Activity

Executes an action flow to do work without the intervention of the end-user.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Text displayed in the back-office when an instance of this Automatic Activity is executed. |  |  | If not defined, the displayed text will be the Automatic Activity name. |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Advanced |  |  |  |  |
| Start Date | Optional date that defines when the activity is scheduled to become available to be handled. Can be an expression. |  |  | Not supported when using Light Process Execution. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| ClosedInstant | Date and time when the process activity instance was closed. | Yes | Date Time |  |
| ActivityId | Identifier of the process activity instance at runtime. | Yes |  |  |

