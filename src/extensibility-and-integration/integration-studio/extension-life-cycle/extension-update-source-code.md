# Update the Extension Source Code

The Update Source Code operation synchronizes the source code you added in the .NET IDE with the definition of the extension elements. This operation involves the following steps:

1. **Generate the template files** according to the definition of your [actions](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/action-define.md%3E), [structures](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/structure-define.md%3E), and [entities](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-define.md%3E).

   If one of these files does not exist as an extension resource, then this operation implicitly adds the file as a resource, except when the extension does not contain any [source files](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/getting-started/extension-source-files.md%3E) at all.

2. **Update** the [extension implementation files](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/getting-started/extension-source-files.md%3E), according to the extension definition in Integration Studio.

    Any changes you have made directly in these files are overridden in this step.

3. **Merge** the `<extension_name>.cs` file. This operation updates the signatures of the methods with the action definition, but it is applied only to the signatures: the body of the methods remains as is.

    Any changes you have made in the signatures of the methods directly in the IDE are overridden in this step.

## How to update the extension source code

In the File menu or Toolbar, click Update Source Code ![](../../../../.gitbook/assets/update-source-code%20%282%29.gif) or [1-Click Publish](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-1-cp.md%3E) ![](../../../../.gitbook/assets/1-click-publish-icon%20%283%29.gif).

![](../../../../.gitbook/assets/tip%20%2810%29.gif) The Update Source Code operation is also executed when you [edit source code](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-code-edit.md%3E) or [verify](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-verify.md%3E) the extension.

## Merge Algorithm

The merge algorithm is responsible for updating the source code with the changes made in the extension definition. The next steps describe the merge algorithm:

* Scan the source files that contain the signatures of the actions and, by name, verifies whether the signatures in these files are according to the action definition in Integration Studio.

  To perform this verification, Integration Studio compares the content of the actions template, generated previously, and `<extension_name>.cs`:

  1. If the signature in the template is the same as in the source file, then proceed to next action.
  2. If the signature in the template is different from the source file, then update `<extension_name>.cs` with the new definition as defined in the template.
  3. If the signature in the template does not exist in the source file, then add the new definition as defined in the template to `<extension_name>.cs`.

In some situations, the Merge algorithm might not be able to establish the correspondence between an element in the template file and in the source files, for example if you change an action name. In this situation, you should use the [Compare with Template](../../../ref/integration-studio/editor/resource.md#comparing-with-template%3E) operation.

