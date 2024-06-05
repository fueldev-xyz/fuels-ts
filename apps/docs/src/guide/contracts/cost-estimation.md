# 估算合约调用成本

[Provider](../../api/Account/Provider.md) 提供的 `getTransactionCost` 函数允许你估算特定合约调用的成本。返回类型 `TransactionCost` 是一个包含估算相关信息的对象：

<<< @/../../../packages/account/src/providers/provider.ts#cost-estimation-1{ts:line-numbers}

以下示例演示了如何获取以下情况的估算交易成本：

## 1. 单个合约调用交易：

<<< @/../../docs-snippets/src/guide/contracts/cost-estimation.test.ts#cost-estimation-1{ts:line-numbers}

## 2. 多个合约调用交易：

<<< @/../../docs-snippets/src/guide/contracts/cost-estimation.test.ts#cost-estimation-2{ts:line-numbers}

你可以使用交易成本估算来为实际调用设置气体限制，或向用户显示估算成本。