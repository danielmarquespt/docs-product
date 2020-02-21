---
tags: runtime-traditionalweb;
summary: Tag styles small texts in a colored tag format.
---

# Tag

Style small texts in a colored tag format.

Use Tags to display status, labels or categories thus providing great user experience.

**How to use**

Drag the pattern to the screen and add the text in the placeholder.

1. Drag the Tag pattern into the preview.
2. Drag your text to this placeholder.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/tag-image-1.png?width=500%3E)

3. Set the Input Parameters to extend the default values.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/tag-image-2.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Color | Set the backgound color. | Color Identifier | _False_ | Entities.Color.Primary |
| Shape | Set the shape. | Shape Identifier | _False_ | Entities.Shape.Rounded |
| Size | Set the size. | Size Identifier | _False_ | None |
| IsLight | Use the lightest color version for the background and the darker color  version for the text. | Boolean | _False_ | False |
| ExtendedClass | Add custom style classes to this Block. | Text | _False_ | None |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/tag-image-3.png%3E)

## Advanced Use Case

### Use only border in Tag Pattern

1. Set the Color parameter to Transparent.
2. In the ExtendedClass property, set the text color.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/tag-image-4.png%3E)

3. Set the border size.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/tag-image-5.png%3E)

4. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/tag-image-6.png%3E)

