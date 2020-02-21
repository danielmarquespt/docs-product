---
tags: runtime-traditionalweb;
summary: Sidebar shows additional content on the side of the screen.
---

# Sidebar

Shows additional content on the side of the screen.

Use the Sidebar to place additional information in the margin of the main content. The additional information supports the end-user's understanding of the main content.

**How to use**

To trigger the sidebar, call a new screen action through a button with Ajax submit and use the ToggleSidebar action \(found in the Logic Tab\) to open/close it. Use the parameters to define if it has Overlay in the page.

1. Drag the Sidebar pattern into the preview.
2. Set the content in the placeholders.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/sidebar-image-1.png%3E)

3. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/sidebar-image-2.png?width=750%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| HasOverlay | When set to true enables a clickable overlay. | Boolean | False | False |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/sidebar-image-3.png%3E)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .sidebar | .sidebar.is--hidden | When Sidebar is closed |
| .sidebar | .sidebar.is--visible | When Sidebar is open |

