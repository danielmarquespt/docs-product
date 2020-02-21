---
tags: runtime-mobileandreactiveweb;
summary: null
---

# Columns Pattern

The Columns pattern enables you to split content into multiple columns. You can configure the behavior using the input parameters. They will define how columns will stack in different devices. This is ideal to improve the way information is displayed across different devices. You can use this pattern to display a list of elements side by side, with a different number of items per row on different devices.

Here's the preview , in Service Studio, of the different ways columns can be split into:

![](../../../../../.gitbook/assets/column_gutter.png)

![](../../../../../.gitbook/assets/column_columns.png)

## How to Use the Columns Pattern

Configure the behavior using the input parameters to define how columns will stack in different devices.

For an uneven number of columns, the following splits apply:

**Entities.ColumnBreak.BreakNone \(default\)**

![](../../../../../.gitbook/assets/column_break_none.png)

**Entities.ColumnBreak.BreakMiddle**

![](../../../../../.gitbook/assets/column_break_middle.png)

**Entities.ColumnBreak.BreakLast**

![](../../../../../.gitbook/assets/column_break_last.png)

**Entities.ColumnBreak.BreakFirst**

![](../../../../../.gitbook/assets/column_break_first.png)

## Input Parameters

| **Input Name** | **Description** | **Default Value** |
| :--- | :--- | :--- |
| ![](../../../../../.gitbook/assets/input%20%281%29.png) UseGutter | Creates a space between columns. | True |
| ![](../../../../../.gitbook/assets/input%20%287%29.png) PhonePortraitBreak | Behavior of the columns in a Phone with Portrait orientation. | BreakNone |
| ![](../../../../../.gitbook/assets/input%20%283%29.png) PhoneLandscapeBreak | Behavior of the columns in a Phone with Landscape orientation. | BreakNone |
| ![](../../../../../.gitbook/assets/input%20%2814%29.png) TabletPortraitBreak | Behavior of the columns in a Tablet with Portrait orientation. | BreakNone |
| ![](../../../../../.gitbook/assets/input%20%2815%29.png) TabletLandscapeBreak | Behavior of the columns in a Tablet with Landscape orientation. | BreakNone |

## Layout and Classes

![](../../../../../.gitbook/assets/column_layout.png)

## Samples

See how the [Account Dashboard sample](https://silkui.outsystems.com/Samples_Mobile.aspx#Mobile_Details-Samples_AccountDashboard) uses the Columns pattern:

![](../../../../../.gitbook/assets/sample_account_dashboard.png)

