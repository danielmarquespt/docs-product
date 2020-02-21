---
kinds: ServiceStudio.Plugin.SAP.SapClientDescriptor
helpids: 17252
---

# SAP Connection

Defines a connection to a SAP system.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| Icon | Picture to be displayed to help identify this element. | Yes |  |  |
| Default Connection Settings |  |  |  |  |
| Application Server | Hostname of the SAP application server where the remote function calls are executed. |  |  |  |
| System ID | Three-letter identifier of the SAP installation to which to connect. |  |  |  |
| Instance Number | Two-digit identifier of the SAP instance to which to connect. |  |  |  |
| SAP Router String | Router string to connect to the SAP application server, e.g.: /H/sap.acme.com/S/3299/H/ |  |  |  |
| Client | Three-digit client number that identifies which tenant's data to use in the remote function calls. |  | 800 |  |
| Language | Two-letter language key used for translating language-specific data when retrieving data from SAP. |  |  |  |
| Username | Username to authenticate in SAP. |  |  |  |
| Advanced |  |  |  |  |
| Send Default Value | Set to Yes to send the default value for an optional atribute or parameter in the payload of the request. | Yes | No |  |
| On Before Connection | The action that allows you to customize the connection and its parameters. Executed before every SAP remote function call. |  |  |  |
| On Before Call | The action that allows you to customize values passed to a SAP remote function. Executed before every remote function call. |  |  |  |
| On After Call | The action that allows you to customize the values received from a SAP remote function. Executed after every remote function call. |  |  |  |

