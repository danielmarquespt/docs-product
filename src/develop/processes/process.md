---
summary: >-
  Check how to create and execute processes, which are elements that allow you
  to integrate your business processes into your applications.
tags: support-webapps
---

# Processes

A **Process** is an element that allows you to integrate your business processes into your applications. A process is designed in a **process flow**, which usually represents the activities that have to be carried out during an entity life cycle.

## Create a Process

1. In the **eSpace tree**, under the **Processes Layer**, right-click on the **Processes** folder and select **Add Process**.
2. Rename it as desired. OutSystems Platform automatically opens the process flow on the flow canvas.
3. Design the behavior of the process \(i.e. the [process flow](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/processes/process-flow/intro.md%3E)\) using the [Process Flow Editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/processes/process-flow/process-flow-editor.md%3E).

A process can have input parameters and output parameters.

## Process Scope

When editing expressions in your process flow, you have access to the following elements in the scope:

* Input and Output parameters defined in the process.
* Output parameters of process activities in the process flow. Take note that, to use a process activity output parameter, that process activity must precede in all the process flow paths the process activity where you want to use the output parameters. For example, to use the output parameters of an Automatic Activity in a Decision element, the Automatic Activity element must precede the Decision element in all paths to the Decision element in the process flow.

Anyway, when you're editing your process flow, all of the process activities available in the scope are present in the Scope tree of the Expression Editor, in a case where you're editing an expression, or in the variables tree of the Select Variable window, in a case where you're trying to use a variable.

## Launching a Process

In your application, a process may be either **automatically launched** when an entity is created, or **explicitly launched** in an action flow of your actions. In the first case, simply set the `Launch On` process property with the Create entity action.

When a process is automatically launched as result of a Create entity action, an input parameter with the entity identifier is automatically added to the process so that you know which created entity launched that process.

To explicitly launch the process in your application use the [process extended actions](actions-extended/intro.md).

A process can also be [executed](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/Class.Execute%20Process.final.md%3E) in another process flow.

### Using Process References

Service Studio provides you with mechanisms to reuse Processes among eSpaces. You can expose your Processes to other eSpaces or use Processes defined in another eSpace.

If you are using an Oracle or DB2 database, commit the transaction before launching a Process instance.

## Process Execution

When a process is launched a process instance is created and executed starting at the **Start** element of its flow. The process flow is then followed and each process activity found in the path has an **activity instance** created and executed.

If you have a cycle in your process flow, each time the same process activity is found a new instance of it is created and executed.

You may add business logic to validate your process instance execution, for example, when the process is launched, to validate whether the process instance can be executed.

### Process Activities Life Cycle

Each activity instance has its own life cycle with several states followed from the beginning to the end of the execution. To enforce your activity execution consistency, you may **add business logic** at some points of the activity life cycle.

## Upgrading Your Process

To upgrade your process flow, simply edit the process flow and publish your eSpace. OutSystems automatically performs the process flow upgrade for all executing process instances.

## Using Process Entities

You may set a process to have a Process Entity associated with it. This allows you to persist process information and use it in your application logic.

## Using the Processes API

To customize and extend the design of your Processes, you can use the [Processes API](../../ref/apis/processes-api.md) which allows extracting information from the platform data model.

