# Format

| Name | Description |
| :--- | :--- |
| [FormatCurrency](builtinfunction.format.md#FormatCurrency)\(​Currency, Text, Integer, Text, Text\) | Builds a Text output of the specified Currency 'value', preceded by the currency 'symbol', using 'decimal\_digits' after the decimal point. The decimal point is specified using 'decimal\_separator', while the thousands can be separated with the 'group\_separator'.  When rounding, the function behaves differently depending on where you use it:  - In the **application server**, it applies the method round half up \(rounds to the nearest integer, 0.5 rounds up\). - In **client-side logic**, it applies the method round half to even \(rounds to the nearest integer, 0.5 rounds to the nearest even integer\). |
| [FormatDecimal](builtinfunction.format.md#FormatDecimal)\(​Decimal, Integer, Text, Text\) | Builds a Text output of the specified Decimal 'value', using 'decimal\_digits' after the decimal point. The decimal point is specified using 'decimal\_separator', while the thousands can be separated with the 'group\_separator'.  When rounding, the function behaves differently depending on where you use it:  - In the **application server**, it applies the method round half up \(rounds to the nearest integer, 0.5 rounds up\). - In **client-side logic**, it applies the method round half to even \(rounds to the nearest integer, 0.5 rounds to the nearest even integer\). |
| [FormatPercent](builtinfunction.format.md#FormatPercent)\(​Decimal, Integer, Text\) | Builds a Text output of the specified Decimal 'value', followed by '%' using 'decimal\_digits' after the decimal point. The decimal point is specified using 'decimal\_separator'.  When rounding, the function behaves differently depending on where you use it:  - In the **application server**, it applies the method round half up \(rounds to the nearest integer, 0.5 rounds up\). - In **client-side logic**, it applies the method round half to even \(rounds to the nearest integer, 0.5 rounds to the nearest even integer\). |
| [FormatPhoneNumber](builtinfunction.format.md#FormatPhoneNumber)\(​Text, Integer, Integer, Integer, Text, Text, Text\) | Builds a Text output of the specified phone number Text 'value', starting with the international separator 'int\_separator', followed by the first 'int\_code\_digits' of 'value', then the 'area\_separator', then the following 'area\_code\_digits' of 'value', then the 'phone\_separator' and finally the following 'phone\_digits' of 'value'. |
| [FormatText](builtinfunction.format.md#FormatText)\(​Text, Integer, Integer, Boolean, Text\) | Builds a Text output of the specified Text 'value', by limiting it to the specified 'max\_chars' count. If 'value' has less than the 'min\_chars' characters limit, enough 'padding\_char' characters are added to expand the length to that limit. In this case, 'left\_padding' determines where the padding should be added. |
| [FormatDateTime](builtinfunction.format.md#FormatDateTime)\(​DateTime, Text\) | Builds a Text output of the specified Date Time 'value' using the specified 'format'. Formatting pattern can be any combination of the following: Day: - d: day without leading zero; - dd: day WITH leading zero; - ddd: abbreviated day name; - dddd: full day name; Month: - M: month without leading zero; - MM: month WITH leading zero; - MMM: abbreviated month name; - MMMM: full month name; Year: - y: last one or two digits of the year; - yy: last two digits of the year; - yyyy: year; Hour: - h: hour from 0 to 12 without leading zero; - hh: hour from 0 to 12 WITH leading zero; - H: hour from 0 to 24 without leading zero; - HH: hour from 0 to 24 WITH leading zero; Minute: - m: minutes without leading zero; - mm: minutes WITH leading zero; Second: - s: seconds without leading zero; - ss: seconds WITH leading zero; AM Designator: - t: first letter of AM or PM; - tt: AM or PM.  If you want to output any of these characters then precede it with '\'. Changing the environment date format does not change the way the FormatDateTime function formats the dates. |

## FormatCurrency { \#FormatCurrency }

Builds a Text output of the specified Currency 'value', preceded by the currency 'symbol', using 'decimal\_digits' after the decimal point. The decimal point is specified using 'decimal\_separator', while the thousands can be separated with the 'group\_separator'.

When rounding, the function behaves differently depending on where you use it:

* In the **application server**, it applies the method round half up \(rounds to the nearest integer, 0.5 rounds up\).  
* In **client-side logic**, it applies the method round half to even \(rounds to the nearest integer, 0.5 rounds to the nearest even integer\).  

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

value : Type: Currency. Mandatory.  
The Currency value to be formatted.

symbol : Type: Text. Mandatory.  
The currency symbol.

decimal\_digits : Type: Integer. Mandatory.  
The number of decimal digits.

decimal\_separator : Type: Text. Mandatory.  
The decimal separator symbol.

group\_separator : Type: Text. Mandatory.  
The group separator symbol.

### Output

Type: Text

### Examples

```text
FormatCurrency(1.2, "$", 1, "#", ".") = "$1#2"
FormatCurrency(1.2, "$", 3, ",", ".") = "$1,200"
FormatCurrency(1.24, "$", 1, ",", ".") = "$1,2"
FormatCurrency(1.25, "$", 1, ",", ".") = "$1,3" (in the application server) or "$1,2" (in client-side logic)
FormatCurrency(1.251, "$", 1, ",", ".") = "$1,3"
FormatCurrency(1.35, "$", 1, ",", ".") = "$1,4"
FormatCurrency(12345.67, "$", 2, ",", ".") = "$12.345,67"
FormatCurrency(-12345.67, "$", 2, ",", ".") = "$-12.345,67"
```

## FormatDecimal { \#FormatDecimal }

Builds a Text output of the specified Decimal 'value', using 'decimal\_digits' after the decimal point. The decimal point is specified using 'decimal\_separator', while the thousands can be separated with the 'group\_separator'.

When rounding, the function behaves differently depending on where you use it:

* In the **application server**, it applies the method round half up \(rounds to the nearest integer, 0.5 rounds up\).  
* In **client-side logic**, it applies the method round half to even \(rounds to the nearest integer, 0.5 rounds to the nearest even integer\).  

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

value : Type: Decimal. Mandatory.  
The Decimal value to be formatted.

decimal\_digits : Type: Integer. Mandatory.  
The number of decimal digitis.

decimal\_separator : Type: Text. Mandatory.  
The decimal separator symbol.

group\_separator : Type: Text. Mandatory.  
The group separator symbol.

### Output

Type: Text

### Examples

```text
FormatDecimal(1.2, 1, "#", ".") = "1#2"
FormatDecimal(1.2, 3, ",", ".") = "1,200"
FormatDecimal(1.24, 1, ",", ".") = "1,2"
FormatDecimal(1.25, 1, ",", ".") = "1,3" (in the application server) or "1,2" (in client-side logic)
FormatDecimal(1.251, 1, ",", ".") = "1,3"
FormatDecimal(1.35, 1, ",", ".") = "1,4"
FormatDecimal(12345.67, 2, ",", ".") = "12.345,67"
FormatDecimal(-12345.67, 2, ",", ".") = "-12.345,67"
```

## FormatPercent { \#FormatPercent }

Builds a Text output of the specified Decimal 'value', followed by '%' using 'decimal\_digits' after the decimal point. The decimal point is specified using 'decimal\_separator'.

When rounding, the function behaves differently depending on where you use it:

* In the **application server**, it applies the method round half up \(rounds to the nearest integer, 0.5 rounds up\).  
* In **client-side logic**, it applies the method round half to even \(rounds to the nearest integer, 0.5 rounds to the nearest even integer\).  

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

value : Type: Decimal. Mandatory.  
The Decimal value to format as a percentage.

decimal\_digits : Type: Integer. Mandatory.  
The number of decimal digits to use.

decimal\_separator : Type: Text. Mandatory.  
The symbol to use as decimal separator.

### Output

Type: Text

### Examples

```text
FormatPercent(0.12, 3, "#") = "12#000%"
FormatPercent(0.124, 0, ",") = "12%"
FormatPercent(0.125, 0, ",") = "13%" (in the application server) or "12%" (in client-side logic)
FormatPercent(0.1251, 0, ",") = "13%"
FormatPercent(0.135, 0, ",") = "14%"
FormatPercent(12345.6789, 2, ",") = "1234567,89%"
FormatPercent(-12345.6789, 2, ",") = "-1234567,89%"
```

## FormatPhoneNumber { \#FormatPhoneNumber }

Builds a Text output of the specified phone number Text 'value', starting with the international separator 'int\_separator', followed by the first 'int\_code\_digits' of 'value', then the 'area\_separator', then the following 'area\_code\_digits' of 'value', then the 'phone\_separator' and finally the following 'phone\_digits' of 'value'.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

value : Type: Text. Mandatory.  
The phone number to be formatted.

int\_code\_digits : Type: Integer. Mandatory.  
The number of digits composing the international code.

area\_code\_digits : Type: Integer. Mandatory.  
The number of digits composing the area code.

phone\_digits : Type: Integer. Mandatory.  
The number of digitis composing the phone number without international or area codes.

int\_separator : Type: Text. Mandatory.  
The symbol for the international code.

area\_separator : Type: Text. Mandatory.  
The symbol to use as separator between the international code and the area code.

phone\_separator : Type: Text. Mandatory.  
The symbol to use as separator between the area code and the phone number.

### Output

Type: Text

### Examples

```text
FormatPhoneNumber("351214153737", 3, 2, 7, "+", "-", ".") = "+351-21.4153737"
```

## FormatText { \#FormatText }

Builds a Text output of the specified Text 'value', by limiting it to the specified 'max\_chars' count. If 'value' has less than the 'min\_chars' characters limit, enough 'padding\_char' characters are added to expand the length to that limit. In this case, 'left\_padding' determines where the padding should be added.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

value : Type: Text. Mandatory.  
The Text to be formatted.

min\_chars : Type: Integer. Mandatory.  
The minimum number of characters in the output.

max\_chars : Type: Integer. Mandatory.  
The maximum number of characters in the output.

left\_padding : Type: Boolean. Mandatory.  
Indicates in which side the Text is padded.

padding\_char : Type: Text. Mandatory.  
The character to use for padding the string to the minimum length.

### Output

Type: Text

### Examples

```text
FormatText("123456789", 3, 9, True, "#") = "123456789"
FormatText("123456789876", 3, 9, True, "#") = "456789876"
FormatText("123456789876", 3, 9, False, "#") = "123456789"
FormatText("12345", 10, 20, True, "#") = "#####12345"
FormatText("12345", 10, 20, False, "#") = "12345#####"
```

## FormatDateTime { \#FormatDateTime }

Builds a Text output of the specified Date Time 'value' using the specified 'format'. Formatting pattern can be any combination of the following:  
Day:

* d: day without leading zero;  
* dd: day WITH leading zero;  
* ddd: abbreviated day name;  
* dddd: full day name;  

  Month:  

* M: month without leading zero;  
* MM: month WITH leading zero;  
* MMM: abbreviated month name;  
* MMMM: full month name;  

  Year:  

* y: last one or two digits of the year;  
* yy: last two digits of the year;  
* yyyy: year;  

  Hour:  

* h: hour from 0 to 12 without leading zero;  
* hh: hour from 0 to 12 WITH leading zero;  
* H: hour from 0 to 24 without leading zero;  
* HH: hour from 0 to 24 WITH leading zero;  

  Minute:  

* m: minutes without leading zero;  
* mm: minutes WITH leading zero;  

  Second:  

* s: seconds without leading zero;  
* ss: seconds WITH leading zero;  

  AM Designator:  

* t: first letter of AM or PM;  
* tt: AM or PM.  

If you want to output any of these characters then precede it with '\'.  
Changing the environment date format does not change the way the FormatDateTime function formats the dates.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

value : Type: DateTime. Mandatory.  
The Date Time to be formatted.

format : Type: Text. Mandatory.  
The formatting pattern.

### Output

Type: Text

### Examples

```text
FormatDateTime(#2015-06-09 10:05:20#, "ddd, dd MMM yyyy") = "Tue, 09 Jun 2015"
FormatDateTime(CurrDateTime(),"To\da\y i\s: dddd") = "Today is: Tuesday"
```

