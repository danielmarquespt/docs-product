---
tags: runtime-traditionalweb;
summary: >-
  DropdownSelect allows a search functionality or multiple selection in lists
  with enhanced UX experience.
---

# DropdownSelect

DropdownSelect enables you to implement a search functionality or multiple selection in lists. You must bind it to the main widget.

Use the Dropdown Select when you need an enhanced combo or list box in forms, as it offers a richer user experience than the list.

**How to use**

To add DropdownSelect to your application, follow these steps:

1. Place Combo Box or List Box in the main editor. This is your main widget.
2. Make sure you enter a value in the Name property of the main widget.
3. Drag DropdownSelect pattern into the preview next to your main widget.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/dropdownselect_1.png%3E)

4. Set the mandatory value `WidgetId` in the properties pane that corresponds to the main widget.
5. Adjust the widget width by adjusting the width of the outer container.

How this pattern behaves depends on the way it is bound.

* If you bind it to a Combo Box widget, DropdownSelect works as a selectable Dropdown.
* If you bind it to a List Box, DropdownSelect works as a multi-select with removable tags.

## Input parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| WidgetId | Element Name \(Combo Box and List Box\) that triggers the element to be visible. | Text | True | none |
| NoResultsText | Text to display when there are no results. | Text | False | "No results found." |
| SearchEnabled | If set to false, removes the search functionality. Doesn't work with ListBox. | Boolean | False | True |
| SearchResultsLimit | Limits number of results shown. | Long Integer | False | 10 |
| AdvancedFormat | Enables more options beyond what's provided through the inputs. To find more options go to [Choices library](https://github.com/jshjohnson/Choices). Example: `{ searchPlaceholderValue: 'Search' }` | Text | False | `{}` |
| ExtendedClass | Set a class. You can then use it to bind all other ComboBox/ListBox in your screen. | Text | False | "" |

## Layout and classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/dropdownselect_3.png%3E)

## CSS selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| Dropdown | .choices\_\_list--dropdown.is-active | Defines if the drop-down is closed or opened |

## Advanced Use Case

### Change the border color

Write the following CSS in the CSS editor and change the `yourcolor` variable:

`.choices__inner { border: var(--border-size-s) solid yourcolor; }`

Or using the CSS variable `var(--color-yourcolor)` example:

`.choices__inner { border: var(--border-size-s) solid var(--color-yourcolor); }`

### Change removable tags color

Write the following CSS in the CSS editor and change the `yourcolor` variable:

`.choices__list--multiple .choices__item.choices__item--selectable { background: yourcolor; }`

Or using the CSS variable `var(--color-yourcolor)` example:

`.choices__list--multiple .choices__item.choices__item--selectable { background: var(--color-yourcolor); }`

## Browser previews

With Combo Box:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/dropdownselect.gif?width=600%3E)

With List Box:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/dropdownselect2.gif?width=600%3E)

## Notes

The SearchEnabled parameter doesn't work with ListBox.

