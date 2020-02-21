---
kinds: ServiceStudio.Model.Nodes+AdvancedQuery+Kind
helpids: 9002
---

# SQL

Fetches data from the database using your own SQL statement.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Timeout | Time in seconds after which, if the data request is not fulfilled, the request is aborted and an exception is raised. |  |  | If there is no value specified in this property, the timeout corresponds to the "Default query timeout" parameter specified in the Platform Server Configuration Tool. |
| Cache in Minutes | Maximum time content or results are stored in memory. When undefined, nothing is cached. |  |  |  |
| Max. Records | Maximum number of records read from the database. The SQL statement is not changed by this setting; the limit applies only to the results received from the database. |  |  | If undefined, the default value is:  – In widgets: StartIndex + LineCount + 1;  – Exporting to Excel: No limit. |
| Statement | SQL statement to fetch data from the database. |  | SELECT |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| List | The records returned by the query. |  | Record List |  |
| Count | Number of records returned by the Count query. |  | Long Integer |  |

