---
summary: >-
  OutSystems permission model allows you to limit the creation of new
  applications in an environment to some users, such as IT architects.
---

# Control Who Creates Applications

OutSystems permission model allows you to limit the creation of new applications in an environment to some users, such as IT architects.

In this example we want to:

* Allow junior developers to see and work only on the applications of their respective teams but **without being able to create new applications**.
* Allow architects to **create applications** for their teams.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/control-app-creation-1.png?width=250)

To do this, configure the junior developers:

1. [Create a new role](create-an-it-role.md#create-a-new-role) that has the permission level **Access**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/lt-control-app-creation-2.png?width=450)

2. [Create IT users](create-an-it-user.md) for all junior developers with this new role set as the default role. This defines base permissions that only allow all junior developers to log in to an environment without granting access to any application.
3. [Create another role](create-an-it-role.md#create-a-new-role) called Junior Developer that has the permission level **Change and Deploy Applications** and set the permission **Create Applications** to OFF.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/lt-control-app-creation-3.png?width=450)

4. [Add the junior developers to their respective teams](create-an-it-team.md#add-it-users-to-the-team) with the role Junior Developer. This allows junior developers to make changes to the existing applications in their teams but does not allow them to create new applications.

Then, configure the architects:

1. [Create a new role](create-an-it-role.md#create-a-new-role) called Architect that has the permission level **Change and Deploy Applications** and set the permission **Create Applications** to **ON**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/lt-control-app-creation-4.png?width=450)

2. [Add the architects to their respective teams](create-an-it-team.md#add-it-users-to-the-team) with the role Architect.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/lt-control-app-creation-5.png?width=750)

This allows architects to [create new applications directly in their teams](create-an-it-team.md#create-a-new-application-in-the-team) through LifeTime. The new applications will be automatically added to the corresponding team. Therefore, the junior developers that have the permission level **Change and Deploy Applications** for the team can use Service Studio to create modules in the new application.

