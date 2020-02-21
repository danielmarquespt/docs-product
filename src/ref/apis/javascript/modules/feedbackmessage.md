---
tags: runtime-mobileandreactiveweb
summary: >-
  Displays feedback messages to the user. Used to display personalized feedback
  messages, specifying options like custom style and auto-close behavior.
---

# FeedbackMessage

Displays feedback messages to the user. Used to display personalized feedback messages, specifying options like custom style and auto-close behavior.

## Summary

| Functions |  |
| :--- | :--- |
| \[closeFeedbackMessage\]\(feedbackmessage.md\#closefeedbackmessage\) |  Closes the FeedbackMessage that is currently open. |
| \[showFeedbackMessage\]\(feedbackmessage.md\#showfeedbackmessage\) |  Shows a FeedbackMessage with the specified message, style, auto-closing behavior and HTML encoding options. |

## Functions

### closeFeedbackMessage

**closeFeedbackMessage\(\): void**

Closes the FeedbackMessage that is currently open.

Returns: void

### showFeedbackMessage

**showFeedbackMessage\(message: string, messageType: FeedbackMessageType, \[encodeHTML: boolean = true\], \[extraCssClasses: string\], \[closeOnClick: boolean = true\], \[onClick: function\]\): void**

Shows a FeedbackMessage with the specified message, style, auto-closing behavior and HTML encoding options.

Example:

```javascript
// prevent feedback message's default close-on-click behavior
$public.FeedbackMessage.showFeedbackMessage("Your data has been submitted.", 1, true, "", false);
```

Parameters:

* **message**: string  Message to be displayed.
* **messageType**: FeedbackMessageType  Type of feedback message to show \(0 = Info, 1 = Success, 2 = Warning or 3 = Error\).
* \(Default value\) **encodeHTML**: boolean \(default: true\)   Whether to escape HTML characters \(default is `true` so the message is treated as text\).
* \(Optional\) **extraCssClasses**: string  Whitespace-separated class names to be added to the feedback message container to customize the appearance of the message.
* \(Default value\) **closeOnClick**: boolean \(default: true\)   When `true`, indicates that the message box will be closed when the user clicks on it.
* \(Optional\) **onClick**: function  Function to be executed whenever the feedback message is clicked.

Returns: void

