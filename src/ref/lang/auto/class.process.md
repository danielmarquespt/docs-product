---
kinds: >-
  ServiceStudio.Model.Flows+Process+Kind,
  ServiceStudio.Model.ReferenceProcess+Kind
helpids: 17016
---

# Process

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No | This property is only available for processes that were created in the current module. When a process is set to public its process entity is also made public. |
| Launch On | Entity action that automatically starts the execution of a new process instance. |  |  | When an entity action is chosen, the primary key of the entity is automatically added as an input parameter of the process. This way, each process instance has a reference indicating the entity record it is related to. |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| End-User Information |  |  |  |  |
| Label | Name of the Process to be displayed to the end-user. |  |  |  |
| Detail | Description to be used as the default Detail property of Human Activities in the process flow. |  |  | This property should be defined when the Launch On property is not defined or, if defined, when the Entity referred in it does not have any Text attribute. These properties are used to calculate a default value for the Detail property of Human Activities that don't have that property specified.  You can use expressions to build dynamic descriptions, giving more contextual information to the end-user. |
| Advanced |  |  |  |  |
| Expose Process Entity | Set to Yes to make the corresponding Process Entity become available in the Entities folder. | Yes | No |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| ProcessId | Identifier of the process instance at runtime. | Yes |  |  |

