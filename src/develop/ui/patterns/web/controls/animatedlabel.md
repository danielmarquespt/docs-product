---
tags: runtime-traditionalweb;
summary: AnimatedLabel allows end-users to keep context by focusing on the input.
---

# AnimatedLabel

An input label that animates when there is user input.

Use AnimatedLabel inputs to allow end-users to keep context by focusing on the input.

**How to use**

Drag the pattern to the screen and configure the input and label text. You may use the IsInline parameter to define if it should use the default input style.

1. Drag AnimatedLabel pattern into the preview.
2. Set the Variable property of the Input widget.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/animatedlabel-image-1.png%3E)

3. Change the text in Label Placeholder.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/animatedlabel-image-2.png%3E)

4. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/animatedlabel-image-3.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| IsInline | If set as false, the input style in the block as default \(white background\). | Boolean | False | True |
| ExtendedClass | Add custom style classes to this Block. | Text | False | None |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/animatedlabel-image-4.png%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .animated-label | .animated-label-inline | When IsInline Input Parameter is true |

## Advanced Use Case

### Change the position of the label when it is active

1. Write the following CSS code in the CSS editor.

   ```css
    .animated-label.active .animated-label-text {
        top: 50px;
    }
   ```

2. Publish and test.

Before

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/animatedlabel-image-5.png%3E)

After

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/animatedlabel-image-6.png%3E)

