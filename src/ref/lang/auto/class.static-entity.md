---
kinds: >-
  ServiceStudio.Model.Entity+Kind, ServiceStudio.Model.SyntheticEntity+Kind,
  ServiceStudio.Model.ReferenceEntity+Kind
helpids: 15005
---

# Static Entity

A static entity is an entity that has static data associated to it. This static data is managed at design time and can be used directly in the business logic design of the application, benefiting from strong typing.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies the entity in the module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Label | Label used to describe the entity in the user interface of the application. |  |  |  |
| Label \(plural\) | Label used to described the plural of the entity in the user interface of the application. |  |  |  |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Identifier Attribute | Attribute that uniquely identifies the entity. |  | Id |  |
| Label Attribute | Label used to describe the attribute. |  | Label |  |
| Order By Attribute | Attribute used for the default ordering of the records of the entity. |  | Order |  |
| Is Active Attribute | Specifies a Boolean attribute of the entity which defines if the record is to be fetched in a query. |  | Is\_Active |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| Advanced |  |  |  |  |
| Use Translations | Indicates whether to use existing translation for the records of the static entity or not. | Yes | Yes |  |

