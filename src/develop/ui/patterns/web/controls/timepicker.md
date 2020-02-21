---
tags: runtime-traditionalweb;
summary: TimePicker selects a single time from a list.
---

# TimePicker

Selects a single time from a list.

Use the Time Picker to enable end-users to select a single time from a dropdown.

**How to use**

1. Drag the TimePicker pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-1.png%3E)

2. Set a variable of type Time to the input.
3. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-gif-1.gif%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| StartTime | The time that the dropdown options will scroll to in order to have it as the first item. Make sure that the time is according to the interval that you set to begin with. Default is NewTime\(0,0,0\) -&gt; 12:00am. Example: If you set the interval as 30, but the Start Time as 10:05:00. Then while it will be the time that it'll appear on the input, the drop down won't scroll down to the hour since it doesn't match the interval. | Time | No | NewTime\(0,0,0\) |
| Interval | Interval of time \(in minutes\) between options. Example: If 30, then the options will appear as: 08:00:00, 08:30:00, 09:00:00... | Integer | No | 30 |
| Is24hFormat | If true, then time format will be 24 hour. If false, then 12 hour. | Boolean | No | True |
| AdvancedFormat | Allows for more options than the ones given in the input parameters. Inputs: TimePickerAdvancedFormat:  DisabledTimes \(Time List\), MinTime \(Time\), MaxTime \(Time\), StartEmpty \(Boolean\) | TimePickerAdvancedFormat | No | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-2.png%3E)

## Events

| **Event Name** | **Description** | **Mandatory** |
| :--- | :--- | :--- |
| OnSelect | Event will be triggered when a time is selected returning it. | False |

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .time-option | .time-option-selected | When the time option is selected |
| .time-option | .time-picker .dropdown-content-list .time-option\[disabled="disabled"\] | When the time option is disabled |

## Advanced Use Case

### Use the OnSelect event

1. Drag the TimePicker pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-1.png%3E)

2. Set a variable of type Time to the input.
3. Set the StartTime Parameter to a variable Time.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-3.png%3E)

4. In the preparation, set the Time variable to the start time you want for the picker.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-4.png%3E)

5. Set the OnSelect Event to TimePatternOnSelect.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-5.png%3E)

6. In the TimePatternOnSelect action, assign TimeSelected to the Time variable.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-6.png%3E)

7. Set a Feedback\_Message action and show the Timein the message.
8. Create a container Timepicker\_Container around the TimePicker.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-7.png%3E)

9. In the action TimePatternOnSelect, add an Ajax refresh for the Timepicker\_Container.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-8.png%3E)

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-gif-2.gif%3E)

### Disable specific times

1. Drag the TimePicker pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-1.png%3E)

2. Set a variable of type Time to the input.
3. Click the plus before the AdvancedFormat parameter.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-9.png%3E)

4. Click the plus before the DisabledTimes parameter.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-10.png%3E)

5. Add the times NewTime\(4,0,0\) and NewTime\(7,0,0\).

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-11.png%3E)

6. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-gif-3.gif%3E)

### Start Input as Empty

1. Drag the TimePicker pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-1.png%3E)

2. Set a variable of type time to the input.
3. Click the plus before the AdvancedFormat parameter.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-9.png%3E)

4. Set the StartEmpty parameter to True.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-12.png%3E)

5. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/timepicker-image-13.png%3E)

