---
kinds: >-
  ServiceStudio.Model.WebWidgets+EmailWebBlockInstance+Kind,
  ServiceStudio.Model.WebWidgets+WebBlockInstance+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceEmailWebBlockInstance+Kind,
  ServiceStudio.Model.WebWidgets+ReferenceWebBlockInstance+Kind
helpids: 0
---

# Web Block Widget

Displays a reusable screen element.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Source Web Block | Web block to display. | Yes |  | It might be necessary to specify additional input arguments. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Id | Identifies the widget instance at runtime \(HTML 'id' attribute\). You can use it in JavaScript and Extended Properties. | Yes | Text |  |

