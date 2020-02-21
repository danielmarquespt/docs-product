---
summary: >-
  Platform tab showing specific configuration settings for the Oracle database
  provider.
---

# Platform Tab in Oracle

In the Platform tab, once you set the 'Database Provider' property to 'Oracle', the following configurations become available.

## Database Section

This area contains general configurations for the Oracle database.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| Naming Method | The method to connect to the Oracle database server. | `Service Name` |
| Host | The hostname or IP address to the database server.%%This option is only available when the 'Naming Method' is set to 'Service Name'. | `localhost` |
| Port | The port on which the database service listens.%%This option is only available when the 'Naming Method' is set to 'Service Name'. | `1521` |
| Service Name | The Oracle database service name.%%This option is only available when the 'Naming Method' is set to 'Service Name'. |  |
| TNS Name | An address name defined in the tnsnames.ora configuration file.%%This option is only available when the 'Naming Method' is set to 'TNS Name'. |  |

For advanced settings, click on the Advanced Settings link.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
|  \*\*Advanced Connection Settings\*\* |  |  |
| Runtime Applications | Allows you to configure the behavior of database connections when used by OutSystems applications at runtime. |  |
| OutSystems Services | Allows you to configure the behavior of database connections when used by OutSystems services. |  |
| Error Messages Language | Allows you to set the NLS\_LANGUAGE setting when connecting to your database.  [Check the Oracle documentation](http://docs.oracle.com/cd/B28359_01/server.111/b28298/applocaledata.htm) to learn what are the supported values. |  |
| Linguistic Sorting | Allows you to set the NLS\_SORT parameter. Choose one of the following values:  BINARY\_AI – Collation-sensitive SQL operations use a binary sort that is accent-insensitive and case-insensitive.  BINARY\_CI – Collation-sensitive SQL operations use a binary sort that is case-insensitive, but accent-sensitive. Using this value can help prevent issues in languages where accents are relevant for SQL operations. For example, in Japanese "Seto" \(セト\) and "Zeto" \(ゼト\) would both be valid query results for the "セト" search when using the BINARY\_AI linguistic sort. | \`BINARY\_AI\` |
| Default Query Timeout | Defines the default maximum time \(in seconds\) the platform waits for queries to be executed \(since the database connection is established\). | \`30\` |
|  \*\*1-Click Publish\*\* |  |  |
| Database Update Query Timeout | Defines the default maximum time \(in seconds\) the platform waits for queries to be executed in a 1-Click Publish operation \(since the database connection is established\). | \`600\` |

OutSystems supports Unicode for Oracle databases. To start developing with support for Unicode you just need to ensure that your Oracle database is set to use `AL32UTF8` as the database character set.

## Administrator Section

The 'Administrator' section allows you to configure the database user that manages the platform. This user owns the OutSystems metamodel tables, views, and indexes.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| User | Name of the user that is the owner of OutSystems metamodel tables. | `OSADMIN` |
| Password | Password for the user. |  |
| Tablespace | Table space where the system tables are stored. | `OSSYS` |
| Index Tablespace | Table space where all indexes of the platform are stored. | `OSIDX` |

## Runtime Section

In this section you specify the login for the user that owns user tables.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| User | Name of the user that is the owner of tables created in the development environment. | `OSRUNTIME` |
| Password | Password for the user. |  |
| Tablespace | Table space where tables created in the development environment are stored. | `OSUSR` |

## Create/Upgrade Database Button

To create all the database objects \(tables, indexes, views, etc\) the platform requires, click 'Create/Upgrade Database'.

This button creates all necessary database objects \(tables, indexes, views, stored procedures, etc\) to run the OutSystems Platform Server version you are installing.

To install or upgrade OutSystems, you should follow the installation checklist.

