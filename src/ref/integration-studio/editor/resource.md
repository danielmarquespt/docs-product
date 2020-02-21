# Resource Editor

The Resource Editor allows you to edit the properties of a resource that belongs to your extension. This editor is displayed when a resource is selected in the [Resources tree](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/resources-tree.md%3E) or in the [Multi-tab Editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/multi-tab-editors.md%3E).

## Resource Storage

The value of the Deploy Action property indicates where the resource is stored when the module that added a reference to this extension is published. The next table describes the possible values, their behavior, and in what types of files they should be used.

|  Deploy Action |  Description |  Files extensions |
| :--- | :--- | :--- |
|  Copy to Binaries directory |  The resources are copied to the Platform Server where the module is published. The files are stored in the \`bin2\` directory, under the module directory. !\[\]\(images/note.gif\) Files stored in this directory are not accessible through the Internet browser. |  dll, config, manifest, jar |
|  Copy to Application directory |  The resources are copied to the Platform Server where the module is published. The files are stored in the module directory. |  css, js, asmx, aspx |
|  Copy to Images directory |  The resources are copied to the Platform Server where the module is published. The files are stored in the \`img\` directory under the module directory. |  bmp, eps, jpg, jpeg, gif, tiff, ico and other image format files |
|  Ignore |  The resources are not copied to the Platform Server. They belong to the extension but are not available in the server. |  source files, documentation, etc. |

![](../../../../.gitbook/assets/warning%20%285%29.gif) You can change the Deploy Action property but this operation should be done with care because if a DLL or a JAR is not copied to the Binaries directory, the module won't be able to use the actions implemented by that DLL or JAR.

## Comparing with Template

Integration Studio has the necessary mechanisms for merging the changes in Integration Studio and the IDE \(Integrated Development Environment\), through the [Update Source Code](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-update-source-code.md%3E) operation.

The [Resources tree](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/resources-tree.md%3E) contains the ![](../../../../.gitbook/assets/resource-compare%20%281%29.gif) Compare With Template operation, which allows you to compare the differences between the resource file, stored in the file system, and the template file.

To use this operation, you have to specify the "Compare files using" parameter in the [Options Window](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/menu/edit/options.md%3E).

![](../../../../.gitbook/assets/tip%20%286%29.gif) The "Compare With Template" operation is very useful if the changes made in the extension elements are more complex and it becomes impossible to merge the two definitions. For example, if you changed the name of an element, it is not possible for the merge operation to relate the two elements.

## Change a Resource's Properties

You can change the properties of a resource at any time. Simply double-click in the resource in the [Resources tree](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/resources-tree.md%3E) or select the resource in the [Multi-tab editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/multi-tab-editors.md%3E), if the resource editor is already opened.

Import Details : This button is enabled when this resource was added due to [importing actions from a .NET assembly](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/net-assembly-import-action.md%3E) and displays a report where you can check for additional information. The following information is displayed:

* Resource: Name of the resource with the following syntax:

  `Resource <resource_name>: <additional_information>`

