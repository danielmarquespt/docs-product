# Define Extension Structures

Integration Studio provides some base data types, such as Integer or Text, but you can define more complex data types using Structures. Once structures are defined, they can be used in the data type definition of parameters and attributes. In such cases, you should use the Record data type or the Record List data type.

A structure is necessary when you are integrating with a component that handles complex data in a .NET class. For example, suppose that, in this component, you have a File class with two attributes: File Name and File Size. In Integration Studio, you may create a Structure with this definition and, afterward, use it in the definition of your records or record lists.

To create a structure do the following:

1. Right-click on the Structures folder in the Multi-tree Navigator and select the ![](../../../../.gitbook/assets/structure.gif) Add Structure option.
2. Specify the following properties:
   * **Name**: name of the structure
   * **Description**: description of the structure

     For more details about these properties, see [Structure Properties](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/element-property/structure.md%3E).
3. Specify the attributes of the structure by simply editing the [Attributes Editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/editor/attributes.md%3E).

![](../../../../.gitbook/assets/tip%20%287%29.gif) The [Structure editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/editor/structure.md%3E) allows you to change the structure properties.

Once the structures are defined and the extension is published on the Platform Server, the Service Studio developer simply needs to add a reference to these structures in order to [use them](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-use.md%3E) in the module.

