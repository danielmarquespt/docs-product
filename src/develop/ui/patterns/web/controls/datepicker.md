---
tags: runtime-traditionalweb;
summary: >-
  DatePicker allows the end-user to select a single or a range of dates using a
  calendar.
---

# DatePicker

Select a single date or a range of dates.

Use the DatePicker to allow the end-user to select a single or a range of dates using a calendar.

**How to use**

Drag an input and the DatePicker to the screen and set up the parameters. Only the InputWidgetId parameter is mandatory and must reference an input widget that will show the date picked on the page.

For advanced options, you can check the official documentation of the [Pikaday library](https://github.com/dbushell/Pikaday).

1. Drag an Input widget into the preview.
2. Give a name to the input \(for instance, datepicker\).

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-1.png%3E)

3. Set a variable of type **date** to the input.
4. Drag the DatePicker into the preview.
5. Set the InputWidgetId to the input name.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-2.png%3E)

6. In the Events, create the OnClose and OnSelect events.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-7.png%3E)

7. Use the date in the input parameter in your logic.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-8.png%3E)

8. Publish and test.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| InputWidgetId | Input Element Name that will trigger the element to be visible. | Text | _True_ | none |
| ButtonWidgetId | Element Name \(example: button\) that will trigger the element to be visible. | Text | False | "" |
| DisabledDates | List of dates for the disabled days. | Date List | False | none |
| MinDate | Date Picker enables dates from this date onwards and disables dates before this date. | Date | False | none |
| MaxDate | Date Picker enables dates that come before this date and disables dates after this date. | Date | False | none |
| InitialDate | If set, the calendar will initially display the set date, otherwise it will display the  current Date. | Date Time | False | CurrDate\(\) |
| DateFormat | Defaults to the date format defined in the server configuration. The default is the server date format. | Text | False | "" |
| AdvancedFormat | Allows for more options than the ones given in the input parameters. | DatePickerAdvancedFormat | False | CurrDate\(\) |
| SelectInterval | Allows the selection between two dates. If set to True, the Block Event "On Select" has the values for both parameters. | False |  |  |

### DatePickerAdvancedFormat information

Here is the overview of some advanced properties.

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| EventsList | A list of events \(type Date Time\) | Date Time List | False | none |
| AdvancedFormatJSON | A string with options such as: `{ disableWeekends: true,  BeginEmpty: true }`. For more advanced options, read the official documentation: [https://github.com/dbushell/Pikaday](https://github.com/dbushell/Pikaday) | Date Time List | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-3.png?width=600%3E)

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-4.png?width=600%3E)

### Month Picker

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-5.png?width=600%3E)

### Year Picker

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-6.png?width=600%3E)

## Events

| **Event Name** | **Description** | **Mandatory** |
| :--- | :--- | :--- |
| onClose | Event that will be triggered once you close the date picker which returns the last selected date. | False |
| onOpen | Event that will be triggered once you open the date picker. | False |
| OnSelect | Event will be triggered when a date is selected returning it. | False |

## Advanced Use Case

### Start with a blank input

1. Drag the DatePicker to the preview.
2. Expand the AdvancedFormat property.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-9.png%3E)

3. Add `{ BeginEmpty: true }` in the AdvancedFormatJSON.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-11.png%3E)

### Have a flat datepicker

1. Drag the DatePicker to the preview.
2. Expand the AdvancedFormat property.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-9.png%3E)

3. Add `{ bound: false }` in the AdvancedFormatJSON.
4. To use events to pick the chosen date, use OnSelect instead of OnClose.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-10.png%3E)

### Add Events

1. Drag the DatePicker to the preview.
2. Expand the AdvancedFormat property.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-9.png%3E)

3. Add your date time list in the EventList.

### Use Date Format

1. Drag the DatePicker to the preview.
2. Set the format of the date \(for instance, `"DD MMM of YYYY"` will be displayed as 12 Dec of 2018\).
3. Create an onClose or OnSelect event and use the date for your logic.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-image-12.png%3E)

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/datepicker-gif-1.gif%3E)

## Device Compatibility

When used on mobile devices, it should be used horizontally to avoid issues related to the positioning of the DatePicker.

