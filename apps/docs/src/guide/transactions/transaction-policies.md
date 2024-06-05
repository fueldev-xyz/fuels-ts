# 交易策略

交易策略是可以规定交易如何处理的规则，由您传递给交易请求的[交易参数](./transaction-parameters.md)引入。可用的策略如下：

1. 燃气价格 - 交易的最大燃气价格。
2. 见证人限制 - 交易允许的见证人数据的最大数量。
3. 成熟期 - 交易不能被包含的区块。
4. 最大费用 - 该交易可支付的最大费用。

## 设置交易策略

下面的片段将显示哪些交易参数设置了哪些策略：

<<< @/../../docs-snippets/src/guide/transactions/transaction-policies.test.ts#transaction-policies-1{ts:line-numbers}

## 从交易中检索交易策略

可以使用 `TransactionResponse` 从交易中检索用于交易的策略。下面的片段将显示如何从交易中检索策略：

<<< @/../../docs-snippets/src/guide/transactions/transaction-policies.test.ts#transaction-policies-2{ts:line-numbers}
