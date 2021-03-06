---
tags: support-application_development; support-webapps
---

# Use Process Extended Actions

To manage the life cycle of your [processes](../process.md) or [process activities](../process-flow/process-flow-toolbox.md) of your eSpace you're provided with **Process Extended Actions** and **Process Activities Extended Actions**. You can find them under your processes and process activities in the Processes Layer of the eSpace Tree.

## Execute a Process Extended Action or Process Activity Extended Action

In the **Processes Layer** of the **eSpace Tree**, drag the **Extended action** of the process or process activity and drop it on the action flow.

An extended action can have input parameters and output parameters.

### Input parameters

Instantiated when the action is invoked, through the `Arguments` property of the **Launch&lt;Process Name&gt;** element.

### Output parameters

You can use the output parameters of the **Launch&lt;Process Name&gt;** process extended action in one of the following ways:

* Type directly **Launch&lt;Process Name&gt;.Id**

  Example: after using the `LaunchPayment` action for the `Payment` process you can use `LaunchPayment.Id` to access the launched process identifier.

* Through the specific editors with access to the **Locals** folder

  Example: when editing an expression in the **Expression Editor**, the **Scope Tree** lists the **Locals** folder.

## Reference

The extended actions for the process and process activities are the following:

| Element | Extended Action | Description |
| :--- | :--- | :--- |
| ![](../../../../.gitbook/assets/process.png) Process | ![](../../../../.gitbook/assets/process-extended-action%20%281%29.png) Launch&lt;Process Name&gt; | Launches an instance of the Process. |
| ![](../../../../.gitbook/assets/human-activity.png) Human Activity | ![](../../../../.gitbook/assets/process-extended-action%20%282%29.png) Close&lt;Human Activity Name&gt; | Closes a Human Activity. |
| ![](../../../../.gitbook/assets/wait-activity.png) Wait | ![](../../../../.gitbook/assets/process-extended-action%20%283%29.png) Close&lt;Wait Name&gt; | Closes a Wait activity. |
| ![](../../../../.gitbook/assets/conditional-start.png) Conditional Start | ![](../../../../.gitbook/assets/process-extended-action.png) Start&lt;Conditional Start Name&gt; | Starts a Conditional Start activity. |

