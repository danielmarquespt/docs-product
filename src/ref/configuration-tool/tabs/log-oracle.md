---
summary: Log tab showing specific settings for the 'Oracle' database provider.
---

# Log Tab in Oracle

The following configurations are available in the Log tab when the 'Database Provider' property is set to 'Oracle'.

## Database Section

This area contains general configurations for the Oracle database.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| Naming Method | The method to connect to the Oracle database server. | `Service Name` |
| Host | The hostname or IP address to the database server.%%This option is only available when the 'Naming Method' is set to 'Service Name'. | `localhost` |
| Port | The port on which the database service listens.%%This option is only available when the 'Naming Method' is set to 'Service Name'. | `1521` |
| Service Name | The Oracle database service name.%%This option is only available when the 'Naming Method' is set to 'Service Name'. |  |
| TNS Name | An address name defined in the tnsnames.ora configuration file.%%This option is only available when the 'Naming Method' is set to 'TNS Name'. |  |

For advanced settings, click the Advanced Settings link.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
|  \*\*Advanced Connection Settings\*\* |  |  |
| Runtime Applications | Allows you to configure the behavior of database connections when used by OutSystems applications at runtime. |  |
| Error Messages Language | Allows you to set the NLS\_LANGUAGE setting when connecting to your database.  [Check the Oracle documentation](http://docs.oracle.com/cd/B28359_01/server.111/b28298/applocaledata.htm) to learn what are the supported values. |  |
| Linguistic Sorting | Allows you to set the NLS\_SORT parameter. Choose one of the following values:  BINARY\_AI – Collation-sensitive SQL operations use a binary sort that is accent-insensitive and case-insensitive.  BINARY\_CI – Collation-sensitive SQL operations use a binary sort that is case-insensitive, but accent-sensitive. Using this value can help prevent issues in languages where accents are relevant for SQL operations. For example, in Japanese "Seto" \(セト\) and "Zeto" \(ゼト\) would both be valid query results for the "セト" search when using the BINARY\_AI linguistic sort. | \`BINARY\_AI\` |
| Log Service Port | The port the log service listens to. Note: This setting is not available in fresh installs. | \`12003\` |
| Log Cycle Period | Indicates for how long \(in weeks\) the log files are kept. After this time, the log tables are rotated and information is lost. | \`4\` |

OutSystems supports Unicode for Oracle databases. To start developing with support for Unicode you just need to ensure that your Oracle database is set to use `AL32UTF8` as the database character set.

## Administrator Section

The 'Administrator' section allows you to configure the database user that manages the logging database. This user owns the log tables, views, and indexes.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| User | Name of the user that is the owner of log tables and associated objects. | `OSADMIN_LOG` |
| Password | Password for the user. |  |
| Tablespace | Table space where the system tables are stored. | `OSSYS_LOG` |
| Index Tablespace | Table space where all indexes of the platform are stored. | `OSIDX_LOG` |

## Runtime Section

In this section you specify the login for the user that owns user tables in the logging database.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| User | Name of the user that is the owner of user tables created in the logging database. | `OSRUNTIME_LOG` |
| Password | Password for the specified user. |  |
| Tablespace | Table space where user tables created in the logging database are stored. | `OSUSR_LOG` |

## Create/Upgrade Database Button

To create all the database objects \(tables, indexes, views, etc\) required for logging purposes, click 'Create/Upgrade Database'.

