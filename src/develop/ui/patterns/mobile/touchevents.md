---
tags: runtime-mobileandreactiveweb;
summary: null
---

# TouchEvents Pattern

The TouchEvents pattern enables touch events on a specific widget.

![](../../../../../.gitbook/assets/touch_events_utilities.png)

## How to Create Custom Patterns with TouchEvents

You can call the **event.preventDefault\(\)** to prevent the default action associated with each event from occurring. The touchstart and touchend events don't need this action, but touchmove requires it to stop screen scrolling when the user is moving the finger inside the element.

![](../../../../../.gitbook/assets/touch_events_custom_patterns.png)

To use the **event.preventDefault\(\)** , use this string of code:

`$parameters.Evt.preventDefault();`

## How to Hide a Header During a Scroll Action

You can use the pattern to hide a header during a scroll action.

1. Add the **TouchEvents** pattern to the **Layout** block.

![](../../../../../.gitbook/assets/touch_events_layour.png)

2. Add an **End** event.

![](../../../../../.gitbook/assets/add_end_event.png)

3. Add logic.

![](../../../../../.gitbook/assets/touch_events_logic.png)

| Element | Code |
| :--- | :--- |
| ![](../../../../../.gitbook/assets/js_hide.png) | var header = document.querySelector\(".hearder"\);%%header.classList.add\("hide"\);%%header.classList.add\("header-on-scroll"\); |
| ![](../../../../../.gitbook/assets/js_show.png) | var header = document.querySelector\(".header"\);%%header.classList.remove\("hide"\);%%header.classList.remove\("header-on-scroll"\); |

Result:

![](../../../../../.gitbook/assets/touchevents_endresult.gif)

## Input Parameters

| **Input Name** | **Description** | **Default Value** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/input%20%2810%29.png) WidgetId | This is the element that responds to the touch you configure. | none |

## Events

| **Event Name** | **Description** | **Mandatory** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/event%20%281%29.png) End | The event is triggered after the movement event finishes. | _False_ |
| ![](../../../../../.gitbook/assets/event.png) Move | The event is triggered after the movement starts. | _False_ |
| ![](../../../../../.gitbook/assets/event%20%284%29.png) Start | The event is triggered as the touch movement starts. | _False_ |

## Compatibility with other Patterns

There might be conflicts with any pattern with touch events used together with this pattern \(unless the code is altered to expect this behavior\).

## Samples

The following sample uses the TouchEvents pattern:

![](../../../../../.gitbook/assets/touchevents-sample-1.PNG)

