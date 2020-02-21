---
tags: runtime-traditionalweb;
summary: LayoutTopMenu uses the space available on the top for navigation.
---

# LayoutTopMenu

Custom layout with a fixed menu on top.

Useful for simple applications, without a complex navigation structure.

**How to use**

Fill in the placeholders with the content that you need.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-tm-image-2.png?width=600%3E)

## Input parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| ExtendedClass | Adds custom style classes to this Block | Text | False | none |
| DeviceConfiguration | Configuration to change the default values that set when the application is seen as phone, tablet or desktop. | DeviceConfig | False | none |

## Layout and classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-tm-image-1.png%3E)

## Responsive behavior

This layout comes with a default responsive behavior. On tablets it remains the same as on desktop. But on phones it breaks the content vertically, making the placeholders Title and Actions full-width.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-tm-image-3.png%3E)

The menu also adapts to mobile, moving the navigation to a sidebar, toggled by a hamburger icon.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-tm-image-4.gif%3E)

On a mobile phone and tablet:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-tm-image-7.png%3E)

## Advanced

Here are some more advanced use-cases of the widget.

### Customize your responsive breakpoints

1. Go to the Common Flow.
2. Double-click on your Layout to open the widget tree. 
3. Go to the LayoutTopMenu parameters.
4. Toggle the DeviceConfiguration 'plus icon'.
5. Set your custom breakpoints \(in pixels\). On the example below the phone breaks is set to happen only when the Device with is at 200px.
6. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-tm-image-5.png%3E)

### Customize your content max-width

1. Go to Themes.
2. In the Grid section, set your custom width \(default value is 1280px\) in the Max. Width parameter.
3. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-tm-image-6.png%3E)

## Device compatibility

In Internet Explorer we made specific CSS that uses 'position: fixed' instead of 'position: sticky', as 'sticky' is not supported in Internet Explorer.

## Notes

In Internet Explorer 10 and 11, we added some specific behaviors to account for the flicker caused by the slow loading time of polyfill CSS Variables. If there are any JavaScript errors, this will cause the screen to appear white.

To override this behavior, add the following code snippet to your CSS theme:

```css
.ie10,
.ie11 {
   display: block;
}
```

