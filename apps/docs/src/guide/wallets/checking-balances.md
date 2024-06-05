# 检查余额

## 理解 UTXO 模型

在 UTXO（未花费交易输出）模型中，每个币都是唯一的，类似于物理货币的不同面额。

UTXO 表示具有特定金额的硬币，类似于拥有 10 美元或 5 美元钞票。了解 UTXO 的这个独特特性非常重要，因为它与以太坊的基于账户的系统有很大不同。

在以太坊中，余额被跟踪为累积总数，类似于银行账户，而不是作为不同的“硬币”或“钞票”。

## UTXO 的重要性

每个 UTXO 对应于一个唯一的硬币，并带有关联的金额。这种模型允许在加密货币交易中实现更大的透明度和控制。了解 UTXO 对于有效管理和跟踪您的数字资产至关重要。

## 获取钱包余额

要检查特定资产的余额，您可以使用 [`getBalance`](../../api/Account/Account.md#getbalance) 方法。此函数汇总了您钱包中给定资产的所有未花费硬币的金额。

<<< @/../../docs-snippets/src/guide/wallets/checking-balances.test.ts#checking-balances-1{ts:line-numbers}

要检索钱包中所有资产的余额，请使用 [`getBalances`](../../api/Account/Account.md#getbalances) 方法，它返回一个 [`CoinQuantity`](../../api/Account/index.md#coinquantity) 数组。这对于全面了解您的持有非常有用。

<<< @/../../docs-snippets/src/guide/wallets/checking-balances.test.ts#checking-balances-2{ts:line-numbers}
