# 交易请求

交易请求提供了提交交易和与区块链交互的基础。

在 Fuel 中，我们有以下类型的交易：

- 脚本 (Script)
- 创建 (Create)
- 铸币 (Mint)

SDK 提供了处理脚本和创建交易的类助手：`ScriptTransactionRequest` 和 `CreateTransactionRequest`。

> **注意**: 铸币交易只能由区块生产者创建，并且在区块创建之外没有任何用途。因此，SDK 仅提供了解码铸币交易的功能。

## 创建交易请求

要创建交易请求，您首先必须实例化 `ScriptTransactionRequest` 或 `CreateTransactionRequest` 中的一个。

`ScriptTransactionRequest` 用于脚本交易，允许您在链上执行字节码以执行任务或任务链。在 SDK 中，它们可以这样创建：

<<< @/../../docs-snippets/src/guide/transactions/transaction-request.test.ts#transaction-request-1{ts:line-numbers}

`CreateTransactionRequest` 用于创建交易，这些交易会在区块链上创建一个新的合约。

<<< @/../../docs-snippets/src/guide/transactions/transaction-request.test.ts#transaction-request-2{ts:line-numbers}

> **注意**: 我们建议您使用 `ContractFactory` 来部署合约，因为这将为您塑造创建交易请求。有关此信息，请参阅[合约部署指南](../contracts/deploying-contracts.md#4-deploying-the-contract)。

## 修改交易请求

一旦实例化了交易请求，就可以通过设置交易参数和策略来修改它。这可以通过直接修改交易请求对象手动完成，也可以通过上述类上可用的辅助方法完成。

### 向交易请求添加资源

资源填充了交易请求的输入和输出。这可以采取硬币、消息或合约的形式。SDK 提供了一系列处理资源的方法。以下将详细说明如何将硬币和消息添加到交易请求中。

<<< @/../../docs-snippets/src/guide/transactions/transaction-request.test.ts#transaction-request-3{ts:line-numbers}

### 向交易请求添加合约

脚本可以在链上执行多个操作，因此您可能希望链式调用合约。为此，您需要将合约添加到交易请求中。可以像这样添加：

<<< @/../../docs-snippets/src/guide/transactions/transaction-request.test.ts#transaction-request-4{ts:line-numbers}

### 向交易请求添加断言

断言用于定义执行交易的条件。因此，您可能希望向交易请求添加断言以解锁由脚本使用的资金。可以像这样添加：

<<< @/../../docs-snippets/src/guide/transactions/transaction-request.test.ts#transaction-request-5{ts:line-numbers}

> **注意**: 有关断言的更多信息，包括有关如何配置、资助和使用它们解锁资金的信息，请参阅[断言指南](../predicates/index.md)。

### 添加见证人并签署交易请求

SDK 提供了一种直接修改交易请求的见证人的方法，也可以通过传递账户来完成。这将使用账户的私钥对交易请求进行签名。以下将详细说明如何向交易请求添加见证人：

<<< @/../../docs-snippets/src/guide/transactions/transaction-request.test.ts#transaction-request-6{ts:line-numbers}

在交易请求中添加多个见证人的更复杂示例可以在[多签者指南](../cookbook/transactions-with-multiple-signers.md)中看到，该指南验证脚本内的签名。

> **注意**: 一旦调用了 `addAccountWitnesses`，对交易请求的任何其他修改都会使签名失效，因为交易 ID 会发生变化。因此，建议在最后添加见证人。

### 获取交易请求的交易 ID

交易 ID 是整个交易请求的 SHA-256 哈希。这对于在链上跟踪交易非常有用。要获取交易 ID，可以使用以下方法：

<<< @/../../docs-snippets/src/guide/transactions/transaction-request.test.ts#transaction-request-7{ts:line-numbers}

> **注意**: 对交易请求进行的任何更改都会改变交易 ID。因此，应仅在进行所有修改后获取交易 ID。
