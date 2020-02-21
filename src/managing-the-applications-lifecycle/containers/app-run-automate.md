---
summary: >-
  Basic instructions on how to automate application deployment to containers
  using an automatic deployment tool.
tags: support-Application_Lifecycle
---

# Deploy an Application to Containers using an Automated Deployment Tool

 \*\*Before you start\*\*, make sure that: \* You know the \[limitations, network architecture and requirements\]\(\) of running an OutSystems application in a container; \* You have read \[the manual deployment process\]\(\) for the targeted container hosting technology before proceeding with the automated deployment tool.

You can use an automated deployment tool, namely a CI/CD \(Continuous Integration/Continuous Delivery\) platform like Jenkins, to deploy your application to a container.

The automated deployment tool should fulfill these requirements:

* Trigger URL handlers defined in the automated deployment tool are able to respond to HTTP "GET" requests;
* Each trigger URL handler must provide a synchronous 2xx OK response to OutSystems as soon as possible, stating that the task has started;
* Each automation job must create the expected result file at the end of the corresponding task \(a file with a `.preparedone`, `.deploydone`, `.configsdone` or `.undeploydone` extension\), stating that the task was completed. 

To configure automated application deployment for a given deployment zone in OutSystems 11, follow these steps:

1. Define different jobs in your automated deployment tool of choice to handle all the different steps of OutSystems application deployment: "Preparing Deploy", "Deploying", "Update Configs" and "Undeploy";
2. Configure the deployment zone of your container-bound application to "Automatic Deployment" mode;
3. Configure the job execution trigger URLs that will handle all the different application deployment steps. 

The following diagram displays an overview of the actions involved in deploying an application through a CI/CD tool, both on the CI/CD tool side and on OutSystems side.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/containers/images/containers-automated-deployment-steps.png?width=952%3E)

**Note:** The "Update Configs" and "Undeploy" steps were omitted for brevity. Check the [Automatic Deployment Fields](../deploy-applications/zones/reference.md#automatic-deployment-fields%3E) reference for more information on what actions should be taken on these steps.

When invoking the configured trigger URLs, OutSystems will **append** the following query string parameters to the URL with application deployment data:

* Address
* ApplicationName
* ApplicationKey
* OperationId
* TargetPath
* ResultPath
* ConfigPath
* ModuleNames

These parameter names are **reserved** for OutSystems use and cannot be included in the trigger URLs configured in the deployment zone \(they will be added to the final trigger URL by the platform at runtime\).

All the values of these **reserved** query string parameters will be **serialized in Base64 encoding**. All other query string values, set by the user in the deployment zone configuration, will be as defined.

The filename of the application bundle ZIP file created by the platform in "ResultPath" before invoking the "Preparing Deploy" trigger URL handler is defined in the following manner:

`<ApplicationKey>_<OperationId>.zip`

Check the [Automatic Deployment Fields](../deploy-applications/zones/reference.md#automatic-deployment-fields%3E) reference for more information on these parameters.

 Check "\[How to automate container deployment by using LifeTime API v2 and Jenkins\]\(\)" for a step-by-step description of how to automate the deployment of OutSystems applications to containers.

