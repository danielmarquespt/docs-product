---
summary: >-
  Enables you to access the content of requests and responses used by methods
  consumed from other REST APIs in .NET.
tags: support-application_development; support-Integrations_Extensions
---

# REST Extensibility API

The OutSystems REST Extensibility API enables you to access the content of requests and responses used by methods consumed from other REST APIs. It is automatically imported to your environment at installation.

To manipulate the request/response, create an extension module, and use its methods in the OnBeforeRequestAdvanced/OnAfterResponseAdvanced callback of the consumed REST API. [Learn more about how to customize the request/response](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/rest/consume-rest-apis/advanced-customizations.md%3E).

The components described in this topic are available under the following .NET namespace: `OutSystems.RuntimePublic.REST`

To see examples of how to use them, look for [modules that use REST APIs](https://www.outsystems.com/forge/list?q=REST%20API&t=&o=&tr=False&oss=False&c=&a=&v=11&hd=False&tn=&scat=forge) in the Components category of [OutSystems Forge](https://www.outsystems.com/forge/>).

## RestRequest Class

This object provides low-level access to the request objects used when executing methods of consumed REST APIs. To manipulate the request, create an extension module, and use its methods in the OnBeforeRequestAdvanced callback of the consumed REST API.

### Methods

| Name | Description |
| :--- | :--- |
| static %%RestRequest GetCurrent\(\) | Returns the request object used by methods consumed from REST APIs. Should only be used inside the OnBeforeRequestAdvanced callback, otherwise null is returned. %%Example: to obtain the instance of this class, use RestRequest.GetCurrent\(\) |
| string %%GetActionName\(\) | Returns the name of the method that invoked the extension. |
| HttpWebRequest %%GetHttpWebRequest\(\) | Returns the native HttpWebRequest object used to execute the web request. |
| byte\[\] %%GetRequestBodyAsBinary\(\) | Returns the message body of the web request as binary content. |
| string %%GetRequestBodyAsText\(\) | Returns the message body of the web request as a string. |
| void %%SetRequestBody\(byte\[\] bytes\) | Sets the message body of the web request with binary content. |
| void %%SetRequestBody\(string text\) | Sets the message body of the web request with text. If the method has its 'Request Format' property set to 'Binary', no changes are made to the message body. |

## RestResponse Class

This object provides low-level access to the response objects when executing OnAfterResponseAdvanced callback of the consumed REST API.

### Methods

| Name | Description |
| :--- | :--- |
| static %%RestResponse GetCurrent\(\) | Returns the response object used by methods consumed from REST APIs. Should only be used inside the OnAfterResponseAdvanced callback of a consumed REST API, otherwise null is returned. %%Example: to obtain the instance of this class, use RestResponse.GetCurrent\(\) |
| string %%GetActionName\(\) | Returns the name of the method that invoked the extension. |
| HttpWebResponse %%GetHttpWebResponse\(\) | Returns the native HttpWebResponse object that resulted from the web request. |
| byte\[\] %%GetResponseBodyAsBinary\(\) | Returns the message body of the web response as binary content. |
| string %%GetResponseBodyAsText\(\) | Returns the message body of the web response as a string, respecting the encoding specified in the Content-Type header. |
| void %%SetResponseBody\(byte\[\] bytes\) | Sets the message body of the web response with binary content. |
| void %%SetResponseBody\(string text\) | Sets the message body of the web response with text. If the method has its 'Response Format' property set to 'Binary', no changes are made to the message body. |

