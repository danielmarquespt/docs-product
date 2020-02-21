---
summary: Exposing REST APIs in your OutSystems applications.
tags: support-application_development; support-Integrations_Extensions
---

# Expose REST APIs

OutSystems allows you to [expose methods using a REST API](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/rest/expose-rest-apis/expose-a-rest-api.md%3E). These methods can be organized under multiple REST APIs.

 If you want to \*\*consume\*\* a REST API, check \[Consume REST APIs\]\(../consume-rest-apis/intro.md\).

## REST API Method Flow

When a request to your REST API Method is received, OutSystems executes the following flow:

![](../../../../.gitbook/assets/diagram-rest-expose-method-flow.png)

1. **Security Validations:** After receiving the REST API Method request, OutSystems executes the security validations according to the settings in [REST API properties](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/ServiceStudio.Plugin.RESTService.RestService.final.md) **HTTP Security** and **Internal Access Only**. 
2. **OnRequest\(\):** OnRequest callback allows you to [run logic over the requests](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/rest/expose-rest-apis/preprocess-rest-api-requests.md%3E) after receiving them. 
3. **OnAuthentication\(\):** OnAuthentication callback allows you to add [basic authentication](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/rest/expose-rest-apis/add-basic-authentication-to-an-exposed-rest-api.md%3E) or [custom authentication](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/rest/expose-rest-apis/add-custom-authentication-to-an-exposed-rest-api.md%3E) to requests. 
4. **Parameters Deserialization and Validation:** Deserialization of the input parameters and validation of the data types, mandatory values, etc. 
5. **Execute Method:** Executes the action that implements the REST API Method. 
6. **Parameters Serialization:** Serialization of the output parameters to return in the response. 
7. **OnResponse\(\):** OnResponse callback allows you to [run logic over the responses](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/rest/expose-rest-apis/customize-rest-api-responses.md%3E) before sending them. It is always executed, even in an error situation. 

