---
summary: Refactor your application by moving some modules to a new application.
---

# Refactor an Application

This topic describes how to refactor an application by moving some modules to a new application and, this way, split the original business logic into two different applications.

In this example, the modules that integrate with PayPal are going to be decoupled from the eCommerce application to be autonomous and widely used by other applications. This way, the PayPal extension and PayPalGateway modules are going to be moved to a new application, the one which will provide PayPal services to other applications.

## Refactor the Business Logic

Open the detail of the eCommerce application in Service Center and look for the implementation of PayPal integration which is already separated in the following modules: PaypalGateway and PayPal \(extension\).

![](../../../.gitbook/assets/refactor-an-application-1.png)

The refactoring of applications depends on how they are designed, but it usually starts with the following procedures:

1. Identify business logic that is to be used by other applications.
2. Create a new module in the application and move the business logic into it.
3. Change the logic of the original module to reference the logic now isolated in the new module.
4. The business logic is now isolated into a single module.
5. Repeat this procedure for more business logic that has to be refactored.

In the above procedure Service Center and its TrueChange feature assist you in refactoring by providing real-time analysis and guiding you through the process.

## Create a New Application

Once the business logic is isolated in new modules, i.e. separated from the rest of the business logic, you can move those new modules to a new application to attain an autonomous development cycle.

Create a new application as follows:

1. Open Service Studio and log into a development environment.
2. Click on the **New Application** button.
3. Change the application name to **PayPal Services** and save it.

## Move Modules to the New Application

Go back to the Applications screen and open the eCommerce application to list all its modules again.

Hover the mouse over the PayPalGateway, click on the ▼ button, click on the **Move to Another Application** option, and choose the PayPal Services application as your target application.

Follow the same procedure to move the PayPal extension to the PayPal Services application.

![](../../../.gitbook/assets/refactor-an-application-2.png)

## Deploy to Quality Assurance

With all PayPal modules isolated into the PayPal Services application, you can now propagate this refactoring to the other environments in your infrastructure by [deploying the PayPal Services application](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/deploy-an-application.md%3E) to those environments. For example, to propagate it to Quality Assurance do as follows:

1. Click on **Deploy...** button between 'Development' and 'Quality Assurance'.
2. Go to the PayPal Services application, hover over 'Do Nothing' and click on the suggested option: **Deploy 0.1**. Then, tap on **Validate Now**.
3. LifeTime now runs the impact analysis and confirms that the deployment plan is OK.
4. Click on the **Continue** button to check the deployment plan and run it. LifeTime will automatically synchronize the eCommerce application in the destination environment to remove the PayPalGateway module and the PayPal extension.

After the deployment is finished, the refactoring is done in the Quality Assurance environment.

![](../../../.gitbook/assets/refactor-an-application-3.png)

