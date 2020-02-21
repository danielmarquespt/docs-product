---
kinds: 'ServiceStudio.Model.Script+Kind, ServiceStudio.Model.ReferenceScript+Kind'
helpids: 0
---

# Script

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Runtime Path | Path to the image. | Yes |  |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |
| JavaScript | JavaScript associated with this element. |  |  | Click on "..." to edit the property value. |
| Required Scripts |  |  |  |  |
| Required Script | Script\(s\) required by the element. |  |  |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| URL | The runtime URL of the script. | Yes | Text |  |

