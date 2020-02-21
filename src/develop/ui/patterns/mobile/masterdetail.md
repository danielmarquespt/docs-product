---
tags: runtime-mobileandreactiveweb;
summary: null
---

# MasterDetail Pattern

The MasterDetail pattern is similar to the SplitScreen pattern, but it receives an item list for the left panel. You can use this pattern in tablet apps, to display the detail of a list of items.

Here's the preview in Service Studio:

![](../../../../../.gitbook/assets/pasted_image_at_2017_05_10_04_53_pm.png)

## How to Use the MasterDetail Pattern

Start by binding a List to the **ItemList** parameter and leverage the Block events to change the content placeholder.

1. Create a local boolean variable and set it on **OpenedOnPhone**.

![](../../../../../.gitbook/assets/masterdetail_list_open.png)

2. To open the detail of the clicked element, use a link for an action, set your local variable to _True_ , and add logic to open the correct detail.

![](../../../../../.gitbook/assets/masterdetail_assignments.png)

3. To close the detail, create an action and set your local variable to _False_ , and use this action in the **DetailClose** event. Add necessary logic.

![](../../../../../.gitbook/assets/masterdetail_close_detail.png)

![](../../../../../.gitbook/assets/masterdetail_list_open_false.png)

### Phone Landscape with the Same Behavior as Tablet

You can have your phone in landscape to work the same way as a tablet:

```text
.phone.landscape .split-left {
     width: **x; /* This is width value for the left side */**
}



.phone.landscape .split-right {
     -webkit-transform: translateX(0) translateZ(0);
      transform: translateX(0) translateZ(0);
    width: **x; /* This is the width value for the right side */**
     left: auto;
    right: 0;
    border-left: 1px solid #d3d3d3;
}


.phone.landscape .detail-open .split-right-close {
    opacity: 0;
    pointer-events: none;
}


.phone.landscape .detail-open .app-menu-icon {
    opacity: 1;
    pointer-events: auto;
}
```

## Input Parameters

| **Input Name** | **Description** | **Default Value** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/input%20%281%29.png) ItemList | These are the items for the list on the left side of the MasterDetail. | N/A |

## Events

| **Event Name** | **Description** | **Mandatory** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/event%20%283%29.png) DetailClose | Triggered when the detail \(or right side of the MasterDetail\) is closed. | _False_ |
| ![](../../../../../.gitbook/assets/event%20%283%29.png) ItemSelected | Triggered when an item of the list \(or left side of the MasterDetail\) is selected. | _False_ |

## Layout and Classes

![](../../../../../.gitbook/assets/masterdetail_layout.png)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/css_selector%20%282%29.png) MasterDetail Wrapper | .split-screen-wrapper | Container that wraps elements in the left and right containers. |
| ![](../../../../../.gitbook/assets/css_selector%20%285%29.png) Left Content | .split-left | Add content to the left side. |
| ![](../../../../../.gitbook/assets/css_selector%20%281%29.png) Right Content | .split-right | Add content to the right side. In phone view, this Element is off-canvas. |
| ![](../../../../../.gitbook/assets/css_selector%20%288%29.png) Close Right Content | .split-right-close |  |

## Compatibility with Other Patterns

This pattern should be used alone inside the screen content because it will adapt to the height of the parent. Additionally, you should avoid using the MasterDetail pattern inside patterns with swipe events, like [Tabs](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/mobile/tabs.md%3E).

## Samples

You can use the MasterDetail pattern as a sample:

![](../../../../../.gitbook/assets/masterdetail-sample-1.PNG)

