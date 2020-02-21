---
kinds: 'ServiceStudio.Model.Image+Kind, ServiceStudio.Model.ReferenceImage+Kind'
helpids: 0
---

# Image

An image resource. The supported image formats are GIF, JPEG, and PNG.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Width | Width of the image in pixels. | Yes |  |  |
| Height | Height of the image in pixels. | Yes |  |  |
| Runtime Path | Path to the image. | Yes |  |  |
| Original Filename | Name of the file from which the image was imported. |  |  |  |
| Original Format | File format of the imported image. |  |  |  |
| Public | Set to Yes to allow the element to be added as dependency by other modules. | Yes | No |  |
| Original Name | Name of the element as defined in the module which implements it \(producer module\). This property is read-only. | Yes |  | This property is only visible for referenced elements. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| URL | The runtime URL of the image. | Yes | Text | Only available in mobile apps. |

