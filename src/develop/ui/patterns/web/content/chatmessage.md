---
tags: runtime-traditionalweb;
summary: ChatMessage displays conversation posts in notifications or chat screens.
---

# ChatMessage

Display conversational content such as display photos, text, images, delivery time and status.

A ChatMessage is used to display conversation posts in notifications or chat screens.

**How to use**

1. Drag the ChatMessage pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/chatmessage-image-1.png%3E)

2. Set the content that you need in the placeholders.
3. Publish and test.

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| IsRight | When set to true, aligns the pattern to right. | Boolean | No | none |
| IsInline | If set as true, the chat balloon styles are changed to something similar to a post pattern. | Boolean | No | False |
| Color | Set the backgound color. | Color Identifier | No | Entities.Color.Neutral3 |
| ExtendedClass | Add custom style classes to this Block. | Text | No | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/chatmessage-image-2.png?width=600)

## Events

| **Event Name** | **Description** | **Mandatory** |
| :--- | :--- | :--- |
| OnClick | Event triggered when the user clicks the message container. | False |

## CSS Selectors

| **Element** | **CSS Class** | **Description** |
| :--- | :--- | :--- |
| .chat-message-actions | is--hidden | When the server action ToggleChatActions hides the content |
| .chat-message-actions | is--visible | When the server action ToggleChatActions shows the content |

## Advanced Use Case

### Change ChatMessage styles according to user

1. Drag a ListRecords widget into the preview with the chat users as the Source Record List.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/chatmessage-image-6.png%3E)

2. In the ListRecords widget, drag a ChatMessage pattern.
3. In the IsRight parameter, type `If(Chat.List.Current.ChatUser.Sender, True, False)` to make the message appear on the right for the active user.
4. In the Color parameter, type `If(Chat.List.Current.ChatUser.Sender, Entities.Color.Primary, Entities.Color.Neutral3)` to change the background according to the user.
5. In the ExtendedClass property, use `If(Chat.List.Current.ChatUser.Sender, "color-neutral-0", "")` to change the color of text to white, if the background has the primary color. If the primary color is white, change the following code to `color-neutral-10`.
6. In the the UserInitials pattern, set the Color parameter inside the Image placeholder to `If(Chat.List.Current.ChatUser.Sender, Entities.Color.Primary, Entities.Color.Neutral3)` in order to change the text color and to match the same conditions set above.
7. Set the IsLight parameter to `If(Chat.List.Current.ChatUser.Sender, True, False)`.
8. Publish and test.

The result would be something like this:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/chatmessage-image-3.png%3E)

### Show/Hide Actions Placeholder on click

1. Drag the ChatMessage Pattern into the preview.
2. Type a name for the pattern.
3. In the Events property, choose a New Screen Action for the Handler.
4. In this new action, drag the ToggleChatActions. You can find it under the Logic tab - OutSystemsUIWeb - ChatMessage folder.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/chatmessage-image-4.png%3E)

5. In the WidgetId parameter, type the name of the ChatMessage pattern.
6. Publish and test.

The result is something like this:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/content/images/chatmessage-gif-1.gif%3E)

