---
tags: runtime-mobileandreactiveweb;
summary: null
---

# DatePicker Pattern

The DatePicker pattern provides you with a date and time picker with a flat UI to display inline on the screen. It can receive lists of dates with events and it enables you have a selection within a range of days. The DatePicker was created using the [Pikaday.js library](https://github.com/dbushell/Pikaday/blob/master/README.md) .

You can use this pattern to display a list of elements side by side, with a different number of items per row on different devices.

## How to Use the DatePicker Pattern

Use static data or a **List** widget inside this block to display items in a gallery pattern.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/mobile/images/datepicker.png?width=600)

1. Upon dragging the DatePicker to the page, you'll be prompted to create an event.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/mobile/images/datepicker_create_an_event.png?width=500)

2. To have access to the picked date, you need to create an assign to the **startDate** \(if SelectInterval is False \).

3. Set the default value of the variable **PickedDate** as CurrDateTime\(\).

![](../../../../../.gitbook/assets/datepicker_start.png)

**Result**:

![](../../../../../.gitbook/assets/datepicker_basicexample.gif)

### Listing Events of a Selected Day

1. Set the area where you want to put the list of events.

![](../../../../../.gitbook/assets/add_new_date.png)

2. Create an entity with a **DateTime** attribute.

3. Set the entity in your **EventList** parameter on eventList, using the right attribute to map.

![](../../../../../.gitbook/assets/interaction_datepicker.png)

4. Add the list to the page.

![](../../../../../.gitbook/assets/date_time.png)

5. Create a Local Variable.

![](../../../../../.gitbook/assets/date_local_variable.png)

6. Get another Aggregate for the Events and set a filter on the aggregate:  
DateTimeToDate\(Events.DateTime\) = Date

![](../../../../../.gitbook/assets/datepicker_filter.png)

**Result**:

![](../../../../../.gitbook/assets/datepicker_profit.gif)

## Input Parameters

| **Input Name** | **Description** | **Default Value** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/input.png)  EventList | Receives a List of DateTime records that are used to highlight days as event days. | none |
| ![](../../../../../.gitbook/assets/input.png) MinDate | Days before this date will be disabled. | none |
| ![](../../../../../.gitbook/assets/input.png) MaxDate | Days after this date will be disabled. | none |
| ![](../../../../../.gitbook/assets/input.png) InitialDate | The initially selected day for the DatePicker. If not set, it will be the current day by default. | Current Date |
| ![](../../../../../.gitbook/assets/input.png) ShowWeekNumbers | Displays the week number on the left side of the DatePicker. | True |
| ![](../../../../../.gitbook/assets/input.png) FirstWeekDay | Defines which weekday should be displayed first. %%  0: Sunday %% 1: Monday %% 2: Tuesday %% 3: Wednesday %% 4: Thursday %% 5: Friday %% 6: Saturday | 1 |
| ![](../../../../../.gitbook/assets/input.png) ShowTime | Displays a time picker below the DatePicker. | False |
| ![](../../../../../.gitbook/assets/input.png) Show24HourFormat | Changes the time picker to a 24-hour format. | True |
| ![](../../../../../.gitbook/assets/input.png) DisabledDaysList | Receives a List of DateTime records that will be disabled on the DatePicker. If this parameter is not set, all days between the MinDate and MaxDate are enabled. No default value. | none |
| ![](../../../../../.gitbook/assets/input.png) DisabledWeekDays | String containing disabled weekdays. If the string is empty, all weekdays are active. Example with Sunday and Friday disabled: "0,5,6". %% 0: Sunday %% 1: Monday %% 2: Tuesday %% 3: Wednesday %% 4: Thursday %% 5: Friday %% 6: Saturday | none |
| ![](../../../../../.gitbook/assets/input.png) SelectInterval | Allows the selection between two dates. If set to True, the Block Event "On Select" has the values for both parameters. | False |

## Events

| **Event Name** | **Description** | **Mandatory** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/event.png) OnSelect | Action to execute after selecting a DatePicker day. If SelectInterval is enabled, both parameters return values. If not, only the StartDate has a value. | True |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/mobile/images/datepicker_layout_classes.png?width=700)

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/css_selector.png) td | .is-selected | Clicked day. |
| ![](../../../../../.gitbook/assets/css_selector.png) td | .is-startrange | If SelectInterval is True , this class will be the start range value. |

