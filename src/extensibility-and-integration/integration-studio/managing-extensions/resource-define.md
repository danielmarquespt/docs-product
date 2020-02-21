# Define Resources

Once you have created your extension, simply define the resources that your extension requires. The resources of your extension are displayed in the [Resources tree](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/resources-tree.md%3E).

All these resources are packed in the XIF \(Extension and Integration Framework\) file when the extension is saved.

The resources can be added implicitly by Integration Studio; or you can add any file as a resource of your extension. For example, icons associated with the extension actions or help files that must be available for Service Studio developers.

When creating a new extension or updating the extension source code, Integration Studio implicitly adds the source files as resources, which are generated based on the template files. For more information, see [Extension Source Files](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/getting-started/extension-source-files.md%3E).

To add a resource do the following:

1. Copy the file you want to add to the resources directory. Once the file is copied, the status of the resource, in the [Resources tree](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/resources-tree.md%3E), is ![](../../../../.gitbook/assets/resource-faded%20%281%29.gif) Excluded.

   ![](../../../../.gitbook/assets/tip%20%282%29.gif) To determine the resources directory, right-click in the Resources icon and select the Open option.

2. Right-click on this file and select the ![](../../../../.gitbook/assets/resource-include.gif) Include in Extension option. Once the file is added as resource, the status is ![](../../../../.gitbook/assets/resource-add%20%281%29.gif) Included.
3. Specify the following properties:
   * **Name**: name of the resource.
   * **Last Modified**: Read-only property that indicates the date and time when the resource was last modified since the last save.
   * **Deploy Action**: indicates where, in the Platform Server, the resource is stored when the module that added the extension is published.
   * **Description**: description of the resource.

![](../../../../.gitbook/assets/tip.gif) The [Resource editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/editor/resource.md%3E) allows you to later change the resource properties.

