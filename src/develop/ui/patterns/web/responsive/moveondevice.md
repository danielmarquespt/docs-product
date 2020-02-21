---
tags: runtime-traditionalweb;
summary: >-
  MoveOnDevice defines where information is displayed thereby improving the
  display on different devices.
---

# MoveOnDevice

Defines the target container for several elements in different devices without duplicating them.

Use Move on Device to define where information is displayed thereby improving the display on different devices.

**How to use**

1. Drag the MoveOnDevice pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/responsive/images/moveondevice-image-1.png%3E)

2. Set the required content in the placeholder.
3. Set the Ids of the target containers you want to move the content to.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/responsive/images/moveondevice-image-2.png%3E)

4. Publish and test.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| PhoneWidgetId | Target container that will receive this block on phones. | Text | No | none |
| TabletWidgetId | Target container that will receive this block on tablets. | Text | No | none |

