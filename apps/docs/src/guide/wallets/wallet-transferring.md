# 钱包转账

本指南演示了如何在帐户和合约之间转移资产，以及在转账之前如何验证您的余额。

## 在钱包之间转账

在 SDK 中，在钱包之间转移资产非常简单。

<<< @/../../docs-snippets/src/guide/wallets/wallet-transferring.test.ts#wallet-transferring-1{ts:line-numbers}

等待交易处理完成后，资产将成功转移到接收者的钱包中。

您还可以将接收者的地址指定为字符串：

<<< @/../../docs-snippets/src/guide/wallets/wallet-transferring.test.ts#wallet-transferring-2{ts:line-numbers}

当转移基本链币种如 ETH 时，您可以省略 `assetId`：

<<< @/../../docs-snippets/src/guide/wallets/wallet-transferring.test.ts#wallet-transferring-3{ts:line-numbers}

## 转账到多个钱包

要将资产转移至多个钱包，使用 `Account.batchTransfer` 方法：

<<< @/../../docs-snippets/src/guide/wallets/wallet-transferring.test.ts#wallet-transferring-6{ts:line-numbers}

## 转账到合约

从您的钱包向部署的合约转移资产非常简单。您只需要合约的地址。

您可以通过使用其 `id` 将资产转移到已部署的合约实例：

<<< @/../../docs-snippets/src/guide/wallets/wallet-transferring.test.ts#wallet-transferring-4{ts:line-numbers}

或者，您可以简单地使用合约的字符串地址，格式为 [`Bech32`](../types/bech32.md)：

<<< @/../../docs-snippets/src/guide/wallets/wallet-transferring.test.ts#wallet-transferring-5{ts:line-numbers}

# 余额

在转移资产之前，请确保您的钱包有足够的资金。如果资金不足，则尝试转账将导致错误：`not enough coins to fit the target`。

您可以查看如何检查您的余额在 [`checking-balances`](./checking-balances.md) 页面。
