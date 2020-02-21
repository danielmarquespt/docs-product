---
summary: Learn how to define and run JavaScript code in your web application.
tags: runtime-traditionalweb
---

# Define and Run JavaScript Code

## How to Define JavaScript Functions

To add or edit the JavaScript functions of your elements, open the JavaScript editor by clicking "..." on the JavaScript property of the element:

![](../../../../.gitbook/assets/run-js-code-4.png)

The example below shows a JavaScript function defined locally for a Web Screen:

![](../../../../.gitbook/assets/run-js-code-2.png)

## How to Run JavaScript

You can run JavaScript code in your web application in the following ways:

* Using the Extended Properties of Web Screens or widgets
* Within unescaped Expressions
* Using the **RunJavaScript** action of the **HTTPRequestHandler** extension

In all the cases, the JavaScript code will run in the context of the browser.

### Extended Properties Example

The example below shows a JavaScript function that is invoked when the `onclick` event occurs in a button:

![](../../../../.gitbook/assets/run-js-code-1.png)

Since the value of an Extended Property is an expression, you can also type the JavaScript source code directly in the Extended Property value:

![](../../../../.gitbook/assets/run-js-code-6.png)

### Unescaped Expressions Example

You can use unescaped Expressions to add JavaScript at a specific point of your Web Screen, setting the Escape Content property to `No`:

![](../../../../.gitbook/assets/run-js-code-7.png)

![](../../../../.gitbook/assets/run-js-code-5.png)

### RunJavaScript Action Example

In your Action Flows, either in a Screen Action or a Server Action, you can use the **RunJavaScript** action of the **HTTPRequestHandler** extension to get your JavaScript code to run in the context of the browser:

![](../../../../.gitbook/assets/run-js-code-3.png)

