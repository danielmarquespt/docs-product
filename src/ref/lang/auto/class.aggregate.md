---
kinds: >-
  ServiceStudio.Model.Nodes+DataSet+Kind,
  ServiceStudio.Model.NRNodes+WebScreenDataSet+Kind
helpids: 17203
---

# Aggregate

Fetches and computes data from a database.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Timeout | Maximum time in seconds to wait for the Aggregate to return data before triggering a Communication Exception. Overrides the default timeout defined on the module. |  |  | If there is no value specified in this property, the timeout corresponds to the "Default query timeout" parameter specified in the Platform Server Configuration Tool. Property not available in client actions. |
| Cache in Minutes | Maximum time content or results are stored in memory. When undefined, nothing is cached. |  |  | Property not available in client actions. |
| Max. Records | Maximum number of records read from the database. |  |  | If undefined, the default value is:  – In widgets: StartIndex + LineCount + 1;  – Exporting to Excel: No limit. |
| Start Index | Index of the first List item to iterate. Can be an expression. |  |  | The expression used in this property \(if present\) is evaluated before the web screen preparation. |
| Fetch |  | Yes | At start |  |
| Events |  |  |  |  |
| On After Fetch | Action executed after the aggregate fetches data from the data source. |  |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| List | Collection of records returned by the performed query. |  | Record List |  |
| Count | Number of records returned by the Count query. |  | Long Integer |  |
| IsDataFetched | True when data has been fetched from the database and is ready to be used. | Yes | Boolean |  |
| HasFetchError | True when there is an error during data fetch due to a server error or communication timeout. | Yes | Boolean |  |

