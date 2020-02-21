---
summary: >-
  Learn how to allow developers in the team to create integrations with external
  databases.
---

# Allow Integrations With External Databases

In this example, we want to allow one developer in the team to [create integrations with external databases](../../extensibility-and-integration/connect-external-db.md). This developer must be able to publish extensions, through Integration Studio, that use specific database connections. However, the developer must not be able to change the settings of the database connections.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/allow-external-db-integration-1.png?width=250)

To do this:

1. [Create a new role](create-an-it-role.md#create-a-new-role) that has the permission level **Change and Deploy Applications**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/lt-allow-external-db-integration-2.png?width=450)

2. [Set the developer's default role](create-an-it-role.md#set-the-user-default-role) to the new role.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/lt-allow-external-db-integration-3.png?width=450)

3. Go to the environment's Service Center console \(`http://<your_environment>/ServiceCenter`\) and select **Administration » Database Connections**.
4. Edit the database connection and grant the security level **Publish** to the role Integrator.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/sc-allow-external-db-integration-4.png?width=600)

This way, the developers assigned with the Integrator role as Default Role will be able to publish extensions, through Integration Studio, that use this database connection. However, other developers will only be able to use those extensions to access data on the external database after a user with the security level **Full Control** over the database connection [configures the extensions in Service Center](../../extensibility-and-integration/connect-external-db.md#configure-the-extension-to-use-a-database-connection) to use the database connection.

