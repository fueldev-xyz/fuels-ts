# 资产转移

考虑一个场景，您正在与智能合约进行交互，并且需要将资产转移到接收方的钱包中。`addTransfer`方法使您能够将这些操作无缝地组合到单个交易中。

`addTransfer`方法允许您将资产转移附加到您的合约调用交易中。您可以按照以下示例使用它：

<<< @/../../docs-snippets/src/guide/contracts/add-transfer.test.ts#add-transfer-1{ts:line-numbers}

在上面的示例中，我们首先使用合约调用调用 `echo_u64` 函数。随后，`addTransfer` 被添加到链式调用中，以在交易中包含对 `BaseAssetId` 的 `100` 单位的转移。

## 批量转移

您可以使用 `addBatchTransfer` 将一批转移添加到单个交易中：

<<< @/../../docs-snippets/src/guide/contracts/add-transfer.test.ts#add-transfer-2{ts:line-numbers}