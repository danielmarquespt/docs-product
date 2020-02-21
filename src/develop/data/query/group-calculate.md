---
summary: Use aggregate functions to calculate values based on groups of identical data.
tags: support-application_development; support-Database; support-webapps
---

# Calculate Values from Grouped Data

Putting data into groups to calculate aggregated values allows you to extract more information from your data sets. In OutSystems, you can use aggregate functions to calculate values based on groups of identical data. [Fetch the data](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/data/query/fetch-display.md%3E) in an aggregate and do the following:

1. In the attribute with identical data, use the ![Aggregate Menu](../../../../.gitbook/assets/aggregate-menu%20%282%29.png) menu and select Group by &lt;attribute&gt;.
2. In the attribute to calculate, use the  ![Aggregate Menu](../../../../.gitbook/assets/aggregate-menu.png) menu and select an aggregate function such as Count. 

Once you group or use aggregate functions on attributes, those attributes become the only output of the aggregate.

## Example

In the GoOutWeb application to find, review, and rate places, we want to show the average rating of places to help to take a decision. Consider we already have an aggregate that fetches all the reviews of a place from the database. Open the aggregate and do the following:

1. On the Place.Id attribute, open the ![Aggregate Menu](../../../../.gitbook/assets/aggregate-menu%20%283%29.png) menu and choose Group By Id.

   ![](../../../../.gitbook/assets/group-calculate.png)

2. On the Review.Rate attribute, open the ![Aggregate Menu](../../../../.gitbook/assets/aggregate-menu%20%281%29.png) menu and choose Average.
3. Use the calculated values to display the average rating for each place on the screen.

