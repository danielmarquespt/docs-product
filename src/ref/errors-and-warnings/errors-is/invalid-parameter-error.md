# Invalid Parameter Error

Message : `<parameter> data type is invalid.`

Cause : The data type of the parameter is not valid.

Recommendation : Edit the [action parameter](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/action-parameter.md%3E) and set a valid data type for it.

Message : `'<parameter>' data type is invalid: '<entity>' has no attribute set as Identifier.`

Cause : The attribute set in the output parameter is not an Identifier attribute and there's no Identifier attribute defined in the entity.

Recommendation : Edit the [entity](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/entity-define.md%3E), define the Identifier attribute, and set it on the [action parameter](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/action-parameter.md%3E).

Message : `<parameter> must be set as 'Input' to use 'Mandatory'.`

Cause : The output parameter is set as Mandatory but only input parameters can be set as Mandatory.

Recommendation : Edit the [action parameter](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/action-parameter.md%3E) and un-set it as mandatory.

