---
kinds: >-
  ServiceStudio.Model.ProcessNodes+WaitActivity+Kind,
  ServiceStudio.Model.ReferenceWaitActivity+Kind
helpids: 0
---

# Wait

Pauses the process flow until a specific event occurs.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Text displayed in the back-office when an instance of this Wait activity is executed. |  |  | If not defined, the displayed text will be the Wait process activity name. |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Public | Indicates whether this process activity can be used by other modules. | Yes | No | This property is only available for process activities that were created in the current module. When a process activity is public its process must also be public. |
| Close On | Entity action that automatically ends the Wait Activity execution. |  |  | The event that automatically closes \(ends\) the process activity execution:   **Create &lt;entity&gt;:** the Wait is ended when a record is created for the specified entity;   **Update &lt;entity&gt;:** the Wait is ended when a record is updated for the specified entity. |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Advanced |  |  |  |  |
| Timeout | Date and time until the Wait activity pauses the process flow execution. |  |  | You may set the timeout date in two ways:   **Absolute:** the timeout date is fixed.  For example: `#2015-01-01 00:00:00#`   **Relative:** the timeout date depends on the current moment. For example, if you want to wait a day then define your timeout date as: `AddDays(CurrDateTime(),1)`  This value is defined as a Date Time. |
| Allow Skip | If set to True, the activity execution may be skipped. | Yes | No |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| ClosedInstant | Date and time when the process activity instance was closed. | Yes | Date Time |  |
| Expired | True if the process activity instance ended because of a timeout. | Yes | Boolean |  |
| Skipped | True if the process activity instance ended because it was skipped. | Yes | Boolean |  |
| ActivityId | Identifier of the process activity instance at runtime. | Yes |  |  |

