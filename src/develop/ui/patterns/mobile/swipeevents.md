---
tags: runtime-mobileandreactiveweb;
summary: null
---

# SwipeEvents Pattern

The SwipeEvents pattern enables swiping on a specific widget.

![](../../../../../.gitbook/assets/swipe_events.png)

## How to Use the SwipeEvents Pattern

You can use the SwipeEvents pattern to open a sidebar.

![](../../../../../.gitbook/assets/swipe_area.png)

Create a local variable, called isOpen to be used in the sidebar.

![](../../../../../.gitbook/assets/swipe_events_create.png)

Result:

![](../../../../../.gitbook/assets/swipeevents_endresult.gif)

## Input Parameters

| **Input Name** | **Description** | **Default Value** |  |
| :--- | :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/input%20%284%29.png) | WidgetId | Element that will be swipeable. | none |

## Events

| **Event Name** | **Description** | **Mandatory** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/event%20%286%29.png) SwipeDown | The event is triggered after a swipe down. | _False_ |
| ![](../../../../../.gitbook/assets/event%20%285%29.png) SwipeLeft | The event is triggered after a swipe left. | _False_ |
| ![](../../../../../.gitbook/assets/event%20%288%29.png) SwipeRight | The event is triggered after a swipe right. | _False_ |
| ![](../../../../../.gitbook/assets/event%20%283%29.png) SwipeUp | The event is triggered after a swipe up. | _False_ |

## Compatibility with other Patterns

There might be conflicts with any pattern with touch events \(unless the code is altered to support the behavior\). For example: using the id of a sidebar instead of a container in the previous example.

* HorizontalScroll 
* [Carousel](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/mobile/carousel.md%3E)
* [TouchEvents](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/mobile/touchevents.md%3E)
* [StackedCards](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/mobile/stackedcards.md%3E)
* Notification 
* Sidebar 

## Samples

The following sample uses the SwipeEvents pattern:

![](../../../../../.gitbook/assets/swipeevents-sample-1.PNG)

