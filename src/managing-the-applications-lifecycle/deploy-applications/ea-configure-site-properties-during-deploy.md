---
summary: >-
  This early access feature enables you to set application Site Properties in
  the target environment while performing a deployment in LifeTime.
tags: support-Application_Lifecycle-featured
---

# Early Access - Configure Site Properties During Deployment

 Read how \[early access to OutSystems features\]\(https://success.outsystems.com/Support/Enterprise\_Customers/Upgrading/Early\_access\_to\_OutSystems\_features\) works. We encourage you to try these features out and to \[send us your feedback\]\(https://www.outsystems.com/forums/discussion/48360/configure-site-properties-during-deployment/\#Post177757\).

This early access feature adds a new step during the deployment plan that enables the configuration of Site Properties in the target environment. With this feature disabled, when you deploy an application with a setting that must be different in the target environment, you need to use the Service Center console to [update it in the target environment after deployment](configure-application-settings-after-deployment.md).

![](../../../.gitbook/assets/configure-settings-during-deploy-1.gif)

 \*\*To use this feature, make sure that:\*\* \* The feature was \[activated in LifeTime\]\(https://success.outsystems.com/Support/Enterprise\_Customers/Upgrading/Early\_access\_to\_OutSystems\_features\). \* The \*\*source\*\* and \*\*target\*\* environments for the deployment are running Platform Server 11 Release Apr.2019 CP1 or later. \* The user executing the deployment has the "Change & Deploy Applications" permission for all applications in the deployment plan.

After activating the early access feature **Configure Site Properties during deployment**, a new deployment plan wizard will be used when deploying applications in LifeTime. This wizard has four steps:

1. Add the applications to deploy
2. Configure application settings
3. Review deployment plan
4. Execute deployment plan

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/configure-settings-during-deploy-2.png?width=800)

While you are already familiar with the other steps, during the step **Configure application settings** you can now configure the Site Properties of the applications being deployed, as described below.

## Configure application settings

After adding the applications to your deployment plan, you now have a new step to configure the settings of the applications being deployed. For now, it is possible to configure the following settings:

* The Site Properties of the application modules.

  ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/configure-site-settings-during-deploy-3.png?width=800)

* The [Deployment Zone](zones/intro.md) for the applications being deployed, when the target environment has more than one Deployment Zone.

  ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/configure-settings-during-deploy-4.png?width=800)

The deployment plan wizard includes this step when there are **new settings** to configure:

* There are applications in the plan with new Site Properties that were never set in the target environment. In this step, you can define the effective value for those Site Properties in the target environment.
* There are application modules using [Deployment Zones](zones/intro.md), and that application will be deployed to the target environment for the first time. In this step, you can choose the deployment zone to which your application will be deployed.

You can also see and change the existing settings of the applications to deploy. Click the button **All settings** to see the existing settings.

Select an application from the applications list to the left to see the settings for that application. If your deployment plan contains applications with no changes, you will not be able to change the settings for those applications.

There are some situations when this step is **skipped** or **disabled**:

* The step will be **skipped** when there are no new settings to configure. However, if you need to change any existing setting, you can manually go back to **Configure application settings** by clicking the step in the wizard.

  ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/configure-site-settings-during-deploy-4.png?width=800)

* The step will be **disabled** when there aren't any settings to configure or the user executing the deployment does not have the required permissions.

The Site Properties of the applications to deploy are set in the target environment after the applications are published. Beware of Timers that run `When Published`, since the Site Properties that the Timers may use are not yet updated when the Timers run.

This feature does not apply to multi-tenant Site Properties.

