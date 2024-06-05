# 自定义交易

在某些情况下，您可能需要构建涉及多种程序类型和资产的交易；这可以通过实例化一个 [`ScriptTransactionRequest`](../../api/Account/ScriptTransactionRequest.md) 来实现。这个类允许您将多个程序类型和资产附加到单个交易中。

考虑以下脚本，它将多个资产转移到一个合约中：

<<< @/../../docs-snippets/test/fixtures/forc-projects/script-transfer-to-contract/src/main.sw#custom-transactions-1{ts:line-numbers}

可以通过创建一个 [`ScriptTransactionRequest`](../../api/Account/ScriptTransactionRequest.md)，附加资源和合约输入/输出，然后发送交易来执行这个脚本，如下所示：

<<< @/../../docs-snippets/src/guide/scripts/script-custom-transaction.test.ts#custom-transactions-2{ts:line-numbers}
