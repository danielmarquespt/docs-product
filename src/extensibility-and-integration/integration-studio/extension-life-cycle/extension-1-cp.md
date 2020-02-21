# 1-Click Publish the Extension

The 1-Click Publish executes, in a single step, all the operations necessary to publish an extension in a Platform Server.

## 1-Click Publish Operations

The 1-Click Publish involves the following operations:

Verify : Checks whether the extension is valid. For more information, see [Verify the Extension](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-verify.md%3E).

Update Source Code : Synchronizes the source code you added in the .NET IDE with the definition of the extension elements. See [Update the Extension Source Code](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-update-source-code.md%3E).

Compile : Generates the main DLL \(Dynamic Link Library\) of the extension. See [Compile the Extension](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-compile.md%3E).

Save : Saves the extension and packs all the resources in an XIF \(Extension and Integration Framework\) file.

Upload : Uploads the extension to the Platform Server you are connected to.

Publish : Publishes the extension in the Platform Server you are connected to. This operation makes the extension available in this Platform Server.

## 1-Click Publishing

To execute the 1-Click Publish follow the steps below:

1. In the File menu or Toolbar, select 1-Click Publish ![](../../../../.gitbook/assets/1-click-publish-icon%20%283%29.gif).

   This operation requires that you be connect to the server where the extension will be deployed and hosted. If you are not yet connected, Integration Studio automatically prompts you to select a server, after which it establishes the connection. See how to [Select Server window](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/menu/file/server-select-window.md%3E).

2. Check the [1-Click Publish Window](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/menu/file/extension-1-cp-window.md%3E) to see how the process is going.

## 1-Click Publish Access Rights

To publish a new extension you must be granted the "Change & Deploy Applications" permission.

 If you don't have LifeTime installed in your infrastructure, User Management is done in Service Center. In this case, to publish a new extension you must be granted the "Allow Extensions" permission. The "Allow Foreign Entities" permission is also required if your extension exports entities.

