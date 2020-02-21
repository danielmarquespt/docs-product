---
summary: >-
  How to send a specific HTTP Status Code in the response of an exposed REST API
  method.
tags: null
---

# Change the HTTP Status Code of a REST API

OutSystems uses [a set of built-in HTTP Status Codes](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/extensibility-and-integration/rest-apis/exposed-rest-api/built-in-http-status-codes.md%3E) in the Responses of your exposed REST API Methods.

However, there are situations where you might want to send a different HTTP Status Code. For example, when a record is successfully created, it's common to use the "201 Created" Status Code.

To set a different HTTP Status Code in the Response, do the following:

1. Go to **Manage Dependencies...** and add the [SetStatusCode](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/httprequesthandler-api.final.md#SetStatusCode%3E) action of the [HTTPRequestHandler](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/httprequesthandler-api.final.md%3E) extension. 
2. Use the [SetStatusCode](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/httprequesthandler-api.final.md#SetStatusCode%3E) action in your REST API Method or callback flow right before the end node. 
3. Set its "StatusCode" property to the desired status code. 

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/rest/expose-rest-apis/images/ss-rest-change-http-code.png?width=800)

