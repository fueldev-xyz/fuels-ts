# 资产转移

本文档介绍了如何使用 SDK 在钱包之间和向合约转移资产的指南。

## 在账户之间转移资产

`account.transfer` 方法用于发起一个转账事务请求，将资产从一个钱包转移到另一个。此方法需要三个参数：

1. 接收方的钱包地址。
2. 要转移的资产数量。
3. 要转移的资产的 ID（可选 - 默认为基本资产 ID）。

执行后，此函数返回一个解析为事务响应的 Promise。要等待事务处理完成，调用 `response.wait()`。

### 示例

下面是如何使用 `account.transfer` 函数的示例：

<<< @/../../docs-snippets/src/guide/cookbook/transferring-assets.test.ts#transferring-assets-1{ts:line-numbers}

在上面的示例中，我们使用了 `transfer` 方法，它本质上创建了一个 `ScriptTransactionRequest`，并将其数据填充到提供的转账信息中，然后提交了事务请求到节点。

然而，有时您可能需要在实际提交到节点之前获得事务 ID。为了实现这一点，您可以简单地调用 `createTransfer` 方法。

此方法也创建了一个 `ScriptTransactionRequest` 并填充了提供的数据，但是它不是将其提交到节点，而是返回请求。

<<< @/../../docs-snippets/src/guide/cookbook/transferring-assets.test.ts#transferring-assets-2{ts:line-numbers}

需要注意的是，一旦您获得了这个事务请求，对其进行的任何修改都将导致一个新的独立事务。因此，这将导致不同的事务 ID。因此，请确保不要更改事务请求，如果您期望 ID 保持不变。

<<< @/../../docs-snippets/src/guide/cookbook/transferring-assets.test.ts#transferring-assets-3{ts:line-numbers}

## 向合约转移资产

当向部署的合约转移资产时，我们使用 `transferToContract` 方法。此方法在参数结构上与 `account.transfer` 方法非常相似。

但是，在转移方法中将目标钱包地址提供给 `destination.address` 时，我们需要提供一个从部署的合约 ID 创建的 [Address](../types/address.md) 实例。

如果您有部署的合约的 [Contract](../contracts/) 实例，您可以简单地使用其 `id` 属性。但是，如果合约是使用 `forc deploy` 部署的，或者不是由您部署的，那么您可能只有其 ID 的十六进制字符串格式。在这种情况下，您可以使用 `Address.fromAddressOrString('0x123...')` 从合约 ID 创建一个 [Address](../types/address.md) 实例。

### 示例

以下是演示如何使用 `transferToContract` 的示例：

<<< @/../../docs-snippets/src/guide/cookbook/transferring-assets.test.ts#transferring-assets-4{ts:line-numbers}

请记住始终在事务响应上调用 `waitForResult()` 函数。这确保了在继续之前事务已成功上链。
