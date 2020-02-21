# Create an Extension

Integration Studio enables you to create an extension — a set of **Actions**, **Entities**, and **Structures** available in Service Studio but implemented in third-party technologies. An extension can be [used in any module](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-use.md%3E) after it's published in the Platform Server.

To publish a new extension you must be granted the "Change & Deploy Applications" permission.

If you don't have LifeTime installed in your infrastructure, User Management is done in Service Center. In this case, to publish a new extension you must be granted the "Allow Extensions" permission. The "Allow Foreign Entities" permission is also required if your extension exports entities.

## How to create an extension

1. In the File menu or in the Toolbar, click ![](../../../../.gitbook/assets/new.gif) New.
2. Provide the information in the **Connect to Environment** window and click **Connect**. This step is required only once per session.
3. Specify the values for the following properties:
   * **Name**: name of the extension.
   * **DBMS**: indicates the Database Management System \(DBMS\) type that the extension is prepared to work with.
   * **Description**: description of the extension.

You can later change the properties in [Extension Editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/editor/extension.md%3E).

## Extension Elements

After creating the extension, you define [actions](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/action-define.md%3E), [structures](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/structure-define.md%3E), [entities](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-define.md%3E), and [resources](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/resource-define.md%3E) that correspond to the elements exported by the external component you are using.

Integration Studio automatically creates the necessary [source files](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/getting-started/extension-source-files.md%3E) that allow you to start developing the behavior of the actions. You can check them in the [Resources](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/resources-tree.md%3E) tree of this extension.

