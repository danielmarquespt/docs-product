---
summary: Learn more about Integrated Windows Authentication in OutSystems.
tags: support-Mobile_Apps; support-webapps
---

# Integrated Authentication

OutSystems natively supports Integrated Windows Authentication so you can use a centralized management of the end-users and have automatic authentication in your applications. Integrated authentication allows the end-users to access applications using their domain credentials.

When the end-user tries to access a web screen that requires authentication, the application server returns an HTTP 401 status, signaling that the end-user is trying to access a resource that requires authentication. The browser then sends the credentials the end-user used to authenticate in the Windows operating system, or if unable to do so, prompts the end-user to provide the credentials. From then on, the browser automatically sends the credentials when they are required, without the end-user having to insert the domain credentials again.

## Elements that Support Integrated Authentication

You can [enable integrated authentication for all applications](configure-active-directory.md) or for specific elements inside an application. Enable Integrated Authentication for specific elements by setting their `Integrated Authentication` property to `Yes`.

The elements that support Integrated Authentication are the following.

Web Screens : The end-users accessing it will have to be authenticated by Integrated Authentication.

Web Flows : All screens that don't have set the `Integrated Authentication` property inherit its value form the web flow.

Exposed and Consumed SOAP Web Services : For exposed Web Services, the OutSystems application always asks the web service client for its credentials while processing the request. Note that, depending on the client that invokes the SOAP Web Service, it may not be possible to send the credentials and to consume its services.  
For consumed Web Services, OutSystems sends its credentials to the Web Service server. Note that delegation is not supported if your system is configured to use NTLM when you invoke a Web Service inside a web screen.

Tip: If you need to support Integration Windows Authentication in an exposed REST API you can do it by [implementing your own custom logic](../../../../extensibility-and-integration/rest/expose-rest-apis/add-custom-authentication-to-an-exposed-rest-api.md).

## Integrated Authentication Built-in Actions

OutSystems has built-in actions and functions that use Integrated Windows Authentication.

* [IntegratedSecurityGetDetails](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#IntegratedSecurityGetDetails%3E): Gets information about the current Windows user.
* [IntegratedSecurityCheckRole](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/system-actions.final.md#IntegratedSecurityCheckRole%3E): Checks whether the current Windows user has access to a specific Windows role.

## Remarks

To use integrated authentication, both the client and front-end server must be in the same domain and must have an Active Directory that stores information about the end-users and their credentials.

