---
summary: >-
  If your existing mobile applications were based on a version of Silk UI Mobile
  previous to 1.3.0, learn how to update them to display the App Feedback
  instructions screen.
---

# Update Your Mobile App to Display App Feedback Instructions

If you are using the latest version of [Silk UI Framework](https://success.outsystems.com/Documentation/SILK_UI_Framework), your newly created mobile apps based on Silk UI Mobile templates will include a Block in the HomeScreen containing the instructions to access App Feedback. If App Feedback is enabled for the app, the users accessing the app for the first time will see this screen:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/app-feedback/images/app-feedback-send-mobile-1.png?width=300)

However, if you have existing mobile apps that were created based on a version of Silk UI Mobile [previous to 1.3.0](https://success.outsystems.com/Documentation/SILK_UI_Framework/Upgrading_Silk_UI#Mobile), you can adapt those apps to display the App Feedback instructions by doing the following:

1. Make sure you have the [latest version of Silk UI Framework](https://success.outsystems.com/Documentation/SILK_UI_Framework/Upgrading_Silk_UI) installed in your environment.
2. Open the application module containing the screens where you want to add the App Feedback instructions.
3. Go to **Manage Dependencies...**.
4. Find the module **MobilePatterns** and add the block **AppFeedbackHelp** from the flow **AppFeedback**:

   ![](../../../.gitbook/assets/app-feedback-add-onboard-screen-1.png)

5. Go to the screen where you want to add the App Feedback instructions. For example, the first screen after the user login.
6. Expand the module **MobilePatterns** and the flow **AppFeedback**.
7. Drag and drop the block **AppFeedbackHelp** to the screen:

   ![](../../../.gitbook/assets/app-feedback-add-onboard-screen-2.png)

When running the mobile app, **AppFeedbackHelp** block will check if App Feedback is enabled for the app. If App Feedback is enabled, the instructions to access App Feedback are displayed when users access the screen for the first time. After users dismiss the information, they will not see the App Feedback instructions again.

