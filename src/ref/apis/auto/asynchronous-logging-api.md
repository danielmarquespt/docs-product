# Asynchronous Logging API

For Platform Version 9.0.99.11. Provides methods to asynchronously insert records or event logs into the database. Records are kept in a message queue and bulk inserted after a short period.

## Summary

| Action | Description |
| :--- | :--- |
| [LogError](asynchronous-logging-api.md#LogError%3E) | Asynchronously inserts a error into the database. Errors are kept in a message queue and inserted into the database in bulk after a short period. |
| [LogRecord](asynchronous-logging-api.md#LogRecord%3E) | Asynchronously inserts a record into the database. Records are kept in a message queue and inserted into the database in bulk after a short period. |
| [LogRequestEvent](asynchronous-logging-api.md#LogRequestEvent%3E) | Asynchronously logs a request event. The events are kept in a message queue and inserted in bulk after a short period. |

## Actions

### LogError { \#LogError }

Asynchronously inserts a error into the database. Errors are kept in a message queue and inserted into the database in bulk after a short period. Note that the message queue is non-persistent.

_Inputs_

Instant : Type: DateTime. Mandatory.  
Date and time when the error occurred.

RequestKey : Type: Text.  
The GUID that identifies the request. Use the Request\_GetKey action of the RuntimePlatform API to get this value.

ModuleName : Type: Text. Mandatory.  
Name of the module where the event occurred.

Message : Type: Text. Mandatory.  
A text with the error main message.

Detail : Type: Text.  
A text with the error details.

### LogRecord { \#LogRecord }

Asynchronously inserts a record into the database. Records are kept in a message queue and inserted into the database in bulk after a short period. Note that the message queue is non-persistent.

_Inputs_

Record : Type: Object. Mandatory.  
The record you want to save to the database, converted to Object type. Use the ToObject built-in function for the conversion.

### LogRequestEvent { \#LogRequestEvent }

Asynchronously logs a request event. The events are kept in a message queue and inserted in bulk after a short period.

_Inputs_

Instant : Type: DateTime. Mandatory.  
Date and time when the event occurred.

RequestKey : Type: Text. Mandatory.  
The GUID that identifies the request. Use the Request\_GetKey action of the RuntimePlatform API to get this value.

RequestEventName : Type: Text. Mandatory.  
Name of the event.

ModuleKey : Type: Text. Mandatory.  
Unique identifier of the module where the event occurred. Use the GetEspace action with the GetOwnerEspaceIdentifier\(\) built-in function to get this information.

ModuleName : Type: Text. Mandatory.  
Name of the module where the event occurred. Use the GetEspace action with the GetOwnerEspaceIdentifier\(\) built-in function to get this information.

ApplicationKey : Type: Text. Mandatory.  
Unique identifier of the application where the event occurred. Query the ‘Application’ system entity to get this information.

ApplicationName : Type: Text. Mandatory.  
Name of the application where the event occurred. Query the ‘Application’ system entity to get this information.

RequestEventDetails : Type: Text.  
A text with event details in JSON format. It is a regular JSON object with the fields ‘Key’ and ‘Value’.

