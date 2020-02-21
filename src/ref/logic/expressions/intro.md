---
tags: null
---

# Expressions

An Expression is composed of [operands](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/logic/expressions/operands.md%3E) and [operators](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/logic/expressions/operators.md%3E). It may be edited in one of the following ways:

* Typed inline: type the expression in the Expression property box. By using the drop-down list, you can access the variables declared so far.
* Use the Expression editor: to launch this editor, simply use the drop-down in the Expression property box, or double-click the Expression property or the widget element itself.

## Handling an expression

* There are many functions to manipulate the type `Text`, but the only operand that can be used directly over text is "+", which concatenates the left operand \(string\) with the right operand \(also a string\).
* You cannot use any of the numeric operators to handle the types `Date`, `Time`, and `DateTime`. There are specific [built-in functions](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Date%20and%20Time.final.md%3E) to handle these types.
* You cannot make any calculation on the type `BinaryData`.
* You cannot make any calculation on the type `Identifier`. There are specific [built-in functions](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/lang/auto/builtinfunction.Data%20Conversion.final.md%3E) to handle this type.
* You can only use the operators "=" and "&lt;&gt;" for the type `Record`.
* You cannot make any calculations on the type `Record List`.

