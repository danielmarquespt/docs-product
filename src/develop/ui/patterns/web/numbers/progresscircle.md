---
tags: runtime-traditionalweb;
summary: >-
  ProgressCircle shows the current progress of a task using circular or
  semi-circular progress indicators.
---

# ProgressCircle

Easy to create circular or semi-circular progress indicators.

**When to use**

Use the Progress Circle to show the current progress of an operation flow. The progress is incremented in fractions of the circular badge. You can also show progress in a Progress Bar or Progress Circle Fraction display type. Be consistent when using a pattern to show progress of a task, for instance, if an action displays a linear indicator on one screen, that same action should not use a circular indicator elsewhere in the app.

**How to use**

Create your custom content and put it inside the content placeholder.

1. Drag the ProgressCircle pattern into the preview.
2. Define the progress value.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progresscircle-image-1.png%3E)

3. Set the required content in the placeholder.
4. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progresscircle-image-2.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Progress | Percentage to display, you can use functions or local variables. | Integer | True | none |
| ProgressColor | The color of the stroke on progress circle. | Color Identifier | False | Entities.Color.Primary |
| TrailColor | The color of the empty part of the progress circle. | Color Identifier | False | Entities.Color.Neutral5 |
| CircleThickness | The thickness of the circle that marks the progress. | Integer | False | 4 |
| AnimateInitialProgress | Animate the progress circle from zero to progress value. | Boolean | False | True |
| IsSemiCircle | Change the type of progress bar from circle to semi circle. | Boolean | False | False |
| AdvancedFormat | Allow for more options beyond what it's provided through the input parameters. For more information visit: [https://kimmobrunfeldt.github.io/progressbar.js/](https://kimmobrunfeldt.github.io/progressbar.js/). Example: `{ easing: 'bounce' }` | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progresscircle-image-3.png?width=650%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .progress-circle | .progress-circle .progress-circle-content | When IsSemiCircle parameter is False |
| .progress-circle | .progress-circle .progress-semi-circle-content | When IsSemiCircle parameter is True |

## Advanced Use Case

### Change color of progress circle based on value

1. In your screen, create a local variable "Progress" of type Integer.
2. Drag the ProgressCircle pattern into the preview.
3. Set the Value of the ProgressCircle's Progress parameter.
4. To change the color of the ProgressCircle based on values, create a condition and set limits.

   In this example, 3 colors represent diferent states of progress. Set the value of the ProgressColor parameter to `If(Progress <= 50, Entities.Color.Red, If( Progress > 50 and Progress < 75, Entities.Color.Yellow , Entities.Color.Green))`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progresscircle-image-4.png%3E)

5. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progresscircle-image-5.gif%3E)

### Remove the round corners of ProgressCircle

To remove the round corners, use this CSS snippet.

```css
.progress-circle svg {
    stroke-linecap: square;
}
```

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progresscircle-image-6.png%3E)

### Change the trail thickness of ProgressCircle

To change the trail thickness, set the AdvancedFormat property to `{trailWidth: 1}`.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/progresscircle-image-7.png%3E)

