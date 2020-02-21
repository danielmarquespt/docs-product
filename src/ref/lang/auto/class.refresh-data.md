---
kinds: ServiceStudio.Model.Nodes+RefreshQuery+Kind
helpids: 0
---

# Refresh Data

Obtains refreshed data from an existing data source.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Data Source | Specifies the data source to be fetched. | Yes |  |  |
| Max. Records | Maximum number of records read from the database. |  |  | If undefined, the default value is:  – In widgets: StartIndex + LineCount + 1;  – Exporting to Excel: No limit. |
| Start Index | Index of the first List item to iterate. Can be an expression. |  |  | The expression used in this property \(if present\) is evaluated before the web screen preparation. |

