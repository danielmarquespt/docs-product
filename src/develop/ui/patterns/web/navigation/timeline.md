---
tags: runtime-traditionalweb;
summary: Timeline indicates related events in chronological order.
---

# Timeline

Indicates related events in chronological order.

Use the Timeline to show related events in chronological order such as an end-user’s upcoming, current and past activities.

**How to use**

1. Drag the Timeline pattern into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/timeline-image-2.png?width=500)

2. Set the content in the placeholders. By default, the pattern comes with a circular icon in the Icon placeholder. To change it, drag an icon widget to this placeholder.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/timeline-image-3.png%3E)

3. Drag as many TimelineItems as required.

## Input Parameters

**Timeline**

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

**Timeline Item**

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Color | Background color of the icon. | Color Identifier | False | Entities.Color.Primary |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/timeline-image-1.png?width=750)

## Advanced Use Case

### Use Timeline with ListRecords

1. Drag the Timeline Pattern into the preview.
2. In the Content placeholder, drag a ListRecords widget.
3. In the ListRecords widget, drag a TimelineItem.
4. In the TimelineItem, use expressions to display the database content you need.
5. To disable the vertical line on the last TimelineItem, write the following CSS code in the application Theme:

   ```css
    .ListRecords .timeline-item:last-of-type .timeline-item-separator {
        display: none;
    }
   ```

6. In the ListRecords Widget, set Line Separator to None to avoid additional margin between elements.
7. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/navigation/images/timeline-image-4.png%3E)

