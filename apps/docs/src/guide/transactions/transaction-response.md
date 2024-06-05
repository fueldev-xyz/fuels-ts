# 交易响应

一旦提交了交易，您可能想要提取有关交易结果的信息。SDK 提供了一个 `TransactionResponse` 类，其中包含帮助方法来公开以下信息：

- 交易 ID
- 状态 (已提交、成功、被挤出或失败)
- 收据 (返回数据、日志、铸造/销毁、转账和恐慌/回滚)
- 气体费用和使用情况
- 交易的原始载荷，包括输入和输出
- 交易的日期和时间
- 包含交易的区块

首先，我们可以从已提交的交易结果中提取这些信息：

<<< @/../../docs-snippets/src/guide/transactions/transaction-response.test.ts#transaction-response-1{ts:line-numbers}

我们还可以使用交易请求的结果提取交易摘要：

<<< @/../../docs-snippets/src/guide/transactions/transaction-response.test.ts#transaction-response-2{ts:line-numbers}

或者，我们可以从存储的交易 ID 构建交易摘要：

<<< @/../../docs-snippets/src/guide/transactions/transaction-response.test.ts#transaction-response-3{ts:line-numbers}
