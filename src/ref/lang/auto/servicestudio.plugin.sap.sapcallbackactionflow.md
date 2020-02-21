---
kinds: ServiceStudio.Plugin.SAP.SapCallbackActionFlowDescriptor
helpids: 30068
---

# SAP Callback

Action that allows the customization of the calls to SAP remote functions. Once defined, they are executed on every call to any SAP remote functions under the connection. There are three available action flows for implementing these customizations: OnBeforeConnection, OnBeforeCall, OnAfterCall \(defined in the SAP Connection element\).

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |

