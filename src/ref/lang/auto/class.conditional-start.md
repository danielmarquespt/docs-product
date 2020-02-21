---
kinds: >-
  ServiceStudio.Model.ProcessNodes+ConditionalStart+Kind,
  ServiceStudio.Model.ReferenceConditionalStart+Kind
helpids: 0
---

# Conditional Start

Starts an alternative flow in the process flow.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Text displayed in the back-office when an instance of this Conditional Start activity is executed. |  |  | If not defined, the displayed text will be the Conditional Start activity name. |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Public | Indicates whether this process activity can be used by other modules. | Yes | No | This property is only available for process activities that were created in the current module. When a process activity is public its process must also be public. |
| Start On | Entity action that automatically starts the execution of the Conditional Start flow. |  |  | When an entity event is chosen, the primary key of the entity is automatically added as an input parameter of the process. In this way each process instance has a reference indicating which entity record it is related to.   Entity actions that start the exectution:  **Create &lt;entity&gt;:** the Conditional Start begins the execution of the flow when a record is created for the specified entity;   **Update &lt;entity&gt;:** the Conditional Start begins the execution of the flow when a record is updated for the specified entity.   |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| StartedBy | Identifier of the user who started the process activity instance. | Yes |  |  |
| StartedInstant | Date and time when the process activity instance was started. | Yes | Date Time |  |
| ActivityId | Identifier of the process activity instance at runtime. | Yes |  |  |

