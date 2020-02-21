---
tags: runtime-traditionalweb;
summary: Iframe displays information from other apps on the screen in small previews.
---

# Iframe

Display additional information in one view.

Use Iframe to display information from other apps on the screen in small previews.

**How to use**

1. Drag the Iframe pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/iframe-image-1.png%3E)

2. Set the mandatory values.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/iframe-image-2.png%3E)

3. Publish and test.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| SourceURL | The target URL to load on the Iframe. | Text | Yes | none |
| Title | Title for the iframe element. | Text | No | none |
| Height | Iframe height, default is 100%. | Text | No | 100% |
| Width | Iframe width, default is 100%. | Text | No | 100% |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/iframe-image-3.png%3E)

## Advanced Use Case

### Change the Iframe width according to the device

This can be very useful if you are using a fixed width.

1. Set the Width to `If(IsDesktop(), "500px", "100%")`.
2. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/iframe-image-4.png%3E)

You can change the condition of the width used. This code makes the width 500px on desktop, but on mobile, it is still full-width as the fixed width would probably overflow the screen.

