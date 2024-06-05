# 查询链

一旦您设置了提供者，就可以与 Fuel 区块链进行交互了。

我们可以连接到 _*本地*_ 或 _*外部*_ 节点：

> 1. _运行[本地节点](../getting-started/connecting-to-a-local-node.md)_
> 2. _连接到[外部节点](../getting-started/connecting-to-testnet.md)_

让我们来看一些示例。

## 获取基础资产ID

基础资产是用于在链上执行任何交易的基础资产。应该从提供者中获取，然后在交易中使用。

<<< @/../../docs-snippets/src/guide/provider/provider.test.ts#provider-getBaseAssetId{ts:line-numbers}

## 从地址获取所有硬币

此方法返回钱包中的所有硬币（可选给定资产ID），包括已花费的硬币。

<<< @/../../docs-snippets/src/guide/provider/querying-the-chain.test.ts#wallet-query{ts:line-numbers}

## 从地址获取可花费的资源

最后一个参数表示您想要花费多少。此方法仅返回可花费的、即未花费的硬币（给定资产ID）。如果您要求可花费的金额大于您拥有的未花费硬币的金额，则会返回错误。

<<< @/../../docs-snippets/src/guide/provider/querying-the-chain.test.ts#wallet-get-spendable-resources{ts:line-numbers}

## 从地址获取余额

获取地址的所有可花费资产的余额。这与获取硬币不同，因为我们只返回数字（每个资产ID的UTXO硬币金额总和），而不返回UTXO硬币本身。

<<< @/../../docs-snippets/src/guide/provider/querying-the-chain.test.ts#wallet-get-balances{ts:line-numbers}

## 获取区块

此方法返回与给定查询匹配的区块链上的所有块。下面的代码片段显示如何获取最后 10 个块。

<<< @/../../docs-snippets/src/guide/provider/querying-the-chain.test.ts#Provider-get-blocks{ts:line-numbers}

## 通过其 nonce 获取消息

您可以使用 `getMessageByNonce` 方法通过其 nonce 检索消息。

<<< @/../../docs-snippets/src/guide/provider/querying-the-chain.test.ts#getMessageByNonce{ts:line-numbers}


<!-- TODO: fix these examples to not reference hardcoded values after #1356 which introduces message generation tools
### Get messages

You can use the `getMessages` method to retrieve a list of messages from the blockchain.

<<< @/../../docs-snippets/src/guide/provider/querying-the-chain.test.ts#Message-getMessages{ts:line-numbers}

## Get resources

You can use the `getResourcesToSpend` method to retrieve a list of all the resources (coins + assets) that can be spent by a given address.

<<< @/../../docs-snippets/src/guide/provider/querying-the-chain.test.ts#Message-getResourcesToSpend{ts:line-numbers}

## Get message proof

A message proof is a cryptographic proof that a message was included in a block. You can use the `getMessageProof` method to retrieve a message proof for a given transaction ID and message ID.

<<< @/../../docs-snippets/src/guide/provider/querying-the-chain.test.ts#Message-getMessageProof{ts:line-numbers}

--->

<!-- TODO: Add docs for the two new parameters `commitBlockId` and `commitBlockHeight` -->
