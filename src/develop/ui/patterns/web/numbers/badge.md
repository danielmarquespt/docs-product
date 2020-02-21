---
tags: runtime-traditionalweb;
summary: Badge display numerical information as notification.
---

# Badge

Display numerical information as notification.

Use the Badge to notify the user about numerical information such as new messages or tasks.

**How to use**

Use the parameters to choose some options such as color, shape, size and light theme.

1. Drag Badge pattern into the preview.
2. Set the Input Parameters to extend the default values.
3. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/badge-image-1.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Number | Number that will appear inside the badge. | Integer | False | 8 |
| Color | Set the color. | Color Identifier | False | Entities.Color.Primary |
| Shape | Set the shape. | Shape Identifier | False | Entities.Shape.Rounded |
| Size | Set the size. | Size Identifier | False | none |
| IsLight | Use the lightest color version for the background and the darker color version for the text. | Boolean | False | False |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/badge-image-2.png%3E)

## Advanced Use Case

### Use a transparent Badge Pattern with a border

1. Use Transparent in Color Value.
2. In the ExtendedClass Input Parameter, choose the desired text color.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/badge-image-3.png%3E)

3. Choose the border size of the Badge.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/badge-image-4.png%3E)

4. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/badge-image-5.png%3E)

## Notes

If the number on Badge pattern is greater then 99, it is displayed as 99+.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/badge-image-6.png%3E)

