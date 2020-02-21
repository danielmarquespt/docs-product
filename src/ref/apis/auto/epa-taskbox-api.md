# EPA Taskbox API

For Platform Version 9.0.0.0. The Embedded Process Automation \(EPA\) automatically displays in the user's web browser all pending activities in a floating taskbox. Each item includes instructions and a link that will lead the user to the web page where the activity can be completed. In Mobile Apps a custom taskbox needs to be created.

## Summary

| Action | Description |
| :--- | :--- |
| [API\_GetActivities](epa-taskbox-api.md#API_GetActivities%3E) | Returns the activities of a user.%%Activity filtering and pagination are allowed. |
| [API\_GetActivityGuidanceHtml](epa-taskbox-api.md#API_GetActivityGuidanceHtml%3E) | Encodes the activity guidance instructions in HTML format. |
| [API\_GetActivityPagination](epa-taskbox-api.md#API_GetActivityPagination%3E) | Returns the pagination information of all activities currently displayed in the Taskbox of the user. |
| [API\_GetActivityVisualization](epa-taskbox-api.md#API_GetActivityVisualization%3E) | Returns information on how an open activity is displayed in the Taskbox. |
| [API\_GetDynamicHtml](epa-taskbox-api.md#API_GetDynamicHtml%3E) | \[Deprecated\] Returns the JavaScript code for the Taskbox and its current content. |
| [API\_GetNewOpenActivity](epa-taskbox-api.md#API_GetNewOpenActivity%3E) | Returns the activity that is currently open by the user and has the indicated activity as one of the previous activities in the process flow. |
| [API\_GetStaticHtml](epa-taskbox-api.md#API_GetStaticHtml%3E) | \[Deprecated\] Returns the HTML of the Taskbox with absolute URLs, i.e., starting with "[http://&lt;Server](http://<Server) Name&gt;/". |
| [API\_MarkActivitiesAsSeen](epa-taskbox-api.md#API_MarkActivitiesAsSeen%3E) | Displays all Taskbox activities for the user as already seen, i.e., only new activities will be displayed as not seen in the Taskbox. |
| [API\_SetActivityVisualization](epa-taskbox-api.md#API_SetActivityVisualization%3E) | Sets how an open activity is displayed in the Taskbox. |
| [Inbox\_DisableInServer](epa-taskbox-api.md#Inbox_DisableInServer%3E) | Disables the Taskbox in the environment. |
| [Inbox\_EnableInServer](epa-taskbox-api.md#Inbox_EnableInServer%3E) | Enables the Taskbox in the environment. |

| Structure | Description |
| :--- | :--- |
| [Inbox\_FilterCriteria](epa-taskbox-api.md#Structure_Inbox_FilterCriteria%3E) |  |
| [Inbox\_PaginationCriteria](epa-taskbox-api.md#Structure_Inbox_PaginationCriteria%3E) |  |
| [Activity](epa-taskbox-api.md#Structure_Activity%3E) | The structure with the information of an activity in the TaskBox. |
| [PaginationInfo](epa-taskbox-api.md#Structure_PaginationInfo) | The structure with information of the number of activities in the TaskBox. |

## Actions

### API\_GetActivities { \#API\_GetActivities }

Returns the activities of a user.  
Activity filtering and pagination are allowed.

_Inputs_

UserId : Type: mandatory, User Identifier.  
The identifier of the user.

FilterCriteria : Type: optional, [Inbox\_FilterCriteria](epa-taskbox-api.md#Structure_Inbox_FilterCriteria%3E).  
The criteria for filtering activities.  
Leave it empty for no filtering.

PaginationCriteria : Type: mandatory, [Inbox\_PaginationCriteria](epa-taskbox-api.md#Structure_Inbox_PaginationCriteria%3E).  
The pagination criteria for displaying the activities in the Taskbox of the user.  
Leave it empty for no pagination.

_Outputs_

ActivityList : Type: [Activity](epa-taskbox-api.md#Structure_Activity) Record List.  
The list of activities.

PaginationInfo : Type: [PaginationInfo](epa-taskbox-api.md#Structure_PaginationInfo).  
The definite pagination information for displaying the activities in the Taskbox of the user.

### API\_GetActivityGuidanceHtml { \#API\_GetActivityGuidanceHtml }

Encodes the activity guidance instructions in HTML format.

_Inputs_

Guidance : Type: mandatory, Text.  
The activity guidance instructions.

_Outputs_

GuidanceHtml : Type: Text.  
The activity guidance instructions encoded in HTML format.

### API\_GetActivityPagination { \#API\_GetActivityPagination }

Returns the pagination information of all activities currently displayed in the Taskbox of the user.

_Inputs_

UserId : Type: mandatory, User Identifier.  
The identifier of the user.

FilterCriteria : Type: optional, [Inbox\_FilterCriteria](epa-taskbox-api.md#Structure_Inbox_FilterCriteria%3E).  
The criteria for filtering activities.  
Leave it empty for no filtering.

_Outputs_

PaginationInfo : Type: [PaginationInfo](epa-taskbox-api.md#Structure_PaginationInfo).  
The pagination information of all activities currently displayed in the Taskbox of the user.

### API\_GetActivityVisualization { \#API\_GetActivityVisualization }

Returns information on how an open activity is displayed in the Taskbox.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.  
The identifier of the activity.

_Outputs_

HideDone : Type: Boolean.  
If True, the 'Done' button is not available when the activity is open in the Taskbox.

HideRelease : Type: Boolean.  
If True, the 'Release' button is not available when the activity is open in the Taskbox.

CustomInstructions : Type: Text.  
The text/HTML of custom instructions displayed below the normal activity instructions when the activity is open in the Taskbox.  
The instructions have a maximum length of 500 characters.

### API\_GetDynamicHtml { \#API\_GetDynamicHtml }

\[Deprecated\] Returns the JavaScript code for the Taskbox and its current content.

_Inputs_

EspaceId : Type: mandatory, Espace Identifier.  
\[Deprecated\]

UserId : Type: mandatory, User Identifier.  
The identifier of the user.

Locale : Type: mandatory, Text.  
\[Deprecated\]

Data : Type: mandatory, Text.  
\[Deprecated\]

_Outputs_

Html : Type: Text.  
The JavaScript code for the Taskbox and its current content.

### API\_GetNewOpenActivity { \#API\_GetNewOpenActivity }

Returns the activity that is currently open by the user and has the indicated activity as one of the previous activities in the process flow.

_Inputs_

UserId : Type: mandatory, User Identifier.  
The identifier of the user.

PreviousActivityId : Type: mandatory, Activity Identifier.  
The identifier of one of the previous activities in the process flow.

_Outputs_

ActivityId : Type: Activity Identifier.  
The activity that is currently open by the user.

### API\_GetStaticHtml { \#API\_GetStaticHtml }

\[Deprecated\] Returns the HTML of the Taskbox with absolute URLs, i.e., starting with "[http://&lt;Server](http://<Server) Name&gt;/".

_Inputs_

EspaceId : Type: mandatory, Espace Identifier.  
The identifier of the eSpace.

UserId : Type: mandatory, User Identifier.  
The identifier of the user.

Locale : Type: mandatory, Text.  
The language locale.

Data : Type: mandatory, Text.  
\[Deprecated\]

_Outputs_

Html : Type: Text.  
The HTML of the Taskbox with absolute URLs, i.e., starting with "[http://&lt;Server](http://<Server) Name&gt;/".

### API\_MarkActivitiesAsSeen { \#API\_MarkActivitiesAsSeen }

Displays all Taskbox activities for the user as already seen, i.e., only new activities will be displayed as not seen in the Taskbox.

_Inputs_

UserId : Type: mandatory, User Identifier.  
The identifier of the user.

### API\_SetActivityVisualization { \#API\_SetActivityVisualization }

Sets how an open activity is displayed in the Taskbox.

_Inputs_

ActivityId : Type: mandatory, Activity Identifier.  
The identifier of the activity.

HideDone : Type: optional, Boolean.  
If True, the 'Done' button is not available when the activity is open in the Taskbox.

HideRelease : Type: optional, Boolean.  
If True, the 'Release' button is not available when the activity is open in the Taskbox.

CustomInstructions : Type: optional, Text.  
The text/HTML for custom instructions displayed below the normal activity instructions when the activity is open in the Taskbox.  
The custom instructions have a maximum length of 500 characters.

### Inbox\_DisableInServer { \#Inbox\_DisableInServer }

Disables the Taskbox in the environment.

### Inbox\_EnableInServer { \#Inbox\_EnableInServer }

Enables the Taskbox in the environment.

## Structures

### Inbox\_FilterCriteria { \#Structure\_Inbox\_FilterCriteria }

_Attributes_

ActivityLabel : Type: Text \(50\).

### Inbox\_PaginationCriteria { \#Structure\_Inbox\_PaginationCriteria }

_Attributes_

StartIndex : Type: Integer.

LineCount : Type: Integer.

### Activity { \#Structure\_Activity }

The structure with the information of an activity in the TaskBox.

_Attributes_

Id : Type: EntityReference. The identifier of the Activity.

Label : Type: Text \(50\). The label of the Activity.

LabelLang : Type: Text \(50\). The code of the language locale of the label.

Details : Type: Text \(50\). The details of the Activity.

DueDate : Type: DateTime. The due date of the Activity.

IsOpened : Type: Boolean. Is True if the activity is already open by a user.

IsSeen : Type: Boolean. Is False if the activity is not visible in the TaskBox due to pagination.

### PaginationInfo { \#Structure\_PaginationInfo }

The structure with information of the number of activities in the TaskBox.

_Attributes_

Total : Type: Integer. The total number of activities in the TaskBox.

Unseen : Type: Integer. The number of unseen activities due to pagination.

