---
summary: Customize the authentication logic used in your exposed REST APIs.
tags: null
---

# Add Custom Authentication to an Exposed REST API

OutSystems allows you to customize the authentication logic to be used in your exposed REST APIs.

For that, do the following:

1. In the **Logic** tab, open the **Integrations** folder.
2. Select the exposed REST API you want to change and set its "Authentication" property to `Custom`.

   ![](../../../../.gitbook/assets/ss-rest-authentication-options.png)

   As a result, OutSystems creates the "OnAuthentication" action in your REST API, which will be executed for every incoming request of this REST API, before the called method's action flow.

   ![](../../../../.gitbook/assets/ss-rest-onauthentication-custom-flow.png)

3. In the "OnAuthentication" action, design the logic to authenticate the client. If you need to access data received in the URL, header or body of the HTTP request, you can use the [GetFormValue](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/httprequesthandler-api.final.md#GetFormValue), [GetRequestHeader](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/httprequesthandler-api.final.md#GetRequestHeader) or [GetRequestContent](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/httprequesthandler-api.final.md#GetRequestContent) actions of the [HTTPRequestHandler](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/httprequesthandler-api.final.md) extension.

