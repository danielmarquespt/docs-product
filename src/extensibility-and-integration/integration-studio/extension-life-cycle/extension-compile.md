# Compile the Extension

The Compile operation generates the main DLL \(Dynamic Link Library\) of the extension. The .NET Compiler Tool is launched in background, and then opens the .NET solution of that extension and finally builds the solution. The solution is compiled according to the .NET Compiler Options you specify in the [Options window](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/integration-studio/menu/edit/options.md%3E).

Even if your extension contains only entities, this step is executed and a DLL file is generated with the entities definition.

