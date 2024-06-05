# 通过合约调用创建自定义交易

在上一个示例中，我们演示了如何实例化一个 [`ScriptTransactionRequest`](../../api/Account/ScriptTransactionRequest.md) 来通过脚本定制并构建一个更复杂的交易。同样的方法也适用于合约，但这样做可以利用合约中可用的函数并访问链上状态。这样我们就可以利用调用作用域和交易请求的全部功能。

这个示例演示了如何利用合约调用来构建自定义交易，允许我们更新链上状态并将资产转移到接收地址。

<<< @/../../docs-snippets/src/guide/cookbook/custom-transactions-contract-calls.test.ts#custom-transactions-contract-calls{ts:line-numbers}
