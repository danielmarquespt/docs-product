---
kinds: ServiceStudio.Model.Nodes+ExcelToRecordList+Kind
helpids: 10001
---

# Excel To Record List

Imports the contents of an MS Excel sheet into a list.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Record Definition | Entity or structure that defines the structure of the data that you want to load. | Yes |  |  |
| File Content | Holds the Excel file. | Yes |  | The expected data type is Binary Data. |
| Sheet Name | Name of the Excel sheet to import. By default imports the first sheet. |  |  |  |

