# URL

| Name | Description |
| :--- | :--- |
| [AddPersonalAreaToURLPath](builtinfunction.url.md#AddPersonalAreaToURLPath)\(​Text\) | Returns a string where the Personal Area is added \(if applicable\) to the URL path set in Text 't' input parameter. This function enables you to run any page \(or resource\) of your module in the Personal Area without having to manually change their paths. This function adds the Personal Area of the developer that is running the module to the URL path provided by the input parameter. |
| [GetBookmarkableURL](builtinfunction.url.md#GetBookmarkableURL)\(\) | Returns the URL of the screen that is currently being processed. The URL returned by this function is a complete URL with the format http://server/module/personal\_area/screen?param1=value&param2=value... Parameters and their values aren't included when parameters are optional and their values aren't set. |
| [GetPersonalAreaName](builtinfunction.url.md#GetPersonalAreaName)\(\) | Returns the name of the Personal Area where the module is currently running. |
| [GetOwnerURLPath](builtinfunction.url.md#GetOwnerURLPath)\(\) | Returns the URL path of the module that owns the element that is being processed. Note that this function does not return the complete URL but only the component containing the location of the resource within the domain and, if applicable, the personal area. |
| [GetExceptionURL](builtinfunction.url.md#GetExceptionURL)\(\) | Returns the absolute URL of the screen where the last exception was raised. |

## AddPersonalAreaToURLPath { \#AddPersonalAreaToURLPath }

Returns a string where the Personal Area is added \(if applicable\) to the URL path set in Text 't' input parameter. This function enables you to run any page \(or resource\) of your module in the Personal Area without having to manually change their paths.  
This function adds the Personal Area of the developer that is running the module to the URL path provided by the input parameter.

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

url : Type: Text. Mandatory.  
The url to add the personal area path to.

### Output

Type: Text

### Examples

```text
Consider that Dave Lauper is running the Customers module in his Personal Area and that his username is 'dlauper':
AddPersonalAreaToURLPath("/Customers/ListCustomers.aspx") = "/Customers/dlauper/ListCustomers.aspx"
AddPersonalAreaToURLPath("http://myserverat.outsystemscloud.com/Customers/ListCustomers.aspx") = "http://myserverat.outsystemscloud.com/Customers/dlauper/ListCustomers.aspx"

In this next example the same developer is running the module in the public area:
AddPersonalAreaToURLPath("/Customers/ListCustomers.aspx") = "/Customers/ListCustomers.aspx"
```

## GetBookmarkableURL { \#GetBookmarkableURL }

Returns the URL of the screen that is currently being processed.  
The URL returned by this function is a complete URL with the format [http://server/module/personal\_area/screen?param1=value&amp;param2=value](http://server/module/personal_area/screen?param1=value&amp;param2=value)...  
Parameters and their values aren't included when parameters are optional and their values aren't set.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: Text

### Examples

```text
GetBookmarkableURL() = "http://myserverat.outsystemscloud.com/Customers/EditCustomer.aspx?CustomerId=1"
```

## GetPersonalAreaName { \#GetPersonalAreaName }

Returns the name of the Personal Area where the module is currently running.

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: Text

### Examples

```text
Consider that Dave Lauper is running the Customers module in his Personal Area and that his username is 'dlauper':
GetPersonalAreaName() = "dlauper"
```

## GetOwnerURLPath { \#GetOwnerURLPath }

Returns the URL path of the module that owns the element that is being processed. Note that this function does not return the complete URL but only the component containing the location of the resource within the domain and, if applicable, the personal area.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: Text

### Examples

```text
GetOwnerURLPath() = "/Customers/"
```

## GetExceptionURL { \#GetExceptionURL }

Returns the absolute URL of the screen where the last exception was raised.

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: Text

### Examples

```text
GetExceptionURL() = "http://myserverat.outsystemscloud.com/Customers/ListCustomers.aspx"
```

