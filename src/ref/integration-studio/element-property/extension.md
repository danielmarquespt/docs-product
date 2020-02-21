# Extension Properties

To access the properties of an [extension](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-create.md%3E), simply double-click on the extension in the Extension tab, in the [Multi-tree Navigator](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/multi-tree-navigator.md%3E).

The extension properties are explained below.

Name : Name of the extension. See [rules for naming elements](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/element-naming.md%3E).

DBMS : Indicates the Database Management System \(DBMS\) type that the extension is prepared to work with. This property is used during the validation of the extension to, for example, check whether the physical table name associated with an entity is valid or not.

```text
The possible values are: `Oracle`, `SqlServer`, and `(All)`.

Default value: `(All)`.
```

Description : Free text that describes the extension. Useful for documentation and knowledge transfer purposes. The maximum size of this property is 255 characters.

