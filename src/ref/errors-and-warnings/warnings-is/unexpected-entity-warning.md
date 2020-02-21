# Unexpected Entity Warning

Message : `<entity> should not be exclusively composed of an 'Auto Number' attribute.`

Cause : You have an entity with just one sequential attribute and this situation is not allowed by some of databases supported by OutSystems.

Recommendation : Depending on your requirements, either add a new attribute to your entity; or un-check the Auto Number property. Learn more about [entity attributes](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-attribute.md%3E).

Message : `<entity> should only have one attribute of 'Binary Data' data type.`

Cause : Your entity has more than one Binary data attributes and this situation is not supported by the database.

Recommendation : Depending on your requirements, either change the data type of one of these attributes or [create](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-add.md%3E) a new entity and move one of these attributes to this new entity.

Message : `<table> is an invalid table name in <database>.`

Cause : The physical table name you specified has an invalid table for SQL Server and/or Oracle databases.

Recommendation : [Edit this entity](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-add.md%3E) and specify the Table Name property.

