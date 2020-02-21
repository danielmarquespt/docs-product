---
kinds: ServiceStudio.Model.Nodes+ExecuteAction+Kind
helpids: 30107
---

# Run Server Action

Executes an action that runs logic on the server side.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Action | Action with logic to run on the server. | Yes |  | It might be necessary to specify additional action input arguments. |
| Animation Effect | Type of animation applied to the widget when refreshed. | Yes | None | The possible values are: None, Highlight, Fade, Vertical Slide. |
| Server Request Timeout | Maximum time in seconds to wait for the Execute Action to complete before triggering a Communication Exception. Overrides the default timeout defined on the module. |  |  |  |

