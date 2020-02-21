---
summary: >-
  Learn how to manage User Groups by modifying the System reference or accessing
  OutSystems database directly.
tags: support-Mobile_Apps; support-webapps
---

# Customize Groups

The Users application does not support Group hierarchies by default so it's not possible to make one group part of another. However, OutSystems was designed to support this by either using the OutSystems platform or an external system.

## Using custom Group management in OutSystems

1. Create a new Application.
2. In the references window find the **Group** entity under **\(System\)**.
3. Model and create entities that reference the Group entity using foreign keys.
4. Design screens to manage these groups.
5. Use a database management tool to connect to the OutSystems database.
6. Edit the records in the `OSSYS_Group` table and, for each group that has these customizations, set its `HasCustomManagement` attribute to `True`. These groups will no longer be visible in the Users application.

## Using external custom Group management

1. Use a database management tool to connect to the OutSystems database.
2. Edit the records in the `OSSYS_Group` table and set the `HasCustomManagement` field to `True` for the groups you want to manage yourself. These groups will no longer be visible in the Users application.
3. Model and create tables that reference the `OSSYS_Group` using the foreign keys.
4. Design your external systems to manage the tables you created.

