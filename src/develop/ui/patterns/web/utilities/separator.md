---
tags: runtime-traditionalweb;
summary: Separator distributes content into clear groups and ease visual organization.
---

# Separator

Separate content clearly to help visual organization.

Use the Separator to distribute content into clear groups and ease visual organization.

**How to use**

To use the vertical separator, the parent element needs to have a defined height.

1. Drag Separator pattern into the preview.
2. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/separator-image-1.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Color | Set the color. | Color Identifier | False | Entities.Color.Neutral4 |
| Space | Set the space around the Separator line. | Space Identifier | False | Entities.Space.Base |
| IsVertical | If set as true, then the Separator becomes vertical. | Boolean | False | False |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/separator-image-2.png%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .separator | .separator-horizontal | When IsVertical parameter is False |
| .separator | .separator-vertical | When IsVertical parameter is True |

## Advanced Use Case

### Use the vertical separator

1. Drag a container into the preview.
2. Create a class called "separator-height".

   ```css
    .separator-height {
        height: 100px;
    }
   ```

3. Drag the Separator pattern into the container.
4. Set the IsVertical parameter to True.
5. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/separator-image-3.png%3E)

