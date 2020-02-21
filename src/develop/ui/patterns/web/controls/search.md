---
tags: runtime-traditionalweb;
summary: >-
  Search allows the user to find pieces of content without the use of
  navigation.
---

# Search

Allow the user to find pieces of content without the use of navigation.

Use the Search so that end-users can easily find pieces of content by entering queries. Unlike navigation, knowledge of the content's location isn't required.

**How to use**

1. Drag Search pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/search-image-1.png%3E)

2. Set a Local Variable for the input of type Text.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/search-image-2.png%3E)

3. Publish and test.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| ExtendedClass | Add custom style classes to this Block. | Text | No | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/search-image-3.png%3E)

## Advanced Use Case

### Make a reset search button

For this example, refer to the [FourColumns Screen Template](https://outsystemsui.outsystems.com/OutSystemsUILiveStyleGuide/FourColumnGallery.aspx).

1. Go to the Search Pattern presented in Column2 inside the Filters\_Wrapper container.
2. Drag a container inside the Actions placeholder.
3. Drag a Icon Widget inside that container and choose `Entities.IconName.times` for the Name parameter. This is the X icon.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/search-image-4.png%3E)

4. In the container, set the Display parameter to `If(SearchKeyword <> "", True, False)`. This uses the already existing SearchKeyword Local Variable and only displays the container if the search input has text.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/search-image-5.png%3E)

5. Add an OnClick event and set the handler to the RefreshTable action.
6. Set the parameters ResetFilters and ResetPagination to True. 
7. In the Category property, set the ProductCategory Local Variable. This way you reset the search input as well as the screen to the default state.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/search-image-6.png%3E)

8. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/search-gif-1.gif%3E)

