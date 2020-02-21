---
kinds: ServiceStudio.Model.Timer+Kind
helpids: 13001
---

# Timer

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Action | Action that is executed when the Timer is awakened. | Yes |  |  |
| Schedule | Schedule the start time and frequency of the Timer. |  |  | The value of this property can only be specified using the Timer Schedule Editor. Open it by double-clicking on the property name or by clicking on "...". |
| Advanced |  |  |  |  |
| Timeout in Minutes | Maximum time in minutes that Platform Server waits for the timer execution to end. | Yes | 20 |  |
| Priority | Defines the order by which the Timers are prioritized. | Yes | 3 - Normal |  |
| Is Multi-tenant | Set to Yes to run the Timer isolatedly for each tenant or 'No' to run once for data shared among tenants. If not set, it inherits the module setting. | Yes |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Schedule | Indicates the time and the frequency that the Timer is awakened. |  | Text | When setting this runtime property, you must use one of the supported schedule formats. The schedule formats are case-sensitive. Examples:  `"16:15"` \(awake the Timer every day at 16:15\);  `"22:00 Mon Fri"` \(awake the Timer every Monday and Friday at 22:00\);  `"15:30 16"` \(awake the Timer on the 16th day of every month at 15:30\);  `"00:15 2nd Tue"` \(awake the Timer on the 2nd Tuesday of every month at 00:15\);  `"When Published"` \(awake the Timer after each 1-Click Publish operation\).  Be aware that no format validations are done at development time. You must be careful to use the correct format when assigning a value to the Schedule runtime property, otherwise the Timer might not run. |
| LastRun | Indicates the last calendar day and time when the Timer awoke, automatically or explicitly. | Yes | Date Time |  |
| NextRun | Indicates the next calendar day and time when the Timer is schedule to awaken. | Yes | Date Time |  |

