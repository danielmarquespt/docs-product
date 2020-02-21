---
kinds: >-
  ServiceStudio.Model.Structure+Kind,
  ServiceStudio.Model.SystemActionStructure+Kind,
  ServiceStudio.Model.WebReferenceStructure+Kind,
  ServiceStudio.Model.ReferenceStructure+Kind
helpids: '15007, 30102'
---

# Structure

A Structure is a compound data type used to encapsulate groups of related attributes.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |

