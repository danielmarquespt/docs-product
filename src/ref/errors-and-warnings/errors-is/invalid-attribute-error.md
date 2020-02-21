# Invalid Attribute Error

Message : `'<attribute>' data type is invalid.`

Cause : The data type of the attribute is not valid.

Recommendation : Edit the [entity attribute](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-attribute.md%3E) or structure attribute and set a valid data type for it.

Message : `'<attribute>' data type is invalid: '<entity>' has no attribute set as Identifier.`

Cause : The attribute set in the Identifier property in not an Identifier attribute and there's no Identifier attribute defined in the entity.

Recommendation : Edit the [entity](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-define.md%3E), define the Identifier attribute, and set it on the Identifier property.

Message : `<attribute> data type must be set to 'Integer' to use 'Auto Number'.`

Cause : The attribute is set as `Auto Number` but you can only use Auto Numbers with attributes of `Integer` data type.

Recommendation : Edit the [entity attribute](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-attribute.md%3E) and either set its data type to `Integer` or disable it as `Auto Number`.

