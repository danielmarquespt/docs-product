# BPT API

For Platform Version 9.0.99.11. Low-level API to create custom inboxes for process activities.

## Summary

| Action | Description |
| :--- | :--- |
| [Activity\_Discard](bpt-api.md#Activity_Discard%3E) | Discards an Activity and the execution of the current Process flow stops, that is, none of the following activities in the flow is executed.%%Remarks:%%This action commits the current transaction. |
| [Activity\_IsValidId](bpt-api.md#Activity_IsValidId%3E) | Checks whether an Activity Identifier is valid for a Kind of activity. |
| [HumanActivity\_AssignToUser](bpt-api.md#HumanActivity_AssignToUser%3E) | Assigns a Human Activity to a User. The human activity is only shown in that user's Taskbox.%%Remarks:%%This action commits the current transaction. |
| [HumanActivity\_CheckRole](bpt-api.md#HumanActivity_CheckRole%3E) | Checks whether a User has the role for executing a Human Activity. |
| [HumanActivity\_FlushPendingEvents](bpt-api.md#HumanActivity_FlushPendingEvents%3E) | Forces a Human Activity to handle immediately all its pending events.%%Remarks:%%This action commits the current transaction. |
| [HumanActivity\_SetDueDate](bpt-api.md#HumanActivity_SetDueDate%3E) | Sets the due date for a Human Activity.%%Remarks:%%This action commits the current transaction. |
| [Process\_BulkDelete](bpt-api.md#Process_BulkDelete%3E) | Deletes all the logged information of instances of top level Processes that have terminated or closed before the given date.%%The information that is deleted is all the logging of: process instances, activities instances, input parameters values, output parameters values, process instances executed within other process instances, etc.%%This action finds all top level process instances and recursively deletes all its subprocess instances, ensuring the meta-model remains consistent.%%In the meta-model, a top level process instance is identified in the Process entity by the condition: Top\_Process\_Id = Id.%%Remarks:%%This action does NOT commit the current transaction. |
| [Process\_Delete](bpt-api.md#Process_Delete%3E) | Deletes all the logged information of an instance of a top level Process, which must be either terminated or closed.%%The information that is deleted is all the logging of: process instance, activities instances, input parameters values, output parameters values, processes instances executed within other process instance, etc.%%This action finds the specified top level process instance and recursively deletes all its subprocess instances, ensuring the meta-model remains consistent.%%In the meta-model, a top level process instance is identified in the Process entity by the condition: Top\_Process\_Id = Id.%%This action will raise an exception in the following situations:%%- The process instance does not exist;%%- The process instance is not a top level process instance;%%- The process instance is not terminated or closed.%%Remarks:%%This action does NOT commit the current transaction. |
| [Taskbox\_Hide](bpt-api.md#Taskbox_Hide%3E) | Add this action to a Preparation to disable the TaskBox on a screen. |

## Actions

### Activity\_Discard { \#Activity\_Discard }

Discards an Activity and the execution of the current Process flow stops, that is, none of the following activities in the flow is executed.

Remarks:  
This action commits the current transaction.

_Inputs_

ActivityId : Type: EntityReference. Mandatory.  
The identifier of the Activity.

### Activity\_IsValidId { \#Activity\_IsValidId }

Checks whether an Activity Identifier is valid for a Kind of activity.

_Inputs_

ActivityId : Type: EntityReference. Mandatory.  
The identifier of the Activity.

Kind : Type: EntityReference. Mandatory.  
The kind of the Activity.

_Outputs_

IsValid : Type: Boolean.  
Returns True if it is a valid identifier of an Activity.

### HumanActivity\_AssignToUser { \#HumanActivity\_AssignToUser }

Assigns a Human Activity to a User. The human activity is only shown in that user's Taskbox.

Remarks:  
This action commits the current transaction.

_Inputs_

HumanActivityId : Type: EntityReference. Mandatory.  
The identifier of the Human Activity.

UserId : Type: EntityReference. Mandatory.  
The identifier of the User.

### HumanActivity\_CheckRole { \#HumanActivity\_CheckRole }

Checks whether a User has the role for executing a Human Activity.

_Inputs_

HumanActivityId : Type: EntityReference. Mandatory.  
The identifier of the Human Activity.

UserId : Type: EntityReference. Mandatory.  
The identifier of the User.

_Outputs_

HasPermission : Type: Boolean.  
Returns True if the user has the role to execute the activity.

### HumanActivity\_FlushPendingEvents { \#HumanActivity\_FlushPendingEvents }

Forces a Human Activity to handle immediately all its pending events.

Remarks:  
This action commits the current transaction.

_Inputs_

HumanActivityId : Type: EntityReference. Mandatory.  
The identifier of the Human Activity.

_Outputs_

ProcessedEvents : Type: Integer.  
Returns the number of pending events handled in the flush.

### HumanActivity\_SetDueDate { \#HumanActivity\_SetDueDate }

Sets the due date for a Human Activity.

Remarks:  
This action commits the current transaction.

_Inputs_

HumanActivityId : Type: EntityReference. Mandatory.  
The identifier of the Human Activity.

DueDate : Type: DateTime. Mandatory.  
The date and time limit for the human activity to be finished.

### Process\_BulkDelete { \#Process\_BulkDelete }

Deletes all the logged information of instances of top level Processes that have terminated or closed before the given date.  
The information that is deleted is all the logging of: process instances, activities instances, input parameters values, output parameters values, process instances executed within other process instances, etc.

This action finds all top level process instances and recursively deletes all its subprocess instances, ensuring the meta-model remains consistent.  
In the meta-model, a top level process instance is identified in the Process entity by the condition: Top\_Process\_Id = Id.

Remarks:  
This action does NOT commit the current transaction.

_Inputs_

ProcessesOlderThan : Type: DateTime. Mandatory.  
The date and time before which processes are to be deleted.

ProcessDefinitionId : Type: EntityReference.  
The identifier of the process definition.

MaxDeletedProcesses : Type: Integer. Default: 1000.  
The maximum number of processes to be deleted. The default is 1000. Set to 0 \(zero\) for unlimited deletes.

_Outputs_

HasMoreToDelete : Type: Boolean.  
Returns True if there are still process instances left to be deleted.

### Process\_Delete { \#Process\_Delete }

Deletes all the logged information of an instance of a top level Process, which must be either terminated or closed.  
The information that is deleted is all the logging of: process instance, activities instances, input parameters values, output parameters values, processes instances executed within other process instance, etc.

This action finds the specified top level process instance and recursively deletes all its subprocess instances, ensuring the meta-model remains consistent.  
In the meta-model, a top level process instance is identified in the Process entity by the condition: Top\_Process\_Id = Id.

This action will raise an exception in the following situations:  
- The process instance does not exist;  
- The process instance is not a top level process instance;  
- The process instance is not terminated or closed.

Remarks:  
This action does NOT commit the current transaction.

_Inputs_

ProcessId : Type: EntityReference. Mandatory.  
The identifier of the process instance.

### Taskbox\_Hide { \#Taskbox\_Hide }

Add this action to a Preparation to disable the TaskBox on a screen.

