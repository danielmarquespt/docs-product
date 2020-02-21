---
summary: >-
  Allow users to send feedback while they are using your web or mobile
  application.
---

# Enable User Feedback for Applications

You can allow your users to send feedback while they are using a web or mobile application in a specific environment. For example, you can enable QA teams or key users to send suggestions or report problems in an application running in the QA environment.

## Turn Feedback On for an Application

You will use App Feedback system application to configure user feedback. To access App Feedback and enable users to send feedback for an application in a specific environment, do the following:

1. Open the LifeTime console.
2. In the Applications section, select "App Feedback" option in the drop-down menu next to the environment where you want to enable user feedback. This will open the App Feedback application in that environment:

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/app-feedback/images/app-feedback-enable-1.png?width=800)

3. In App Feedback application, go to the Configuration section.
4. Turn the feedback switch on for the application you want to enable user feedback:

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/app-feedback/images/app-feedback-enable-2.png?width=800)

5. **If you are enabling user feedback for a mobile app, you must regenerate the app.** Only the next generated app will include the feedback feature.

 If you don't have LifeTime installed, you can access directly to the App Feedback application of your environment by typing \`https:///ECT\_Provider\` in your browser.

You can disable user feedback for an application the same way as described above, this time turning the feedback switch off. Again, **if you are disabling user feedback for a mobile app, you must regenerate the app to remove the feedback feature**.

## Restrict the Users Who Can Submit Feedback

When you enable user feedback for an application, by default all users are allowed to submit feedback.

If you want to restrict the feedback to a specific group of users, select the name of the group in the drop down list next to the feedback switch:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/app-feedback/images/app-feedback-enable-3.png?width=800)

If the group of users to whom you want to enable feedback does not exist yet, do the following:

1. Select "Create a New Group..." in the drop down list next to the feedback switch.
2. The browser opens a new tab with the Users application.
3. Go to the Groups section and create the new group of users you want to get feedback from.
4. Back to the App Feedback configuration screen, refresh the page, and select the newly created group.

