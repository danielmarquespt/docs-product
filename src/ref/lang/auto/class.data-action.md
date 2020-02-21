---
kinds: ServiceStudio.Model.NRFlows+DataScreenActionFlow+Kind
helpids: 0
---

# Data Action

System defined action to manipulate entity records.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Server Request Timeout | Maximum time in seconds to wait for the Data Action to return data before triggering a Communication Exception. Overrides the default timeout defined on the module. |  |  |  |
| Fetch |  | Yes | At start |  |
| Events |  |  |  |  |
| On After Fetch | Action executed after the aggregate fetches data from the data source. |  |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| IsDataFetched | True when data has been fetched from the database and is ready to be used. | Yes | Boolean |  |
| HasFetchError | True when there is an error during data fetch due to a server error or communication timeout. | Yes | Boolean |  |

