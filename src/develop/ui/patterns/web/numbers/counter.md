---
tags: runtime-traditionalweb;
summary: >-
  Counter shows the total number of occurrences of several values regarding a
  single topic.
---

# Counter

Give feedback about the current count of several elements.

Use the Counter to show the total number of occurrences of several values regarding a single topic.

**How to use**

Add content to the placeholder and set the orientation and height of the pattern.

1. Drag the Counter pattern into the preview.
2. Set the Input Parameters to extend the default values.
3. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/counter-image-1.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Orientation | Set the orientation. | Orientation Identifier | False | Entities.Orientation.Horizontal |
| Height | Height of the block, use Pixel units. | Text | False | 100 |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/counter-image-2.png%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .center-align | .flex-direction-column | When Orientation is Vertical |

## Advanced Use Case

### Add a new style to the Counter pattern

1. Drag the Counter pattern into the preview.
2. Set the Orientation to `Vertical`, Height to `200` and ExtendedClass property to `background-blue shadow-xl`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/counter-image-3.png%3E)

3. Drag a container into Counter placeholder and type '26'.
4. Set the Style Classes property of the container to `font-size-display text-neutral-0`.
5. Drag a container into Counter placeholder and type 'Completed Requests'.
6. Drag another container into Counter placeholder.
7. Drag an Icon Widget into the container and set the Name property to `Entities.IconName.check` and Size to `Entities.IconSize.Size_3x`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/counter-image-4.png%3E)

8. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/counter-image-5.png%3E)

