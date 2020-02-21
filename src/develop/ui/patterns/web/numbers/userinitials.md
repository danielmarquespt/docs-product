---
tags: runtime-traditionalweb;
summary: UserInitials display user information in a circular badge.
---

# UserInitials

Display user information in a circular badge.

Use the User Initials to identify the users by their initials or an image in a circular badge.

**How to use**

Add the pattern to your screen and provide the username in the Name property to display the user initials.

1. Drag the UserInitials pattern into the preview.
2. Set the Input Parameters to extend the default values.
3. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/userinitials-image-1.png%3E)

## Input Parameters

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| Name | The username to be used in the pattern. | Text | False | JD |
| Color | Set the color. | Color Identifier | False | Entities.Color.Primary |
| Shape | Set the shape. | Shape Identifier | False | Entities.Shape.Rounded |
| Size | Set the size. | Size Identifier | False | none |
| IsLight | Use the lightest color version for the background and the darker color version for the text. | Boolean | False | False |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/userinitials-image-2.png%3E)

## Advanced Use Case

### Use UserInitials on tables

1. Drag the Users table into preview.
2. Remove the expression from the Name and drag the UserInitials pattern to it.
3. In the UserInititals, set the name parameter to the value of the name field from the database.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/userinitials-image-3.png%3E)

4. Change the pattern values.
5. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/userinitials-image-4.png%3E)

### Use UserInitials on IF conditions

1. Create a custom class called "table-image-size".

```css
.table-image-size {
    height: 100px;
    width: 100px;
}
```

1. Drag the Users Entity into the preview.
2. Remove the expression from the Name and drag a container into the cell.
3. Drag an IF condition tool into the container and set the condition to `UserTable.List.Current.User.Is_Active`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/userinitials-image-5.png%3E)

4. In the True branch, drag the UserInitials pattern and set the name parameter to the value of the name field from the database.
5. To adapt the UserInitials to the size of container, set the ExtendedClass parameter to `full-width full-height`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/userinitials-image-6.png%3E)

6. In the False branch, drag an image and set the Style Classes to `border-radius-circle`.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/userinitials-image-7.png%3E)

7. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/numbers/images/userinitials-image-8.png?width=750%3E)

