# Close Wait Action

Use the **Close&lt;Wait Name&gt;** [process activity extended action](intro.md) in an action flow to close a **Wait** activity. Once closed, the Wait activity ends its execution.

 Closing \[Wait\]\(\) activities demands advanced knowledge about the Platform to either obtain the Wait activity identifier or supply the activity identifier to the Screen Actions.

## Input parameters

* **ActivityId**: id of the activity instance. \(Type: Activity Identifier; Mandatory\)
* **Wait Input Parameters**: one parameter for each input parameter in the Wait activity definition.

 The input parameters must be in the same order and of the same type as what is defined in the Wait activity.

