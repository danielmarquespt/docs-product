# Text API

For Platform Version 9.0.99.11. Provides actions to manipulate character strings such as joining, splitting, search and replace using regular expressions, and custom formatting of DateTime expressions.

## Summary

| Action | Description |
| :--- | :--- |
| [Format\_DateTime](text-api.md#Format_DateTime%3E) | Formats a DateTime by replacing the allowed keywords with their values.%%Available Keywords:%%\[yyyy\] - Represents the year as a four-digit number;%%\[MM\] - Represents the month as a number from 01 through 12;%%\[MMM\] - Represents the abbreviated name of the month;%%\[MMMM\] - Represents the full name of the month;%%\[dd\] - Represents the day of the month as a number from 01 through 31;%%\[ddd\] - Represents the abbreviated name of the day of the week;%%\[dddd\] - Represents the full name of the day of the week;%%\[hh\] - Represents the hour as a number from 01 through 12;%%\[HH\] - Represents the hour as a number from 00 through 23;%%\[mm\] - Represents the minute as a number from 0 through 59;%%\[ss\] - Represents the seconds as a number from 00 through 59; |
| [Regex\_Replace](text-api.md#Regex_Replace%3E) | Replaces all occurrences of a specified regular expression pattern with a replacement string. |
| [Regex\_Search](text-api.md#Regex_Search%3E) | Searches the input string for an occurrence of a regular expression. |
| [String\_Join](text-api.md#String_Join%3E) | Concatenates all the strings in a List, yielding a single string. The individual elements are separated, in the resulting string, by the string Separator. |
| [String\_LastIndexOf](text-api.md#String_LastIndexOf%3E) | Reports the index position of the last occurrence of a specified Pattern within a Text. |
| [String\_Split](text-api.md#String_Split%3E) | Splits a string into individual elements delimited by any of the characters in Delimiters. |
| [StringBuilder\_Append](text-api.md#StringBuilder_Append%3E) | Appends a string to a StringBuilder. |
| [StringBuilder\_Create](text-api.md#StringBuilder_Create%3E) | Creates a StringBuilder. Use it if you need to create a string by repeatedly appending substrings. A StringBuilder optimizes memory management when dealing with highly dynamic strings. |
| [StringBuilder\_ToString](text-api.md#StringBuilder_ToString%3E) | Returns the content of the StringBuilder's buffer. |

| Structure | Description |
| :--- | :--- |
| [Text](text-api.md#Structure_Text%3E) | Structure with single Text attribute |

## Actions

### Format\_DateTime { \#Format\_DateTime }

Formats a DateTime by replacing the allowed keywords with their values.  
Available Keywords:  
\[yyyy\] - Represents the year as a four-digit number;  
\[MM\] - Represents the month as a number from 01 through 12;  
\[MMM\] - Represents the abbreviated name of the month;  
\[MMMM\] - Represents the full name of the month;  
\[dd\] - Represents the day of the month as a number from 01 through 31;  
\[ddd\] - Represents the abbreviated name of the day of the week;  
\[dddd\] - Represents the full name of the day of the week;  
\[hh\] - Represents the hour as a number from 01 through 12;  
\[HH\] - Represents the hour as a number from 00 through 23;  
\[mm\] - Represents the minute as a number from 0 through 59;  
\[ss\] - Represents the seconds as a number from 00 through 59;

_Inputs_

DateTime : Type: DateTime. Mandatory.  
The Datetime to be formated.

Format : Type: Text. Mandatory.  
The Text with the available keywords used to format the Date Time.

_Outputs_

FormattedDateTime : Type: Text.  
The Text with the formatted Date Time according to the specified Format.

### Regex\_Replace { \#Regex\_Replace }

Replaces all occurrences of a specified regular expression pattern with a replacement string.

_Inputs_

Text : Type: Text. Mandatory.  
Text in which to search for a Pattern.

Pattern : Type: Text. Mandatory.  
The string to modify.

Replace : Type: Text. Mandatory.  
The replacement string.

IgnoreCase : Type: Boolean. Default: True.  
Specifies case-insensitive matching.

MultiLine : Type: Boolean. Default: False.  
Changes the meaning of ^and $ so the match at the beginning and end, respectively, of each line, and not just the beginning and end of the entire string.

SingleLine : Type: Boolean. Default: False.  
Changes the meaning of the dot \(.\) so it matches every character \(instead of every character except \n\).

_Outputs_

Result : Type: Text.  
The modified character string.

### Regex\_Search { \#Regex\_Search }

Searches the input string for an occurrence of a regular expression.

_Inputs_

Text : Type: Text. Mandatory.  
Text in which to search for a Pattern.

Pattern : Type: Text. Mandatory.  
Pattern to search in Text.

IgnoreCase : Type: Boolean. Default: True.  
Specifies case-insensitive matching.

MultiLine : Type: Boolean. Default: False.  
Changes the meaning of ^and $ so the match at the beginning and end, respectively, of each line, and not just the beginning and end of the entire string.

SingleLine : Type: Boolean. Default: False.  
Changes the meaning of the dot \(.\) so it matches every character \(instead of every character except \n\).

_Outputs_

Found : Type: Boolean.  
True if Pattern is found in the Text.

PatternResult : Type: Text.  
Represents the matched string.

FirstIndex : Type: Integer.  
Index of the first occurrence of Pattern in Text.

### String\_Join { \#String\_Join }

Concatenates all the strings in a List, yielding a single string. The individual elements are separated, in the resulting string, by the string Separator.

_Inputs_

List : Type: RecordList of [Text](text-api.md#Structure_Text%3E). Mandatory.  
List of strings to be concatenated.

Separator : Type: Text. Mandatory.  
Separating element.

_Outputs_

Text : Type: Text.  
Result of concatenation.

### String\_LastIndexOf { \#String\_LastIndexOf }

Reports the index position of the last occurrence of a specified Pattern within a Text.

_Inputs_

Text : Type: Text.  
The Text to analyse.

Pattern : Type: Text. Mandatory.  
The pattern to seek.

_Outputs_

Position : Type: Integer.  
The index position of the pattern if it was found, or -1 if it was not. If the Text is empty, the returned Position is 0.

### String\_Split { \#String\_Split }

Splits a string into individual elements delimited by any of the characters in Delimiters.

_Inputs_

Text : Type: Text. Mandatory.  
Text to be splitted into individual strings.

Delimiters : Type: Text. Mandatory.  
Contains all the characters that should be considered as separators.

_Outputs_

List : Type: RecordList of [Text](text-api.md#Structure_Text%3E).  
List of strings that results from splitting the original Text.

### StringBuilder\_Append { \#StringBuilder\_Append }

Appends a string to a StringBuilder.

_Inputs_

StringBuilder : Type: Object. Mandatory.  
The StringBuilder instance. Returned by the Action StringBuilder\_Create.

String : Type: Text. Mandatory.  
The string to append to the StringBuilder's buffer.

### StringBuilder\_Create { \#StringBuilder\_Create }

Creates a StringBuilder. Use it if you need to create a string by repeatedly appending substrings. A StringBuilder optimizes memory management when dealing with highly dynamic strings.

_Inputs_

InitialCapacity : Type: Integer. Mandatory.  
Initial capacity of the StringBuilder buffer. The buffer will be automatically resized if its capacity is exceeded. Set it to the maximum expected capacity to avoid buffer resizing.

_Outputs_

StringBuilder : Type: Object.  
The StringBuilder instance. Use it as input to the other StringBuilder Actions.

### StringBuilder\_ToString { \#StringBuilder\_ToString }

Returns the content of the StringBuilder's buffer.

_Inputs_

StringBuilder : Type: Object. Mandatory.  
The StringBuilder instance. Returned by the Action StringBuilder\_Create.

_Outputs_

String : Type: Text.  
The content of the StringBuilder's buffer.

## Structures

### Text { \#Structure\_Text }

Structure with single Text attribute

_Attributes_

Value : Type: Text \(50\). Mandatory.

