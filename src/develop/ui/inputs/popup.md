---
summary: Learn how to create and use a popup in your application.
tags: >-
  support-application_development; support-Front_end_Development;
  support-Mobile_Apps; support-webapps
---

# Create and Use a Popup

You can use a popup to provide information to the end-users or ask for their input. This results in a better experience for end-users because they are kept in context while entering the input.

## In Reactive Web and Mobile

To create and use a popup in Reactive Web and Mobile apps:

1. Drag the Popup widget to the screen.
2. Add a variable of Boolean type to the screen to control the popup visibility \(you can use it to show or hide the popup\).
3. Set the Show Popup property with the variable. This will effectively toggle the popup according to the variable value.
4. Implement a Client Action in the screen to display the popup by assigning `True` to the variable.
5. Implement the popup content.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/inputs/images/popup-mobile.png?width=750)

## In Traditional Web

To create and use a popup in Traditional Web apps:

1. Name the link that will open the popup and check that its OnClick Method property is set to Navigate.
2. Create a new screen for the popup. In the widget tree, set the **Source Web Block** of the layout of the screen to `Layouts\LayoutPopup`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/inputs/images/popup-web-2.png?width=500)

3. In the previous screen, set the link’s Destination to the popup screen.
4. Use the search bar \(Ctrl + F\) to look for the Popup\_Editor and drag it to the screen with the link.
5. Set the LinkOrButtonWidget property of the Popup\_Editor to the Id runtime property of the link.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/inputs/images/popup-web-1.png?width=750)

6. Choose **\(New Screen Action\)** in the OnNotify Destination property of the Popup\_Editor and leave the flow of the action empty.
7. Implement the popup content.

