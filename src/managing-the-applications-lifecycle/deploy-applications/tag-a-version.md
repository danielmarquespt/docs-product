---
summary: >-
  Learn how OutSystems allows you to take a snapshot of the application and its
  modules, tag it with a version, and then use it for deploying.
tags: support-Application_Lifecycle-featured
---

# Tag a Version

Tagging an application version in LifeTime means a snapshot is taken of the development state of the application and associates a version number to it. When [deploying the application](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/deploy-an-application.md%3E), just select the tagged version and LifeTime deploys the application in the exact development state in which it was tagged.

A typical situation of tagging an application is when it reaches a development milestone:

1. The application is tagged
2. The development continues
3. The tagged version of the application is deployed to another environment for tests

When tagging a mobile app, there is an extra section called Mobile Versions that allows tagging the mobile package. That operation is not frequently needed because the platform automatically updates the app without generating new packages. In some [update scenarios](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/deliver-mobile/mobile-app-update-scenarios.md%3E) new packages have to be tagged and generated.

Here's an example of tagging applications.

## Tag a Web and a Mobile Application

In this example, we have two applications in Development environment:

* A mobile app \(MyApp\)
* A web application \(MyWebApp\)

They have reached a development milestone and must be tagged.

![](../../../.gitbook/assets/tag-a-version-1.png)

The plus \('+'\) sign means the applications have changed since their last tag.

### Tag the Mobile App

To tag the mobile app, do the following:

1. Click on **MyApp** to show its details.

   ![](../../../.gitbook/assets/tag-a-version-2.png)

2. Click on **TAG VERSION**, set version to **0.2** and type a description. In the Mobile Versions section, there's no plus \('+'\) sign, meaning that the changes in the app don't make generating a new mobile package necessary. And so, there's no need to tag the package.

   ![](../../../.gitbook/assets/tag-a-version-3.png)

3. Click on **TAG VERSION** to finish.

   ![](../../../.gitbook/assets/tag-a-version-4.png)

### Tag the Web Application

To tag the web application, do the following:

1. Click on **MyWebApp** to show its details.

   ![](../../../.gitbook/assets/tag-a-version-5.png)

2. Click on **TAG VERSION**. For the application: set version to **0.3** and type a description.

   ![](../../../.gitbook/assets/tag-a-version-6.png)

3. Click on **TAG VERSION** to finish.

   ![](../../../.gitbook/assets/tag-a-version-7.png)

The applications are now tagged and can be [deployed](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/deploy-an-application.md%3E) to Quality at any time.

