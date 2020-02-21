---
summary: >-
  Specify a container-based deployment zone for an application when you are
  deploying it to a target environment for the first time in LifeTime.
---

# Deploy an Application to a Container

 Containers is a \[Technical Preview\]\(\).

You can specify the deployment zone of an application when you are deploying it to a target environment for the first time using LifeTime. This allows you to define the desired deployment zone, namely a containers deployment zone, for an application from the start, instead of having to deploy it to the default deployment zone first and then move it to a different deployment zone.

This option is only available when there is **more than one deployment zone** configured in the target environment and when the application is being deployed for the first time to the target environment.

To define the deployment zone for an application in LifeTime, do the following:

1. In LifeTime, follow the [usual procedure](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/deploy-an-application.md%3E) to deploy an application to a target environment up to the final deployment screen containing the "Deploy Now" button. You will need to: a\) Click the 'Deploy...' button between source and target environments; b\) Select the application to deploy; c\) Validate the deployment; d\) Click "Continue".
2. In the final deployment screen \(the one with the "Deploy Now" button\), click the "Change Deployment Settings" link for the desired application to change its deployment zone.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/lifetime-change-deployment-zone.png%3E)

3. Select the desired deployment zone in the pop-up window.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/lifetime-deployment-settings.png%3E)

4. Click the "Deploy Now" button.

To complete the deployment, follow the same steps presented in [Publish an Application to a Container](../containers/app-run.md#publish-an-application-to-a-container%3E) using Service Center from stage 2 onwards, taking into account the activity log messages presented in the LifeTime deployment progress screen.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/lifetime-deployment-log-messages.png%3E)

## Identifying applications deployed to containers

Applications that were deployed to a containers deployment zone will have a "Container" badge in LifeTime close to the version information, like in the following example:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/lifetime-containers-badge.png%3E)

