# Email

| Name | Description |
| :--- | :--- |
| [EmailAddressCreate](builtinfunction.email.md#EmailAddressCreate)\(​Text, Text\) | Returns a full email address string containing the display name \(usually it's the name of the email address owner\) and the email address itself. The resulting full email address may then be used in the Send Email element \(action flows\) or in the Send Email activity \(process flows\). To build a list of email addresses use the EmailAddressesConcatenate built-in function. |
| [EmailAddressesConcatenate](builtinfunction.email.md#EmailAddressesConcatenate)\(​Text, Text\) | Returns the concatenation of email addresses, or list of email addresses, into a a new list of email addresses separated by a comma \(','\). The resulting list may then be used in the Send Email element \(action flows\) or in the Send Email activity \(process flows\). |
| [EmailAddressValidate](builtinfunction.email.md#EmailAddressValidate)\(​Text\) | Returns true if Text 'address' is a valid email address. Note that EmailAddressValidate\(""\) returns True. This built-in function implements the validation specified by HTML5 \(https://html.spec.whatwg.org/multipage/input.html\#valid-e-mail-address\) which has a practical approach to RFC 5322. |

## EmailAddressCreate { \#EmailAddressCreate }

Returns a full email address string containing the display name \(usually it's the name of the email address owner\) and the email address itself. The resulting full email address may then be used in the Send Email element \(action flows\) or in the Send Email activity \(process flows\).  
To build a list of email addresses use the EmailAddressesConcatenate built-in function.

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

name : Type: Text. Mandatory.  
The display name of the email address which usually is the name of the email address owner as, for example, "John Smith".

email : Type: Text. Mandatory.  
The email address itself, for example, john.smith@worldmail.com.

### Output

Type: Text

### Examples

```text
EmailAddressCreate("John Smith", "john.smith​@​worldmail.com") = "John Smith" <john.smith​@​worlmail.com>
EmailAddressCreate("Mary Jones", "mary.jones​@​company.com") = "Mary Jones" <mary.jones​@​company.com>
```

## EmailAddressesConcatenate { \#EmailAddressesConcatenate }

Returns the concatenation of email addresses, or list of email addresses, into a a new list of email addresses separated by a comma \(','\). The resulting list may then be used in the Send Email element \(action flows\) or in the Send Email activity \(process flows\).

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

address1 : Type: Text. Mandatory.  
The email address or email addresses list

address2 : Type: Text. Mandatory.  
The email address or email addresses list

### Output

Type: Text

### Examples

```text
EmailAddressesConcatenate(EmailAddressCreate("John Smith", "john.smith​@​worldmail.com"), EmailAddressCreate("Mary Adams", "mary.adams​@​adamsinc.com")) = "John Smith" <john.smith​@​worldmail.com>, "Mary Adams" <mary.adams​@​adamsinc.com>
```

## EmailAddressValidate { \#EmailAddressValidate }

Returns true if Text 'address' is a valid email address. Note that EmailAddressValidate\(""\) returns True.  
This built-in function implements the validation specified by HTML5 \([https://html.spec.whatwg.org/multipage/input.html\#valid-e-mail-address](https://html.spec.whatwg.org/multipage/input.html#valid-e-mail-address)\) which has a practical approach to RFC 5322.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Parameters

address : Type: Text. Mandatory.  
The email address to validate.

### Output

Type: Boolean

### Examples

```text
EmailAddressValidate(EmailAddressCreate("John Smith", "john.smith​@​worldmail.com")) = True
EmailAddressValidate("John Smith <john.smith​@​>") = False
```

