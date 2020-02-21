---
tags: runtime-traditionalweb;
summary: Dropdown allows end-users to make a choice from several options.
---

# Dropdown

Allow end-users to make a choice from several options.

Use the Dropdown to offer a choice of more than four options. For a very large number of options, consider using the Dropdown Select to avoid loss of context.

**How to use**

Fill in the label of the Dropdown and add the required links in the DropdownList placeholder.

1. Drag the Dropdown pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/dropdown-image-1.png?width=500%3E)

2. Set your content in the placeholders.
3. Publish and test.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/dropdown-image-2.png%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .dropdown | .is--hidden | Defines if the dropdown list is closed |
| .dropdown | .is--visible | Defines if the dropdown list is open |

## Advanced Use Case

### Use with ListRecords to make a list of links

1. Drag the Dropdown Pattern into the page.
2. In the DropdownList placeholder, drag a ListRecords widget.
3. Set the Line Separator property of the ListRecords widget to None.
4. In the ListRecords widget, drag a link and connect it to the required destination.
5. Inside the List, use expressions to display the content.
6. In the Prompt placeholder, set the text you want to define as the prompt.
7. Publish and test.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/dropdown-image-3.png%3E)

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/dropdown-gif-1.gif%3E)

