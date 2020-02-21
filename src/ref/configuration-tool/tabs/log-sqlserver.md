---
summary: >-
  Log tab showing specific settings for the 'SQL Server / Azure SQL' database
  provider.
---

# Log Tab in SQL Server / Azure SQL

The following configurations are available in the Log tab when the 'Database Provider' property is set to `SQL Server / Azure SQL`.

## Database Section

This section contains general configurations for the SQL Server / Azure SQL database connection to the logging database.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| Server | The hostname or IP address to the database server. | `localhost` |
| Database | The database catalog to be used for the logging database. | `outsystems_log` |

For advanced settings, click the Advanced Settings link.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
|  \*\*Advanced Connection Settings\*\* |  |  |
| Runtime Applications | Allows you to use a specific connection string for OutSystems applications. |  |
| Log Service Port | The port the log service listens to. | \`12003\` |
| Log Cycle Period | Indicates for how long \(in weeks\) the log files are kept. After this time, the log tables are rotated and information is lost. | \`4\` |

## Administrator Section

The 'Administrator' section allows you to configure the database user that manages the logging database. This user owns the log tables, views, and indexes.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| User | Name of the user that is the owner of log tables and associated objects. | `OSADMIN_LOG` |
| Password | Password for the user. |  |

Note: these configurations will be read-only when Authentication is set to `Windows Authentication` in Platform tab.

## Runtime Section

The 'Runtime' section allows you to configure the database user used by the applications at runtime for logging purposes. This user owns the tables created by developers in the development environment.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| User | Name of the user used by the applications at runtime for logging purposes. | `OSRUNTIME_LOG` |
| Password | Password of the specified user. |  |

Note: these configurations will be read-only when Authentication is set to `Windows Authentication` in Platform tab.

## Create/Upgrade Database Button

To create all the database objects \(tables, indexes, views, etc\) required for logging purposes, click 'Create/Upgrade Database'.

