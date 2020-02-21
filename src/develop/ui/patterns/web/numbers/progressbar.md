---
tags: runtime-traditionalweb;
summary: ProgressBar displays the progress of a task by incrementing values in a bar.
---

# ProgressBar

Display progress of a task by incrementing values in a bar.

Use the Progress Bar to show the current progress of a task flow. You can also show progress in a Progress Circle or a Progress Circle Fraction. Be consistent when using a pattern to show progress of a task, for instance, if an action displays a linear indicator on one screen, that same action should not use a circular indicator elsewhere in the app.

**How to use**

Configure the variable that defines the percentage. You can also change the shape, size, orientation and color of the ProgressBar.

1. Drag the ProgressBar pattern into the preview.
2. Use a variable to set the percentage value to display.
3. Set the content in the placeholders.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progressbar-image-1.png%3E)

4. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progressbar-image-2.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Percentage | Percentage to display, you can use functions or local variables. | Integer | False | 50 |
| Color | Set the background color. | Color Identifier | False | Entities.Color.Primary |
| Shape | Set the shape. | Shape Identifier | False | Entities.Shape.Rounded |
| Size | Set the size. | ProgressBarSize Identifier | False | Entities.ProgressBarSize.Base |
| IsInline | Set the orientation of the value placeholder. When true, the value placeholder will be placed at the end of the line and the label placeholder is hidden.When False, value and label of the placeholder will be placed over the line. | Boolean | False | False |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progressbar-image-3.png?width=650%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .progress-container | .progress-container.flex-direction-column | When IsInline parameter is False |
| .progress-container | .progress-container.flex-direction-row | When IsInline parameter is False |

## Advanced Use Case

### Change color of progress bar based on value

1. Create a local Integer variable "Value".
2. Drag the ProgressBar pattern into the preview.
3. Set the Value of the ProgressBar's Percentage parameter.
4. To change the color of your ProgressBar based on values, create a condition and set limits to use color. In this example, 3 colors represent diferent states of progress. Set the Color parameter to `If(Value <= 50, Entities.Color.Red, If( Value > 50 and Value < 75, Entities.Color.Yellow , Entities.Color.Green))`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progressbar-image-4.png%3E)

5. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progressbar-image-5.gif%3E)

### Change the style of Progress bar

It is possible to change the style of Progress bar by using custom CSS. To implement this in your application, copy the CSS and add it to the theme.

```css
.progress {
    padding: var(--space-s);`
    border: var(--space-xs) solid var(--color-primary);`
}
```

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progressbar-image-6.png%3E)

### Remove background of Progress Bar

To remove the background, use this CSS snippet.

```css
.progress {
    background-color: transparent;
}
```

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progressbar-image-7.png%3E)

