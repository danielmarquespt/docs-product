# Use the Extension in a Module

All the extensions [published](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-1-cp.md%3E) in the Platform Server can be used by Service Studio developers to expand the functionality or extend the database model of their modules.

To use an extension in your module you must add this extension as a Reference. A module reference is an element \(Action, Entity, or Structure\) exposed and implemented in a Producer module or extension, but that can be invoked from another module, called a Consumer.

## Add an Extension Reference to Your Module

Do the following:

1. Launch Service Studio and open your module.
2. Connect to the Platform Server where the extension was published. Simply use the ![](../../../../.gitbook/assets/connect-server%20%281%29.gif) Select server operation in the File menu or Toolbar.
3. Launch the ![](../../../../.gitbook/assets/add-rem-refs.gif) Add/Remove References window, available in the File menu or in the Toolbar, and select the extension that you want to use.
4. Select the actions, structures, or entities from this window and press the OK button.

## Use the Extension in Your Module

After adding these references to your module, they become available as follows:

* The entities and structures are available in the module tree in Entities and Structures folders, respectively.
* The actions are available in the Tools tree under the Reference Actions folder. All actions with property Function set to Yes, are also available in the Referenced Functions folder, in Service Studio Expression editor.

To use these elements, simply drag and drop them as you'd normally do if they were owned by your module.

