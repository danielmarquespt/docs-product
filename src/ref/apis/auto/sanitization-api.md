# Sanitization API

Starting in Platform Version 9.1.0.21., this API provides methods to avoid code injection in HTML, Javascript and SQL snippets that need to include untrusted content, i.e., content gathered from end-users.

## Summary

| Action | Description |
| :--- | :--- |
| [BuildSafe\_InClauseIntegerList](sanitization-api.md#BuildSafe_InClauseIntegerList%3E) | Returns a comma-delimited text value containing all the integer values provided as input. The returned value can be safely used in a SQL "IN" clause. |
| [BuildSafe\_InClauseTextList](sanitization-api.md#BuildSafe_InClauseTextList%3E) | Returns a comma-delimited text value with the encoded version of all the text values provided as input. The returned value can be safely used in a SQL "IN" clause. |
| [SanitizeHtml](sanitization-api.md#SanitizeHtml%3E) | Sanitizes the provided HTML using the HtmlSanitizer NuGet package. |
| [VerifyJavascriptLiteral](sanitization-api.md#VerifyJavascriptLiteral%3E) | Ensure the provided JavaScript only contains literals. If it contains anything else, an INVALID JAVASCRIPT LITERAL exception is thrown. |
| [VerifySqlLiteral](sanitization-api.md#VerifySqlLiteral%3E) | **Deprecated**. Ensure the provided SQL only contains literals. If it contains anything else, an INVALID SQL LITERAL exception is thrown. |

## Actions

### BuildSafe\_InClauseIntegerList { \#BuildSafe\_InClauseIntegerList }

Returns a comma-delimited text value containing all the integer values provided as input. The returned value can be safely used in a SQL "IN" clause.

_Inputs_

ValueList : Type: RecordList of [IntegerLiteral](sanitization-api.md#Structure_IntegerLiteral%3E). Mandatory.  
List of integer values to include in the returned value.

_Outputs_

Output : Type: Text.  
A string containing comma-separated integer values to be used in a SQL "IN" clause.

### BuildSafe\_InClauseTextList { \#BuildSafe\_InClauseTextList }

Returns a comma-delimited text value with the encoded version of all the text values provided as input. The returned value can be safely used in a SQL "IN" clause.

_Inputs_

ValueList : Type: RecordList of [TextLiteral](sanitization-api.md#Structure_TextLiteral%3E). Mandatory.  
List of text values to include in the returned value.

_Outputs_

Output : Type: Text.  
A string containing a set of encoded text values separated by commas to be used in a SQL "IN" clause.

### SanitizeHtml { \#SanitizeHtml }

Sanitizes the provided HTML using the HtmlSanitizer NuGet package.  
Note: The underlying library was recently changed from OWASP Java HTML Sanitizer Project. Check the [Release Notes](https://success.outsystems.com/Support/Release_Notes/11/Platform_Server>) for a summary of what changed.

_Inputs_

Html : Type: Text. Mandatory.  
The HTML to sanitize.

_Outputs_

SanitizedHtml : Type: Text.  
The sanitized HTML.

### VerifyJavascriptLiteral { \#VerifyJavascriptLiteral }

Ensures the provided JavaScript only contains literals. If it contains anything else, an INVALID JAVASCRIPT LITERAL exception is thrown.

_Inputs_

JavascriptLiteral : Type: Text. Mandatory.  
The JavaScript literal to sanitize.

_Outputs_

SanitizedJavascriptLiteral : Type: Text.  
The sanitized JavaScript literal.

### VerifySqlLiteral { \#VerifySqlLiteral }

**Deprecated**. Ensures the provided SQL only contains literals. If it contains anything else, an INVALID SQL LITERAL exception is thrown.

_Inputs_

SqlLiteral : Type: Text. Mandatory.  
The SQL to sanitize.

_Outputs_

SanitizedSqlLiteral : Type: Text.  
The sanitized SQL.

## Structures

### IntegerLiteral { \#Structure\_IntegerLiteral }

Simple structure holding a long integer value. Used as a record definition when providing a list of IntegerLiteral records to include in a SQL "IN" clause.

_Attributes_

Value : Type: LongInteger. Mandatory.  
An integer value to consider when creating a SQL "IN" clause.

### TextLiteral { \#Structure\_TextLiteral }

Simple structure holding a text value. Used as a record definition when providing a list of TextLiteral records to include in a SQL "IN" clause.

_Attributes_

Value : Type: Text \(2000\). Mandatory.  
A text value to consider when creating a SQL "IN" clause.

