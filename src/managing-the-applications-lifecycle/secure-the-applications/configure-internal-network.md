---
summary: >-
  Configure the range of IP addresses that are considered part of your internal
  network.
tags: support-Security-overview
---

# Configure an Internal Network

OutSystems applications can set the access to specific elements \(Web UI Flows, exposed SOAP services, and exposed REST APIs\) to be available only within an internal network, while other parts of the application are kept available to the general public.

 Procedure applicable only to on-premises installations. For OutSystems PaaS subscriptions, contact OutSystems Technical Support.

To configure an internal network for your OutSystems environment, do the following:

1. Go to the Service Center management console of your OutSystems environment.
2. Go to the **Administration** section and select the **Security** tab.
3. Select the **Network Security** area.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/secure-the-applications/images/configure-internal-network-1.png?width=600)

4. Fill in the **Internal network addresses** field with the list of IP addresses or ranges from which you want to allow the access to the management consoles and the endpoints of your applications defined as Internal Access Only. Assure you include also the IP addresses/ranges of the controller, all front-end servers and monitoring tools.
5. Click the **Save** button.

Clicking Save will invalidate the Service Center cache. After checking the cache was invalidated, all the running applications in the environment will load the new settings.

When you define an internal network for a specific OutSystems environment, it will affect the access to the following tools:

* The Service Center console of the environment
* The LifeTime console of the environment, if the environment where the configuration was applied is a LifeTime environment
* Connections from Service Studio, Integration Studio and OSP Tool to the environment

In the case you inadvertently define an internal network configuration that blocks you from accessing Service Center, you can [use the Configuration Tool to clear the internal network settings](../../ref/configuration-tool/tabs/network.md) currently defined.

