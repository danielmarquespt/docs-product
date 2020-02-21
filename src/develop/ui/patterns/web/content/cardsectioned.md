---
tags: runtime-traditionalweb;
summary: >-
  CardSectioned groups short pieces of information in sections and highlights
  them on the screen.
---

# CardSectioned

Groups information in a small block organized with different sections for title, image and content that can be easily noticeable in the screen.

Use the CardSectioned pattern to group short pieces of information and highlight them on the screen.

**How to use**

Add content to the placeholders and use the parameters to define the orientation, direction and padding properties.

1. Drag the CardSectioned pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/cardsectioned-image-1.png?width=600)

2. Set the content you need in the placeholders.
3. Set the Input Parameters to extend the default values.
4. Publish and test.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Orientation | Set the orientation of the card. | Orientation Identifier | False | Entities.Orientation.Vertical |
| ImagePadding | When true, content has 24px of padding. | Boolean | False | True |
| IsRight | Aligns content to the right. This will only go into effect if the Orientation parameter is set to Horizontal. | Text | False | False |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/cardsectioned-image-2.png%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .card-sectioned | .flex-direction-row | When the parameter Orientation of the card is set to horizontal |
| .card-sectioned | .flex-direction-column | When the parameter Orientation of the card is set to vertical |
| .card-image | .padding-none | When the parameter ImagePadding of the card is set to False |
| .card-sectioned | .card-sectioned-right | When the parameter IsRight is set to True |

## Advanced Use Case

### Change Orientation according to device

1. Drag the CardSectioned Pattern into the preview.
2. Set the Orientation parameter to `If(IsPhone(),Entities.Orientation.Vertical, Entities.Orientation.Horizontal)`. Use the server action IsPhone as the condition to set the orientation for a phone. You can also use the IsTablet action or invert the False & True statements, according to your needs. This way, the CardSectioned pattern will be horizontal on Desktop and Tablet. On the Phone, it will be vertical.
3. Publish and test.

Desktop & Tablet:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/cardsectioned-image-3.png%3E)

Phone:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/cardsectioned-image-4.png%3E)

## Notes

The parameter IsRight only works if the paramater Orientation is not Vertical.

