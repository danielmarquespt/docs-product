---
summary: >-
  Learn how to deploy your integration with an external database from your
  Development environment to another environment.
tags: null
---

# Deploy an Integration With an External Database

Follow the steps in this guide to deploy an application with a connection to an external database from an OutSystems environment \(in this case, the Development environment\) to the next environment \(in this case, the Quality environment\).

Use this guide after you [created the integration with the external database](../../extensibility-and-integration/connect-external-db.md) in your Development environment and if your application needs to connect to a different external database in each environment.

 \*\*Before you begin following this step by step guide, make sure that:\*\* \* Your infrastructure uses \*\*LifeTime 11.4.2\*\* or later. \* Both the source and target environments use \*\*Platform Server 11 Release Jul.2019 CP1\*\* or later. \* You have \*\*Change & Deploy Applications\*\* permission for the applications that you want to deploy. \* You created the \*\*Extension\*\* that integrates with an external database while connected to an environment running \*\*Platform Server 11 Release Jul.2019 CP1\*\* or later. Otherwise, republish the Extension in Integration Studio while connected to an environment running \*\*Platform Server 11 Release Jul.2019 CP1\*\* or later.

## Define a Database Connection in the Quality environment

In the Quality environment, define a Database Connection:

1. Open the **Service Center** management console of your **Quality environment**.
2. On the **Administration** tab, select **Database Connections**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-05.png?width=800)

3. Click **New Database Connection** and fill in the fields to set up the connection to the external database.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-06.png?width=800)

4. Click **Test** to check if the connection is working correctly.

    The database user must have permissions to: \* List the necessary tables and views in the external database. \* Perform the operations Create, Read, Update, and Delete on those tables and views.

5. Click **Create** to create the Database Connection.

## Deploy the application to the Quality environment

To deploy the application to the Quality environment follow these steps:

1. Open LifeTime for your Infrastructure.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-07.png?width=800)

   Tip: Open LifeTime directly from Service Center by clicking **Manage all environments**.

2. Select the **Applications** tab and select the **DEPLOY...** button between the Development environment and the Quality environment.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-08.png?width=800)

3. Select **Add Applications** and, in the **Choose one or more Applications** dialog, select your application and select **Add to Deployment Plan**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-09.png?width=400)

4. Select the **VALIDATE NOW** button between the Development environment and the Quality environment.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-10-ea.png?width=800)

5. Select the **CONTINUE** button between the Development environment and the Quality environment.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-11-ea.png?width=800)

6. Verify the deployment plan, select **Deploy Now** and then in the **Deploy applications as planned** dialog select **Deploy Now** to start the deployment.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-12.png?width=800)

7. In the **Configure applications settings** step, enter the three-part **Physical Table Name** of each external database Entity. Make sure you enter the correct **Physical Table Name** for the target environment.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-16-ea.png?width=800)

    If your application connects to the same external database/schema for both your environments, select \*\*Copy from Source\*\* to copy the \*\*Physical Table Name\*\* from the source environment.

8. After the deployment stops, click the **configuration or confirmation** link in the warning banner to open Service Center and map the database name of the extension to the database connection.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-13-ea.png?width=800)

9. Associate the logical database name of the extension to the Database Connection that you created previously.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-14.png?width=800)

After the Deployment finishes your Extension is ready to be used by other applications in the Quality environment.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/deploy-applications/images/ext-db-15.png?width=800)

