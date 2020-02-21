---
tags: runtime-traditionalweb;
summary: >-
  CharacterCount displays the number of characters left to be entered in a
  target input field.
---

# CharacterCount

Displays the number of characters left to be entered in a target input field.

Use CharacterCount to inform users about the maximum number of characters they can enter in a given text area. Also show how many more characters can be entered.

**How to use**

1. Drag an input into the preview.
2. Give a name to the input \(for instance, CharacterCount\).
3. Set a variable type **text** to the input.
4. Drag the CharacterCount pattern into the preview.
5. Set the InputWidgetId to the input name.
6. Set the Limit property \(for instance, 50\).

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/charactercount-image-1.png%3E)

7. Publish and test.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| InputWidgetId | Input Element Name that will trigger the count. | Text | True | none |
| Limit | The character count limit. This value should be the same as the Max Length property in the input. | Integer | True | none |
| IsDescending | When set to false, the count will go from 0 to the limit that has been chosen on the Limit parameter. | Boolean | True | True |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/charactercount-image-2.png%3E)

