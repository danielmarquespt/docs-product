---
tags: runtime-traditionalweb;
summary: >-
  LayoutLoginSplit is a custom page layout for the login screen that divides the
  page into 2 columns.
---

# LayoutLoginSplit

A custom page layout for the login screen that divides the page into 2 columns.

**How to use**

1. In the Login screen, select the object tree and use LayoutLoginSplit instead of the current Layout. 
2. OutSystems UI Layout Login already has the LoginForm by default. Add input widgets to the correct placeholders as required.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| DeviceConfiguration | Configuration to change the default values that set when the application will be seen as phone, tablet or desktop | DeviceConfig | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-loginsplit-image-1.png%3E)

### Login

Drag login related content to this placeholder.

## Advanced Use Case

### Change background to image

1. In the Interface tab, go to the Login screen.
2. Remove the background container and drag an image. 
3. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-loginsplit-gif-1.gif?width=600%3E)

### Change Layout structure

1. In the Interface tab, go to the Login screen.
2. Change the Column type by using the corresponding parameter \(for instance, ColumnsMediumRight\).
3. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-loginsplit-gif-2.gif?width=600%3E)

## Compatibility with other Patterns

LoginForm

