# Add an Action

Once you have created your extension you may manually add the actions that you want to expose in the extension.

Once the actions are defined and the extension is published on the Platform Server, add a reference in Service Studio to these actions, in order to [use them in the module](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-use.md%3E).

Do the following:

1. Right-click on the Actions folder in the Multi-tree Navigator and select the ![](../../../../.gitbook/assets/action.gif) Add Action option.
2. Specify the following properties:
   * **Name**: name of the action
   * **Icon**: icon associated with the action used in Service Studio to graphically identify this action
   * **Description**: description of the action
   * **Function**: when set to `Yes`, allows the action to be used as a user function in Service Studio

     For more details about these properties, see [Action Properties](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/element-property/action.md%3E).
3. Specify the parameters of the action by editing them in the [Action Parameters](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/action-parameter.md%3E) editor.

You can later change any of the action properties, in the [Action editor](../../../ref/integration-studio/editor/action.md#import-details%3E).

Integration Studio also provides the [Import Actions from .Net Assembly](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/net-assembly-import-action.md%3E) wizard that allows you to add several actions with less effort by using introspection.

## Web Services

When creating custom extensions to consume Web Services you can use the Import Actions from a .Net Assembly wizard, which supports Web Service proxies. Learn how to [Import Web Services from a .Net Assembly](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/net-assembly-import-web-service.md%3E).

