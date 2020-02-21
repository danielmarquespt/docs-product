---
summary: >-
  Learn more about persistent login, to enable end-users not having to log in
  every time after their first successful login.
tags: support-Mobile_Apps; support-webapps
---

# Persistent Login

When authenticating the end-users, you can choose to use a persistent login. After logging in for the first time in the application the end-user will not have to provide the credentials again, unless:

* The end-user explicitly logs out through the [User\_Logout](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/users-api.final.md#User_Logout%3E) action.
* The persistent login times out because the end-user does not access the application for a certain amount of days.

In Web Applications persistent login will only work if the end-user has enabled the use of cookies in the browser. It keeps independent sessions in different browsers allowing end-users to have different persistent login sessions for the same application in different browsers and devices.

To use persistent login the `RememberLogin` input from the [User\_Login](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/auto/users-api.final.md#User_Login%3E) action has to be set to `True`.

The default duration of a persistent login session is 10 days in Traditional Web apps, and 30 days in Reactive Web and Mobile apps.  
For Traditional Web apps you can customize this duration by using the supported Forge Component [Factory Configuration](https://www.outsystems.com/forge/component/25/factory-configuration/) and changing the `Remember Login(days)` parameter in the Platform Configurations Tab.  
For Reactive and Mobile apps you can customize this duration in Service Center by [changing the `Max Idle Time` parameter](../../../../managing-the-applications-lifecycle/secure-the-applications/configure-authentication.md#configure-app-authentication-settings%3E) for persistent authentication.

For example, when you create a mobile application that uses one of the built-in [Application Templates](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/application-templates/intro.md%3E) for mobile apps \(Phone, Tablet or Universal\) the use of persistent login is the default.

![](../../../../../.gitbook/assets/userlogin-remember.png)

