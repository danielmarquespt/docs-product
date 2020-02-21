---
tags: runtime-traditionalweb;
summary: Fieldset labels groups of related interface elements and fields.
---

# Fieldset

Group thematically related elements such as controls and labels.

Use the Fieldset to label groups of related interface elements and fields. This improves the layout and helps users understand the information.

**How to use**

Set the label of the Fieldset and then drag Input widgets to the content placeholder.

1. Drag the Fieldset pattern into the preview.
2. Set the Title parameter.
3. Set the content you need on the placeholder.
4. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/fieldset-image-1.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Title | The title that will be the legend of the Fieldset. | Text | True | none |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/fieldset-image-2.png%3E)

## Advanced Use Case

### Change the style of Fieldset

Use custom CSS to change the style of Fieldset. The following examples are only two ways of doing it. To use these in your application, copy the CSS code from below and add it to your theme.

Example 1

```css
.fieldset {
  position: relative;
}

.fieldset-legend {
  background: var(--color-background-body);
  padding: 0 var(--space-xs);
  position: absolute;
  right: var(--space-m);
  top: -15px;
}
```

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/fieldset-image-3.png%3E)

Example 2

```css
.fieldset {
  border: 0;
  padding: var(--space-m) 0;
}

.fieldset-legend {
  border-bottom: 1px solid var(--color-neutral-5);
  padding-bottom: var(--space-s);
  width: 100%;
}
```

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/utilities/images/fieldset-image-4.png%3E)

