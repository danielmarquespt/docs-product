# HTTPRequestHandler API

For Platform Version 9.0.0.0. Provides actions to manipulate HTTP Requests and Responses.

## Summary

| Action | Description |
| :--- | :--- |
| [AddAttributeToHtmlTag](httprequesthandler-api.md#AddAttributeToHtmlTag%3E) | Adds an attribute to the outermost HTML tag of the document \(e.g. xmlns, manifest...\).%%This method has no effect in Ajax Requests. |
| [AddFaviconTag](httprequesthandler-api.md#AddFaviconTag%3E) | Allows setting the favicon for the current page. You can use "omlresources" to add an icon file to your oml.%%This method has no effect in Ajax Requests. |
| [AddHeader](httprequesthandler-api.md#AddHeader%3E) | Adds a header to the current HTTP response.%%This method has no effect in Ajax Requests. |
| [AddJavaScriptTag](httprequesthandler-api.md#AddJavaScriptTag%3E) | Adds a &lt;script&gt; tag to the HTML of the current HTTP response.%%This method has no effect in Ajax Requests. |
| [AddLinkTag](httprequesthandler-api.md#AddLinkTag%3E) | Adds a &lt;link&gt; tag to the HTML of the current HTTP response.%%This method has no effect in Ajax Requests. |
| [AddMetaHttpEquivTag](httprequesthandler-api.md#AddMetaHttpEquivTag%3E) | Adds a &lt;meta&gt; tag with the http-equiv attribute to the HTML of the current HTTP response.%%This method has no effect in Ajax Requests. |
| [AddMetaTag](httprequesthandler-api.md#AddMetaTag%3E) | Adds a &lt;meta&gt; tag to the HTML of the current HTTP response.%%This method has no effect in Ajax Requests. |
| [AddPostProcessingFilter](httprequesthandler-api.md#AddPostProcessingFilter%3E) | This method has no effect in Ajax Requests.%%Not implemented in Java. |
| [AddSessionToURL](httprequesthandler-api.md#AddSessionToURL%3E) | Adds the current session identifier to a specified URL. |
| [AddStyleSheetTag](httprequesthandler-api.md#AddStyleSheetTag%3E) | Adds a &lt;link rel="stylesheet"&gt; tag to the HTML of the current HTTP response.%%This method has no effect in Ajax Requests. |
| [GetCookie](httprequesthandler-api.md#GetCookie%3E) | Gets a cookie value. |
| [GetEntryURL](httprequesthandler-api.md#GetEntryURL%3E) | Returns the URL of an Entry. Includes the Personal Area and the session identifier if applicable. |
| [GetFormValue](httprequesthandler-api.md#GetFormValue%3E) | Gets the value of a form field of the current HTTP request.%%If the field does not exist in the request an empty String will be returned. The same applies when the field exists but has an empty string as a value. |
| [GetIP](httprequesthandler-api.md#GetIP%3E) | Gets the IP host address of the remote client \(IP of the user machine performing the HTTP request\). |
| [GetPageExtension](httprequesthandler-api.md#GetPageExtension%3E) | Returns the extension of the physical page that corresponds to the current screen, including the dot. Examples: ".aspx" or ".jsf". |
| [GetPageName](httprequesthandler-api.md#GetPageName%3E) | Returns the name of the physical page that corresponds to the current screen. It is usually the same as the screen name, except when name clashes occur. |
| [GetRawURL](httprequesthandler-api.md#GetRawURL%3E) | Returns the current relative requested URL, without the [http://\[server](http://[server)\] part and without the session identifier.%%If SEO rules are being applied, the URL displayed in the user's browser is returned, and not the final URL after the rule is applied. |
| [GetReferrerURL](httprequesthandler-api.md#GetReferrerURL%3E) |  |
| [GetRequest\_AddArgument](httprequesthandler-api.md#GetRequest_AddArgument%3E) | Builds the arguments string for an HTTP request with method GET, adding a new parameter to the arguments string. |
| [GetRequest\_Submit](httprequesthandler-api.md#GetRequest_Submit%3E) | Submit an HTTP GET request given the GET arguments and the URL. Returns the response content as a string and as binary data. |
| [GetRequestContent](httprequesthandler-api.md#GetRequestContent%3E) | Gets the content of the current HTTP request. |
| [GetRequestDomain](httprequesthandler-api.md#GetRequestDomain%3E) | Returns the host part of the current HTTP request as seen by the browser.%%Example: when the browser uses the address "[http://support.domain.com/site/welcome.aspx?id=12345&quot](http://support.domain.com/site/welcome.aspx?id=12345&quot);, GetRequestDomain\(\) returns "support.domain.com". |
| [GetRequestFiles](httprequesthandler-api.md#GetRequestFiles%3E) | Returns the list of files submitted in the current HTTP request. |
| [GetRequestHeader](httprequesthandler-api.md#GetRequestHeader%3E) | Gets the value of a specific header in the current HTTP request. Returns an empty string if the header is not present or has no value. |
| [GetRunningESpaceJQueryVersion](httprequesthandler-api.md#GetRunningESpaceJQueryVersion%3E) | Returns the jQueryVersion of the Running ESpace |
| [GetSessionId](httprequesthandler-api.md#GetSessionId%3E) | Gets the session identifier of the current HTTP request. |
| [GetURL](httprequesthandler-api.md#GetURL%3E) | Returns the current absolute requested URL, without the session identifier.%%If SEO rules are being applied, the final URL after the rule is applied is returned, and not the URL displayed in the user's browser. |
| [GetURLMethod](httprequesthandler-api.md#GetURLMethod%3E) | Gets the request method \(GET or POST\) of the current requested URL. |
| [GetURLWithSession](httprequesthandler-api.md#GetURLWithSession%3E) | Gets the current requested URL \(with the session identifier\). |
| [GetUserAgent](httprequesthandler-api.md#GetUserAgent%3E) | Gets the user agent of the current HTTP request. |
| [GetUserLanguages](httprequesthandler-api.md#GetUserLanguages%3E) | Gets a sorted record list of client language preferences. |
| [GetValueFromInputId](httprequesthandler-api.md#GetValueFromInputId%3E) |  |
| [GetValueFromInputIdDecoded](httprequesthandler-api.md#GetValueFromInputIdDecoded%3E) |  |
| [IsAjaxRequest](httprequesthandler-api.md#IsAjaxRequest%3E) | Returns true if this is running in an AJAX request.%%Not Implemented in Java. |
| [IsSecureConnection](httprequesthandler-api.md#IsSecureConnection%3E) | Tells if the current request is being made via HTTPS. |
| [MakeAbsoluteURL](httprequesthandler-api.md#MakeAbsoluteURL%3E) | Makes an absolute URL based on the URL provided. |
| [PostRequest\_AddArgument](httprequesthandler-api.md#PostRequest_AddArgument%3E) | Builds arguments list for a POST HTTP request, adding a new text parameter to the arguments list. If argument name is not supplied, the post will only submit the supplied value \(this can be used for xml posts for example\). |
| [PostRequest\_AddBinaryArgument](httprequesthandler-api.md#PostRequest_AddBinaryArgument%3E) | Builds arguments list for an HTTP request, adding a new binary parameter to the arguments list. If argument name is not supplied, the post will only submit the supplied value \(this can be used for xml posts for example\). |
| [PostRequest\_Submit](httprequesthandler-api.md#PostRequest_Submit%3E) | Submit an HTTP POST request given the POST arguments and the URL. Returns the response content as a string and as binary data. |
| [ReplaceURLDomain](httprequesthandler-api.md#ReplaceURLDomain%3E) | Replaces the domain in the URL by the new domain. This function doesn't accept JavaScript as an URL. If the new domain is not provided, the domain of the current request is used. |
| [RunJavaScript](httprequesthandler-api.md#RunJavaScript%3E) | Runs the provided JavaScript code in the browser. |
| [SetBaseTag](httprequesthandler-api.md#SetBaseTag%3E) | Sets the base tag of the HTML of the current HTTP response.%%This method has no effect in Ajax Requests. |
| [SetCookie](httprequesthandler-api.md#SetCookie%3E) | Sets a cookie. |
| [SetLastModified](httprequesthandler-api.md#SetLastModified%3E) | Sets the Last Modified Date HTTP header of the current response. |
| [SetPageTitle](httprequesthandler-api.md#SetPageTitle%3E) | Sets the page title of the HTML of the current HTTP response.%%This method has no effect in Ajax Requests. |
| [SetRequestTimeout](httprequesthandler-api.md#SetRequestTimeout%3E) | Sets the timeout of the current HTTP request. |
| [SetStatusCode](httprequesthandler-api.md#SetStatusCode%3E) | Sets the status code of the current HTTP response. |
| [URLEncode](httprequesthandler-api.md#URLEncode%3E) | Encodes a URL string for reliable HTTP transmission from the Web server to a client |

| Structure | Description |
| :--- | :--- |
| [RequestFile](httprequesthandler-api.md#Structure_RequestFile%3E) |  |
| [UserLanguage](httprequesthandler-api.md#Structure_UserLanguage%3E) |  |

## Actions

### AddAttributeToHtmlTag { \#AddAttributeToHtmlTag }

Adds an attribute to the outermost HTML tag of the document \(e.g. xmlns, manifest...\).  
This method has no effect in Ajax Requests.

_Inputs_

Name : Type: Text. Mandatory.

Value : Type: Text. Mandatory.

### AddFaviconTag { \#AddFaviconTag }

Allows setting the favicon for the current page. You can use "omlresources" to add an icon file to your oml.  
This method has no effect in Ajax Requests.

_Inputs_

IconFilename : Type: Text. Mandatory.  
The filename of the icon, e.g. "outsystems.ico".

MimeType : Type: Text. Default: "image/x-icon".  
The mime type of the icon file. By default this is "image/x-icon".

### AddHeader { \#AddHeader }

Adds a header to the current HTTP response.  
This method has no effect in Ajax Requests.

_Inputs_

Name : Type: Text. Mandatory.  
Name of the header.

Value : Type: Text. Mandatory.  
Value of the header.

### AddJavaScriptTag { \#AddJavaScriptTag }

Adds a &lt;script&gt; tag to the HTML of the current HTTP response.  
This method has no effect in Ajax Requests.

_Inputs_

JavaScriptURL : Type: Text. Mandatory.  
The URL of the JavaScript file.

Defer : Type: Boolean. Default: False.  
Defines if the defer attribute is added to the &lt;script&gt; tag. Defaults to False.

Charset : Type: Text. Default: "UTF-8".  
The charset attribute of the &lt;script&gt; tag. Defaults to UTF-8.

### AddLinkTag { \#AddLinkTag }

Adds a &lt;link&gt; tag to the HTML of the current HTTP response.  
This method has no effect in Ajax Requests.

_Inputs_

Rel : Type: Text. Mandatory.

Href : Type: Text. Mandatory.

Type : Type: Text.

### AddMetaHttpEquivTag { \#AddMetaHttpEquivTag }

Adds a &lt;meta&gt; tag with the http-equiv attribute to the HTML of the current HTTP response.  
This method has no effect in Ajax Requests.

_Inputs_

HttpEquiv : Type: Text. Mandatory.

Content : Type: Text. Mandatory.

### AddMetaTag { \#AddMetaTag }

Adds a &lt;meta&gt; tag to the HTML of the current HTTP response.  
This method has no effect in Ajax Requests.

_Inputs_

Name : Type: Text. Mandatory.

Content : Type: Text. Mandatory.

### AddPostProcessingFilter { \#AddPostProcessingFilter }

This method has no effect in Ajax Requests.  
Not implemented in Java.

_Inputs_

matchingRegexp : Type: Text. Mandatory.

replacement : Type: Text. Mandatory.

### AddSessionToURL { \#AddSessionToURL }

Adds the current session identifier to a specified URL.

_Inputs_

URL : Type: Text. Mandatory.  
URL without session id.

_Outputs_

URLWithSession : Type: Text.  
URL with session id.

### AddStyleSheetTag { \#AddStyleSheetTag }

Adds a &lt;link rel="stylesheet"&gt; tag to the HTML of the current HTTP response.  
This method has no effect in Ajax Requests.

_Inputs_

StyleSheetURL : Type: Text. Mandatory.  
The URL of the CSS file.

Charset : Type: Text. Default: "UTF-8".  
The charset attribute of the &lt;script&gt; tag. Defaults to UTF-8.

### GetCookie { \#GetCookie }

Gets a cookie value.

_Inputs_

CookieName : Type: Text. Mandatory.  
Cookie name.

_Outputs_

CookieValue : Type: Text.  
Value for the specified cookie.

### GetEntryURL { \#GetEntryURL }

Returns the URL of an Entry. Includes the Personal Area and the session identifier if applicable.

_Inputs_

EntryName : Type: Text. Mandatory.  
Name of the Entry.

eSpaceName : Type: Text.  
Name of the eSpace. If not specified, assumes the current eSpace and gives a relative URL.

FirstParameterName : Type: Text.  
First parameter name.

FirstParameterValue : Type: Text.  
First parameter value.

SecondParameterName : Type: Text.  
Second parameter name.

SecondParameterValue : Type: Text.  
Second parameter value.

ThirdParameterName : Type: Text.  
Third parameter name.

ThirdParameterValue : Type: Text.  
Third parameter value.

FourthParameterName : Type: Text.  
Fourth parameter name.

FourthParameterValue : Type: Text.  
Fourth parameter value.

FifthParameterName : Type: Text.  
Fifth parameter name.

FifthParameterValue : Type: Text.  
Fifth parameter value.

_Outputs_

URL : Type: Text.  
URL of the Entry.

### GetFormValue { \#GetFormValue }

Gets the value of a form field of the current HTTP request.  
If the field does not exist in the request an empty String will be returned. The same applies when the field exists but has an empty string as a value.

_Inputs_

Name : Type: Text. Mandatory.

_Outputs_

Value : Type: Text.

### GetIP { \#GetIP }

Gets the IP host address of the remote client \(IP of the user machine performing the HTTP request\).

_Outputs_

UserIP : Type: Text.  
IP of the user machine performing the HTTP request.

### GetPageExtension { \#GetPageExtension }

Returns the extension of the physical page that corresponds to the current screen, including the dot. Examples: ".aspx" or ".jsf".

_Outputs_

PageExtension : Type: Text.  
Extension of the physical page that corresponds to the current screen.

### GetPageName { \#GetPageName }

Returns the name of the physical page that corresponds to the current screen. It is usually the same as the screen name, except when name clashes occur.

_Outputs_

PageName : Type: Text.  
Name of the physical page that corresponds to the current screen.

### GetRawURL { \#GetRawURL }

Returns the current relative requested URL, without the [http://\[server](http://[server)\] part and without the session identifier.  
If SEO rules are being applied, the URL displayed in the user's browser is returned, and not the final URL after the rule is applied.

_Outputs_

RawURL : Type: Text.

### GetReferrerURL { \#GetReferrerURL }

_Outputs_

ReferrerURL : Type: Text.

### GetRequest\_AddArgument { \#GetRequest\_AddArgument }

Builds the arguments string for an HTTP request with method GET, adding a new parameter to the arguments string.

_Inputs_

ArgumentsIn : Type: Text.  
Current arguments string.

Name : Type: Text. Mandatory.  
New argument name.

Value : Type: Text. Mandatory.  
New argument value.

_Outputs_

ArgumentsOut : Type: Text.  
Inputed arguments string concatenated with the pair &lt;argument name&gt; = &lt;argument value&gt;.

### GetRequest\_Submit { \#GetRequest\_Submit }

Submit an HTTP GET request given the GET arguments and the URL. Returns the response content as a string and as binary data.

_Inputs_

URL : Type: Text. Mandatory.  
URL for which to create the GET HTTP request.  
Ex: "[http://mydomain.com/hello/test.aspx&quot](http://mydomain.com/hello/test.aspx&quot);

Arguments : Type: Text. Mandatory.  
GET arguments string.  
Ex: "param1=valueOne&param2=valueTwo"

Timeout : Type: Integer.  
Number of milliseconds to wait before the request times out.

KeepAlive : Type: Boolean.  
Indicates whether to make a persistent connection \(True\) to the Internet resource or not \(False\).

_Outputs_

TextContent : Type: Text.  
Response text content.

BinaryContent : Type: BinaryData.  
Response binary content.

BinaryContentType : Type: Text.  
Value of the Content-Type header returned with the response.

### GetRequestContent { \#GetRequestContent }

Gets the content of the current HTTP request.

_Inputs_

IncludeHeaders : Type: Boolean. Default: True.  
Defines if the headers are included. Defaults to True.

_Outputs_

RawContent : Type: Text.  
The content of the current HTTP request.

### GetRequestDomain { \#GetRequestDomain }

Returns the host part of the current HTTP request as seen by the browser.  
Example: when the browser uses the address "[http://support.domain.com/site/welcome.aspx?id=12345&quot](http://support.domain.com/site/welcome.aspx?id=12345&quot);, GetRequestDomain\(\) returns "support.domain.com".

_Outputs_

Domain : Type: Text.  
The domain of the current HTTP request.

### GetRequestFiles { \#GetRequestFiles }

Returns the list of files submitted in the current HTTP request.

_Outputs_

RequestFiles : Type: RecordList of [RequestFile](httprequesthandler-api.md#Structure_RequestFile%3E).

### GetRequestHeader { \#GetRequestHeader }

Gets the value of a specific header in the current HTTP request. Returns an empty string if the header is not present or has no value.

_Inputs_

HeaderName : Type: Text. Mandatory.  
The name of the header

_Outputs_

Value : Type: Text.  
Returns an empty string if the header is not present or has no value.

### GetRunningESpaceJQueryVersion { \#GetRunningESpaceJQueryVersion }

Returns the jQueryVersion of the Running ESpace

_Outputs_

JQueryVersion : Type: Text.

### GetSessionId { \#GetSessionId }

Gets the session identifier of the current HTTP request.

_Outputs_

SessionId : Type: Text.  
Session identifier.

### GetURL { \#GetURL }

Returns the current absolute requested URL, without the session identifier.  
If SEO rules are being applied, the final URL after the rule is applied is returned, and not the URL displayed in the user's browser.

_Outputs_

URL : Type: Text.  
Current requested URL.

### GetURLMethod { \#GetURLMethod }

Gets the request method \(GET or POST\) of the current requested URL.

_Outputs_

Method : Type: Text.  
Current request method \(GETor POST\).

### GetURLWithSession { \#GetURLWithSession }

Gets the current requested URL \(with the session identifier\).

_Outputs_

URL : Type: Text.  
Current requested URL with the session identifier.

### GetUserAgent { \#GetUserAgent }

Gets the user agent of the current HTTP request.

_Outputs_

UserAgent : Type: Text.

### GetUserLanguages { \#GetUserLanguages }

Gets a sorted record list of client language preferences.

_Outputs_

Languages : Type: RecordList of [UserLanguage](httprequesthandler-api.md#Structure_UserLanguage%3E).  
Sorted record list of client language preferences.

### GetValueFromInputId { \#GetValueFromInputId }

_Inputs_

InputId : Type: Text. Mandatory.

_Outputs_

Value : Type: Text.

### GetValueFromInputIdDecoded { \#GetValueFromInputIdDecoded }

_Inputs_

InputId : Type: Text. Mandatory.

_Outputs_

Value : Type: Text.

### IsAjaxRequest { \#IsAjaxRequest }

Returns true if this is running in an AJAX request.  
Not Implemented in Java.

_Outputs_

IsAjaxRequest : Type: Boolean.  
Returns true if this is running in an AJAX request.

### IsSecureConnection { \#IsSecureConnection }

Tells if the current request is being made via HTTPS.

_Outputs_

IsSecureConnection : Type: Boolean.

### MakeAbsoluteURL { \#MakeAbsoluteURL }

Makes an absolute URL based on the URL provided.

_Inputs_

URL : Type: Text. Mandatory.  
Relative or absolute URL.

_Outputs_

AbsoluteURL : Type: Text.  
Absolute URL.

### PostRequest\_AddArgument { \#PostRequest\_AddArgument }

Builds arguments list for a POST HTTP request, adding a new text parameter to the arguments list. If argument name is not supplied, the post will only submit the supplied value \(this can be used for xml posts for example\).

_Inputs_

ArgumentsIn : Type: BinaryData.  
Current arguments list in Binary format.

Name : Type: Text.  
New text argument name.

Value : Type: Text. Mandatory.  
New text argument value.

_Outputs_

ArgumentsOut : Type: BinaryData.  
Inputed arguments list concatenated with the pair &lt;argument name&gt; = &lt;argument value&gt; in binary format.

### PostRequest\_AddBinaryArgument { \#PostRequest\_AddBinaryArgument }

Builds arguments list for an HTTP request, adding a new binary parameter to the arguments list. If argument name is not supplied, the post will only submit the supplied value \(this can be used for xml posts for example\).

_Inputs_

ArgumentsIn : Type: BinaryData.  
Current arguments list in Binary format.

Name : Type: Text.  
New text argument name.

Value : Type: BinaryData. Mandatory.  
New binary argument value.

_Outputs_

ArgumentsOut : Type: BinaryData.  
Inputed arguments list concatenated with the pair &lt;argument name&gt; = &lt;argument value&gt; in binary format.

### PostRequest\_Submit { \#PostRequest\_Submit }

Submit an HTTP POST request given the POST arguments and the URL. Returns the response content as a string and as binary data.

_Inputs_

URL : Type: Text. Mandatory.  
URL for which to create the GET HTTP request.

Arguments : Type: BinaryData.  
POST arguments.

Timeout : Type: Integer.  
Number of milliseconds to wait before the request times out.

KeepAlive : Type: Boolean.  
Indicates whether to make a persistent connection \(True\) to the Internet resource or not \(False\).

_Outputs_

TextContent : Type: Text.  
Response text content.

BinaryContent : Type: BinaryData.  
Response binary content.

BinaryContentType : Type: Text.  
Value of the Content-Type header returned with the response.

### ReplaceURLDomain { \#ReplaceURLDomain }

Replaces the domain in the URL by the new domain. This function doesn't accept JavaScript as an URL. If the new domain is not provided, the domain of the current request is used.

_Inputs_

URL : Type: Text. Mandatory.  
The URL to replace the domain

Domain : Type: Text.  
The new domain to put in the URL.

_Outputs_

SafeURL : Type: Text.  
The URL with the new domain.

### RunJavaScript { \#RunJavaScript }

Runs the provided JavaScript code in the browser.

_Inputs_

Script : Type: Text. Mandatory.  
JavaScript code to be sent to the browser.

### SetBaseTag { \#SetBaseTag }

Sets the base tag of the HTML of the current HTTP response.  
This method has no effect in Ajax Requests.

_Inputs_

HREF : Type: Text. Mandatory.

Target : Type: Text. Default: "".

### SetCookie { \#SetCookie }

Sets a cookie.

_Inputs_

CookieName : Type: Text. Mandatory.  
Cookie name.

CookieValue : Type: Text.  
Cookie value.

CookieExpirationSpan : Type: Integer.  
Cookie expiration span in minutes. If lower than or equal to zero the cookie will only be valid during current session.

CookiePath : Type: Text.  
Cookie path. Defaults to path of the current eSpace, Tenant and Personal Area combination.

CookieDomain : Type: Text.  
Cookie domain. Defaults to the current domain.

### SetLastModified { \#SetLastModified }

Sets the Last Modified Date HTTP header of the current response.

_Inputs_

LastModifiedDate : Type: DateTime. Mandatory.  
Last Modified Date.

### SetPageTitle { \#SetPageTitle }

Sets the page title of the HTML of the current HTTP response.  
This method has no effect in Ajax Requests.

_Inputs_

Title : Type: Text. Mandatory.

### SetRequestTimeout { \#SetRequestTimeout }

Sets the timeout of the current HTTP request.

_Inputs_

Timeout : Type: Integer. Mandatory.  
Timeout in seconds, or -1 for an infinite timeout.

### SetStatusCode { \#SetStatusCode }

Sets the status code of the current HTTP response.  
Note: Setting custom HTTP status codes is an advanced extensibility scenario, so be sure to test if it works as intended in your specific infrastructure \(for example, HTTP status code 204 is known to cause issues\). Check the list of standard HTTP status codes used in OutSystems.

_Inputs_

StatusCode : Type: Integer. Mandatory.  
Status code of the response. Examples: 404, 403.

### URLEncode { \#URLEncode }

Encodes a URL string for reliable HTTP transmission from the Web server to a client

_Inputs_

StrIn : Type: Text. Mandatory.  
String URL

Encoding : Type: Text.  
Encoding type: ASCII, Unicode, UTF7 or UTF8

_Outputs_

StrOut : Type: Text.  
Encoded string URL

## Structures

### RequestFile { \#Structure\_RequestFile }

_Attributes_

FileName : Type: Text \(50\). Mandatory.

FileType : Type: Text \(50\). Mandatory.

FileSize : Type: Integer. Mandatory.

BinaryContent : Type: BinaryData. Mandatory.

### UserLanguage { \#Structure\_UserLanguage }

_Attributes_

Value : Type: Text \(50\). Mandatory.

