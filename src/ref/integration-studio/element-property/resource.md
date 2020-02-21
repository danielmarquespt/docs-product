# Resource Properties

The next table presents the properties of the [resource](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/resource-define.md%3E) element.

|  Property |  Description |  Optionality |  Default value |  Obs. |
| :--- | :--- | :--- | :--- | :--- |
|  Name |  Name of the resource. |  Mandatory |  |  See \[rules for naming elements\]\(\). |
|  Last Modified |  Date when the file was last modified, since the resource was added or updated. |  |  |  |
|  Deploy Action |  Indicates where, in the Platform Server, the resource is stored when the module that references this extension is published. |  Mandatory |  Depends on the type of the resource you are adding:%% \`Copy to Binaries directory\`: default of DLLs or JARs, configuration and compilation files.%% \`Copy to Application directory\`: default of .NET \`.aspx\` and \`.asmx\` pages, style sheets and JavaScript files.%% \`Copy to Images directory\`: default of image files.%% \`Ignore\`: when the file is not supposed to be published with the module. Used for help files, source code, etc. |  You can change the property value but, in most cases, the default is correct. For more details, see the \[possible values for this property\]\(\). |
|  Description |  Free text that describes the resource. |  Optional |  |  Useful for documentation and knowledge transfer purposes.%% The maximum size of this property is 255 characters. |
|  Import Details... |  Presents information about the import operation. |  Optional |  |  Only available when the resource was added during the Import Actions from .NET Assembly wizard. For more information, see \[Resource Editor\]\(\). |

