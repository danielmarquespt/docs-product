---
tags: null
---

# Available Data Types

This page describes the data types available in OutSystems, their default values and constraints, and the built-in functions to convert them into another data type.

## Basic Data Types

| Type | Default Value | Example | Comment |
| :--- | :--- | :--- | :--- |
| Binary Data | Byte array with no elements | n/a |  |
| Boolean | false | true or false |  |
| Currency | 0.0 | 545870.025 | See Decimal type. |
| Date | \#1900-01-01\# | \#1988-08-28\# | The  supported range is \[\#1900-01-01\#, \#3000-12-31\#\] |
| Time | \#00:00:00\# | \#12:20:56\# | Minimum value: \#00:00:00\# %% %% Maximum value: \#23:59:59\# |
| Date Time | \#1900-01-01 00:00:00\# | \#1988-08-28 23:59:59\# | The supported range is \[\#1900-01-01 00:00:00\#, \#3000-12-31 23:59:59\#\]%% %%Refer to the [additional notes](available-data-types.md#date-time-notes%3E) about the time zone conversions. |
| Integer | 0 | 2147483600 | Minimum value: -2^31, which is -2147483648.%% %% Maximum value: 2^31-1, which is 2147483647. |
| Long Integer | 0 | 5645245584135987412 | Minimum value: -2^63%% Maximum value: 2^63-1 |
| Decimal | 0.0 | -158121.025 4000.0 | Integer and decimal parts must be separated by a period. %% %% Minimum value: -2^96 %% %%Maximum value: 2^96-1%% %%The maximum number of digits in the decimal part is 8. |
| Email | "" \(empty string\) | "[fran.wilson@company.com](mailto:fran.wilson@company.com)" |  |
| Phone Number | "" \(empty string\) | "+1 555 565 3730" |  |
| Text | "" \(empty string\) | "My name is Christina Sharp." |  |
| &lt;Entity&gt; Identifier | When an Entity is created, the &lt;Entity&gt; identifier data type is created for the identifier attribute. |  |  |

**Date Time Notes**

* When you work with Date Time data type in the server, you always deal with the time zone of the server.
* Date Time in mobile apps is always UTC, even when requested from the server.
* When you use Date Time in the mobile app UI, the value is converted to the local time of the device.

Here is an example for a server that is in GMT+01 \(Paris\) and a mobile device in GMT-05 \(New York\). The mobile device requests a certain Date Time value from the server, for example `#2007-12-18 17:00:00#`. What happens is:

1. The value is converted by the server to UTC `#2007-12-18 16:00:00#` and sent to the mobile device.
2. When you store the value in the mobile app, the value is handled as UTC and saved as `#2007-12-18 16:00:00#`.
3. When you display the value in the UI, the end-users see `#2007-12-18 11:00:00#`.

If you do not need this scenario in your logic, use data types Date and Time separately to deal with the respective values.

## Compound Data Types <a id="date-time-notes"></a>

| Type | Comments |
| :--- | :--- |
| &lt;Entity&gt; or &lt;Structure&gt; | When an Entity or \[Structure\]\(../../../develop/data/structure-create-use.md\) is created, a data type is also created with all the attributes of that Entity or Structure. For example, when the Customer entity is created, the Customer data type is created. To create a variable of this data type, simply set its 'Data Type' property to 'Customer'. To access an attribute of the variable, use the following syntax: \`.\`, e.g. \`MyCustomerVar.Name\`. |
| Object | OutSystems supports the Object data type to allow to reuse your own .NET classes. The default value is NullObject\(\). |
| Record |  A \[Record\]\(../../../develop/data/structure-create-use.md\) is a data type that's composed of a fixed number of attributes, each one with its own data type. Use a Record to define a compound data type that is used for a single variable. If you need to define more than one variable with the same compound data type, use a Structure instead. Some use cases for using the Record data type are:  • You need to return the result of an Aggregate on a User Action. In this case, you can define the user action output parameter using the record data type.  • You need a user action that returns compound information, but don't want to define a new Structure. |

## Collection Data Types

| Type | Comments |
| :--- | :--- |
|  List |  A \[List\]\(list.md\) is a sequence of elements of the same data type, either basic or compound. Elements can be inserted, fetched, and removed from a List. |

## Default and Null Values

OutSystems does not use the concept of the NULL value, except for the Entity Identifier data type. Therefore, each data type has an associated default value that is assigned at creation.

## Data Type Conversions

OutSystems enables the conversion between different data types. This can be made implicitly, or explicitly by using [data type conversion functions](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md).

### Implicit Conversion

OutSystems automatically converts values of the following types:

| Expected Type | Accepted Types | Obs. |
| :--- | :--- | :--- |
| Boolean | - |  |
| Currency | Decimal, Integer, Boolean, Entity Identifier\(Integer\) |  |
| Date | Date Time |  |
| Date Time | Date, Text, Time |  |
| Integer | Decimal, Boolean, Currency, Entity Identifier\(Integer\) | When converting Decimal to Integer implicitly, the decimals are truncated. |
| Long Integer | Long Integer, Integer, Decimal, Boolean, Currency, Entity Identifier\(Integer\), Entity Identifier\(Long Integer\) |  |
| Decimal | Integer, Boolean, Currency, Entity Identifier\(Integer\) |  |
| Entity Identifier | Entity Identifier | A certain Entity Identifier can be converted into another Entity's Identifier, but a warning is displayed. |
| Email | Text, Phone Number, Integer, Decimal, Boolean, Currency, Entity Identifier\(Integer\), Entity Identifier\(Text\), Date Time, Date, Time |  |
| Phone Number | Text, Email, Integer, Decimal, Boolean, Currency, Entity Identifier\(Integer\), Entity Identifier\(Text\), Date Time, Date, Time |  |
| Text | Integer, Decimal, Boolean, Currency, Phone Number, Email, Entity Identifier\(Integer\), Entity Identifier\(Text\) |  |

### Explicit Conversion Functions

To convert values from one data type to another use [data type conversion functions](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md).

Here is a summary about the possible explicit conversions:

| From | To | Function |
| :--- | :--- | :--- |
| Boolean | Integer %%Text | [BooleanToInteger](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#BooleanToInteger)%% [BooleanToText](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#BooleanToText) |
| Date | Date Time %%Text | [DateToDateTime](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#DateToDateTime)%% [DateToText](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#DateToText) |
| Date Time | Date %%Text %%Time | [DateTimeToDate](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#DateTimeToDate)%% [DateTimeToText](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#DateTimeToText)%% [DateTimeToTime](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#DateTimeToTime) |
| Integer | Boolean %%Decimal %%Text %%Integer Identifier | [IntegerToBoolean](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#IntegerToBoolean)%% [IntegerToDecimal](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#IntegerToDecimal)%% [IntegerToText](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#IntegerToText)%% [IntegerToIdentifier](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#IntegerToIdentifier) |
| Long Integer | Long Integer Identifier %%Integer %%Text | [LongIntegerToIdentifier](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#LongIntegerToIdentifier)%% [LongIntegerToInteger](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#LongIntegerToInteger)%% [LongIntegerToText](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#LongIntegerToText) |
| Decimal | Boolean %%Integer %%Text | [DecimalToBoolean](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#DecimalToBoolean)%% [DecimalToInteger](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#DecimalToInteger)%% [DecimalToText](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#DecimalToText) |
| Entity Identifier \(Integer\) | Integer | [IdentifierToInteger](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#IdentifierToInteger) |
| Entity Identifier \(Long Integer\) | Long Integer | [IdentifierToLongInteger](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#IdentifierToLongInteger) |
| Entity Identifier \(Text\) | Text | [IdentifierToText](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#IdentifierToText) |
| Text | Date %%Date Time %%Decimal %%Integer %%Time %%Text Identifier | [TextToDate](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#%3ETextToDate)%% [TextToDateTime](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#TextToDateTime)%% [TextToDecimal](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#TextToDecimal)%% [TextToInteger](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#TextToInteger)%% [TextToTime](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#TextToTime)%% [TextToIdentifier](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#TextToIdentifier) |
| Time | Text | [TimeToText](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#TimeToText) |
| Any data type | Object | [ToObject](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md#ToObject) |

