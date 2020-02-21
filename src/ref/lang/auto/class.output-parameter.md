---
kinds: >-
  ServiceStudio.Model.Variables+ActivityOutput+Kind,
  ServiceStudio.Model.Variables+GenericOutputParameter+Kind,
  ServiceStudio.Model.Variables+JSOutputParameter+Kind,
  ServiceStudio.Model.Variables+ProcessOutput+Kind,
  ServiceStudio.Model.Variables+SerializableOutputParameter+Kind,
  ServiceStudio.Model.Variables+WebReferenceGenericOutputParameter+Kind,
  ServiceStudio.Model.Variables+ReferenceActivityOutput+Kind,
  ServiceStudio.Model.Variables+ReferenceGenericOutputParameter+Kind,
  ServiceStudio.Model.Variables+ReferenceProcessOutput+Kind,
  ServiceStudio.Model.Variables+ReferenceSerializableOutputParameter+Kind
helpids: '7012, 30101'
---

# Output Parameter

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Default Value | Initial value of this element. If undefined, the default value of the data type is used. |  |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Data Type | The data type of the output parameter. | Yes |  |  |
| Is Start Activity Input/ Is Close Activity Input | Indicates if the output parameter is also used as an input parameter of the process activity's extended action. | Yes | Yes, Mandatory | The possible values are:  – "Yes, Mandatory": The output parameter is a mandatory input parameter of the Start&lt;Activity&gt;/Close&lt;Activity&gt; extended action;  – "Yes, Optional": The output parameter is an optional input parameter of the Start&lt;Activity&gt;/Close&lt;Activity&gt; extended action;  – "No": The output parameter is not an input parameter of the Start&lt;Activity&gt;/Close&lt;Activity&gt; extended action.  The property "Is Start Activity Input" is only available when specifying an output parameter for a Conditional Start process activity.  The property "Is Close Activity Input" is only available when specifying an output parameter for a Human Activity or a Wait process activities. |

