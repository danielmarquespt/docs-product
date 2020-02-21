# Add an Entity

You can manually [add an entity](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-define.md%3E) to your extension as explained below. Integration Studio also provides you the [Import Entities from Database wizard](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-import-from-database.md%3E), which, through introspection, allows you to add several entities with less effort.

To create an entity do the following:

1. Right-click on the Entities folder in the Multi-tree Navigator and select the ![](../../../../.gitbook/assets/entity.gif) Add Entity option.
2. Specify the following properties:
   * **Name**: name of the entity.
   * **Logical Database**: the external database logical name. This name is used in Service Center to map the entity to its physical database.
   * **Physical Table Name**: physical table name.
   * **Identifier**: attribute that uniquely identifies the entity rows.
   * **Description**: description of the entity.
   * **Default Value behavior**: define how the entity's attributes default values are stored in and retrieved from the database regarding being converted to `Null` or not. See [Entity Properties](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/element-property/entity.md%3E) for further information.
3. Specify the **attributes** of the entity by simply editing the [Attributes Editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/editor/attributes.md%3E).

![](../../../../.gitbook/assets/tip.gif) The [Entity editor](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/editor/entity.md%3E) allows you to late change the action properties.

Once the entities are defined and the extension is published on the Platform Server the Service Studio developer simply needs to add a reference to these entities in order to [use them](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/extension-use.md%3E) in the module.

