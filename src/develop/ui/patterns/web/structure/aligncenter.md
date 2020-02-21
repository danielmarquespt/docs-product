---
tags: runtime-traditionalweb;
summary: AlignCenter places content horizontally or vertically within a container.
---

# AlignCenter

Place content to horizontally or vertically align to the center of the container.

Use AlignCenter to center content horizontally or vertically within a container and to align many elements with different heights or widths.

**How to use**

Add two or more elements inside the placeholder and they will be centered according to the selected orientation.

1. Drag AlignCenter pattern into the preview.
2. Drag the UserInitials pattern into AlignCenter placeholder.
3. In the Name input parameter, type "Scott Ritchie" \(for instance\).

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/structure/images/aligncenter-image-1.png%3E)

4. Drag the Text widget into AlignCenter placeholder and type "Scott Ritchie".

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/structure/images/aligncenter-image-2.png%3E)

5. Publish and test.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/structure/images/aligncenter-image-3.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Orientation | Set the orientation of the content inside. | Orientation Identifier | False | Entities.Orientation.Horizontal |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/structure/images/aligncenter-image-4.png%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .center-align | .center-align.flex-direction-row | When Orientation parameter is Horizontal |
| .center-align | .center-align.flex-direction-column | When Orientation parameter is Vertical |

## Advanced Use Case

### Set vertical align with custom content

1. Drag the AlignCenter pattern into the preview.
2. Set the Orientation parameter to Vertical.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/structure/images/aligncenter-image-5.png%3E)

3. Drag an image into the AlignCenter placeholder and add the `border-radius-circle` class.
4. Drag a container into AlignCenter placeholder and set the horizontal alignment to Center.
5. In the container, add a Text widget with the text "Scott Ritchie" and have its Style Class set to `heading-4`.
6. Add another Text widget with the text "Marketing Communications Manager" and enclose it in a container.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/structure/images/aligncenter-image-6.png%3E)

7. Drag a container into the AlignCenter placeholder and add a Text widget.
8. Type the text "02 Jan" and have its Style Class set to `font-size-xs text-neutral-6`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/structure/images/aligncenter-image-7.png%3E)

9. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/structure/images/aligncenter-image-8.png%3E)

