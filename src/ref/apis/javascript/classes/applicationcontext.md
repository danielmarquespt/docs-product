---
tags: runtime-mobileandreactiveweb
summary: >-
  Provides contextual information based on the screen that is being presented.
  Used to identify the screen, module and application that is currently running.
---

# ApplicationContext

Provides contextual information based on the screen that is being presented. Used to identify the screen, module and application that is currently running.

## Hierarchy

**ApplicationContext**

## Summary

| Methods |  |
| :--- | :--- |
| \[getCurrentContext\]\(applicationcontext.md\#getcurrentcontext\) |  Gets the current context based on the screen being presented. |

## Methods

### &lt;Static&gt; getCurrentContext

**getCurrentContext\(\): object**

Gets the current context based on the screen being presented.

Returns: object

Returns an object with the following attributes: `applicationKey`, `applicationName`, `moduleKey`, `moduleName`, `screenKey`, `screenName`.

