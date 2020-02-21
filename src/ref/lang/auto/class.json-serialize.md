---
kinds: ServiceStudio.Model.Nodes+JSONSerialize+Kind
helpids: 30002
---

# JSON Serialize

Serializes an OutSystems object to a JSON string.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data | Record or List with the data to be serialized to a JSON string. | Yes |  |  |
| Serialize Default Values | Set to Yes to serialize non-mandatory JSON attributes with a default value set. | Yes | No |  |
| Date Format | Date format used in the JSON string. | Yes | 2014-01-01T00:00:00Z \(ISO\) |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| JSON | String in JSON format. |  | Text |  |

