---
summary: Learn the requirements an external authentication plugin must implement.
---

# Implement an Authentication Plugin

OutSystems allows you to authenticate IT users \(developers, testers operations\), using an external authentication provider. It can be done by using or developing an authentication plugin and assigning it as the authentication provider on the platform. This page contains the requirements an external authentication plugin must implement.

## SOAP Web Service Name

An authentication plugin is a module that exposes a SOAP web service. This web service is invoked by OutSystems when activating the plugin and when authenticating users.

The SOAP web service needs to be called 'OSPlatformAuthentication'.

## SOAP Web Service Methods

The 'OSPlatformAuthentication' SOAP web service needs to expose the following methods.

| Name | Description |
| :--- | :--- |
| [Plugin\_GetAllConfigurations](implement-an-authentication-plugin.md#plugin_getallconfigurations%3E)\(\) | Method invoked synchronously to get all configurations needed by the plugin and their current values. |
| [Plugin\_GetCapabilities](implement-an-authentication-plugin.md#plugin_getcapabilities%3E)\(\) | Method invoked synchronously when the platform is changed to use this plugin for authentication. You should use this method to return the capabilities of your plugin. |
| [Plugin\_OnActivation](implement-an-authentication-plugin.md#plugin_onactivation%3E)\(\) | Called synchronously when the OutSystems authentication method is changed to use this plugin for authentication. As an example, you can use this method to execute your tests and validate the plugin. |
| [Plugin\_OnDeactivation](implement-an-authentication-plugin.md#plugin_ondeactivation%3E)\(\) | Method invoked synchronously when the OutSystems authentication method is changed to stop using this plugin for authentication. As an example, you can use this method to disable your users from the platform. |
| [Plugin\_SetConfigurations](implement-an-authentication-plugin.md#plugin_setconfigurations%3E)\(\) | This method is executed synchronously to update the plugin configuration when changing its configurations in the infrastructure management console \(LifeTime\). |
| [Plugin\_Test](implement-an-authentication-plugin.md#plugin_test%3E)\(\) | Called synchronously when the IT user tests if the plugin is working correctly in the platform. As an example, you can use this method to check if your plugin is valid. |
| [User\_AuthenticateWithCredentials](implement-an-authentication-plugin.md#user_authenticatewithcredentials%3E)\(Text, Text\) | Executed synchronously when the platform authenticates a username and password against the external system. As an example, you can use this method to validate a user in the Active Directory. |
| [User\_AuthenticateWithUsername](implement-an-authentication-plugin.md#user_authenticatewithusername%3E)\(Text\) | Method invoked synchronously when the platform authenticates a username against the external system. As an example, you can use this method to validate a user with Integrated Authentication. |

## Plugin\_GetAllConfigurations

Method invoked synchronously to get all configurations needed by the plugin and their current values.

### Inputs

None.

### Outputs

| Name | Type | Description |
| :--- | :--- | :--- |
| Configuration | [PluginAPIConfigurationParameter](implement-an-authentication-plugin.md#pluginapiconfigurationparameter) Record List | The list of plugin configuration properties and their values. |
| Status | [PluginAPIStatus](implement-an-authentication-plugin.md#pluginapistatus) | The status of invoking this action. It contains the success value and the response information of the action. |

## Plugin\_GetCapabilities

Method invoked synchronously when the platform is changed to use this plugin for authentication. You should use this method to return the capabilities of your plugin.

### Inputs

None.

### Outputs

| Name | Type | Description |
| :--- | :--- | :--- |
| SupportedCapabilities | [Capability](implement-an-authentication-plugin.md#capability) Record List | The list of supported capabilities. |
| Status | [PluginAPIStatus](implement-an-authentication-plugin.md#pluginapistatus) | The status of invoking this action. It contains the success value and the response information of the action. |

## Plugin\_OnActivation

Called synchronously when the OutSystems authentication method is changed to use this plugin for authentication. As an example, you can use this method to execute your tests and validate the plugin.

### Inputs

None.

### Outputs

| Name | Type | Description |
| :--- | :--- | :--- |
| Status | [PluginAPIStatus](implement-an-authentication-plugin.md#pluginapistatus) | The status of invoking this action. It contains the success value and the response information of the action. |

## Plugin\_OnDeactivation

Method invoked synchronously when the OutSystems authentication method is changed to stop using this plugin for authentication. As an example, you can use this method to disable your users from the platform.

### Inputs

None.

### Outputs

None.

## Plugin\_SetConfigurations

This method is executed synchronously to update the plugin configuration when changing its configurations in the infrastructure management console \(LifeTime\). This method is only invoked if the plugin has the 'ConfigurationAPI.Supported' capability value set to 'True'.

Implementations should validate whether configurations are valid \(e.g. values match data types; mandatory setting have values defined\) and signal the status of the operation accordingly.

### Inputs

| Name | Type | Description |
| :--- | :--- | :--- |
| Configuration | [PluginAPIConfigurationParameter](implement-an-authentication-plugin.md#pluginapiconfigurationparameter) Record List | The list of plugin configuration properties to update and their new values. |

### Outputs

| Name | Type | Description |
| :--- | :--- | :--- |
| Status | [PluginAPIStatus](implement-an-authentication-plugin.md#pluginapistatus) | The status of invoking this action. It contains the success value and the response information of the action. |

## Plugin\_Test

Called synchronously when the IT user tests if the plugin is working correctly in the platform. As an example, you can use this method to check if your plugin is valid.

### Inputs

None.

### Outputs

| Name | Type | Description |
| :--- | :--- | :--- |
| Status | [PluginAPIStatus](implement-an-authentication-plugin.md#pluginapistatus) | The status of invoking this action. It contains the success value and the response information of the action. |

## User\_AuthenticateWithCredentials

Executed synchronously when the platform authenticates a username and password against the external system. As an example, you can use this method to validate a user in the Active Directory.

### Inputs

| Name | Type | Description |
| :--- | :--- | :--- |
| Username | Text | The username of the user to authenticate. |
| Password | Text | The password of the user to authenticate. |

### Outputs

| Name | Type | Description |
| :--- | :--- | :--- |
| UserId | User Identifier | The OutSystems user identifier. |
| Status | [PluginAPIStatus](implement-an-authentication-plugin.md#pluginapistatus) | The status of invoking this action. It contains the success value and the response information of the action. |

## User\_AuthenticateWithUsername

Method invoked synchronously when the platform authenticates a username against the external system. As an example, you can use this method to validate a user with Integrated Authentication.

### Inputs

| Name | Type | Description |
| :--- | :--- | :--- |
| Username | Text | The username of the user to authenticate. |

### Outputs

| Name | Type | Description |
| :--- | :--- | :--- |
| UserId | User Identifier | The OutSystems user identifier. |
| Status | [PluginAPIStatus](implement-an-authentication-plugin.md#pluginapistatus) | The status of invoking this action. It contains the success value and the response information of the action. |

## Structures

Below are the structures the plugin needs to have.

### PluginAPIStatus

| Name | Type | Description |
| :--- | :--- | :--- |
| Success | Boolean | True if the operation was successful, False otherwise. |
| ResponseId | Integer | The response code. |
| ResponseMessage | Text | The response message. |
| ResponseAdditionalInfo | Text | The response detailed message. |

You can customize the values for the ResponseId, ResponseMessage, and ResponseAdditionalInfo attributes since these attributes are only used to generate logs.

### Capability

| Name | Type | Description |
| :--- | :--- | :--- |
| Name | Text | The name of the capability. |
| Value | Text | The value of the capability. |

**Supported Values**

Your plugin can expose specific values for the following capabilities \(if a capability is not specified, the default value will be 'False'\):

| Name | Possible Values | Description |
| :--- | :--- | :--- |
| 'UserPassword.Supported' | 'True' or 'False' | Indicates if the plugin supports user credentials validation \(i.e. it implements the [User\_AuthenticateWithCredentials](implement-an-authentication-plugin.md#user_authenticatewithcredentials%3E) method\). |
| 'IntegratedAuthentication.Supported' | 'True' or 'False' | Indicates if the plugin supports authentication through a username \(i.e. if it implements the [User\_AuthenticateWithUsername](implement-an-authentication-plugin.md#user_authenticatewithusername%3E) method\). |
| 'ConfigurationAPI.Supported' | 'True' or 'False' | Indicates if the plugin supports the configuration API methods \([Plugin\_GetAllConfigurations](implement-an-authentication-plugin.md#plugin_getallconfigurations%3E) and [Plugin\_SetConfigurations](implement-an-authentication-plugin.md#plugin_setconfigurations%3E)\). |
| 'Cloud.Supported' | 'True' or 'False' | Indicates if the plugin is supported in OutSystems PaaS. |

### PluginAPIConfigurationParameter

| Name | Type | Description |
| :--- | :--- | :--- |
| Name | Text | Name of the configuration parameter. |
| Value | Text | Value of the parameter. |

