---
tags: runtime-traditionalweb;
summary: LayoutPopup is the layout used to display additional off-canvas information.
---

# LayoutPopup

The Layout for the [RichWidgets Popup Editor](../../../inputs/popup.md).

Useful to display additional off-canvas information.

**How to use**

1. In the Popup screen, select the object tree and set the layout to LayoutPopup.
2. Add your content inside the layout.
3. Use this screen as destination for the [RichWidgets Popup Editor](../../../inputs/popup.md).

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| DeviceConfiguration | Configuration to change the default values that set when the application will be seen as phone, tablet or desktop | DeviceConfig | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-popup-image-1.png%3E)

### MainContent

Drag your content to this placeholder.

## Advanced Use Case

### Customize your responsive breakpoints

1. Go to the Common Flow.
2. Double-click the Layout to open the widget tree. 
3. Go to the LayoutPopup properties.
4. Toggle the DeviceConfiguration 'plus icon'.
5. Set the custom breakpoints \(in pixels\). In the example below, the phone breaks are set to happen only when the Device width is at 200px.
6. Publish and test.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/layout/images/layout-popup-image-2.png%3E)

## Notes

In Internet Explorer 10 and 11, we added some specific behaviors to account for the flicker caused by the slow loading time of polyfill CSS Variables. If there are any JavaScript errors, this will cause the screen to appear white.

You can override the following code to avoid this behavior.

```css
.ie10,
.ie11 {
   display: none;
}

.ie10.ponyfill-ready,
.ie11.ponyfill-ready {
   display: block;
}
```

## Compatibility with other Patterns

[RichWidgets Popup Editor](../../../inputs/popup.md)

