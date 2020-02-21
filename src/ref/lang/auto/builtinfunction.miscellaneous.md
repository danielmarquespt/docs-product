# Miscellaneous

| Name | Description |
| :--- | :--- |
| [GeneratePassword](builtinfunction.miscellaneous.md#GeneratePassword)\(​Integer, Boolean\) | Generates and returns a password string of length 'l'. If 'alpha' is True the string can contain both digits and letters, if False the string can only contain digits. The generated password string is a random combination of letters and digits, or just digits, depending on 'alpha'. |
| [If](builtinfunction.miscellaneous.md#If)\(​Boolean, Generic, Generic\) | Returns 'true\_return' if 'value' is True, otherwise returns 'false\_return'. The return data type of the function is the type of 'true\_return' unless there's an implicit conversion from 'true\_return' type to 'false\_return' type. When there's no implicit type conversion an invalid data type error will occur. |
| [IsLoadingScreen](builtinfunction.miscellaneous.md#IsLoadingScreen)\(\) | Returns true only when invoked within a screen Preparation execution and only if the screen is loading its content. Otherwise, if the screen is just being redrawn, i.e. posted back, it returns False. |
| [CurrentThemeIsMobile](builtinfunction.miscellaneous.md#CurrentThemeIsMobile)\(\) | Returns true when the current web screen is using a mobile theme. |

## GeneratePassword { \#GeneratePassword }

Generates and returns a password string of length 'l'. If 'alpha' is True the string can contain both digits and letters, if False the string can only contain digits. The generated password string is a random combination of letters and digits, or just digits, depending on 'alpha'.

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

l : Type: Integer. Mandatory.  
The length of the Text string to be generated.

alpha : Type: Boolean. Mandatory.  
Indicates if the generated Text string can contain digits and letters or digits only.

### Output

Type: Text

### Examples

```text
GeneratePassword(10, True) = "3fgp7lzmqt"
GeneratePassword(6, False) = "038013"
```

## If { \#If }

Returns 'true\_return' if 'value' is True, otherwise returns 'false\_return'.  
The return data type of the function is the type of 'true\_return' unless there's an implicit conversion from 'true\_return' type to 'false\_return' type.  
When there's no implicit type conversion an invalid data type error will occur.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

value : Type: Boolean. Mandatory.  
The condition to be evaluated.

true\_return : Type: Generic. Mandatory.  
The expression to be evaluated and returned when the condition is true.

false\_return : Type: Generic. Mandatory.  
The expression to be evaluated and returned when the condition is false.

### Output

Type: Generic

### Examples

```text
If(countVar = 0, 0, 1/countVar) = 0 when countVar is 0 or 1/countVar when countVar is different from 0.
If(True, 2.34, "xpto") = "2.34"
If(False, "xpto", #2016-05-02#) = "2016-05-02"
If(False, #2015-05-02#, #2016-05-02#) = #2016-05-02#
If(False, 2.34, #2016-05-02#) = Invalid Data Type error.
```

## IsLoadingScreen { \#IsLoadingScreen }

Returns true only when invoked within a screen Preparation execution and only if the screen is loading its content. Otherwise, if the screen is just being redrawn, i.e. posted back, it returns False.

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: Boolean

## CurrentThemeIsMobile { \#CurrentThemeIsMobile }

Returns true when the current web screen is using a mobile theme.

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: Boolean

