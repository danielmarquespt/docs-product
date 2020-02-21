# Action Properties

The next table presents the properties of the [action](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/integration-studio/managing-extensions/action-define.md%3E) element.

|  Property |  Description |  Optionality |  Default value |  Obs. |
| :--- | :--- | :--- | :--- | :--- |
|  Name |  Name of the action. |  Mandatory |  \`Action\` |  See \[rules for naming elements\]\(\). |
|  Icon |  Icon associated with the action. This icon will be used in Service Studio to graphically identify this action. |  |  By default, Integration Studio associates an icon with the extension action. If the action was initially created in this tool, then the icon associated is !\[\]\(images/action.gif\) \`\(Default\)\`. If the action was imported from a .NET assembly, then the default icon associated is !\[\]\(images/imported-action.gif\). |  See how to \[change the action icon\]\(\). |
|  Description |  Free text that describes the action. |  Optional |  |  Useful for documentation and knowledge transfer purposes. The maximum size of this property is 255 characters. |
|  Function |  Indicates whether this action can be used as a user function in expressions, in Service Studio. |  Mandatory |  No |  |
|  Import Details... |  Presents information about the import operation. |  Optional |  |  Only available when the action was added during the Import Actions from .NET Assembly wizard. For more information, see \[Action editor\]\(\). |

