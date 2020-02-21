---
tags: runtime-traditionalweb;
summary: >-
  Breadcrumbs present the location of the user within the hierarchy of
  applications.
---

# Breadcrumbs

Present the location of the user within the hierarchy of applications.

Use Breadcrumbs to reduce the number of actions required from the user to reach a higher-level page. Breadcrumbs are helpful visual aids in understanding the location within the hierarchy, making sections and pages easier to find and assisting with understanding the context.

**How to use**

1. Drag the Breadcrumbs pattern into preview.
2. Drag as many Breadcrumbs Items as you need.
3. Set the content you need in the placeholders.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/breadcrumbs-image-1.png%3E)

4. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/breadcrumbs-image-2.png%3E)

## Input Parameters

### Breadcrumbs

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

### Breadcrumbs Item

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/breadcrumbs-image-3.png%3E)

## Advanced Use Case

### Use Breadcrumbs with ListRecords

1. Drag the Breadcrumbs Pattern into preview.
2. In the Content placeholder, drag a ListRecords widget.
3. In the ListRecords widget, drag a Breadcrumbs Item.
4. Inside the BreadcrumbsItem Pattern, use expressions to display the content.
5. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/breadcrumbs-image-4.png%3E)

## Notes

The Line Separator property of the ListRecords widget should be set to None.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/breadcrumbs-image-5.png%3E)

