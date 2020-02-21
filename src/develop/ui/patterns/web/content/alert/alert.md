---
tags: runtime-traditionalweb;
summary: >-
  Alert gets the end-user's attention and highlights important information,
  errors or warnings on the screen.
---

# Alert

Highlight important information, errors or warnings.

Use an Alert when you need to get the end-user's attention and provide important information on the screen.

**How to use**

Add the message to the placeholder and set the alert type in the properties of the block.

1. Drag Alert pattern into the preview.
2. Set the mandatory Alert value.
3. Set the Input Parameters to extend the default values.
4. Type the message you want to display.
5. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/alert/images/alert-image-1.png%3E)

## Demo

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| AlertType | Select type of alert. | Alert Identifier | True | none |
| ShowCloseButton | Set the space around the Separator line. | Boolean | False | False |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/alert/images/alert-image-2.png%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .alert | .alert-error | When Alert type selected is Error |
| .alert | .alert-info | When Alert type selected is Info |
| .alert | .alert-success | When Alert type selected is Success |
| .alert | .alert-warning | When Alert type selected is Warning |
| .alert | .alert-close.is--hidden | When ShowCloseButton parameter is False |

## Advanced Use Case

### Add enter animation to Alert pattern

1. Create a local variable of type Boolean called "ShowAlert" and set the default value to False.
2. Drag a container into preview and name it \(for instance, AlertAnimation\).
3. In the properties of the container, change the display from True to ShowAlert.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/alert/images/alert-image-3.png%3E)

4. Drag the Animate pattern into the container.
5. Change the EnterAnimation property to EnterTop.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/alert/images/alert-image-4.png%3E)

6. Drag the Alert pattern into the Animate placeholder.
7. Set the Alert type \(mandatory value\).
8. Type the message you want to display.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/alert/images/alert-image-5.png%3E)

9. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/alert/images/alert-image-6.gif%3E)

