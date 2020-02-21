# Verify Window

The Verify window ![](../../../../../.gitbook/assets/validate%20%282%29.gif) is launched when you are [verifying](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-verify.md%3E) your extension.

The areas and buttons available in the Verify window are presented below.

Verify log : In this area you can watch the evolution of the verify operation. You have a line for each step involved in the verify: [Verify the extension definition](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-verify-definition.md%3E), [Update Source Code](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-update-source-code.md%3E), and [Compile](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-compile.md%3E).

```text
If any errors occurred during the Verify, for example the extension has an error, the process stops and you have to fix them in order to proceed. The Verify window provides you with the necessary interface to continue the process, after fixing the detected error. If any warnings occur during the Verify, they are listed in the Verify window, with each warning on a different line, but the process continues.

Each error, warning, or piece of information is displayed on a separate line. On each line you have the category (error, warning or information), a small description and the details of the message. If the details are too long, you can check it in the Details area. The last line indicates the number of errors and warnings found.

To determine exactly where this error or warning occurs, simply select the corresponding line, double-click the message or click on the ellipsis button at the end.
```

Detail : Presents a complete description of the error, warning, or information.

Progress Bar : Displays the progress of the operation.

Verify Again : Performs a new verification considering the fixes that have already been made. This operation is available when the extension has errors that you have to fix.

Save : This operation belongs to the [1-Click Publish operation](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-1-cp.md%3E).

Upload : This operation belongs to the [1-Click Publish operation](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-1-cp.md%3E).

Publish : This operation belongs to the [1-Click Publish operation](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-1-cp.md%3E).

Close : Closes the Verify window with no further action.

