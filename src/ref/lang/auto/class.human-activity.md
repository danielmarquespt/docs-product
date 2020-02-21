---
kinds: >-
  ServiceStudio.Model.ProcessNodes+HumanActivity+Kind,
  ServiceStudio.Model.ReferenceHumanActivity+Kind
helpids: 0
---

# Human Activity

Activity to be executed by an end-user.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Text displayed in the Taskbox and in the back-office when an instance of this Human Activity is executed. |  |  | If not defined, the displayed text will be the Human Activity name. |
| Public | Indicates whether this process activity can be used by other modules. | Yes | No | This property is only available for process activities that were created in the current module. When a process activity is public its process must also be public. |
| User | Defines the user that is going to complete the activity. Can be an expression. |  |  |  |
| Close On | Entity action that automatically ends the Human Activity execution. |  |  | The event that automatically closes \(ends\) the process activity execution:   **Create &lt;entity&gt;:** the Human Activity is closed when a record is created for the specified entity;   **Update &lt;entity&gt;:** the Human Activity is closed when a record is updated for the specified entity. |
| Destination | Screen where the user will complete the Human Activity work after opening this activity in the Taskbox. |  |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| End-User Information |  |  |  |  |
| Detail | Description of the Human Activity to be displayed to the user in the Taskbox. Can be an expression. |  |  |  |
| Instructions | Instructions on how to complete the Human Activity work to be displayed to the user in the Taskbox. |  |  |  |
| Due Date | Optional date to inform the end-user when is the due date of the activity. Can be an expression. |  |  |  |
| Advanced |  |  |  |  |
| Allow Skip | If set to True, the execution of a failed activity may be skipped. | Yes | No | If skip is allowed, the end user's Taskbox displays an option to skip a failed activity. This option cannot skip a wait activity, use the system action ActivitySkip instead. |
| Start Date | Optional date that defines when the activity is scheduled to become available to be handled. Can be an expression. |  |  |  |
| Roles |  |  |  |  |
| Roles | List of the Roles available in your module. Allows selection of the roles that have grants to carry out the Human Activity work. |  | Registered ApplicationUser |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| ClosedBy | Identifier of the end-user that closed the process activity instance. | Yes |  |  |
| ClosedInstant | Date and time when the process activity instance was closed. | Yes | Date Time |  |
| Skipped | True if the process activity instance ended because it was skipped. | Yes | Boolean |  |
| ActivityId | Identifier of the process activity instance at runtime. | Yes |  |  |

