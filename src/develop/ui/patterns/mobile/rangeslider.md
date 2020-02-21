---
tags: runtime-mobileandreactiveweb;
summary: null
---

# RangeSlider Pattern

The RangeSlider pattern allows you to set a value by dragging a handle within a configured range. It is used to control a variable value with simple and interactive user input.

## How to Use the RangeSlider Pattern

Bind your variable to the **InitialValue** input and use the **OnChange** event to add your logic to handle value changes.

![](../../../../../.gitbook/assets/range_slider.png)

1. After setting the **MinValue** , **MaxValue** and the **InitialValue** , you'll need to create the **OnChange** event.

![](../../../../../.gitbook/assets/range_slider_on_change.png)

2. Create an integer value and assign it.

![](../../../../../.gitbook/assets/range_slder_integer.png)

**Result**:

![](../../../../../.gitbook/assets/rangeslider_basicendresult.gif)

### Changing the Color of the Bar

![](../../../../../.gitbook/assets/range_slider_color_bar_1.png)

![](../../../../../.gitbook/assets/range_slider__change_color.png)

![](../../../../../.gitbook/assets/range_slider_color_bar_2.png)

### Changing the Size of the Handles

![](../../../../../.gitbook/assets/range_slider_handle_size_1.png)

![](../../../../../.gitbook/assets/range_slider_change_size_of_handles.png)

![](../../../../../.gitbook/assets/range_slider_handle_size_2.png)

## Input Parameters

| **Input Name** | **Description** | **Default Value** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/input.png) MinValue | Slider's minimum value. | none |
| ![](../../../../../.gitbook/assets/input.png) MaxValue | Slider's maximum value. | none |
| ![](../../../../../.gitbook/assets/input.png) InitialValue | Value selected by default. Must be between min and max values. | none |
| ![](../../../../../.gitbook/assets/input.png) Step | Slider moves in increments of Step. If Step is 10, the slider will go from 0 to 10, to 20, to 30, etc. | 1 |
| ![](../../../../../.gitbook/assets/input.png) ShowPips | Show pips below the slider. | True |
| ![](../../../../../.gitbook/assets/input.png) PipsStep | Range interval after which a Pip is drawn \(when ShowPips is enabled\). If not specified, the component will try to guess what step fits your data. | -1 |
| ![](../../../../../.gitbook/assets/input.png) ChangeEventDuringSlide | Triggers Change events while the slider is being dragged. If set to _False_ , the Change events will only be triggered when the user releases the slider. **Tip**: If you're refreshing a query based on the value of the slider, you probably want to set this to _False_ . | True |

## Events

| **Event Name** | **Description** | **Mandatory** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/event.png) OnChange | Action to execute after selecting a new value on the slider. Returns the new Value. | _True_ |

## Layout and Classes

![](../../../../../.gitbook/assets/range_slider_layout_and_classes.png)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/css_selector.png) noUi-handle | .noUi-active | Class added when handle is clicked. |

## Samples

This sample uses the RangeSlider pattern:

![](../../../../../.gitbook/assets/rangeslider-sample-1.PNG)

