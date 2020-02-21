# Action Parameters Editor

The Action Parameter Editor allows you to edit the [properties](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/element-property/action-parameter.md%3E) of the action parameter that belongs to your extension.

This editor is displayed together with the [Action Editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/editor/action.md%3E).

## Add and Remove Parameters

To **add** a parameter, simply type a new row in this editor or press the ![](../../../../.gitbook/assets/add.gif) button in the editor or in the right menu.

To **remove** a parameter, select the parameter row and press the ![](../../../../.gitbook/assets/delete.gif) button in the editor or in the right menu.

![](../../../../.gitbook/assets/warning%20%281%29.gif) Since actions set as functions \(property Function equal to `Yes`\) must have exactly one output parameter, the remove operation could cause a violation of this rule. Integration Studio prevents it but allows you to automatically change the action to meet the requirements to be a function by setting property Function to No, if you're deleting a single output parameter of a function action.

## Input and Output Parameters

By default, the parameter is an input parameter. To define an Output parameter, simply click on the Input icon ![](../../../../.gitbook/assets/input%20%281%29.gif) and Integration Studio switches to an Output parameter. In fact, both the Input ![](../../../../.gitbook/assets/input.gif) and Output ![](../../../../.gitbook/assets/output.gif) icons have a toggle behavior, allowing you to easily change the type of the parameter.

![](../../../../.gitbook/assets/warning%20%281%29.gif) Since actions set as functions \(property Function equal to `Yes`\) must have exactly one output parameter, this "toggle" operation could cause a violation of this rule. Integration Studio prevents it but allows you to automatically change the action to meet the requirements to be a function:

* By setting the property Function to `No`, if you're adding another output parameter to a function action.
* By setting the property Function to `No`, if you're deleting a single output parameter of a function action.

## Change the Parameters Order

The order of the parameters must be the same in both the extension action and in the corresponding C\# method. The Action Parameter Editor contains the necessary buttons to define the order of the parameters:

| Button | Description |
| :---: | :--- |
| ![](../../../../.gitbook/assets/bottom-one.gif) | Move the selected parameter down. |
| ![](../../../../.gitbook/assets/bottom-all.gif) | Move the selected parameter to the bottom of the list. |
| ![](../../../../.gitbook/assets/top-one.gif) | Move the selected parameter up. |
| ![](../../../../.gitbook/assets/top-all.gif) | Move the selected parameter to the top of the list. |

## Change the Parameter Properties

You can change the properties of the parameter, at any time. Simply double-click in the action in the [Multi-tree navigator](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/workspace.md%3E) or select the action in the [Multi-tab editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/workspace.md%3E) and change the parameter properties.

