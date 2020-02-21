# Data Conversion

| Name | Description |
| :--- | :--- |
| [BooleanToInteger](builtinfunction.data-conversion.md#BooleanToInteger)\(​Boolean\) | Converts Boolean 'b' to an Integer value, either 1 if 'b' is True or 0 if 'b' is False. |
| [BooleanToText](builtinfunction.data-conversion.md#BooleanToText)\(​Boolean\) | Converts Boolean 'b' to a Text value, either "True" or "False". |
| [DateTimeToDate](builtinfunction.data-conversion.md#DateTimeToDate)\(​DateTime\) | Converts Date Time 'dt' to a Date value dropping the Time component. |
| [DateTimeToText](builtinfunction.data-conversion.md#DateTimeToText)\(​DateTime\) | Converts Date Time 'dt' to a Text value in the format specified in the environment configuration \(by default, "yyyy-MM-dd HH:mm:ss"\). |
| [DateTimeToTime](builtinfunction.data-conversion.md#DateTimeToTime)\(​DateTime\) | Converts Date Time 'dt' to a Time value dropping the Date component. |
| [DateToDateTime](builtinfunction.data-conversion.md#DateToDateTime)\(​Date\) | Converts Date 'd' to a Date Time value, adding the Time component \(\#00:00:00\#\). |
| [DateToText](builtinfunction.data-conversion.md#DateToText)\(​Date\) | Converts Date 'd' to a Text value in the format specified in the environment configuration \(by default, "yyyy-MM-dd"\). |
| [DecimalToBoolean](builtinfunction.data-conversion.md#DecimalToBoolean)\(​Decimal\) | Converts Decimal 'd' to a Boolean value. Decimal value of 0.0 is False. Any other value is True. |
| [DecimalToInteger](builtinfunction.data-conversion.md#DecimalToInteger)\(​Decimal\) | Converts Decimal 'd' to an Integer value. In client-side and server-side logic, the function rounds the input using the round half to even method. In Aggregate expressions the function truncates to the integer part of the input. To check if the conversion is possible you can use the DecimalToIntegerValidate function. |
| [DecimalToIntegerValidate](builtinfunction.data-conversion.md#DecimalToIntegerValidate)\(​Decimal\) | Returns true if Decimal 'd' can be converted to an Integer value. |
| [DecimalToLongInteger](builtinfunction.data-conversion.md#DecimalToLongInteger)\(​Decimal\) | Converts Decimal 'd' to a Long Integer value. In client-side and server-side logic, the function rounds the input using the round half to even method. In Aggregate expressions the function truncates to the integer part of the input. To check if the conversion is possible you can use the DecimalToLongIntegerValidate function. |
| [DecimalToLongIntegerValidate](builtinfunction.data-conversion.md#DecimalToLongIntegerValidate)\(​Decimal\) | Returns true if Decimal 'd' can be converted to a Long Integer value. |
| [DecimalToText](builtinfunction.data-conversion.md#DecimalToText)\(​Decimal\) | Converts Decimal 'd' to a Text value. |
| [LongIntegerToInteger](builtinfunction.data-conversion.md#LongIntegerToInteger)\(​LongInteger\) | Converts Long Integer 'l' to an Integer value. If 'l' is outside the boundaries of the Integer values, the function will return the Integer default value. To check if the conversion is possible you can use the LongIntegerToIntegerValidate function. |
| [LongIntegerToIntegerValidate](builtinfunction.data-conversion.md#LongIntegerToIntegerValidate)\(​LongInteger\) | Returns true if Long Integer 'l' can be converted to an Integer value. |
| [LongIntegerToIdentifier](builtinfunction.data-conversion.md#LongIntegerToIdentifier)\(​LongInteger\) | Converts Long Integer 'l' to a Long Integer Identifier. |
| [LongIntegerToText](builtinfunction.data-conversion.md#LongIntegerToText)\(​LongInteger\) | Converts Long Integer 'l' to a Text value. |
| [IdentifierToInteger](builtinfunction.data-conversion.md#IdentifierToInteger)\(​EntityReference\) | Converts Identifier 'Id' to an Integer value. |
| [IdentifierToLongInteger](builtinfunction.data-conversion.md#IdentifierToLongInteger)\(​EntityReferenceLongInteger\) | Converts Identifier 'Id' to a Long Integer value. |
| [IdentifierToText](builtinfunction.data-conversion.md#IdentifierToText)\(​EntityReferenceText\) | Converts Identifier 'Id' to a Text value. |
| [IntegerToBoolean](builtinfunction.data-conversion.md#IntegerToBoolean)\(​Integer\) | Converts Integer 'i' to a Boolean value. Boolean value of 0 is False. Any other value is True. |
| [IntegerToDecimal](builtinfunction.data-conversion.md#IntegerToDecimal)\(​Integer\) | Converts Integer 'i' to a Decimal value. |
| [IntegerToIdentifier](builtinfunction.data-conversion.md#IntegerToIdentifier)\(​Integer\) | Converts Integer 'i' to an Integer Identifier. |
| [IntegerToText](builtinfunction.data-conversion.md#IntegerToText)\(​Integer\) | Converts Integer 'i' to a Text value. |
| [NullDate](builtinfunction.data-conversion.md#NullDate)\(\) | Returns a null Date value. |
| [NullIdentifier](builtinfunction.data-conversion.md#NullIdentifier)\(\) | Returns a null Identifier valid for Integer and Long Integer Identifiers. |
| [NullObject](builtinfunction.data-conversion.md#NullObject)\(\) | Returns a null Object value. |
| [NullBinary](builtinfunction.data-conversion.md#NullBinary)\(\) | Returns a null Binary Data value. |
| [NullTextIdentifier](builtinfunction.data-conversion.md#NullTextIdentifier)\(\) | Returns a null Text Identifier. |
| [TextToDate](builtinfunction.data-conversion.md#TextToDate)\(​Text\) | Converts Text 't' to a Date value. If 't' can't be converted to a valid Date value, the function will return the Date default value. To check if the conversion is possible you can use the TextToDateValidate function. You should check the limits of the Date data type. You should also ensure that the date you type in the argument complies with the default date format \(yyyy-mm-dd, yyyy/mm/dd, and yyyy.mm.dd\) or the server’s environment configuration. |
| [TextToDateTime](builtinfunction.data-conversion.md#TextToDateTime)\(​Text\) | Converts Text 't' to a Date Time value. If 't' can't be converted to a valid Date Time value, the function will return a Date Time default value. To check if the conversion is possible you can use the TextToDateTimeValidate function. You should check the limits of the Date Time data type. You should also ensure that the Date Time you type in the argument complies with the default Date Time format \(yyyy-mm-dd hh:mm:ss, yyyy/mm/dd hh:mm:ss, and yyyy.mm.dd hh:mm:ss\) or the server’s environment configuration. |
| [TextToDateTimeValidate](builtinfunction.data-conversion.md#TextToDateTimeValidate)\(​Text\) | Returns true if Text 't' can be converted to a Date Time value. |
| [TextToDateValidate](builtinfunction.data-conversion.md#TextToDateValidate)\(​Text\) | Returns true if Text 't' can be converted to a Date value. |
| [TextToDecimal](builtinfunction.data-conversion.md#TextToDecimal)\(​Text\) | Converts Text 't' to a Decimal value. The only allowed decimal separator is the ".". If 't' is outside the boundaries of the Decimal values, the function will return the Decimal default value. To check if the conversion is possible you can use the TextToDecimalValidate function. |
| [TextToDecimalValidate](builtinfunction.data-conversion.md#TextToDecimalValidate)\(​Text\) | Returns true if Text 't' can be converted to a Decimal value. |
| [TextToIdentifier](builtinfunction.data-conversion.md#TextToIdentifier)\(​Text\) | Converts Text 't' to a Text Identifier. |
| [TextToInteger](builtinfunction.data-conversion.md#TextToInteger)\(​Text\) | Converts Text 't' to an Integer value. If 't' is outside the boundaries of the Integer values the function will return an Integer default value. To check if the conversion is possible you can use the TextToIntegerValidate function. |
| [TextToLongInteger](builtinfunction.data-conversion.md#TextToLongInteger)\(​Text\) | Converts Text 't' to a Long Integer value. If 't' is outside the boundaries of the Long Integer values the function will return a Long Integer default value. To check if the conversion is possible you can use the TextToLongIntegerValidate function. |
| [TextToIntegerValidate](builtinfunction.data-conversion.md#TextToIntegerValidate)\(​Text\) | Returns true if Text 't' can be converted to an Integer value. |
| [TextToLongIntegerValidate](builtinfunction.data-conversion.md#TextToLongIntegerValidate)\(​Text\) | Returns true if Text 't' can be converted to a Long Integer value. |
| [TextToTime](builtinfunction.data-conversion.md#TextToTime)\(​Text\) | Converts Text 't' to a Time value. If 't' can't be converted to a valid Time value, the function will return the Time default value. To check if the conversion is possible you can use the TextToTimeValidate function. You should check the limits of the Time data type. You should also ensure that the Time you type in the argument complies with the Time format \(hh:mm:ss\). |
| [TextToTimeValidate](builtinfunction.data-conversion.md#TextToTimeValidate)\(​Text\) | Returns true if Text 't' can be converted to a Time value. |
| [TimeToText](builtinfunction.data-conversion.md#TimeToText)\(​Time\) | Converts Time 't' to a Text value in the format "HH:mm:ss". |
| [ToObject](builtinfunction.data-conversion.md#ToObject)\(​Generic\) | Converts expression 'exp' to an Object value. |

## BooleanToInteger { \#BooleanToInteger }

Converts Boolean 'b' to an Integer value, either 1 if 'b' is True or 0 if 'b' is False.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

b : Type: Boolean. Mandatory.  
The value to be converted

### Output

Type: Integer

### Examples

```text
BooleanToInteger(True) = 1
BooleanToInteger(False) = 0
```

## BooleanToText { \#BooleanToText }

Converts Boolean 'b' to a Text value, either "True" or "False".

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

b : Type: Boolean. Mandatory.  
The value to be converted

### Output

Type: Text

### Examples

```text
BooleanToText(True) = "True" 
BooleanToText(False) = "False"
```

## DateTimeToDate { \#DateTimeToDate }

Converts Date Time 'dt' to a Date value dropping the Time component.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

dt : Type: DateTime. Mandatory.  
The value to be converted

### Output

Type: Date

### Examples

```text
DateTimeToDate(#2013-11-30 22:20:30#) = #2013-11-30#
```

## DateTimeToText { \#DateTimeToText }

Converts Date Time 'dt' to a Text value in the format specified in the environment configuration \(by default, "yyyy-MM-dd HH:mm:ss"\).

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

dt : Type: DateTime. Mandatory.  
The value to be converted

### Output

Type: Text

### Examples

```text
DateTimeToText(#2015-05-21 22:20:30#) = "2015-05-21 22:20:30"
DateTimeToText(#2015-05-21#) = "2015-05-21 00:00:00"
DateTimeToText(#22:20:30#) = "1900-01-01 22:20:30"
```

## DateTimeToTime { \#DateTimeToTime }

Converts Date Time 'dt' to a Time value dropping the Date component.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

dt : Type: DateTime. Mandatory.  
The value to be converted

### Output

Type: Time

### Examples

```text
DateTimeToTime(#1982-05-21 22:20:30#) = #22:20:30#
```

## DateToDateTime { \#DateToDateTime }

Converts Date 'd' to a Date Time value, adding the Time component \(\#00:00:00\#\).

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

d : Type: Date. Mandatory.  
The value to be converted

### Output

Type: DateTime

### Examples

```text
DateToDateTime(#2001-09-14#) = #2001-09-14 00:00:00#
```

## DateToText { \#DateToText }

Converts Date 'd' to a Text value in the format specified in the environment configuration \(by default, "yyyy-MM-dd"\).

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

d : Type: Date. Mandatory.  
The value to be converted

### Output

Type: Text

### Examples

```text
DateToText(#2010-05-17#) = "2010-05-17"
DateToText(#2010-05-17 22:30:32#) = "2010-05-17"
```

## DecimalToBoolean { \#DecimalToBoolean }

Converts Decimal 'd' to a Boolean value. Decimal value of 0.0 is False. Any other value is True.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

d : Type: Decimal. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
DecimalToBoolean(0.0) = False
DecimalToBoolean(0.05) = True
```

## DecimalToInteger { \#DecimalToInteger }

Converts Decimal 'd' to an Integer value.  
In client-side and server-side logic, the function rounds the input using the round half to even method. In Aggregate expressions the function truncates to the integer part of the input.  
To check if the conversion is possible you can use the DecimalToIntegerValidate function.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

d : Type: Decimal. Mandatory.  
The value to be converted

### Output

Type: Integer

### Examples

```text
When used in client-side and server-side logic:
DecimalToInteger(134.2) = 134
DecimalToInteger(134.5) = 134
DecimalToInteger(133.5) = 134
DecimalToInteger(134.7) = 135
DecimalToInteger(134) = 134
DecimalToInteger(12345678999.9) = 0

When used in Aggregates:
DecimalToInteger(134.2) = 134
DecimalToInteger(134.5) = 134
DecimalToInteger(133.5) = 133
DecimalToInteger(134.7) = 134
DecimalToInteger(134) = 134
DecimalToInteger(12345678999.9) = Arithmetic Overflow Error
```

## DecimalToIntegerValidate { \#DecimalToIntegerValidate }

Returns true if Decimal 'd' can be converted to an Integer value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

d : Type: Decimal. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
DecimalToIntegerValidate(134.2) = True
DecimalToIntegerValidate(134.5) = True
DecimalToIntegerValidate(133.5) = True
DecimalToIntegerValidate(134.7) = True
DecimalToIntegerValidate(134) = True
DecimalToIntegerValidate(12345678999.9) = False
```

## DecimalToLongInteger { \#DecimalToLongInteger }

Converts Decimal 'd' to a Long Integer value.  
In client-side and server-side logic, the function rounds the input using the round half to even method. In Aggregate expressions the function truncates to the integer part of the input.  
To check if the conversion is possible you can use the DecimalToLongIntegerValidate function.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

d : Type: Decimal. Mandatory.  
The value to be converted

### Output

Type: LongInteger

### Examples

```text
When used in client-side and server-side logic:
DecimalToLongInteger(134.2) = 134
DecimalToLongInteger(134.5) = 134
DecimalToLongInteger(133.5) = 134
DecimalToLongInteger(134.7) = 135
DecimalToLongInteger(134) = 134
DecimalToLongInteger(157898999999988844444.2) = 0

When used in Aggregates:
DecimalToLongInteger(134.2) = 134
DecimalToLongInteger(134.5) = 134
DecimalToLongInteger(133.5) = 133
DecimalToLongInteger(134.7) = 134
DecimalToLongInteger(134) = 134
DecimalToLongInteger(157898999999988844444.2) = Arithmetic Overflow Error
```

## DecimalToLongIntegerValidate { \#DecimalToLongIntegerValidate }

Returns true if Decimal 'd' can be converted to a Long Integer value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

d : Type: Decimal. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
DecimalToLongIntegerValidate(134.2) = True
DecimalToLongIntegerValidate(134.5) = True
DecimalToLongIntegerValidate(133.5) = True
DecimalToLongIntegerValidate(134.7) = True
DecimalToLongIntegerValidate(134) = True
DecimalToLongIntegerValidate(157898999999988844444.2) = False
```

## DecimalToText { \#DecimalToText }

Converts Decimal 'd' to a Text value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

d : Type: Decimal. Mandatory.  
The value to be converted

### Output

Type: Text

### Examples

```text
DecimalToText(200.482) = "200.482"
DecimalToText(200) = "200"
```

## LongIntegerToInteger { \#LongIntegerToInteger }

Converts Long Integer 'l' to an Integer value. If 'l' is outside the boundaries of the Integer values, the function will return the Integer default value. To check if the conversion is possible you can use the LongIntegerToIntegerValidate function.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

l : Type: LongInteger. Mandatory.  
The value to be converted

### Output

Type: Integer

### Examples

```text
LongIntegerToInteger(3000) = 3000
LongIntegerToInteger(5645245584135987412) = 0
```

## LongIntegerToIntegerValidate { \#LongIntegerToIntegerValidate }

Returns true if Long Integer 'l' can be converted to an Integer value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

l : Type: LongInteger. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
LongIntegerToIntegerValidate(3000) = True
LongIntegerToIntegerValidate(5645245584135987412) = False
```

## LongIntegerToIdentifier { \#LongIntegerToIdentifier }

Converts Long Integer 'l' to a Long Integer Identifier.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

l : Type: LongInteger. Mandatory.  
The value to be converted

### Output

Type: EntityReferenceLongInteger

### Examples

```text
LongIntegerToIdentifier(5090493034304) = 5090493034304
```

## LongIntegerToText { \#LongIntegerToText }

Converts Long Integer 'l' to a Text value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

l : Type: LongInteger. Mandatory.  
The value to be converted

### Output

Type: Text

### Examples

```text
LongIntegerToText(5092039102) = "5092039102"
```

## IdentifierToInteger { \#IdentifierToInteger }

Converts Identifier 'Id' to an Integer value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

id : Type: EntityReference. Mandatory.  
The value to be converted

### Output

Type: Integer

### Examples

```text
IdentifierToInteger(GetUserId()) = 504 (the result may be different in your module)
```

## IdentifierToLongInteger { \#IdentifierToLongInteger }

Converts Identifier 'Id' to a Long Integer value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

id : Type: EntityReferenceLongInteger. Mandatory.  
The value to be converted

### Output

Type: LongInteger

### Examples

```text
IdentifierToLongInteger(GetUserId()) = 30 (the result may be different in your module)
```

## IdentifierToText { \#IdentifierToText }

Converts Identifier 'Id' to a Text value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

id : Type: EntityReferenceText. Mandatory.  
The value to be converted

### Output

Type: Text

### Examples

```text
IdentifierToText(GetUserId()) = "30" (the result may be different in your module)
```

## IntegerToBoolean { \#IntegerToBoolean }

Converts Integer 'i' to a Boolean value. Boolean value of 0 is False. Any other value is True.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

i : Type: Integer. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
IntegerToBoolean(10) = True
IntegerToBoolean(-10) = True
IntegerToBoolean(0) = False
```

## IntegerToDecimal { \#IntegerToDecimal }

Converts Integer 'i' to a Decimal value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

i : Type: Integer. Mandatory.  
The value to be converted

### Output

Type: Decimal

### Examples

```text
IntegerToDecimal(200) = 200
```

## IntegerToIdentifier { \#IntegerToIdentifier }

Converts Integer 'i' to an Integer Identifier.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

i : Type: Integer. Mandatory.  
The value to be converted

### Output

Type: EntityReference

### Examples

```text
IntegerToIdentifier(5) = 5
```

## IntegerToText { \#IntegerToText }

Converts Integer 'i' to a Text value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

i : Type: Integer. Mandatory.  
The value to be converted

### Output

Type: Text

### Examples

```text
IntegerToText(200) = "200"
```

## NullDate { \#NullDate }

Returns a null Date value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Output

Type: Date

### Examples

```text
NullDate() = #1900-01-01#
```

## NullIdentifier { \#NullIdentifier }

Returns a null Identifier valid for Integer and Long Integer Identifiers.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Output

Type: EntityReference

### Examples

```text
NullIdentifier() = 0
```

## NullObject { \#NullObject }

Returns a null Object value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: Object

### Examples

```text
ObjectVariable = NullObject()
```

## NullBinary { \#NullBinary }

Returns a null Binary Data value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: BinaryData

### Examples

```text
BinaryDataVariable = NullBinary()
```

## NullTextIdentifier { \#NullTextIdentifier }

Returns a null Text Identifier.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Output

Type: EntityReferenceText

### Examples

```text
NullTextIdentifier() = ""
```

## TextToDate { \#TextToDate }

Converts Text 't' to a Date value.  
If 't' can't be converted to a valid Date value, the function will return the Date default value. To check if the conversion is possible you can use the TextToDateValidate function.  
You should check the limits of the Date data type. You should also ensure that the date you type in the argument complies with the default date format \(yyyy-mm-dd, yyyy/mm/dd, and yyyy.mm.dd\) or the server’s environment configuration.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Date

### Examples

```text
TextToDate("2002-01-01") = #2002-01-01#
TextToDate("2002/01/01") = #2002-01-01#
TextToDate("2002.01.01") = #2002-01-01#
TextToDate("2002-25-01") = #1900-01-01#
TextToDate("2002/02/31") = #1900-01-01#
TextToDate("10000.01.01") = #1900-01-01#
```

## TextToDateTime { \#TextToDateTime }

Converts Text 't' to a Date Time value.  
If 't' can't be converted to a valid Date Time value, the function will return a Date Time default value. To check if the conversion is possible you can use the TextToDateTimeValidate function.  
You should check the limits of the Date Time data type. You should also ensure that the Date Time you type in the argument complies with the default Date Time format \(yyyy-mm-dd hh:mm:ss, yyyy/mm/dd hh:mm:ss, and yyyy.mm.dd hh:mm:ss\) or the server’s environment configuration.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: DateTime

### Examples

```text
TextToDateTime("2002-01-01 01:01:01") = #2002-01-01 01:01:01#
TextToDateTime("2002/01/01 01:01:01") = #2002-01-01 01:01:01#
TextToDateTime("2002.01.01 01:01:01") = #2002-01-01 01:01:01#
TextToDateTime("20-01-01 01:01:01") = #1900-01-01 00:00:00#
TextToDateTime("date time") = #1900-01-01 00:00:00#
TextToDateTime("2002.1.1 1-1-1") = #1900-01-01 00:00:00#
TextToDateTime("2002-01-01") = #2002-01-01 00:00:00#
TextToDateTime("01-01-01") = #1900-01-01 00:00:00#
```

## TextToDateTimeValidate { \#TextToDateTimeValidate }

Returns true if Text 't' can be converted to a Date Time value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
TextToDateTimeValidate("2002-01-01 01:01:01") = True
TextToDateTimeValidate("2002/01/01 01:01:01") = True
TextToDateTimeValidate("2002.01.01 01:01:01") = True
TextToDateTimeValidate("20-01-01 01:01:01") = False
TextToDateTimeValidate("date time") = False
TextToDateTimeValidate("2002.1.1 1-1-1") = False
TextToDateTimeValidate("2002-01-01") = True
TextToDateTimeValidate("01-01-01") = False
```

## TextToDateValidate { \#TextToDateValidate }

Returns true if Text 't' can be converted to a Date value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
TextToDateValidate("2002-01-01") = True
TextToDateValidate("2002/01/01") = True
TextToDateValidate("2002.01.01") = True
TextToDateValidate("2002-25-01") = False
TextToDateValidate("2002/02/31") = False
TextToDateValidate("10000.01.01") = False
```

## TextToDecimal { \#TextToDecimal }

Converts Text 't' to a Decimal value. The only allowed decimal separator is the ".". If 't' is outside the boundaries of the Decimal values, the function will return the Decimal default value. To check if the conversion is possible you can use the TextToDecimalValidate function.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Decimal

### Examples

```text
TextToDecimal("200") = 200
TextToDecimal("-200") = -200
TextToDecimal("200.482") = 200.482
TextToDecimal("-200.482") = -200.482
TextToDecimal("0.99999999") = 0.99999999
TextToDecimal("abc") = 0
```

## TextToDecimalValidate { \#TextToDecimalValidate }

Returns true if Text 't' can be converted to a Decimal value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
TextToDecimalValidate("200")    = True
TextToDecimalValidate("-200") = True
TextToDecimalValidate("200.482") = True
TextToDecimalValidate("-200.482") = True
TextToDecimalValidate("0.99999999") = True
TextToDecimalValidate("abc") = False
```

## TextToIdentifier { \#TextToIdentifier }

Converts Text 't' to a Text Identifier.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: EntityReferenceText

### Examples

```text
TextToIdentifier("NEW") = 'NEW'
```

## TextToInteger { \#TextToInteger }

Converts Text 't' to an Integer value.  
If 't' is outside the boundaries of the Integer values the function will return an Integer default value. To check if the conversion is possible you can use the TextToIntegerValidate function.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Integer

### Examples

```text
TextToInteger("200") = 200
TextToInteger("-200") = -200
TextToInteger("200.482") = 0
TextToInteger("not a number") = 0
```

## TextToLongInteger { \#TextToLongInteger }

Converts Text 't' to a Long Integer value.  
If 't' is outside the boundaries of the Long Integer values the function will return a Long Integer default value. To check if the conversion is possible you can use the TextToLongIntegerValidate function.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: LongInteger

### Examples

```text
TextToLongInteger("200") = 200
TextToLongInteger("-200") = -200
TextToLongInteger("56452455841359874121") = 0
TextToLongInteger("not a number") = 0
```

## TextToIntegerValidate { \#TextToIntegerValidate }

Returns true if Text 't' can be converted to an Integer value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
TextToIntegerValidate("200") = True
TextToIntegerValidate("-200") = True
TextToIntegerValidate("200.482") = False
TextToIntegerValidate("not a number") = False
```

## TextToLongIntegerValidate { \#TextToLongIntegerValidate }

Returns true if Text 't' can be converted to a Long Integer value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
TextToLongIntegerValidate("200") = True
TextToLongIntegerValidate("-200") = True
TextToLongIntegerValidate("56452455841359874121") = False
TextToLongIntegerValidate("not a number") = False
```

## TextToTime { \#TextToTime }

Converts Text 't' to a Time value.  
If 't' can't be converted to a valid Time value, the function will return the Time default value. To check if the conversion is possible you can use the TextToTimeValidate function.  
You should check the limits of the Time data type. You should also ensure that the Time you type in the argument complies with the Time format \(hh:mm:ss\).

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Time

### Examples

```text
TextToTime("12:12:12") = #12:12:12#
TextToTime("23:68:12") = #00:00:00#
TextToTime("0-0-0") = #00:00:00#
TextToTime("abc") = #00:00:00#
```

## TextToTimeValidate { \#TextToTimeValidate }

Returns true if Text 't' can be converted to a Time value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

t : Type: Text. Mandatory.  
The value to be converted

### Output

Type: Boolean

### Examples

```text
TextToTimeValidate("12:12:12") = True
TextToTimeValidate("23:68:12") = False
TextToTimeValidate("0-0-0") = False
TextToTimeValidate("abc") = False
```

## TimeToText { \#TimeToText }

Converts Time 't' to a Text value in the format "HH:mm:ss".

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

t : Type: Time. Mandatory.  
The value to be converted

### Output

Type: Text

### Examples

```text
TimeToText(#12:30:24#) = "12:30:24"
TimeToText(#2015-07-02 12:30:34#) = "12:30:34"
```

## ToObject { \#ToObject }

Converts expression 'exp' to an Object value.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

exp : Type: Generic. Mandatory.  
The element to be converted

### Output

Type: Object

