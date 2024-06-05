# 交易参数

交易参数允许您配置区块链交易的各个方面。取决于这些参数，可能会引入[交易策略](./transaction-policies.md)。这些参数包括：

1. 燃气价格 - 您愿意为交易执行期间每单位[燃气](https://docs.fueldev.xyz/docs/intro/glossary/#gas)支付的价格。
2. 燃气限制 - 您愿意允许交易消耗的最大燃气量。如果交易将使用的燃气量大于燃气限制，则交易将失败。
3. 最大费用 - 使用基础资产支付交易的最大金额。这是每单位燃气的价格乘以使用的燃气量。
4. 成熟期 - 交易可以被包含在一个块中之前必须经过的块数量。这对于时间敏感的交易非常有用，例如涉及时间锁定资产的交易。
5. 见证人限制 - 交易中允许的最大见证人数量。见证人用于需要多个签名的交易，例如涉及多重签名钱包的交易。
6. 可变输出 - 交易中允许的可变输出数量。可变输出用于具有动态输出数量的交易，例如涉及多个接收方或复杂合约交互的交易。通过设置此值，您可以控制交易中允许的可变输出数量，这对于管理交易大小和复杂性非常有用。

> **注意**：设置交易参数是可选的。如果不指定，SDK 将从链上获取一些合理的默认值。

以下是所有可用参数：

<<< @/../../docs-snippets/src/guide/transactions/transaction-parameters.test.ts#transaction-parameters-1{ts:line-numbers}

## 设置交易参数

要设置交易参数，您可以在交易请求上使用 `txParams` 方法。

<<< @/../../docs-snippets/src/guide/transactions/transaction-parameters.test.ts#transaction-parameters-2{ts:line-numbers}

同样的方法也可以在函数调用作用域内访问，因此在调用合约函数时也可以使用它。

<<< @/../../docs-snippets/src/guide/transactions/transaction-parameters.test.ts#transaction-parameters-3{ts:line-numbers}

> **注意：** 当执行导致交易的操作时（例如合约部署、使用 `.call()` 进行合约调用、资产转移），SDK 将自动根据燃气限制和交易的字节大小估算费用。此估算用于构建交易。作为副作用，您的钱包必须拥有至少一枚基础资产的硬币，无论数量多少。
