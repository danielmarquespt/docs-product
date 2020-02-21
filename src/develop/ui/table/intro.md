---
summary: Show the tabular data with Table.
tags: runtime-reactiveweb;
---

# Creating and editing tables

Use the Table Widget to create a table in your Screens, when you want to show data in cells distributed in rows and columns. This widget is available in Reactive Web Apps.

![Table Widget](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/table/images/table-in-toolbar.png%3E)

## Table Toolbar

When you select a table created with Table Widget, you can us the Table toolbar in the main editor to move, add, or delete the columns.

![Table Widget](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/table/images/table-edit-commands.png%3E)

## Create a table from an Entity

The quickest way to create a table is by dragging an Entity to a Screen. When you create a table by dragging an Entity, the table comes with the built-in features sorting and pagination.

To change the default number of records to show, edit the value of the **MaxRecords** Local Variable associated with the Screen where you dropped the Entity.

![Table Widget](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/table/images/table-from-entity-preview.png?width=700%3E)

## Add a new column

Drag an Attribute to the table to add a new column automatically. Or, follow these steps to add new columns step-by-step.

1. Select the table and click **Add New Column Left** or **Add New Column Right** in the main editor toolbar.
2. Drag a **Text** widget to the header and enter the header text.
3. Drag an **Expression** widget to the column cell and edit the **Expression** to show the data.

