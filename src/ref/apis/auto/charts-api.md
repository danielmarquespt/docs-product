# Charts API

For Platform Version 10.0.0.308. Component with widgets for plotting charts in web apps.

## Summary

| Widget | Description |
| :--- | :--- |
| [AreaChart](charts-api.md#AreaChart%3E) | Area charts illustrate the contribution of values to a total over time. |
| [BarChart](charts-api.md#BarChart%3E) | Bar charts compare multiple values using horizontal bars.%%In this chart, the X-axis runs vertically and the Y-axis runs horizontally. |
| [ColumnChart](charts-api.md#ColumnChart%3E) | Column charts compare multiple values using vertical bars. |
| [LineChart](charts-api.md#LineChart%3E) | Line charts illustrate trends of values over time. |
| [PieChart](charts-api.md#PieChart%3E) | Pie charts illustrate proportions of values. |

| Action | Description |
| :--- | :--- |
| [AdvancedFormat\_Init](charts-api.md#AdvancedFormat_Init%3E) | Initializes an AdvancedFormat record with the values passed as arguments. The record is returned by the action. |
| [ChartFormat\_Init](charts-api.md#ChartFormat_Init%3E) | Initializes a ChartFormat record with the values passed as arguments. The record is returned by the action. |
| [DataPoint\_GetClicked](charts-api.md#DataPoint_GetClicked%3E) | Returns the data point that was clicked on the chart.%%Execute this action in the On Click action of a chart. |
| [DataPoint\_Init](charts-api.md#DataPoint_Init%3E) | Initializes a DataPoint record with the values passed as arguments. The record is returned by the action. |
| [DataPoint\_InitMissing](charts-api.md#DataPoint_InitMissing%3E) | Initializes a DataPoint to plot a gap on the chart. The record is returned by the action. |
| [XAxisFormat\_Init](charts-api.md#XAxisFormat_Init%3E) | Initializes an XAxisFormat record with the values passed as arguments. The record is returned by the action. |
| [YAxisFormat\_Init](charts-api.md#YAxisFormat_Init%3E) | Initializes an YAxisFormat record with the values passed as arguments. The record is returned by the action. |

| Structure | Description |
| :--- | :--- |
| [AdvancedDataPointFormat](charts-api.md#Structure_AdvancedDataPointFormat%3E) | Information to format a data point using Highcharts JSON. |
| [AdvancedDataSeriesFormat](charts-api.md#Structure_AdvancedDataSeriesFormat%3E) | Information to format a data series using Highcharts JSON. |
| [AdvancedFormat](charts-api.md#Structure_AdvancedFormat%3E) | Information to format chart elements using Highcharts JSON. |
| [ChartFormat](charts-api.md#Structure_ChartFormat%3E) | Information to format the chart. |
| [DataPoint](charts-api.md#Structure_DataPoint%3E) | Information to plot a data point on the chart. |
| [XAxisFormat](charts-api.md#Structure_XAxisFormat%3E) | Information to format the X-axis on the chart. |
| [YAxisFormat](charts-api.md#Structure_YAxisFormat%3E) | Information to format the Y-axis on the chart. |

| Static Entity | Description |
| :--- | :--- |
| [LegendPosition](charts-api.md#StaticEntity_LegendPosition%3E) | The position where the legend is displayed on charts. |
| [StackingType](charts-api.md#StaticEntity_StackingType%3E) | The way to plot multiple data series on Area, Bar, or Column charts:%%- ‘NoStacking’: plot data series side by side to compare them;%%- ‘Stacked’: plot data series stacked to show their contribution to a total;%%- ‘Stacked100Percent’: plot data series stacked to show their percentage in a total. |
| [XAxisValuesType](charts-api.md#StaticEntity_XAxisValuesType%3E) | The data type of labels displayed on the X-axis to format them.%%Using ‘Auto’ means the type is inferred from the label of the first data point. |

## Widgets

### AreaChart { \#AreaChart }

Area charts illustrate the contribution of values to a total over time.

_Inputs_

SourceDataPointList : Type: mandatory, [DataPoint](charts-api.md#Structure_DataPoint%3E) List.  
The list of all data points to be plotted on the chart.

StackingType : Type: optional, StackingType Identifier.  
The way to plot multiple data series on the chart:  
- ‘NoStacking’: plot data series overlapped to compare them;  
- ‘Stacked’: plot data series stacked to show their contribution to a total;  
- ‘Stacked100Percent’: plot data series stacked to show their percentage in a total.  
‘Stacked’ is the default option.

Height : Type: optional, Integer.  
The vertical size of the chart in pixels \(300 by default\).  
The horizontal size of the chart is the parent’s width.

LegendPosition : Type: optional, LegendPosition Identifier.  
The position where the legend is displayed on the chart \(‘Bottom’ by default\).  
The legend is hidden if no series name is set in any data point.

XAxisFormat : Type: optional, [XAxisFormat](charts-api.md#Structure_XAxisFormat%3E).  
Formatting options for the X-axis.  
Action XAxisFormat\_Init helps to create and initialize this parameter.

YAxisFormat : Type: optional, [YAxisFormat](charts-api.md#Structure_YAxisFormat%3E).  
Formatting options for the Y-axis.  
Action YAxisFormat\_Init helps to create and initialize this parameter.

ChartFormat : Type: optional, [ChartFormat](charts-api.md#Structure_ChartFormat%3E).  
Formatting options for the chart.  
Action ChartFormat\_Init helps to create and initialize this parameter.

Clickable : Type: optional, Boolean.  
Set to True to allow clicking on plotted values and execute the On Click action \(False by default\).

AdvancedFormat : Type: optional, [AdvancedFormat](charts-api.md#Structure_AdvancedFormat%3E).  
Highcharts JSON to format elements displayed on the chart.  
Action AdvancedOptions\_Init helps to create and initialize this parameter.

### BarChart { \#BarChart }

Bar charts compare multiple values using horizontal bars.  
In this chart, the X-axis runs vertically and the Y-axis runs horizontally.

_Inputs_

SourceDataPointList : Type: mandatory, [DataPoint](charts-api.md#Structure_DataPoint%3E) List.  
The list of all data points to be plotted on the chart.

StackingType : Type: optional, StackingType Identifier.  
The way to plot multiple data series on the chart:  
- ‘NoStacking’: plot data series side by side to compare them;  
- ‘Stacked’: plot data series stacked to show their contribution to a total;  
- ‘Stacked100Percent’: plot data series stacked to show their percentage in a total.  
‘NoStacking’ is the default option.

Height : Type: optional, Integer.  
The vertical size of the chart in pixels \(300 by default\).  
The horizontal size of the chart is the parent’s width.

LegendPosition : Type: optional, LegendPosition Identifier.  
The position where the legend is displayed on the chart \(‘Bottom’ by default\).  
The legend is hidden if no series name is set in any data point.

XAxisFormat : Type: optional, [XAxisFormat](charts-api.md#Structure_XAxisFormat%3E).  
Formatting options for the X-axis.  
Action XAxisFormat\_Init helps to create and initialize this parameter.

YAxisFormat : Type: optional, [YAxisFormat](charts-api.md#Structure_YAxisFormat%3E).  
Formatting options for the Y-axis.  
Action YAxisFormat\_Init helps to create and initialize this parameter.

ChartFormat : Type: optional, [ChartFormat](charts-api.md#Structure_ChartFormat%3E).  
Formatting options for the chart.  
Action ChartFormat\_Init helps to create and initialize this parameter.

Clickable : Type: optional, Boolean.  
Set to True to allow clicking on plotted values and execute the On Click action \(False by default\).

AdvancedFormat : Type: optional, [AdvancedFormat](charts-api.md#Structure_AdvancedFormat%3E).  
Highcharts JSON to format elements displayed on the chart.  
Action AdvancedOptions\_Init helps to create and initialize this parameter.

### ColumnChart { \#ColumnChart }

Column charts compare multiple values using vertical bars.

_Inputs_

SourceDataPointList : Type: mandatory, [DataPoint](charts-api.md#Structure_DataPoint%3E) List.  
The list of all data points to be plotted on the chart.

StackingType : Type: optional, StackingType Identifier.  
The way to plot multiple data series on the chart:  
- ‘NoStacking’: plot data series side by side to compare them;  
- ‘Stacked’: plot data series stacked to show their contribution to a total;  
- ‘Stacked100Percent’: plot data series stacked to show their percentage in a total.  
‘NoStacking’ is the default option.

Height : Type: optional, Integer.  
The vertical size of the chart in pixels \(300 by default\).  
The horizontal size of the chart is the parent’s width.

LegendPosition : Type: optional, LegendPosition Identifier.  
The position where the legend is displayed on the chart \(‘Bottom’ by default\).  
The legend is hidden if no series name is set in any data point.

XAxisFormat : Type: optional, [XAxisFormat](charts-api.md#Structure_XAxisFormat%3E).  
Formatting options for the X-axis.  
Action XAxisFormat\_Init helps to create and initialize this parameter.

YAxisFormat : Type: optional, [YAxisFormat](charts-api.md#Structure_YAxisFormat%3E).  
Formatting options for the Y-axis.  
Action YAxisFormat\_Init helps to create and initialize this parameter.

ChartFormat : Type: optional, [ChartFormat](charts-api.md#Structure_ChartFormat%3E).  
Formatting options for the chart.  
Action ChartFormat\_Init helps to create and initialize this parameter.

Clickable : Type: optional, Boolean.  
Set to True to allow clicking on plotted values and execute the On Click action \(False by default\).

AdvancedFormat : Type: optional, [AdvancedFormat](charts-api.md#Structure_AdvancedFormat%3E).  
Highcharts JSON to format elements displayed on the chart.  
Action AdvancedOptions\_Init helps to create and initialize this parameter.

### LineChart { \#LineChart }

Line charts illustrate trends of values over time.

_Inputs_

SourceDataPointList : Type: mandatory, [DataPoint](charts-api.md#Structure_DataPoint%3E) List.  
The list of all data points to be plotted on the chart.

Height : Type: optional, Integer.  
The vertical size of the chart in pixels \(300 by default\).  
The horizontal size of the chart is the parent’s width.

LegendPosition : Type: optional, LegendPosition Identifier.  
The position where the legend is displayed on the chart \(‘Bottom’ by default\).  
The legend is hidden if no series name is set in any data point.

XAxisFormat : Type: optional, [XAxisFormat](charts-api.md#Structure_XAxisFormat%3E).  
Formatting options for the X-axis.  
Action XAxisFormat\_Init helps to create and initialize this parameter.

YAxisFormat : Type: optional, [YAxisFormat](charts-api.md#Structure_YAxisFormat%3E).  
Formatting options for the Y-axis.  
Action YAxisFormat\_Init helps to create and initialize this parameter.

ChartFormat : Type: optional, [ChartFormat](charts-api.md#Structure_ChartFormat%3E).  
Formatting options for the chart.  
Action ChartFormat\_Init helps to create and initialize this parameter.

Clickable : Type: optional, Boolean.  
Set to True to allow clicking on plotted values and execute the On Click action \(False by default\).

AdvancedFormat : Type: optional, [AdvancedFormat](charts-api.md#Structure_AdvancedFormat%3E).  
Highcharts JSON to format elements displayed on the chart.  
Action AdvancedOptions\_Init helps to create and initialize this parameter.

### PieChart { \#PieChart }

Pie charts illustrate proportions of values.

_Inputs_

SourceDataPointList : Type: mandatory, [DataPoint](charts-api.md#Structure_DataPoint%3E) List.  
The list of all data points to be plotted on the chart.

Height : Type: optional, Integer.  
The vertical size of the chart in pixels \(300 by default\).  
The horizontal size of the chart is the parent’s width.

LegendPosition : Type: optional, LegendPosition Identifier.  
The position where the legend is displayed on the chart \(‘Bottom’ by default\).

ChartFormat : Type: optional, [ChartFormat](charts-api.md#Structure_ChartFormat%3E).  
Formatting options for the chart.  
Action ChartFormat\_Init helps to create and initialize this parameter.

Clickable : Type: optional, Boolean.  
Set to True to allow clicking on plotted values and execute the On Click action \(False by default\).

AdvancedFormat : Type: optional, [AdvancedFormat](charts-api.md#Structure_AdvancedFormat%3E).  
Highcharts JSON to format elements displayed on the chart.  
Action AdvancedOptions\_Init helps to create and initialize this parameter.

## Actions

### AdvancedFormat\_Init { \#AdvancedFormat\_Init }

Initializes an AdvancedFormat record with the values passed as arguments. The record is returned by the action.

_Inputs_

DataPointFormats : Type: optional, [AdvancedDataPointFormat](charts-api.md#Structure_AdvancedDataPointFormat%3E) List.  
Advanced JSON formatting for the data points.

DataSeriesFormats : Type: optional, [AdvancedDataSeriesFormat](charts-api.md#Structure_AdvancedDataSeriesFormat%3E) List.  
Advanced JSON formatting for the data series.

XAxisJSON : Type: optional, Text.  
Advanced JSON formatting for the X-axis.  
Refer to Highcharts API \([http://api.highcharts.com/highcharts\#xAxis](http://api.highcharts.com/highcharts#xAxis)\) for all available options.  
As an example, format the dates on the X-axis to "MMM YYYY" using the following Highcharts JSON:  
"labels:{ formatter: function\(\) { return Highcharts.dateFormat\('%b %Y', this.value\); } }"

YAxisJSON : Type: optional, Text.  
Advanced JSON formatting for the Y-axis.  
Refer to Highcharts API \([http://api.highcharts.com/highcharts\#yAxis](http://api.highcharts.com/highcharts#yAxis)\) for all available options.  
As an example, prevent using decimals in the axis values using the following Highcharts JSON:  
"allowDecimals: false"

HighchartsJSON : Type: optional, Text.  
Advanced JSON formatting for any element of the chart.  
Refer to Highcharts API \([http://api.highcharts.com/highcharts](http://api.highcharts.com/highcharts)\) for all available options.

_Outputs_

AdvancedFormat : Type: [AdvancedFormat](charts-api.md#Structure_AdvancedFormat%3E).  
The initialized AdvancedFormat record.

### ChartFormat\_Init { \#ChartFormat\_Init }

Initializes a ChartFormat record with the values passed as arguments. The record is returned by the action.

_Inputs_

ShowDataPointValues : Type: optional, Boolean.  
Set to True to display the value of the data points.

UseAnimation : Type: optional, Boolean.  
Set to True to plot the chart with animation.

_Outputs_

ChartFormat : Type: [ChartFormat](charts-api.md#Structure_ChartFormat%3E).  
The initialized ChartFormat record.

### DataPoint\_GetClicked { \#DataPoint\_GetClicked }

Returns the data point that was clicked on the chart.  
Execute this action in the On Click action of a chart.

_Outputs_

DataPoint : Type: [DataPoint](charts-api.md#Structure_DataPoint%3E).  
The clicked Data Point.

### DataPoint\_Init { \#DataPoint\_Init }

Initializes a DataPoint record with the values passed as arguments. The record is returned by the action.

_Inputs_

Label : Type: mandatory, Text.  
The label on the X-axis for the data point.  
To display dates in the X-axis use the Platform Server date format \(by default YYYY-MM-DD\).

Value : Type: mandatory, Decimal.  
The value to be plotted.

DataSeriesName : Type: optional, Text.  
Name of the series where the data point belongs.

Tooltip : Type: optional, Text.  
Custom tooltip for the data point when hovering the mouse.

Color : Type: optional, Text.  
Custom color for the data point.

_Outputs_

DataPoint : Type: [DataPoint](charts-api.md#Structure_DataPoint%3E).  
The initialized DataPoint record.

### DataPoint\_InitMissing { \#DataPoint\_InitMissing }

Initializes a DataPoint to plot a gap on the chart. The record is returned by the action.

_Inputs_

Label : Type: mandatory, Text.  
The label on the X-axis for the data point.  
To display dates in the X-axis use the Platform Server date format \(by default YYYY-MM-DD\).

DataSeriesName : Type: optional, Text.  
Name of the series where the data point belongs.

_Outputs_

DataPoint : Type: [DataPoint](charts-api.md#Structure_DataPoint%3E).  
The initialized DataPoint record.

### XAxisFormat\_Init { \#XAxisFormat\_Init }

Initializes an XAxisFormat record with the values passed as arguments. The record is returned by the action.

_Inputs_

Title : Type: optional, Text.  
The text displayed next to the X-axis.

LabelsRotation : Type: optional, Integer.  
The rotation in degrees of all labels displayed on the X-axis.

MinValue : Type: optional, Text.  
The minimum value that is displayed on the X-axis.

MaxValue : Type: optional, Text.  
The maximum value that is displayed on the X-axis.

ValuesType : Type: optional, XAxisValuesType Identifier.  
The data type of labels displayed on the X-axis to format them.  
Using ‘Auto’ means the type is inferred from the label of the first data point.

_Outputs_

XAxisFormat : Type: [XAxisFormat](charts-api.md#Structure_XAxisFormat%3E).  
The initialized XAxisFormat record.

### YAxisFormat\_Init { \#YAxisFormat\_Init }

Initializes an YAxisFormat record with the values passed as arguments. The record is returned by the action.

_Inputs_

Title : Type: optional, Text.  
The text displayed next to the Y-axis.

MinValue : Type: optional, Decimal.  
The minimum value that is displayed on the Y-axis.

MaxValue : Type: optional, Decimal.  
The maximum value that is displayed on the Y-axis.

ValuesPrefix : Type: optional, Text.  
The text prefixing the values displayed on the Y-axis.

ValuesSuffix : Type: optional, Text.  
The text suffixing the values displayed on the Y-axis.

GridLineStep : Type: optional, Decimal.  
The step by which grid lines are displayed on the Y-axis.

_Outputs_

YAxisFormat : Type: [YAxisFormat](charts-api.md#Structure_YAxisFormat%3E).  
The initialized YAxisFormat record.

## Structures

### AdvancedDataPointFormat { \#Structure\_AdvancedDataPointFormat }

Information to format a data point using Highcharts JSON.

_Attributes_

DataPoint : Type: [DataPoint](charts-api.md#Structure_DataPoint%3E).  
Data point to format.

DataPointJSON : Type: Text \(50\).  
Highcharts JSON to format the data point.  
Refer to Highcharts API \([http://api.highcharts.com/highcharts\#series](http://api.highcharts.com/highcharts#series)\) for all available options.  
As an example, show a custom data label in this point, using the following Highcharts JSON:  
"dataLabels: { enabled: true, formatter: function \(\) { return 'top value' } }"

### AdvancedDataSeriesFormat { \#Structure\_AdvancedDataSeriesFormat }

Information to format a data series using Highcharts JSON.

_Attributes_

DataSeriesName : Type: Text \(50\).  
Name of the data series to format.

DataSeriesJSON : Type: Text \(50\).  
Highcharts JSON to format the data series.  
All data points belonging to the data series are affected by this formatting.  
Refer to Highcharts API \([http://api.highcharts.com/highcharts\#series](http://api.highcharts.com/highcharts#series) and [http://api.highcharts.com/highcharts\#plotOptions.series](http://api.highcharts.com/highcharts#plotOptions.series)\) for all available options.  
As an example, plot a series with a thicker line in a Line chart using the following Highcharts JSON:  
"lineWidth: 5"

### AdvancedFormat { \#Structure\_AdvancedFormat }

Information to format chart elements using Highcharts JSON.

_Attributes_

DataPointFormats : Type: [AdvancedDataPointFormat](charts-api.md#Structure_AdvancedDataPointFormat%3E) List.  
Highcharts JSON to format data points.

DataSeriesFormats : Type: [AdvancedDataSeriesFormat](charts-api.md#Structure_AdvancedDataSeriesFormat%3E) List.  
Highcharts JSON to format data series.

XAxisJSON : Type: Text \(50\).  
Highcharts JSON to format the X-axis.  
Refer to Highcharts API \([http://api.highcharts.com/highcharts\#xAxis](http://api.highcharts.com/highcharts#xAxis)\) for all available options.  
As an example, format the dates on the X-axis to "MMM YYYY" using the following Highcharts JSON:  
"labels:{ formatter: function\(\) { return Highcharts.dateFormat\('%b %Y', this.value\); } }"

YAxisJSON : Type: Text \(50\).  
Highcharts JSON to format the Y-axis.  
Refer to Highcharts API \([http://api.highcharts.com/highcharts\#yAxis](http://api.highcharts.com/highcharts#yAxis)\) for all available options.  
As an example, prevent using decimals in the axis values using the following Highcharts JSON:  
"allowDecimals: false"

HighchartsJSON : Type: Text \(50\).  
Highcharts JSON to format any element of the chart.  
Refer to Highcharts API \([http://api.highcharts.com/highcharts](http://api.highcharts.com/highcharts)\) for all available options.

### ChartFormat { \#Structure\_ChartFormat }

Information to format the chart.

_Attributes_

ShowDataPointValues : Type: Boolean.  
Set to True to display the value of the data points.

UseAnimation : Type: Boolean.  
Set to True to plot the chart with animation.

### DataPoint { \#Structure\_DataPoint }

Information to plot a data point on the chart.

_Attributes_

Label : Type: Text \(50\).  
The label on the X-axis for the data point.  
To display dates in the X-axis use the Platform Server date format \(by default YYYY-MM-DD\).

Value : Type: Decimal \(37, 0\).  
The value to be plotted.

DataSeriesName : Type: Text \(50\).  
Name of the series where the data point belongs.

Tooltip : Type: Text \(50\).  
Custom tooltip for the data point when hovering the mouse.

Color : Type: Text \(50\).  
Custom color for the data point.  
As an example, set the color of a data point to red using either of the following values: "Red", "\#FF0000", "rgb\(255,0,0\)" or "rgba\(255,0,0,1\)"

### XAxisFormat { \#Structure\_XAxisFormat }

Information to format the X-axis on the chart.

_Attributes_

Title : Type: Text \(50\).  
The text displayed next to the X-axis.

LabelsRotation : Type: Integer.  
The counterclockwise rotation in degrees of all labels displayed on the X-axis.

MinValue : Type: Text \(50\).  
The minimum value that is displayed on the X-axis.

MaxValue : Type: Text \(50\).  
The maximum value that is displayed on the X-axis.

ValuesType : Type: XAxisValuesType Identifier.  
The data type of labels displayed on the X-axis to format them.  
Using ‘Auto’ means the type is inferred from the label of the first data point.

### YAxisFormat { \#Structure\_YAxisFormat }

Information to format the Y-axis on the chart.

_Attributes_

Title : Type: Text \(50\).  
The text displayed next to the Y-axis.

MinValue : Type: Decimal \(37, 0\).  
The minimum value that is displayed on the Y-axis.

MaxValue : Type: Decimal \(37, 0\).  
The maximum value that is displayed on the Y-axis.

ValuesPrefix : Type: Text \(50\).  
The text prefixing the values displayed on the Y-axis.

ValuesSuffix : Type: Text \(50\).  
The text suffixing the values displayed on the Y-axis.

GridLineStep : Type: Decimal \(37, 0\).  
The step by which grid lines are displayed on the Y-axis.

## Static Entities

### LegendPosition { \#StaticEntity\_LegendPosition }

The position where the legend is displayed on charts.

_Attributes_

Id : Type: Integer.

Order : Type: Integer.

Is\_Active : Type: Boolean.

_Records_

* Bottom
* Top
* Hidden
* Inside
* Right
* Left

### StackingType { \#StaticEntity\_StackingType }

The way to plot multiple data series on Area, Bar, or Column charts:

* ‘NoStacking’: plot data series side by side to compare them;  
* ‘Stacked’: plot data series stacked to show their contribution to a total;  
* ‘Stacked100Percent’: plot data series stacked to show their percentage in a total.

_Attributes_

Id : Type: Integer.

Order : Type: Integer.

Is\_Active : Type: Boolean.

_Records_

* NoStacking
* Stacked100Percent
* Stacked

### XAxisValuesType { \#StaticEntity\_XAxisValuesType }

The data type of labels displayed on the X-axis to format them.  
Using ‘Auto’ means the type is inferred from the label of the first data point.

_Attributes_

Id : Type: Integer.

Label : Type: Text \(50\).

Order : Type: Integer.

_Records_

* Text
* Auto

