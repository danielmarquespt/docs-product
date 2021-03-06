---
summary: These are the instructions for implementing your own pagination and sorting.
tags: runtime-reactiveweb;
---

# Table pagination and sorting

Pagination and sorting are the features you get automatically if you create a table by dragging an Entity to the Screen. However, you may choose to implement pagination and sorting manually. Here are the instructions to help you with that.

## Create pagination

Follow these steps to add pagination to your table. You should already have an Aggregate and a Table Widget added to your Screen.

1. Create **MyStartIndex** and **MyMaxRecords** Local Variables of the Integer Data Type. Set the default values of these variables.
2. In the properties of the Aggregate that fetches your data set **StartIndex** to **MyStartIndex**, **Max. Records** to **MyMaxRecords**.

   ![Aggregate index and max records](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/table/images/pagination-aggregate-props.png?width=370%3E)

3. Drag the Pagination Widget below the Table Widget and set **StartIndex** to **MyStartIndex**, **MaxRecords** to **MyMaxRecords**. Also, set **TotalCount** to the Output Parameter `.Count` of the Aggregate.

   ![Paginate Widget Properties](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/table/images/pagination-paginate-props.png?width=370%3E)

4. Still in the Pagination Widget properties, from the **Handler** drop-down list box select **New Client Action**. Action **PaginationOnNavigate** opens.
5. In the Action **PaginationOnNavigate** assign the value of the **NewStartIndex** Input Parameter to **MyStartIndex** \(MyStartIndex = NewStartIndex\). Drag a Refresh Data Tool to the Flow and set it to refresh the Aggregate.

   ![Pagination logic](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/table/images/pagination-logic.png?width=700%3E)

6. Go back to the Pagination Widget properties and confirm that the **NewStartIndex** property is set to **NewStartIndex** from the Event.
7. Publish the module.

## Sorting

Service Studio automatically creates Actions for sorting the columns in a Table. This makes it quick to change how the sorting works, or remove it completely.

### Add sorting to a Table

In the **OnSort** drop-down list box of your Table Widget properties, select **New On Sort Client Action**. A new Action is created with the sorting logic. At this step all table columns are sortable and you can publish the module.

### Change sorting Attribute

You can change the Attribute used for sorting.

1. In the **Widget Tree**, locate the **Header Cell** of the row you want to sort by \(or select the cell in the content editor\).
2. In the **Sort Attribute** drop-down combo box select the Attribute for sorting.

   ![Pagination logic](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/table/images/table-sort-attribute.png?width=370%3E)

3. Publish the module.

### Remove sorting

To remove the sorting feature from the table column, delete the value of the **Sort Attribute** parameter of the **Header Cell** element.

