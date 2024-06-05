# 提供者

[`Provider`](../../api/Account/Provider.md) 允许您连接到 Fuel 节点（[*本地*](../getting-started/connecting-to-a-local-node.md)或[*外部*](../getting-started/connecting-to-testnet.md)），并与之交互，封装了 SDK 中的常见客户端操作。这些操作包括查询区块链的网络、块和与交易相关的信息（以及[更多](../../api/Account/Provider.md)），以及向区块链发送[交易](../transactions/index.md)。

所有与区块链交互的高级抽象（例如 [`Wallet`](../wallets/index.md)、[`Contract`](../contracts/index.md)）都经过 `Provider`，因此它用于各种操作，如获取钱包的余额、部署合约、查询其状态等。

<<< @/../../docs-snippets/src/guide/provider/provider.test.ts#provider-definition{ts:line-numbers}

您可以在[此处](./querying-the-chain.md)找到更多关于 `Provider` 使用的示例。
