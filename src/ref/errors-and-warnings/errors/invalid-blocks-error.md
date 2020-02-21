# Invalid Blocks Error

The `Invalid Blocks` error is issued in the following situations:

* `Block loop detected`

  `<webBlock1>` -&gt; `<webBlock2>` -&gt; ... -&gt; `<webBlockN>` -&gt; `<webBlock1>`

  You have a sequence of nested web blocks where one of the web blocks is including a prior web block originating a loop.

  Review the web blocks include sequence in order to break the loop.

  To help you identify the problematic web blocks, the error message lists the include sequence. Here you can identify which web blocks include which web blocks.

  Take note that the web block name detail depends on the module operation being done:

  **In the TrueChange tab**

  The web block name is displayed prefixed with the Screen Flow name where it is defined: `<flow>\<web block>`.

  The web block's include sequence will look like:

  `<flowX>\<webBlockA>` -&gt; `<flowY>\<webBlockB>` -&gt; ... -&gt; `<flowZ>\<webBlockC>` -&gt; `<flowX>\<webBlockA>`

  You should read it as:

  Block `<webBlockA>` defined in Flow `<flowX>` includes

  Block `<webBlockB>` defined in Flow `<flowY>` that includes

  ...

  Block `<webBlockC>` defined in Flow `<flowZ>` that includes

  Block `<webBlockA>` defined in Flow `<flowX>`

  If the web block name is shown as `(hidden)`, it means that the web block is in another module and is not visible to your module. This happens when you include another module's public web block that has included a private web block of that same module.

  **In the 1-Click Publish operation \(Compile Step\)**

  The web block name is displayed prefixed with the module name and the Flow name where it is defined: `<module>\<flow>\<web block>`.

  The web block's include sequence will look like:

  `<module1>\<flowX>\<webBlockA>` -&gt; `<module2>\<flowY>\<webBlockB>` -&gt; ... -&gt; `<module3>\<flowZ>\<webBlockC>` -&gt; `<module1>\<flowX>\<webBlockA>`

  You should read it as:

  Block `<webBlockA>` defined in Flow `<flowX>` of the module `<module1>` includes

  Block `<webBlockB>` defined in Flow `<flowY>` of the module `<module2>` that includes

  ...

  Block `<webBlockC>` defined in Flow `<flowZ>` of the module `<module3>` that includes

  Block `<webBlockA>` defined in Flow `<flowX>` of the module `<module1>`

Double-click on the error line to take you directly to select the first invalid web block in the sequence.

