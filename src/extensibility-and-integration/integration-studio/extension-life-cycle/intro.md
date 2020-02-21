# Extension Life Cycle

The integration process revolves around the extension life cycle. The process steps are executed in both OutSystems and third party IDE component environments. The illustration below depicts the most significant steps, showing them next to the component where they are executed.

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/images/extension-life-cycle.png%3E)

These are the generic steps that you should take to implement and use a extension in OutSystems:

1. In **Integration Studio**, [create a new extension module](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-create.md%3E) and set its name and the supported DBMS.
2. [Define the new actions](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-define.md%3E) that will encapsulate your code. Also define any input and output parameters for your action\(s\), as well as any entities or structures.
3. Generate the stubs for the declared actions and edit the code implementing the logic of the actions using a **third party IDE** for .NET.

   Integration Studio provides the necessary facilities to integrate with the IDE you specified in Integration Studio [options](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/menu/edit/options.md%3E), enabling you to:

   * [Implement the logic  of your actions](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-code.md%3E) using the IDE
   * [Edit the extension source code](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-code-edit.md%3E) using the IDE
   * [Update the extension source code](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-update-source-code.md%3E) with the extension definition in order to reflect the changes you have made in Integration Studio

     If your extension does not contain [manually added](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/action-add.md%3E) actions, you can skip this step. However, the extension will still have source code files associated. See [Extension Source Files](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/getting-started/extension-source-files.md%3E) for more information.

4. [Publish the extension module](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-1-cp.md%3E) to the Platform Server from Integration Studio by clicking 1-Click Publish ![](../../../../.gitbook/assets/1-click-publish-icon%20%283%29.gif) in the File menu or Toolbar.
5. [Use the created extension](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-use.md%3E) in any OutSystems applications where you want to use it, adding it as a dependency in **Service Studio**. Once the extension module is a dependency of your application, the logic that the module implements becomes available in the Logic tab of Service Studio.

