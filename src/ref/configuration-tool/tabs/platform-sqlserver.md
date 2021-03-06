---
summary: >-
  Platform tab showing specific configuration settings for the SQL Server /
  Azure SQL database provider.
---

# Platform Tab in SQL Server / Azure SQL

In the Database tab, once you set the 'Database Provider' property to 'SQL Server / Azure SQL', the following configurations become available.

## Database Section

This section contains general configurations for the SQL Server / Azure SQL database.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| Server | The hostname or IP address to the database server. | `localhost` |
| Database | The database catalog to be used by OutSystems. | `outsystems` |
| Authentication | Authentication protocol to be used. | `Database Authentication` |

For advanced settings, click on the Advanced Settings link.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
|  \*\*Advanced Connection Settings\*\* |  |  |
| Runtime Applications | Allows you to use a specific connection string for OutSystems applications. |  |
| OutSystems Services | Allows you to use a specific connection string for OutSystems services. |  |
| Default Query Timeout | Sets the default time \(in seconds\) for database queries to complete. The value can be overridden in the development environment, for each query. | 30 |
|  \*\*1-Click Publish\*\* |  |  |
| Database Update Query Timeout | Sets the default time \(in seconds\) for database updates to run when 1-Click publishing an application. | 600 |

## Administrator Section

The 'Administrator' section allows you to configure the database user that manages the platform. This user owns the OutSystems metamodel tables, views, and indexes.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| User | Name of the user that is the owner of OutSystems metamodel tables. | `OSADMIN` |
| Password | Password for the user. |  |

## Runtime Section

The 'Runtime' section allows you to configure the database user used by the applications at runtime. This user owns the tables created by developers in the development environment.

| Configuration | Description | Default value |
| :--- | :--- | :--- |
| User | Name of the user that is the owner of tables created in the development environment. | `OSRUNTIME` |
| Password | Password for the user. |  |

## Create/Upgrade Database Button

To create all the database objects \(tables, indexes, views, etc\) the platform requires, click 'Create/Upgrade Database'.

This button creates all necessary database objects \(tables, indexes, views, stored procedures, etc\) to run the OutSystems Platform Server version you are installing.

To install or upgrade OutSystems, you should follow the installation checklist.

