---
tags: null
---

# List

A List is a sequence of elements of the same data type, which may contain duplicate values. Elements can be inserted, fetched and removed from a list.

By default a list is empty, meaning that it has no elements. However, you can use the system actions to manipulate an empty list.

On the server side, variables of List data type have a reference to the values and don't contain a copy of the elements. For example, if you have two lists List A and List B and you assign List A to the List B, you will have two variables pointing to the same list instead of two independent copies. When changing values in one variable, the other is also changed.

## Runtime Properties

OutSystems provides the following runtime properties for lists:

| Property | Type | Access type | Comment |
| :--- | :--- | :--- | :--- |
| Current | List element type | Read/write | Allows direct access to the current element. |
| EOF | Boolean | Read only | Indicates whether the end of the list was exceeded. When you are iterating the last element, this property is still FALSE. |
| BOF | Boolean | Read only | Indicates whether you are at the beginning of the list. When you are iterating the first element, this property is True. |
| CurrentRowNumber | Integer | Read only | The index of the current element in the list, starting with 0. %%If the list is empty, this property is 0. |
| Length | Integer | Read only | The number of elements currently in the list. |
| Empty | Boolean | Read only | Indicates whether the list is empty. |

## List System Actions

The following System Actions are available to manipulate a List:

| System Action | Description |
| :--- | :--- |
| [ListAll](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListAll%3E) | Determines if all the elements in the list satisfy the given condition. |
| [ListAny](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListAny%3E) | Determines if any of the elements in the list satisfies the given condition. |
| [ListAppend](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListAppend%3E) | Adds an element to the end of a list. |
| [ListAppendAll](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListAppendAll%3E) | Adds the elements of the source list to the end of the destination list. |
| [ListClear](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListClear%3E) | Removes all elements from a list. |
| [ListDuplicate](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListDuplicate%3E) | Duplicates the elements of a list into another list. |
| [ListFilter](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListFilter%3E) | Produces a new list with the elements of the source list that satisfy the given condition. |
| [ListIndexOf](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListIndexOf%3E) | Returns the position of the first element that satisfies the given condition, or -1 if no element was found. |
| [ListInsert](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListInsert%3E) | Inserts an element in a specific position of a list. |
| [ListRemove](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListRemove%3E) | Removes an element from a specific position of a list. |
| [ListSort](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#ListSort%3E) | Sorts the elements in the list by the given criteria. |

