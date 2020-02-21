---
summary: Learn how to deploy one application from one environment to another.
tags: support-Application_Lifecycle-featured
---

# Deploy an Application

In LifeTime, deployment of an application's [tagged version](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/tag-a-version.md%3E) takes a version of the application from one environment and deploys it in another. Just select the tagged version of the application and LifeTime deploys it in the exact development state in which it was tagged.

Here's an example of deploying applications in LifeTime.

## Deploy a Web and a Mobile Application

In this example, two applications are being developed in the Development environment:

* A mobile app \(MyApp\)
* A web application \(MyWebApp\)

A milestone is reached and the applications are ready to be tested by Quality. They are [tagged](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/tag-a-version.md%3E) as follows:

* The mobile app is tagged with version 0.2
* The web application is tagged wih version 0.3

To deploy both applications to Quality, do the following:

1. Click the **Deploy...** button between Development and Quality.

   ![](../../../.gitbook/assets/deploy-an-application-1.png)

2. Choose **Add Applications** to select the applications to deploy. You can also **Add All Applications** to the deployment plan.

   ![](../../../.gitbook/assets/deploy-an-application-2.png)

3. If you chose **Add Applications** in the previous step, search for the applications to deploy. You can filter by applications with differences or search by the application name.

   ![](../../../.gitbook/assets/deploy-an-application-3.png)

4. Select the applications to deploy and click the **Add to Deployment Plan** button.

   ![](../../../.gitbook/assets/deploy-an-application-4.png)

5. In the deploy options, select **DEPLOY 0.2** for MyApp and **DEPLOY 0.3** for MyWebApp:

   ![](../../../.gitbook/assets/deploy-an-application-5.png)

6. Click **VALIDATE NOW** to validate the deployment in Quality:

   ![](../../../.gitbook/assets/deploy-an-application-6.png)

   Note: If LifeTime detects any changes in the applications included in the plan either in the source or in the target environment, it will show a **Refresh Applications** sticker that you can click to [refresh the applications](deploy-an-application.md#refresh) included in the plan.

7. The deploy is OK \(all green\). Click **CONTINUE** to move on:

   ![](../../../.gitbook/assets/deploy-an-application-7.png)

8. Type the Deployment Notes and click the **Deploy Now** button to execute the deployment:

   ![](../../../.gitbook/assets/deploy-an-application-8.png)

When the deployment finishes, both applications have the same tagged version in both environments.

![](../../../.gitbook/assets/deploy-an-application-9.png)

If the deployment **finishes successfully**, a "Reuse Plan" link appears in the deployment plan progress screen. You can [reuse a deployment plan](deployment-plans.md#reuse) to get faster deployments.

![](../../../.gitbook/assets/lt-reuse-plan-link.png)

If the deployment is **aborted**, a "Retry Plan" link appears in the deployment plan progress screen. [Retrying the plan](deployment-plans.md#retry) creates a copy of the original plan and allows you to customize it before running it again.

![](../../../.gitbook/assets/lt-retry-plan-link.png)

**Note:** If you're deploying a mobile app that is already [configured to generate the mobile app package](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/deliver-mobile/generate-and-distribute-your-mobile-app/intro.md%3E), be aware that some changes you do in your application might cause the generation of a new application package. For example, changing the icon or the main color of the application.  
[Check here](../../deliver-mobile/mobile-app-update-scenarios.md#situations-when-the-user-must-install-a-new-build) all the situations that require the user to install a new application package.

## Refresh Applications in the Deployment Plan { \#refresh }

After creating a deployment plan and adding applications to it, OutSystems notifies you if there are any relevant changes in the source or target environments related to the applications included in the plan.

The detected changes include:

* In the **source** environment, publishing/moving a module of an application included in the plan 
* In the **target** environment, publishing/moving **any** module of an application
* In the **source**/**target** environment, tagging a version of an application included in the plan 

When any of these changes is detected, a **Refresh Applications** sticker appears under the page title heading of the deployment plan creation screen:

![](../../../.gitbook/assets/lt-refresh-applications.png)

To refresh the applications in the current plan, click **Refresh Applications**.

The refresh operation does the following:

* The versions displayed in the deployment plan's source and target environments are updated.
* Applications with the "Tag & Deploy" option selected will be deployed with the most recent code.
* Any new tags created outside the plan are shown in the deployment options and can be selected for deployment.
* All deployment options previously selected are kept, except if they are no longer available.

