# 合约余额

在处理合约时，了解资产的可用合约余额在支付高成本操作时至关重要。本指南将解释 [Contract](../../api/Program/Contract.md) 类中的 `getBalance` 方法，该方法允许你检查合约的可用余额。

## `getBalance` 方法

[`Contract`](../../api/Program/Contract.md) 类包括一个名为 `getBalance` 的方法，用于检索合约的特定资产的可用余额。该方法特别适用于确定向合约发送资产并执行合约调用后的剩余余额。

<<< @/../../../packages/program/src/contract.ts#contract-balance-1{ts:line-numbers}

## 检查合约余额

考虑一个简单的合约，它将指定数量的给定资产转移给一个地址：

<<< @/../../docs-snippets/test/fixtures/forc-projects/transfer-to-address/src/main.sw#contract-balance-2{rust:line-numbers}

`transfer` 函数有三个参数：

1. `amount_to_transfer`：正在转移的数量。

2. `asset`：已部署合约 Token 的地址。

3. `recipient`：接收者钱包的地址。

`transfer` 函数调用了内置的 Sway 函数 `transfer_to_address`，其名称正是其所做的事情。

让我们执行这个合约，并使用 `getBalance` 方法验证合约剩余资产量。

<<< @/../../docs-snippets/src/guide/contracts/contract-balance.test.ts#contract-balance-3{ts:line-numbers}

在这个示例中，我们首先转发一个大于转移所需金额的资产数量，然后执行合约调用。

最后，我们使用 `getBalance` 方法确认合约余额正是总转发金额减去转移金额。

重要提示：该方法返回合约的总可用余额，无论资产已发送多少次或在昂贵操作上花费了多少。