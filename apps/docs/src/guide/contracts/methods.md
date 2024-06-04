# 与合约交互

与合约交互有四种方式：`get`、`dryRun`、`simulate`、`call`。

## `get`

`get` 方法应该用于从区块链中读取数据而不使用资源。它可以与未资助的钱包一起使用，甚至可以完全不使用钱包：

<<< @/../../docs-snippets/src/guide/contracts/interacting-with-contracts.test.ts#interacting-with-contracts-1{ts:line-numbers}

## `dryRun`

`dryRun` 方法应该用于模拟合约调用。它不会消耗资源，可以与未资助的钱包一起使用，甚至可以完全不使用钱包：

<<< @/../../docs-snippets/src/guide/contracts/interacting-with-contracts.test.ts#interacting-with-contracts-2{ts:line-numbers}

## `simulate`

`simulate` 方法应该用于模拟合约调用，确保使用的钱包具有足够的资金来支付交易费用，而不消耗任何资源。

需要一个资助的钱包：

<<< @/../../docs-snippets/src/guide/contracts/interacting-with-contracts.test.ts#interacting-with-contracts-3{ts:line-numbers}

## `call`

`call` 方法应该用于向节点提交真实的合约调用事务。

会消耗真实资源，并且合约函数执行的任何操作都将在区块链上处理。

<<< @/../../docs-snippets/src/guide/contracts/interacting-with-contracts.test.ts#interacting-with-contracts-4{ts:line-numbers}

## `isReadOnly`（实用工具）

如果您想确定一个函数是否是只读的，可以使用 `isReadOnly` 方法：

<<< @/../../docs-snippets/src/guide/contracts/is-function-readonly.test.ts#is-function-readonly-1{ts:line-numbers}

如果函数是只读的，您可以使用 `get` 方法在链上检索数据而不消耗 gas。

如果函数不是只读的，您将不得不使用 `call` 方法在链上提交交易，这会产生 gas 费用。