---
tags: runtime-traditionalweb;
summary: >-
  Modal is a box with content that interrupts the end-user and demands an
  action.
---

# Modal

A box with content that is displayed as an overlay on top of the screen.

Use the Modal to interrupt the end-user and demand an action. It is implemented to direct an end-user’s attention to important information. Ideal for when the end-user is requested to enter information critical to continuing the current process.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/modal-image-1.png%3E)

**How to use**

After placing a Modal on the screen, open it by calling a new screen action using a button with its method set to Ajax submit and use the Toggle Modal action \(found in the Logic Tab\). Use the pattern parameters to define if it has an Overlay, its Position in the page and the Enter/Leave animations.

1. Drag the Modal pattern into the preview.
2. Set the content in the placeholders.
3. Use a Button Widget or a Link with Ajax Submit to open the Modal Pattern.
4. In the Destination property, create a new screen action to trigger the modal.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/modal-image-2.png%3E)

5. Inside the action created, use the action ToggleModal and set the WidgetID.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/modal-image-3.png%3E)

6. Set the Input Parameters to change the default values.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/modal-image-4.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Position | Set the position of the Modal on the screen. | PositionExtended Identifier | False | Entities.PositionExtended.Center |
| HasOverlay | When true, an overlay is enabled behind the modal. | Boolean | False | True |
| EnterAnimation | Set the enter animation. | EnterAnimation Identifier | False | Entities.EnterAnimation.EnterScale |
| LeaveAnimation | Set the leave animation. | LeaveAnimation Identifier | False | Entities.LeaveAnimation.LeaveScale |
| ExtendedClass | Add custom style classes to this Block. | Text | False | None |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/modal-image-5.png%3E)

## Advanced Use Case

### Change the animation speed

It is possible to change the animation speed of Modal by using custom CSS. To implement this in your application, copy the CSS to the theme.

```css
.modal .animate {
    -webkit-animation-duration: 500ms;
            animation-duration: 500ms;
}
```

