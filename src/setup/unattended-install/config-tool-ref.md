---
summary: Complete reference for the Configuration Tool command line.
tags: >-
  support-Installation_Configuration;
  support-Installation_Configuration-overview
---

# Configuration Tool Command Line Reference

 This article applies to: \*\*OutSystems 11\*\*  Other versions available: \[10\]\(https://success.outsystems.com/Documentation/10/Setting\_Up\_OutSystems/Unattended\_Installation\_and\_Upgrade/Configuration\_Tool\_Command\_Line\_Reference\)

The Configuration Tool allows you to configure your OutSystems server.

The default path of the Configuration Tool command line is the following:

```text
C:\Program Files\OutSystems\Platform Server\ConfigurationTool.com
```

The Configuration Tool command line returns non-zero values when an error occurs.

## Syntax

```text
ConfigurationTool.com {/SetupInstall <platform_db_admin_username> <platform_db_admin_password> <logging_db_admin_username> <logging_db_admin_password> [/SetPlatformServerAdminPassword <platform_server_admin_password>] | /UpgradeInstall [<admin_password>] [/SetPlatformServerAdminPassword <platform_server_admin_password>]} [/RebuildSession <session_db_admin_username> <session_db_admin_password>] [/SCInstall] [/CreateUpdateCacheInvalidationService]
    | /GenerateTemplates
    | /ClearInternalNetwork
    | /UploadLicense <license_file>
    | /RegenerateSettingsKey
    | /GetSerial
    | /GetDeploymentZones
    | /ModifyDeploymentZone <configuration_name> <zone_address> [<enable_https>]
    | /EnableServerAPI
    | /DisableServerAPI
```

## Parameters

`/SetupInstall [<platform_db_admin_username> <platform_db_admin_password>] [<logging_db_admin_username> <logging_db_admin_password>]`

: Creates or upgrades the OutSystems platform and logging database model using the `server.hsconf` configuration file.

```text
For SQL Server of Azure SQL databases, you must provide the credentials needed to create or upgrade the platform database. Furthermore, if you specify separate platform and logging databases in `server.hsconf`, you also need to provide the credentials needed to create or upgrade the logging database.

For Oracle databases, you do not need to provide the admin usernames and passwords.
```

`/UpgradeInstall [<admin_password>]`

: Upgrades the OutSystems platform and logging database models, without validating if the database exists or if the permissions are correct.

```text
The admin password is optional and is only used for integrated authentication purposes where the password isn't stored in the server configuration file.
```

`/RebuildSession <session_db_admin_username> <session_db_admin_password>`

: Upgrades the session database model. The username and password provided must belong to a user with permissions to execute these operations.

`/SCInstall`

: Forces the Service Center installation to run after finishing Configuration Tool.

`/GenerateTemplates`

: Generates server configuration file \(`.hsconf`\) templates for each supported database engine in `Platform Server\docs`.

`/ClearInternalNetwork`

: Resets the internal network settings so that internal applications become accessible from any origin.

`/UploadLicense <license_file>`

: Uploads the license file and checks if the license is valid.

`/RegenerateSettingsKey`

: Generates a new private.key file.

`/GetSerial`

: Prints the serial number of this installation.

`/GetDeploymentZones`

: Lists the configured deployment zones for the current installation. The data is presented in JSON format, limited to the relevant settings that can be manipulated with `/ModifyDeploymentZone`, namely: the Configuration Name and Address, and it's Enable HTTPS status.

`/ModifyDeploymentZone <configuration_name> <zone_address> [<enable_https>]`

: Modifies the Address and/or Enable HTTPS settings of a Deployment Zone.

```text
`<configuration_name>` is the Deployment Zone that you want to modify; this argument is case insensitive (for example "GLOBAL" will map to "Global").

`<zone_address>` is the new address for the target Deployment Zone.

`[<enable_https>]` is an optional boolean argument; if this argument is not provided the setting will remain unchanged. If the string "true" (case insensitive) is provided, the Enable HTTPS setting is set to "true"; if any other string is provided the setting Enable HTTPS is set to "false". The applied value of the Enable HTTPS setting is displayed.
```

`/CreateUpgradeCacheInvalidationService`

: Installs cache invalidation service or reconfigures the service given in the configuration file \(`server.hsconf`\).

`/SetPlatformServerAdminPassword <platform_server_admin_password>`

: Defines the password for the Platform Server Admin user, if the user is active.  
Note: This command does not work when using Integrated Authentication.

`/EnableServerAPI`

: Enables Server.API and Server.Identity on this machine. \(Server.API and Server.Identity are enabled by default\)

`/DisableServerAPI`

: Disables Server.API and Server.Identity on this machine. Beware, Service Center will not work without them.

## Example

Perform a clean installation for SQL Server or Azure SQL:

```text
ConfigurationTool.com
    /SetupInstall <platform_db_admin_username> <platform_db_admin_password> <logging_db_admin_username> <logging_db_admin_password>
    /RebuildSession <session_db_admin_username> <session_db_admin_password>
    /CreateUpgradeCacheInvalidationService
    /SCInstall
```

Perform a clean installation for Oracle:

```text
ConfigurationTool.com
    /SetupInstall
    /RebuildSession <session_db_admin_username> <session_db_admin_password>
    /CreateUpgradeCacheInvalidationService
    /SCInstall
```

Perform an upgrade from OutSystems 10 \(or lower\):

```text
ConfigurationTool.com
    /UpgradeInstall [<admin_password>]
    /RebuildSession <session_db_admin_username> <session_db_admin_password>
    /CreateUpgradeCacheInvalidationService
    /SCInstall
```

Perform an upgrade from OutSystems 11:

```text
ConfigurationTool.com
    /UpgradeInstall [<admin_password>]
    /RebuildSession <session_db_admin_username> <session_db_admin_password>
    /SCInstall
```

Modify the Address and/or Enable HTTPS settings of the "Global" deployment zone:

```text
ConfigurationTool.com
    /ModifyDeploymentZone "Global" <zone_address> [<enable_https>]
```

Disable Server.API and Server.Identity:

```text
ConfigurationTool.com
    /DisableServerAPI
```

Enable Server.API and Server.Identity:

```text
ConfigurationTool.com
    /EnabelServerAPI
```

## Logging

By default, the Configuration Tool has logging enabled with log level `4` \(Verbose\), and the predefined log file is defined as `C:\Windows\Temp\ConfigurationTool.log`.

For more information on configuring logs check the \[Change OutSystems Platform logging levels \(OSTrace\)\]\([https://success.outsystems.com/Support/Enterprise\_Customers/Troubleshooting/Change\_OutSystems\_Platform\_logging\_levels\_\(OSTrace](https://success.outsystems.com/Support/Enterprise_Customers/Troubleshooting/Change_OutSystems_Platform_logging_levels_%28OSTrace)\)\) topic.

