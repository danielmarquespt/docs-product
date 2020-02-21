# Refresh an Entity

Once an entity is [added to your extension](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-define.md%3E), the definition of the corresponding table is copied into Integration Studio: columns, data types, and descriptions are imported into the extension. If the table definition changes, for example, if a new column is created, you can refresh the entity definition and retrieve it again from the database.

![](../../../../.gitbook/assets/warning%20%286%29.gif) The entity definition in Integration Studio will be replaced by the information available in the Database. Therefore, all the changes you have made to the entity will be lost. The only property that remains is the name of the entity.

To refresh an entity definition:

* Right-click on the Entities folder and select ![](../../../../.gitbook/assets/refresh.gif) Refresh Entity. Integration Studio connects the database where the corresponding table is stored and fetches the new definition.

You must be [connected to the server](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/extension-life-cycle/server-connect.md%3E) where the extension will be deployed and hosted. The connection between Integration Studio and the database is established through the Platform Server.

If there are invalid attributes names, Integration Studio provides you with a warning where you can see which attributes are invalid. In this situation, the entity definition is refreshed but the invalid attributes are ignored.

![](../../../../.gitbook/assets/tip%20%288%29.gif) If you want to refresh the definition of several entities, you can use the [Import Entity from Database](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-import-from-database.md%3E) wizard.

