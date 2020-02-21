# EnhancedWebReferences API

For Platform Version 9.0.99.11. API to dynamically change Web Service and Web Reference URLs, SOAP headers, credentials, and proxies.

## Summary

| Action | Description |
| :--- | :--- |
| [ClearWebReferenceHeaders](enhancedwebreferences-api.md#ClearWebReferenceHeaders%3E) | Use this action after a call to SetWebReferenceSoapHeaders to make a new Web Reference request without SOAP headers.%%NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.%%This only occurs in Consumer/Producer scenarios. |
| [GetWebReferenceSoapHeaders](enhancedwebreferences-api.md#GetWebReferenceSoapHeaders%3E) | Obtain the SOAP headers sent in the response of a Web Reference call. Use this action after invoking a Web Reference action.%%NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.%%This only occurs in Consumer/Producer scenarios. |
| [GetWebServiceSoapHeaders](enhancedwebreferences-api.md#GetWebServiceSoapHeaders%3E) | Gets the SOAP headers sent to the Web Service. Use this action inside the Web Service logic. |
| [SetWebReferenceCredencials](enhancedwebreferences-api.md#SetWebReferenceCredencials%3E) | Sets Web Reference HTTP credentials. The username can be used in the form of DOMAIN\USER.%%The HTTP credentials persist for the request duration: all Web Reference calls placed during the same request use the specified credentials.%%To invoke Web References in the same request without the credentials, use this action without specifying the Username and Password.%%NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.%%This only occurs in Consumer/Producer scenarios. |
| [SetWebReferenceProxy](enhancedwebreferences-api.md#SetWebReferenceProxy%3E) | Specifies a proxy through which a Web Reference action can be invoked.%%This action allows specifying the credentials to authenticate in the proxy. The specified proxy persists for the request duration: all Web Reference calls placed during the same request use that proxy.%%To invoke Web References in the same request using the default internet configurations, use this action without specifying the ProxyURL.%%NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.%%This only occurs in Consumer/Producer scenarios. |
| [SetWebReferenceSoapHeaders](enhancedwebreferences-api.md#SetWebReferenceSoapHeaders%3E) | Sets SOAP headers to be used in Web Reference calls.%%The SOAP headers persist for the request duration: all Web Reference calls placed during the same request use the specified headers.%%To invoke Web References in the same request without the SOAP headers, use the ClearWebReferenceHeaders action.%%NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.%%This only occurs in Consumer/Producer scenarios. |
| [SetWebReferenceURL](enhancedwebreferences-api.md#SetWebReferenceURL%3E) | Sets another effective URL for the Web Reference%%The specified URL persists for the request duration: all Web Reference calls placed during the same request use the URL.%%To invoke Web References in the same request using the default URL, use this action without specifying the URL.%%NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.%%This only occurs in Consumer/Producer scenarios. |
| [SetWebServiceSoapHeaders](enhancedwebreferences-api.md#SetWebServiceSoapHeaders%3E) | Sets the SOAP headers to be sent by the Web Service in the response. Use this action inside the Web Service Logic. |

| Structure | Description |
| :--- | :--- |
| [SOAPHeader](enhancedwebreferences-api.md#Structure_SOAPHeader%3E) |  |

## Actions

### ClearWebReferenceHeaders { \#ClearWebReferenceHeaders }

Use this action after a call to SetWebReferenceSoapHeaders to make a new Web Reference request without SOAP headers.

NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.  
This only occurs in Consumer/Producer scenarios.

_Inputs_

WebReferenceName : Type: Text. Mandatory.  
The Name of the WebReference In Service Studio.

### GetWebReferenceSoapHeaders { \#GetWebReferenceSoapHeaders }

Obtain the SOAP headers sent in the response of a Web Reference call. Use this action after invoking a Web Reference action.

NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.  
This only occurs in Consumer/Producer scenarios.

_Inputs_

WebReferenceName : Type: Text. Mandatory.  
The Name of the WebReference In Service Studio.

_Outputs_

SoapHeaders : Type: RecordList of [SOAPHeader](enhancedwebreferences-api.md#Structure_SOAPHeader%3E).  
Structure representing the SOAP headers.

### GetWebServiceSoapHeaders { \#GetWebServiceSoapHeaders }

Gets the SOAP headers sent to the Web Service. Use this action inside the Web Service logic.

_Outputs_

SoapHeaders : Type: RecordList of [SOAPHeader](enhancedwebreferences-api.md#Structure_SOAPHeader%3E).  
Structure representing the SOAP headers.

### SetWebReferenceCredencials { \#SetWebReferenceCredencials }

Sets Web Reference HTTP credentials. The username can be used in the form of DOMAIN\USER.  
The HTTP credentials persist for the request duration: all Web Reference calls placed during the same request use the specified credentials.  
To invoke Web References in the same request without the credentials, use this action without specifying the Username and Password.

NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.  
This only occurs in Consumer/Producer scenarios.

_Inputs_

WebReferenceName : Type: Text. Mandatory.  
The Name of the WebReference In Service Studio.

UserName : Type: Text. Mandatory.

Password : Type: Text. Mandatory.

### SetWebReferenceProxy { \#SetWebReferenceProxy }

Specifies a proxy through which a Web Reference action can be invoked.  
This action allows specifying the credentials to authenticate in the proxy. The specified proxy persists for the request duration: all Web Reference calls placed during the same request use that proxy.  
To invoke Web References in the same request using the default internet configurations, use this action without specifying the ProxyURL.

NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.  
This only occurs in Consumer/Producer scenarios.

_Inputs_

WebReferenceName : Type: Text. Mandatory.  
The Name of the WebReference In Service Studio.

ProxyURL : Type: Text. Mandatory.

ProxyUserName : Type: Text.

ProxyPassword : Type: Text.

### SetWebReferenceSoapHeaders { \#SetWebReferenceSoapHeaders }

Sets SOAP headers to be used in Web Reference calls.  
The SOAP headers persist for the request duration: all Web Reference calls placed during the same request use the specified headers.  
To invoke Web References in the same request without the SOAP headers, use the ClearWebReferenceHeaders action.

NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.  
This only occurs in Consumer/Producer scenarios.

_Inputs_

WebReferenceName : Type: Text. Mandatory.  
The Name of the WebReference In Service Studio.

SoapHeaders : Type: RecordList of [SOAPHeader](enhancedwebreferences-api.md#Structure_SOAPHeader%3E). Mandatory.  
Structure representing the SOAP headers.

### SetWebReferenceURL { \#SetWebReferenceURL }

Sets another effective URL for the Web Reference  
The specified URL persists for the request duration: all Web Reference calls placed during the same request use the URL.  
To invoke Web References in the same request using the default URL, use this action without specifying the URL.

NOTE: since this action receives the Web Reference name as a parameter, if two Web References have the same name both are affected by this action.  
This only occurs in Consumer/Producer scenarios.

_Inputs_

WebReferenceName : Type: Text. Mandatory.  
The Name of the WebReference In Service Studio.

URL : Type: Text. Mandatory.  
The URL of the new Web Reference to point to.  
The Web Reference in the specified URL must be compatible with the previous one.  
Generally this action is used to specify the same Web Reference as the original, made available in a different machine.

### SetWebServiceSoapHeaders { \#SetWebServiceSoapHeaders }

Sets the SOAP headers to be sent by the Web Service in the response. Use this action inside the Web Service Logic.

_Inputs_

SoapHeaders : Type: RecordList of [SOAPHeader](enhancedwebreferences-api.md#Structure_SOAPHeader%3E). Mandatory.  
Structure representing the SOAP headers.

## Structures

### SOAPHeader { \#Structure\_SOAPHeader }

_Attributes_

Actor : Type: Text \(500\).  
Recipient of the SOAP header.

DidUnderstand : Type: Boolean.  
A value indicating whether an XML Web service method properly processed a SOAP header.

Element : Type: Text \(500000\). Mandatory.  
XML Header element for a SOAP request or response.

EncodedMustUnderstand : Type: Text \(10\). Default: "0".  
Value of the mustUnderstand XML attribute for the SOAP header when communicating with SOAP protocol version 1.1. Valid values are 0, 1, true or false.

EncodedMustUnderstand12 : Type: Text \(10\). Default: "0".  
Value of the mustUnderstand XML attribute for the SOAP header when communicating with SOAP protocol version 1.2. Valid values are 0, 1, true or false.

EncodedRelay : Type: Text \(10\). Default: "0".  
Relay attribute of the SOAP 1.2 header. Valid values are 0, 1, true or false.

MustUnderstand : Type: Boolean.  
Value indicating whether the SoapHeader must be understood.

Relay : Type: Boolean.  
Value that indicates whether the SOAP header is to be relayed to the next SOAP node if the current node does not understand the header.

Role : Type: Text \(500\).  
Recipient of the SOAP header.

