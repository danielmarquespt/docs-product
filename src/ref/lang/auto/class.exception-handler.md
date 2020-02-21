---
kinds: ServiceStudio.Model.Nodes+ErrorHandler+Kind
helpids: 0
---

# Exception Handler

Logic to catch an exception or set of exceptions.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Exception | Type of exception to handle. | Yes |  | There is a call hierarchy for exceptions that determines the error handler behavior. For more info see Exception Handling Mechanism |
| Abort Transaction | Set to Yes to abort the transaction and rollback changes. | Yes | Yes | This property is only available in web apps. |
| Log Error | Set to Yes to log an error when the exception occurs. | Yes | Yes |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| ExceptionMessage | Text that explains the reason for the last error. | Yes | Text |  |

