---
summary: >-
  Teams allow you to manage the permissions of a large number of IT users over
  the applications in your factory.
---

# Create an IT Team

Teams allow you to manage the permissions of a large number of IT users over the applications in your factory. This way, when new hires join an existing team in the company, you can manage their permissions over the team’s applications without having to grant permissions on each application individually.

## Create a new team

To create a team, do the following:

1. In your LifeTime console \(`https://<lifetime_env>/lifetime`\), go to the **USER MANAGEMENT** area.
2. Choose **TEAMS** and click the **New Team** link.
3. Fill in the team’s Name and Description.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-create-lt.png?width=600)

4. Click the **CREATE** button to create the team.

Now that the team is created, [add users](create-an-it-team.md#add-it-users-to-the-team) and [applications](create-an-it-team.md#add-applications-to-the-team) to the team. You can also [create new applications in the team](create-an-it-team.md#create-a-new-application-in-the-team).

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-lt.png?width=800)

## Add IT users to the team

Adding users to a team will grant them a set of permissions over the team’s applications. As permissions are configured in roles, and you can assign different roles to each user within a team, you are able to have users with different permissions in the same team.

When you assign a role to a user in a team, that role overrides the default role of the user over the team’s applications. Check the OutSystems [permission model for IT users](about-permission-levels.md) to better understand which role should you grant your IT users by default and through a team.

### Add one or more IT users to a team

To add one or more users to the same team, do the following:

1. In the **USER MANAGEMENT** area, choose **TEAMS**.
2. Find the team you want from the list of teams and click the Name of the team to go to the details page.
3. Click the **Add Users** link.
4. Choose one or more users to add to the team and specify the role those users will have within the team.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-add-users-lt.png?width=700)

5. Repeat the previous step for the remaining users with other roles in the team.

To remove users from the team, click the remove icon for those users in the team’s screen:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-remove-users-lt.png?width=800)

### Add one IT user to several teams

If you need to add a user to several teams, you can do it in the user's detail screen:

1. In the **USER MANAGEMENT** area, choose **USERS**.
2. Find the user you want from the list of users and click the Name of the user to go to the details page.
3. Click the **Grant Roles in Teams** link.
4. Choose the teams and the role you want to assign the user in those teams.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-add-user-to-several-teams-lt.png?width=600)

5. Click the **Grant Role in Teams** button.

To remove the user from one or more teams, click the remove icon for those teams in the user’s detail screen:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-remove-user-lt.png?width=700)

## Add applications to the team

Adding applications to a team allows you to grant the permissions over a set of applications to all users in the team, without having to grant permissions on each application individually.

To add an application to a team, do the following:

1. In the **USER MANAGEMENT** area, choose **TEAMS**.
2. Find the team you want from the list of teams and click the Name of the team to go to the details page.
3. Click the **Add Applications** link.
4. Choose the applications that users in this team will have access to. Notice that you will see only the applications that are not part of a team yet, as one application can only be part of a single team.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-add-apps-lt.png?width=400)

5. Click the **Add Applications to Team** button.

To remove an application from the team, click the remove icon for that application in the team’s screen:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-remove-app-lt.png?width=800)

## Create a new application in the team

Creating a new application directly in the team automatically grants the users in the team with permissions over that application.

To create a new application in a team, do the following:

1. In the **USER MANAGEMENT** area, choose **TEAMS**.
2. Find the team you want from the list of teams and click the Name of the team to go to the details page.
3. Click the **Create Application** link.
4. Fill in the application details and click the **Create app** button.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/manage-it-teams/images/team-create-app-lt.png?width=500)

The IT users having **Change and Deploy Applications** permission level for the team now can use Service Studio to create modules in the new application.

