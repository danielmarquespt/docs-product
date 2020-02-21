---
kinds: >-
  ServiceStudio.Model.NRWebWidgets+If+Kind,
  ServiceStudio.Model.WebWidgets+If+Kind,
  ServiceStudio.Model.NRWebWidgets+ReferenceIf+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceIf+Kind
helpids: 4029
---

# If Widget

Displays content based on a condition.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Condition | Boolean literal or expression to decide which content is displayed. | Yes |  |  |
| Animate | Performs an animation on the content when the condition changes its value. | Yes | No |  |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

