---
kinds: ServiceStudio.Model.Nodes+JSONDeserialize+Kind
helpids: 30004
---

# JSON Deserialize

Deserializes a JSON string to an OutSystems object.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| JSON String | JSON string with the data to be deserialized to a Record or List. | Yes |  |  |
| Data Type | Record or List representing the structure of the data in the JSON string. | Yes |  |  |
| Date Format | Date format used in the JSON string. | Yes | 2014-01-01T00:00:00Z \(ISO\) |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Data | The Record or List with the JSON data. |  | Record, Record List |  |

