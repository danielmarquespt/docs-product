---
summary: >-
  Learn how to validate the information users enter in forms. You can use the
  built-in validation for email, currency, numbers, text — or create your own.
  You can also customize the messages that show next to the invalid values.
tags: >-
  support-application_development; support-Front_end_Development;
  support-Mobile_Apps; support-webapps
---

# Validate the fields of a form

When users enter data in a form and click a submit button, it's recommended to check immediately if the data is valid. If it is, the app can continue. If not, you should tell the users which fields contain the errors and how to fix them.

For example, if your users need to enter their emails in the field, and they enter their name instead — that information is not valid. You can use the built-in capabilities of the app to show the error message and ask the users to retry.

 The client-side validation improves the user experience, as it offers quick feedback about the validity of the input. However, you should always check the data that comes from the client side before you commit that data to the database.

## Using accelerators to create initial validation flow

In OutSystems low-code approach, the **automatic client-side form validation is provided by default for the supported data types**. To use the built-in validations, you need to:

1. Set the data types of the values in the form. You can do this manually or [scaffold the form fields from Entity](form-validate.md#generate-form-fields).
2. Set the fields as mandatory, if required.
3. Trigger an accelerator to create a new Client Action with initial validation flow. To automatically create the logic, select the **New Client Action** from the Event list of the element that submits the data inside the form. Check [this example step to create a new Action](form-validate.md#step-new-action) for a Button.

### Set an input field as mandatory

The field is mandatory if users must enter a value in that field. To set a field as mandatory, select the widget and in the **Properties** pane set the **Mandatory** property to **True**.. Widgets have the **Mandatory** field, for example **Input Widget** or **ButtonGroup Widget**, if their common use case requires it.

![Mandatory property of the input widget](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-mandatory-field-servicestudio.png?width=310)

### Set the data type of a form field

To automatically check whether the value user enters is valid, you first need to tell the app which value you expect. Select the data type from the **Input Type** list in the properties of the widget. There are several Data Types you can choose from, such as Integer, Currency, Date, Time, Email.

![Data type of the input value](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-data-type-servicestudio.png?width=310)

### Enable or disable the built-in validation

To activate the built-in client-side validation, set the **Built-In Validations** property of the **Event** that submits the data to **Yes**. This can be, for example, **On Click** Event of a Button Widget or a Link Widget that calls a Client Action.

![Event with Built-In Validations set to on](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-enable-built-in-validation-servicestudio.png?width=310)

### Validate the data in a Client Action

With the built-in validation enabled, you can access the boolean **Valid** property of the Form Widget in the Client Action that submits the form. For example, if you have a form ReorderItemForm, and a user submits correct data, the value of `ReorderItemForm.Valid` is True. If a check for any of the fields fails, the value of `ReorderItemForm.Valid` is False.

In this example, an **If** node has `ReorderItemForm.Valid` in the **Condition**. If the value of `Valid` is False, the validation fails and the **False** branch of the **If** flow runs.

![The If Node evaluates Valid boolean form the form](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validate-if-node.png?width=500)

 Only the fields you set as mandatory are validated. The fields that you don't set as mandatory are skipped during the validation, as they are considered optional.

## Customizing validation error and warning messages

Here are some ways to edit the validation messages.

### Editing the default validation messages

You can edit the default validation messages on the module level. Go to the module properties by clicking the module name \(1\) in any of the main Service Studio tabs \(**Process**, **Interface**, **Logic**, or **Data**\). Then, locate and edit the messages in the **Validation Messages** section \(2\).

![The list of the default validation messages](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validation-edit-default-messages.png?width=300)

### Changing the field validation messages programmatically

You can change the validation messages for fields during the execution of the app. You do that by assigning a text value to the **ValidationMessage** of the widget. Keep in mind that the message shows only after the validation fails, when the value of **Field.Valid** is **False**.

![Editing the validation message for a field](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validation-custom-message.png?width=400)

## Examples of the client-side validation with accelerators

In this section you can find two examples of the client-side validation.

### Auto-creation of form fields with predefined data types

Insert fields in forms using a low-code accelerator, which can help you be more efficient when you're using Entity as the data source. Follow the steps below.

1. Drag a Form Widget to the Screen.
2. Drag an Entity to the Form Widget. The fields of the form populate automatically.
3. Go through the fields and set **Mandatory** to **Yes** for all fields that are not optional.
4. Select the **Save** button. In the button properties, in the **Events** section, from the **On Click** list select **New Client Action**. A new Action opens, with a default validation logic.
5. Add different logic when **Form.Valid** is **True** or **False**.

The form, fields, and the save button in this Screen were created by dragging an Entity to a Form.

![Auto-created form with data types set for fields](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validate-scaffolding.png?width=500)

### Step by step example

The initial logic for validation is created automatically and can speed up your work significantly. Here is a step by step example in which we show an error to the users if they don't enter valid data. In our example, we have a Screen where users can reorder an item, after entering the following information:

* Name — string, optional
* Email — email address, mandatory
* Quantity — integer, mandatory

Here are the steps to create the UI and basic logic.

1. Create a new app and add a Screen. Name the Screen "ReorderItemScreen".
2. Create three Local Variables, and set their properties like this:

   | Name | Data Type |
   | :--- | :--- |
   | EmployeeName | Text |
   | EmployeeEmail | Email |
   | Quantity | Integer |

   It should look like this, with the Local Variables \(1\) and entered **Name** \(2\) and **Data Type** \(3\) properties.

   ![Local variables in Screen](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-variables-servicestudio.png?width=300)

3. Drag a **Form Widget** to the Screen and name it "ReorderItemForm".
4. Drag three **Input Widgets** to the "ReorderItemForm", and set the properties like this:

   | Name | Variable | Mandatory |
   | :--- | :--- | :--- |
   | Input\_EmployeeName | EmployeeName | No |
   | Input\_EmployeeEmail | EmployeeEmail | Yes |
   | Input\_Quantity | Quantity | Yes |

   Notice how the **Input Type** property changes automatically to match the Variable data type.

5. Drag a Button Widget to the form, below the input fields. Set the label of the button as "Reorder". At the end of this step you should have something like this:

   ![Local variables in Screen](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-fields-button-servicestudio.png?width=600)

   There is a form \(1\), and in it the input fields \(2\) with the properties \(3\). The button \(4\) needs to be inside the form.

   We also added labels on top of the input fields. You can do that by dragging a Label Widget above the Input Widget.

6. Select the button, go to the properties, find the **Event** section, and in it **On Click**. Open the **On Click** list and select **New Client Action**. This triggers an accelerator that creates a Client Action with an initial validation flow.

   ![New client Action for On Click](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validate-create-new-action.png?width=300)

   If you go back to the Screen, you can see that Service Studio created the "ReorderOnClick" Client Action \(1\). Select the "Reorder" button \(2\) and confirm that the **Built-In Validation** property in the **Events** section is set to **Yes** \(3\).

   ![Low-code created by an automated action](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validation-accelerator.png?width=600)

7. Finally, let's edit the flow to show an error message if the user enters invalid data, and a success message when the data is valid. Open the ReorderOnClick and it should look something like this:

   ![Initial flow for validation](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validation-initial-flow.png?width=200)

   Drag a **Message** node from the toolbox to the **False** branch of the **If** node. Enter `"Check if all fields have the correct information and then retry."` in the **Message** property of the Message node, and in the **Type** list select **Error** \(1\). Drag another **Message** node from the toolbox, this time to the **True** branch. Enter `""Item reordered!""` and in the **Type** list select **Success** \(2\).

   ![Validation flow with success and error messages in nodes](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validation-initial-flow-messages.png?width=300)

8. Publish and run the app. If you enter valid data, you now get the success message:

   ![All validations pass](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-test-in-browser-success.png?width=400)

   However, if you enter an email in a format that is not supported, or a float instead of an integer, you get the error message:

   ![A field validations failed](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-test-in-browser-error.png?width=400)

   Note that the name field is optional.

## Creating custom validation logic

The built-in validation for supported data types works automatically as long as you provide information about the expected data type.

If you need to extend the validation mechanism for more complex scenarios, create your validation logic and set the **Valid** variables of the widget fields. If you invalidate any of the fields in the form, that invalidates the entire form \(the value of **Form.Valid** is False\).

### Example of custom validation

In this example, the form contains a field to enter a date for the shipment. The validation logic checks if the date is in the past \(1\), and if it is, the field is marked as not valid \(2\) by `Input_Date.Valid=False`. For better usability a custom message is set in `Input_Date.ValidationMessage`, telling users that the date cannot be in the past \(2\).

![Custom date validation logic](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-custom-validation-logic.png?width=500)

Invalidating the date field invalidates the entire form \(3\), and shows the custom message next to the field. Also, we added an extra feedback message on top of the screen \(4\), before the end of the flow. If the validation logic passes successfully, the Server Action is called to finalize the request by the user \(5\).

Here is the custom validation message in the app running in a browser, with a custom validation message \(1\) and the feedback message after the form validation failed \(2\).

![Custom validation message while the app is running](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-custom-validation-browser.png?width=400)

## Validation in Traditional Web

 This section applies to the Traditional Web Apps, where validation runs on the server side.

Use the server action that is executed when the form is submitted to implement the form validations. Add all validations at the beginning of the action flow:

1. For each validation:    
   1. Add the logic to validate the input value. 
   2. If the validation fails, assign the input’s runtime properties as follows:    
      * `Input.Valid = False`
      * `Input.ValidationMessage = "<your error message>"`
2. Check the value of Form.Valid after all input validations because if any of the inputs is not valid, the form is also not valid:     
   1. Add an If element with the following condition: `Form.Valid`
   2. If `True`, continue the action flow. 
   3. If `False`, end the action flow. The form displays validation messages next to all inputs that are not valid. 

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/forms/images/form-validate-web.png?width=600)

If any of the built-in validations fail or you assign `False` to the Valid runtime property of any field of the form, the Valid property of the form is automatically assigned to `False`. In this case, the validation messages are displayed next to all the corresponding inputs that are not valid.

