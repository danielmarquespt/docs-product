# Unexpected Resource Warning

Message : `The Resource <file> should not be included in the Extension.`

Cause : Issued when you [add a resource](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/resource-define.md%3E) that starts with `OutSystemsHubEdition`, which is a reserved prefix.

Recommendation : Rename the resource filename, excluding the reserved prefix.

Message : `The Resource <file> has a reserved file name and therefore its Deploy Action will be ignored.`

Cause : Issued when you verify an extension that has a resource whose filename is a reserved filename, for example, `compressor` and `web.config`.

Recommendation : Rename the resource filename.

