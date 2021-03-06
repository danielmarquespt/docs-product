---
summary: >-
  Enables you to modify the SOAP connection, request and/or response message in
  an extension.
tags: support-application_development; support-Integrations_Extensions
---

# SOAP Extensibility API

 This API can only be used to extend and customize the behavior of consumed SOAP Web Services created in OutSystems 11. To customize consumed SOAP Web Services upgraded from previous versions you must use the \(deprecated\) \[EnhancedWebReferences API\]\(auto/enhancedwebreferences-api.final.md\).

The OutSystems SOAP Extensibility API enables you to modify the SOAP connection, request and/or response message using .NET code. It is automatically imported to your environment at installation.

To manipulate the connection, request and/or response message, create an extension module and use its methods in the On Before Request callback action of the consumed SOAP Web Service.  
Check how to [use the advanced SOAP extensibility in your application](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/soap/consume/advanced-extensibility.md%3E). This topic also contains examples of using the API for address common use cases.

 Note that, unlike the extensibility available for other integration types, the SOAP implementation provides \*\*a single extensibility point\*\* where you can perform all kinds of customizations: adjust the connection parameters, change the request message and adjust the response message.

The components described in this topic are available under the following .NET namespace:  
`OutSystems.SOAP.API`

## SoapRequest Class

This object provides access to the SOAP client object implementing the ISOAPClient interface, allows you to register new a runtime behavior callback and to get the SOAP method that invoked the extension.

### Methods

| Name | Description |
| :--- | :--- |
| static %%[ISOAPClient](soap-extensibility-api.md#isoapclient-interface%3E) GetCurrentClient\(\) | Returns the client used for the request. Should only be used inside the On Before Request callback, otherwise it returns `null`. |
| static void RegisterEndpointBehavior\([IEndpointBehavior](https://docs.microsoft.com/en-us/dotnet/api/system.servicemodel.description.iendpointbehavior?view=netframework-4.6.1>) behavior\) | Registers a callback to modify the request message or/and response message. |
| static string GetActionName\(\) | Returns the name of the SOAP method that invoked the extension. |

## ISOAPClient Interface

ISOAPClient is an OutSystems interface providing an abstraction over Windows Communication Foundation \(WCF\) client implementations that can be used to call web services.

### Properties

| Name | Type | Description |
| :--- | :--- | :--- |
| ClientCredentials | [ClientCredentials](https://docs.microsoft.com/en-us/dotnet/api/system.servicemodel.description.clientcredentials?view=netframework-4.6.1>)%%\(from WCF\) | Ready-only property that returns an object representing the client credentials used to call an operation. |
| Endpoint | [ServiceEndpoint](https://docs.microsoft.com/en-us/dotnet/api/system.servicemodel.description.serviceendpoint?view=netframework-4.6.1>)%%\(from WCF\) | Read-only property that returns the target endpoint for the service to which the WCF client can connect. |
| InnerChannel | [IClientChannel](https://docs.microsoft.com/en-us/dotnet/api/system.servicemodel.iclientchannel?view=netframework-4.6.1>)%%\(from WCF\) | Read-only property that returns the client channel for the WCF client object. |
| State | [CommunicationState](https://docs.microsoft.com/en-us/dotnet/api/system.servicemodel.communicationstate?view=netframework-4.6.1>)%%\(from WCF\) | Read-only property that returns the enum value of the current state of the System.ServiceModel.ClientBase object. |

### Methods

| Name | Description |
| :--- | :--- |
| [ChannelFactory](https://docs.microsoft.com/en-us/dotnet/api/system.servicemodel.channelfactory?view=netframework-4.6.1>) GetChannelFactory\(\) | Returns the inner channel used to send messages to variously configured service endpoints. |

