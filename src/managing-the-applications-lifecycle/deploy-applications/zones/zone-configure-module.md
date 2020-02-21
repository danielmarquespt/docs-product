---
summary: >-
  Check how to configure an application or a module or in Service Center to use
  a specific deployment zone.
---

# Configure an Application or Module to Use a Deployment Zone

 Only available in OutSystems on-premises installations.

After creating a new deployment zone and associating one or more front-end servers to it, you can configure **applications** or **modules** to be deployed to this deployment zone.

Note that if a deployment zone is configured with a [container-based hosting technology](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/containers/intro.md%3E), you will only be able to configure the deployment zone for an entire application and not for its individual modules, since the deployment unit for containers is the application.

## Configure an Application

To configure an **application** to use a given deployment zone do the following:

1. Go to the Service Center management console of your OutSystems environment.
2. Go to the Factory section and select the Applications tab.
3. Click the name of the application that you will be deploying to the new deployment zone.
4. In the Operation tab, select the desired zone in the "Deployment Zone" field.
5. Click the "Save" button.

If the new deployment zone is configured with "Classic Virtual Machines" hosting technology, after applying this change the module will be automatically deployed to the front-end servers that are included in the deployment zone and removed from all front-end servers that don't belong to the deployment zone.

If the new deployment zone is configured with a container-based hosting technology, you need to republish your application for the changes to take effect.

## Configure a Module

To configure a **module** to use a given deployment zone do the following:

1. Go to the Service Center management console of your OutSystems environment.
2. Go to the Factory section and select the eSpaces tab.
3. Click the name of the module that you will be deploying to the new zone.
4. In the Operation tab, select the desired zone in the "Zone" field.
5. Click the "Apply" button.

After applying this change the module will be automatically deployed to the front-end servers that are included in the deployment zone and removed from all front-end servers that don't belong to the deployment zone.

