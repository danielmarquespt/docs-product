# System Actions

## Summary

| Server Action | Description | Is Function? |
| :--- | :--- | :--- |
| [AbortTransaction](system-actions.md#AbortTransaction%3E) | Issues a database ROLLBACK command that undoes all changes performed on the database since the last commit. |  |
| [ActivityClose](system-actions.md#ActivityClose%3E) | Explicitly closes a Human Activity or a Wait Activity ending the execution.%%The the id of the next Human Activity in sequence is returned, if determined. |  |
| [ActivityGetUrl](system-actions.md#ActivityGetUrl%3E) | Returns the URL of the web screen where an activity will be carried out, once opened. | Yes |
| [ActivityOpen](system-actions.md#ActivityOpen%3E) | Explicitly forces a Human Activity instance to be opened in an end-user's Taskbox. |  |
| [ActivityReset](system-actions.md#ActivityReset%3E) | Releases the Human Activity leaving it to be opened and carried out by another end-user. |  |
| [ActivitySchedule](system-actions.md#ActivitySchedule%3E) | Schedules a date for the Human Activity to be available in the Taskbox. |  |
| [ActivitySetGroup](system-actions.md#ActivitySetGroup%3E) | Limit a Human Activity visibility and handling to end-users who belong to a specific group. |  |
| [ActivitySkip](system-actions.md#ActivitySkip%3E) | Explicitly skips the execution of a Human Activity or a Wait Activity.%%The the id of the next Human Activity in sequence is returned, if determined. |  |
| [ActivityStart](system-actions.md#ActivityStart%3E) | Explicitly starts the execution of a ConditionalStart Activity. |  |
| [ClientCertificateGetDetails](system-actions.md#ClientCertificateGetDetails%3E) | Gets the relevant information for the current request client certificate from the .NET framework. |  |
| [ClientCertificateValue](system-actions.md#ClientCertificateValue%3E) | Gets the value of a specific property of the client certificate in the .NET framework. |  |
| [CommitTransaction](system-actions.md#CommitTransaction%3E) | Issues a database COMMIT command that makes effective all changes done on the database since the last commit. |  |
| [Deprecated\_Notify](system-actions.md#Deprecated_Notify%3E) | DEPRECATED: This action is deprecated because Events are now available for Web Blocks. Use Events in Web Blocks to propagate changes from a Web Block to the parent block.%%%%The way a web block has to notify a screen or web block using it. They handle the notification through the action set in their On Notify property. To retrieve a message sent with the notification, use the NotifyGetMessage function. |  |
| [Deprecated\_NotifyGetMessage](system-actions.md#Deprecated_NotifyGetMessage%3E) | DEPRECATED: This action is deprecated because Events are now available for Web Blocks. Use Input Parameters in block Events to send information to the parent block when the Event is triggered.%%%%Returns the notification message sent by the Notify action. | Yes |
| [Deprecated\_NotifyWidget](system-actions.md#Deprecated_NotifyWidget%3E) | The way a web block has to notify a screen or web block using it. They handle the notification through the action set in their On Notify property. To retrieve a message sent with the notification, use the NotifyGetMessage function. |  |
| [EspaceInvalidateCache](system-actions.md#EspaceInvalidateCache%3E) | Invalidates eSpace's specific caches across all Front-end servers and consumer eSpaces. Limit the invalidation to a single tenant by setting the tenant identifier. |  |
| [GenerateGuid](system-actions.md#GenerateGuid%3E) | Generates and returns a new GUID. | Yes |
| [InboundSmsGetDetails](system-actions.md#InboundSmsGetDetails%3E) | DEPRECATED: This action is deprecated because the SMS features are no longer available. Returns information about the inbound SMS that is currently being processed. |  |
| [IntegratedSecurityCheckRole](system-actions.md#IntegratedSecurityCheckRole%3E) | Verifies whether the current Windows user has access to a specific role. | Yes |
| [IntegratedSecurityGetDetails](system-actions.md#IntegratedSecurityGetDetails%3E) | Gets information about the current Windows user that made the request. |  |
| [ListAll](system-actions.md#ListAll%3E) | Determines if all the elements in the list satisfy the given condition. |  |
| [ListAny](system-actions.md#ListAny%3E) | Determines if any of the elements in the list satisfies the given condition. |  |
| [ListAppend](system-actions.md#ListAppend%3E) | Adds an element to the end of a list. |  |
| [ListAppendAll](system-actions.md#ListAppendAll%3E) | Adds the elements of the source list to the end of the destination list. |  |
| [ListClear](system-actions.md#ListClear%3E) | Removes all elements from a list. |  |
| [ListDistinct](system-actions.md#ListDistinct%3E) | Filters duplicate elements from a list. | Yes |
| [ListDuplicate](system-actions.md#ListDuplicate%3E) | Duplicates the elements of a list into another list. | Yes |
| [ListFilter](system-actions.md#ListFilter%3E) | Returns a new list with the elements from the List parameter satisfying the given condition. |  |
| [ListIndexOf](system-actions.md#ListIndexOf%3E) | Returns the position of the first element of the List parameter that satisfies the given condition, or -1 if no element satisfying the condition was found. |  |
| [ListInsert](system-actions.md#ListInsert%3E) | Inserts an element in a specific position of a list. |  |
| [ListRemove](system-actions.md#ListRemove%3E) | Removes an element from a specific position of a list. |  |
| [ListSort](system-actions.md#ListSort%3E) | Sorts the elements of the List parameter by the given criteria. Note that ListSort is different from the dynamic sorting in Aggregates. Multiple attributes having different data types \(such as Text and Integer\) in the criteria may not sort the list correctly. |  |
| [Login](system-actions.md#Login%3E) | Logs a specified user in the application.%%In case of success, 'UserId' and 'Username' session variables are filled with the user data. |  |
| [LoginPassword](system-actions.md#LoginPassword%3E) | Logs a specified user in the application using a password.%%In case of success, 'UserId' and 'Username' session variables are filled with the user data. |  |
| [LogMessage](system-actions.md#LogMessage%3E) | Registers information that can be presented in Service Center in the module general log. |  |
| [Logout](system-actions.md#Logout%3E) | Logs out a specific user from the application.%%The 'UserId' and 'Username' session variables are cleared. |  |
| [ProcessTerminate](system-actions.md#ProcessTerminate%3E) | Explicitly forces a Process to terminate its execution. |  |
| [SetCurrentLocale](system-actions.md#SetCurrentLocale%3E) | Sets the language locale of the user session to change the application presentation language. |  |
| [TenantCreate](system-actions.md#TenantCreate%3E) | Creates a new tenant and associates it with the provisioning site. |  |
| [TenantInvalidateCache](system-actions.md#TenantInvalidateCache%3E) | Invalidates tenant's specific caches across all Front-end servers and eSpaces. This action is now available for compatibility purposes only. Please use the EspaceInvalidateCache action instead and invalidate tenant's specific caches by eSpace to narrow the invalidation scope |  |
| [TenantSwitch](system-actions.md#TenantSwitch%3E) | Change the context to the given tenant identifier. When switching tenant, the session is cleared \(equivalent to an implicit logout, before changing the tenant\), the OnSessionStart actions are executed, and the current transaction is committed. |  |

| Client Action | Description | Is Function? |
| :--- | :--- | :--- |
| [ListAll](system-actions.md#Client_ListAll%3E) | Determines if all the elements in the list satisfy the given condition. |  |
| [ListAny](system-actions.md#Client_ListAny%3E) | Determines if any of the elements in the list satisfies the given condition. |  |
| [ListAppend](system-actions.md#Client_ListAppend%3E) | Adds an element to the end of a list. |  |
| [ListAppendAll](system-actions.md#Client_ListAppendAll%3E) | Adds the elements of the source list to the end of the destination list. |  |
| [ListClear](system-actions.md#Client_ListClear%3E) | Removes all elements from a list. |  |
| [ListDistinct](system-actions.md#Client_ListDistinct%3E) | Filters duplicate elements from a list. | Yes |
| [ListDuplicate](system-actions.md#Client_ListDuplicate%3E) | Duplicates the elements of a list into another list. | Yes |
| [ListFilter](system-actions.md#Client_ListFilter%3E) | Returns a new list with the elements from the List parameter satisfying the given condition. |  |
| [ListIndexOf](system-actions.md#Client_ListIndexOf%3E) | Returns the position of the first element of the List parameter that satisfies the given condition, or -1 if no element satisfying the condition was found. |  |
| [ListInsert](system-actions.md#Client_ListInsert%3E) | Inserts an element in a specific position of a list. |  |
| [ListRemove](system-actions.md#Client_ListRemove%3E) | Removes an element from a specific position of a list. |  |
| [ListSort](system-actions.md#Client_ListSort%3E) | Sorts the elements of the List parameter by the given criteria. Note that ListSort is different from the dynamic sorting in Aggregates. Multiple attributes having different data types \(such as Text and Integer\) in the criteria may not sort the list correctly. |  |
| [LogMessage](system-actions.md#Client_LogMessage%3E) | Registers information that can be presented in Service Center in the module general log. |  |
| [RequireScript](system-actions.md#Client_RequireScript%3E) | Add a Javascript to the html header. Multiple calls for the same Javascript will only add it once. Action flow will proceed after the Javascript has been successfully loaded. |  |

## Server Actions

### AbortTransaction { \#AbortTransaction }

Issues a database ROLLBACK command that undoes all changes performed on the database since the last commit.

### ActivityClose { \#ActivityClose }

Explicitly closes a Human Activity or a Wait Activity ending the execution.  
The the id of the next Human Activity in sequence is returned, if determined.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.

_Outputs_

NextHumanActivityId : Type: Activity Identifier.

### ActivityGetUrl { \#ActivityGetUrl }

Returns the URL of the web screen where an activity will be carried out, once opened.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.

_Outputs_

HandlingUrl : Type: Text.

### ActivityOpen { \#ActivityOpen }

Explicitly forces a Human Activity instance to be opened in an end-user's Taskbox.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.

_Outputs_

HandlingUrl : Type: Text.

### ActivityReset { \#ActivityReset }

Releases the Human Activity leaving it to be opened and carried out by another end-user.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.

ResetActivityUser : Type: mandatory, Boolean.

### ActivitySchedule { \#ActivitySchedule }

Schedules a date for the Human Activity to be available in the Taskbox.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.

StartDate : Type: mandatory, Date Time.

### ActivitySetGroup { \#ActivitySetGroup }

Limit a Human Activity visibility and handling to end-users who belong to a specific group.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.

GroupId : Type: mandatory, Group Identifier.

### ActivitySkip { \#ActivitySkip }

Explicitly skips the execution of a Human Activity or a Wait Activity.  
The the id of the next Human Activity in sequence is returned, if determined.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.

_Outputs_

NextHumanActivityId : Type: Activity Identifier.

### ActivityStart { \#ActivityStart }

Explicitly starts the execution of a ConditionalStart Activity.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.

_Outputs_

NextHumanActivityId : Type: Activity Identifier.

### ClientCertificateGetDetails { \#ClientCertificateGetDetails }

Gets the relevant information for the current request client certificate from the .NET framework.

_Outputs_

cookie : Type: Text.  
Gets the unique Id for the client certificate, if provided.

flags : Type: Integer.  
A set of flags that provide additional client certificate information. Bit0 is set to 1 if the client certificate is present. Bit1 is set to 1 if the Certificate Authority \(CA\) of the client certificate is not in the list of recognized CAs on the server.

isPresent : Type: Boolean.  
Gets a value that indicates whether the client certificate is present.

issuer : Type: Text.  
A string that contains a list of subfield values containing information about the certificate issuer.

isValid : Type: Boolean.  
Gets a value that indicates whether the client certificate is valid.

serialNumber : Type: Text.  
Provides the certificate serial number as an ASCII representation of hexadecimal bytes separated by hyphens. For example, 04-67-F3-02.

serverIssuer : Type: Text.  
Gets the issuer field of the server certificate.

serverSubject : Type: Text.  
Gets the subject field of the server certificate.

subject : Type: Text.  
Gets the subject field of the client certificate.

validFrom : Type: Date Time.  
Gets the date when the certificate becomes valid. The date varies with international settings.

validUntil : Type: Date Time.  
Gets the certificate expiration date

### ClientCertificateValue { \#ClientCertificateValue }

Gets the value of a specific property of the client certificate in the .NET framework.

_Inputs_

key : Type: mandatory, Text.

_Outputs_

value : Type: Text.

### CommitTransaction { \#CommitTransaction }

Issues a database COMMIT command that makes effective all changes done on the database since the last commit.

### Deprecated\_Notify { \#Deprecated\_Notify }

DEPRECATED: This action is deprecated because Events are now available for Web Blocks. Use Events in Web Blocks to propagate changes from a Web Block to the parent block.

The way a web block has to notify a screen or web block using it. They handle the notification through the action set in their On Notify property. To retrieve a message sent with the notification, use the NotifyGetMessage function.

_Inputs_

Message : Type: optional, Text.

### Deprecated\_NotifyGetMessage { \#Deprecated\_NotifyGetMessage }

DEPRECATED: This action is deprecated because Events are now available for Web Blocks. Use Input Parameters in block Events to send information to the parent block when the Event is triggered.

Returns the notification message sent by the Notify action.

_Outputs_

Message : Type: Text.

### Deprecated\_NotifyWidget { \#Deprecated\_NotifyWidget }

The way a web block has to notify a screen or web block using it. They handle the notification through the action set in their On Notify property. To retrieve a message sent with the notification, use the NotifyGetMessage function.

_Inputs_

Message : Type: optional, Text.

### EspaceInvalidateCache { \#EspaceInvalidateCache }

Invalidates eSpace's specific caches across all Front-end servers and consumer eSpaces. Limit the invalidation to a single tenant by setting the tenant identifier.

_Inputs_

EspaceId : Type: optional, Espace Identifier.  
Identifier of the eSpace to invalidate. If not specificed, the identifier of caller eSpace is used.

TenantId : Type: optional, Tenant Identifier.  
Optional tenant identifier to limit the cache invalidation to a specific tenant.

### GenerateGuid { \#GenerateGuid }

Generates and returns a new GUID.

_Outputs_

Guid : Type: Text.

### InboundSmsGetDetails { \#InboundSmsGetDetails }

DEPRECATED: This action is deprecated because the SMS features are no longer available. Returns information about the inbound SMS that is currently being processed.

_Outputs_

MSISDN : Type: Phone Number.

LargeAccount : Type: Phone Number.

Message : Type: Text.

BinaryMessage : Type: Text.

UDH : Type: Text.

MessageId : Type: Text.

Priority : Type: Integer.

Encoding : Type: Text.

Connection : Type: Text.

OperatorCode : Type: Text.

Sent : Type: Date Time.

Custom1 : Type: Text.

Custom2 : Type: Text.

Custom3 : Type: Text.

### IntegratedSecurityCheckRole { \#IntegratedSecurityCheckRole }

Verifies whether the current Windows user has access to a specific role.

_Inputs_

RoleName : Type: mandatory, Text.

_Outputs_

Belongs : Type: Boolean.

### IntegratedSecurityGetDetails { \#IntegratedSecurityGetDetails }

Gets information about the current Windows user that made the request.

_Outputs_

Username : Type: Text.

isGuest : Type: Boolean.

isSystem : Type: Boolean.

isAnonymous : Type: Boolean.

isAuthenticated : Type: Boolean.

### ListAll { \#ListAll }

Determines if all the elements in the list satisfy the given condition.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list that contains the elements to which to apply the condition.

Condition : Type: mandatory, Boolean.  
The boolean expression to check for on each element of the list.

_Outputs_

Result : Type: Boolean.  
True if every element of the List satisfies the condition; otherwise, False.

### ListAny { \#ListAny }

Determines if any of the elements in the list satisfies the given condition.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list that contains the elements to which to apply the condition.

Condition : Type: mandatory, Boolean.  
The boolean expression to check for on each element of the list.

_Outputs_

Result : Type: Boolean.  
True if there is an element of the List satisfying the condition; otherwise, False.

### ListAppend { \#ListAppend }

Adds an element to the end of a list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list to add the element to.

Element : Type: mandatory, Generic Record.  
The element to be added to the end of the list.

### ListAppendAll { \#ListAppendAll }

Adds the elements of the source list to the end of the destination list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The destination List.

SourceList : Type: mandatory, Generic Record List.  
The list whose elements will be added.

### ListClear { \#ListClear }

Removes all elements from a list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list to remove the elements from.

### ListDistinct { \#ListDistinct }

Filters duplicate elements from a list.

_Inputs_

SourceList : Type: mandatory, Generic Record List.  
The list that includes duplicate elements.

_Outputs_

DistinctList : Type: Generic Record List.  
List that only includes the distinct elements of the source list.

### ListDuplicate { \#ListDuplicate }

Duplicates the elements of a list into another list.

_Inputs_

SourceList : Type: mandatory, Generic Record List.  
The list to duplicate.

_Outputs_

DuplicatedList : Type: Generic Record List.  
The duplicate list.

### ListFilter { \#ListFilter }

Returns a new list with the elements from the List parameter satisfying the given condition.

_Inputs_

SourceList : Type: mandatory, Generic Record List.  
The list that contains the elements to which to apply the condition.

Condition : Type: mandatory, Boolean.  
The boolean expression to check for on each element of the list.

_Outputs_

FilteredList : Type: Generic Record List.  
A new list with the elements that satisfy the condition.

### ListIndexOf { \#ListIndexOf }

Returns the position of the first element of the List parameter that satisfies the given condition, or -1 if no element satisfying the condition was found.

**Examples**

```text
ListIndexOf(UserList, Is_Active)

Returns the position of the first user in the list of User records satisfying the condition Is_Active = True.
```

```text
ListIndexOf(UserList, Name = "James")

Returns the position of the first user in the list of User records satisfying the condition Name = "James".
```

_Inputs_

List : Type: mandatory, Generic Record List.  
The list that contains the elements to which to apply the condition.

Condition : Type: mandatory, Boolean.  
The boolean expression to check for on each element of the list.

_Outputs_

Position : Type: Integer.  
The position of the first element of the list that satisfies the given condition; -1 if no element satisfying the condition was found.

### ListInsert { \#ListInsert }

Inserts an element in a specific position of a list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list to add the element to.

Element : Type: mandatory, Generic Record.  
The element to insert in the list.

Position : Type: mandatory, Integer.  
The position where the element is inserted.

### ListRemove { \#ListRemove }

Removes an element from a specific position of a list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list that the element is removed from.

Position : Type: mandatory, Integer.  
Position of the element to be removed.

### ListSort { \#ListSort }

Sorts the elements of the List parameter by the given criteria. Note that ListSort is different from the dynamic sorting in Aggregates. Multiple attributes having different data types \(such as Text and Integer\) in the criteria may not sort the list correctly.

**Examples**

```text
ListSort(UserList, Name)

Sorts UserList (list of User records) by the Name attribute.
```

```text
ListSort(TextList, Value, False)

Sorts TextList (a list of text values) by Value in descending order. 
Value is the runtime property that represents the current Text value being sorted.
```

```text
ListSort(OfficeEmployeesList, Employee.Name + " " + Office.Name)

Sorts OfficeEmployeesList (a list of Employee and Office records) by the employee name and office name. If employees work in multiple offices then this sorted list will have the employee records in the different offices displayed consecutively in ascending order of both their own names and the names of the offices.
```

_Inputs_

List : Type: mandatory, Any List.  
The list that contains the elements to sort by the given criteria.

By : Type: mandatory, Any Data Type.  
The criteria by which to order the elements of the list.

Ascending : Type: optional, Boolean.  
The boolean expression to indicate if the elements are sorted ascending \(True\) or descending \(False\) according to the By parameter. The default value is ascending \(True\).

### Login { \#Login }

Logs a specified user in the application.  
In case of success, 'UserId' and 'Username' session variables are filled with the user data.

_Inputs_

UserId : Type: mandatory, User Identifier.

Persistent : Type: mandatory, Boolean.  
If true, the login will be persistent for 15 days

### LoginPassword { \#LoginPassword }

Logs a specified user in the application using a password.  
In case of success, 'UserId' and 'Username' session variables are filled with the user data.

_Inputs_

UserId : Type: mandatory, User Identifier.

Password : Type: mandatory, Text.

Persistent : Type: mandatory, Boolean.  
If true, the login will be persistent for 15 days

### LogMessage { \#LogMessage }

Registers information that can be presented in Service Center in the module general log.

_Inputs_

Message : Type: mandatory, Text.  
The message to add to the module general log.

ModuleName : Type: mandatory, Text.  
The name of the module to be associated with the log message.

### Logout { \#Logout }

Logs out a specific user from the application.  
The 'UserId' and 'Username' session variables are cleared.

### ProcessTerminate { \#ProcessTerminate }

Explicitly forces a Process to terminate its execution.

_Inputs_

ProcessId : Type: mandatory, Process Identifier.

### SetCurrentLocale { \#SetCurrentLocale }

Sets the language locale of the user session to change the application presentation language.

_Inputs_

Locale : Type: mandatory, Text.

### TenantCreate { \#TenantCreate }

Creates a new tenant and associates it with the provisioning site.

_Inputs_

eSpaceName : Type: mandatory, Text.

TenantName : Type: mandatory, Text.

_Outputs_

TenantId : Type: Tenant Identifier.

### TenantInvalidateCache { \#TenantInvalidateCache }

Invalidates tenant's specific caches across all Front-end servers and eSpaces. This action is now available for compatibility purposes only. Please use the EspaceInvalidateCache action instead and invalidate tenant's specific caches by eSpace to narrow the invalidation scope

_Inputs_

TenantId : Type: mandatory, Tenant Identifier.  
Identifier of the tenant which will have all of its specific caches invalidated.

### TenantSwitch { \#TenantSwitch }

Change the context to the given tenant identifier. When switching tenant, the session is cleared \(equivalent to an implicit logout, before changing the tenant\), the OnSessionStart actions are executed, and the current transaction is commited.

_Inputs_

TenantId : Type: mandatory, Tenant Identifier.

## Client Actions

### ListAll { \#Client\_ListAll }

Determines if all the elements in the list satisfy the given condition.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list that contains the elements to which to apply the condition.

Condition : Type: mandatory, Boolean.  
The boolean expression to check for on each element of the list.

_Outputs_

Result : Type: Boolean.  
True if every element of the List satisfies the condition; otherwise, False.

### ListAny { \#Client\_ListAny }

Determines if any of the elements in the list satisfies the given condition.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list that contains the elements to which to apply the condition.

Condition : Type: mandatory, Boolean.  
The boolean expression to check for on each element of the list.

_Outputs_

Result : Type: Boolean.  
True if there is an element of the List satisfying the condition; otherwise, False.

### ListAppend { \#Client\_ListAppend }

Adds an element to the end of a list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list to add the element to.

Element : Type: mandatory, Generic Record.  
The element to be added to the end of the list.

### ListAppendAll { \#Client\_ListAppendAll }

Adds the elements of the source list to the end of the destination list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list to add the element to.

SourceList : Type: mandatory, Generic Record List.  
The list whose elements will be added.

### ListClear { \#Client\_ListClear }

Removes all elements from a list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list to remove the elements from.

### ListDistinct { \#Client\_ListDistinct }

Filters duplicate elements from a list.

_Inputs_

SourceList : Type: mandatory, Generic Record List.  
The list that includes duplicate elements.

_Outputs_

DistinctList : Type: Generic Record List.  
List that only includes the distinct elements of the source list.

### ListDuplicate { \#Client\_ListDuplicate }

Duplicates the elements of a list into another list.

_Inputs_

SourceList : Type: mandatory, Generic Record List.  
The list to duplicate.

_Outputs_

DuplicatedList : Type: Generic Record List.  
The duplicate list.

### ListFilter { \#Client\_ListFilter }

Returns a new list with the elements from the List parameter satisfying the given condition.

_Inputs_

SourceList : Type: mandatory, Generic Record List.  
The list that contains the elements to which to apply the condition.

Condition : Type: mandatory, Boolean.  
The boolean expression to check for on each element of the list.

_Outputs_

FilteredList : Type: Generic Record List.  
A new list with the elements that satisfy the condition.

### ListIndexOf { \#Client\_ListIndexOf }

Returns the position of the first element of the List parameter that satisfies the given condition, or -1 if no element satisfying the condition was found.

**Examples**

```text
ListIndexOf(UserList, Is_Active)

Returns the position of the first user in the list of User records satisfying the condition Is_Active = True.
```

```text
ListIndexOf(UserList, Name = "James")

Returns the position of the first user in the list of User records satisfying the condition Name = "James".
```

_Inputs_

List : Type: mandatory, Any List.  
The list that contains the elements to which to apply the condition.

Condition : Type: mandatory, Boolean.  
The boolean expression to check for on each element of the list.

_Outputs_

Position : Type: Integer.  
The position of the first element of the list that satisfies the given condition; -1 if no element satisfying the condition was found.

### ListInsert { \#Client\_ListInsert }

Inserts an element in a specific position of a list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list to add the element to.

Element : Type: mandatory, Generic Record.  
The element to insert in the list.

Position : Type: mandatory, Integer.  
The position where the element is inserted.

### ListRemove { \#Client\_ListRemove }

Removes an element from a specific position of a list.

_Inputs_

List : Type: mandatory, Generic Record List.  
The list that the element is removed from.

Position : Type: mandatory, Integer.  
Position of the element to be removed.

### ListSort { \#Client\_ListSort }

Sorts the elements of the List parameter by the given criteria. Note that ListSort is different from the dynamic sorting in Aggregates. Multiple attributes having different data types \(such as Text and Integer\) in the criteria may not sort the list correctly.

**Examples**

```text
ListSort(UserList, Name)

Sorts UserList (list of User records) by the Name attribute.
```

```text
ListSort(TextList, Value, False)

Sorts TextList (a list of text values) by Value in descending order. 
Value is the runtime property that represents the current Text value being sorted.
```

```text
ListSort(OfficeEmployeesList, Employee.Name + " " + Office.Name)

Sorts OfficeEmployeesList (a list of Employee and Office records) by the employee name and office name. If employees work in multiple offices then this sorted list will have the employee records in the different offices displayed consecutively in ascending order of both their own names and the names of the offices.
```

_Inputs_

List : Type: mandatory, Any List.  
The list that contains the elements to sort by the given criteria.

By : Type: mandatory, Any Data Type.  
The criteria by which to order the elements of the list.

Ascending : Type: optional, Boolean.  
The boolean expression to indicate if the elements are sorted ascending \(True\) or descending \(False\) according to the By parameter. The default value is ascending \(True\).

### LogMessage { \#Client\_LogMessage }

Registers information that can be presented in Service Center in the module general log.

_Inputs_

Message : Type: mandatory, Text.  
The message to add to the module general log.

ModuleName : Type: mandatory, Text.  
The name of the module to be associated with the log message.

### RequireScript { \#Client\_RequireScript }

Add a Javascript to the html header. Multiple calls for the same Javascript will only add it once. Action flow will proceed after the Javascript has been successfully loaded.

_Inputs_

Url : Type: mandatory, Text.  
The Url of the Javascript to add to the header

