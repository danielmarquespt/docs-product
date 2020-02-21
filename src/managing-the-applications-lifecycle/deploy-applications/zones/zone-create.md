---
summary: Learn how to create a new zone in Service Center.
---

# Create a New Deployment Zone

 Only available in OutSystems on-premises installations.

To create a new deployment zone do the following:

1. Go to the Service Center management console of your OutSystems environment.
2. Go to the **Administration** section and select the **Deployment Zones** tab.
3. Click the **New Deployment Zone** link.
4. Fill in the [basic parameters](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/zones/reference.md%3E) for the deployment zone, namely its name and Deployment Zone Address.
5. Click the **Create** button.

After creating the zone, define which front-end servers belong to it. Do the following:

1. In the input box under "Associate Servers to this Deployment Zone", type the front-end server names you wish to associate with the zone.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/zones/images/zone-add-front-end.png%3E)

   _Tip:_ The full name of the front-end server will appear as suggested text after you start typing it.

2. Click the **Add Server\(s\)** button to associate the entered front-end server names with the zone.

Note: Instead of defining the servers belonging to the deployment zone, you can check the "Includes all Servers" setting when creating the deployment zone. In this case, the platform will automatically include all servers in the deployment zone, including those added at a later date.

