# 交易

交易是与 Fuel 区块链进行交互的一种方式，可以包括转移资产、部署合约和铸造代币等操作。通过 SDK，可以使用简单的实用方法或构建更定制的交易来执行所有这些操作。

转移资产是最常见的交易类型，可以通过从一个账户调用 `transfer` 函数到接收者地址来执行：

<<< @/../../docs-snippets/src/guide/transactions/transactions.test.ts#transactions-1{ts:line-numbers}

部署和与合约交互是其他常见的交易。有关更多信息，请参阅[合约指南](../contracts/index.md)，可以通过[合约部署指南](../contracts/deploying-contracts.md)或[合约方法指南](../contracts/methods.md)了解更多信息。

本指南将讨论如何创建和修改交易以适应特定的用例，以及使用交易策略和参数将其提交到网络。以及检索有关已提交交易的信息。
