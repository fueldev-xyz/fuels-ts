# 多个合约调用

您可以在单个交易中执行多个合约调用，无论是对同一合约还是对不同合约。这可以提高效率并降低总体交易成本。

## 同一合约多个调用

使用 `multiCall` 方法在单个交易中对同一合约调用多个函数：

<<< @/../../docs-snippets/src/guide/contracts/multicalls.test.ts#multicall-1{ts:line-numbers}

## 不同合约多个调用

`multiCall` 方法还允许您在单个交易中对不同的合约执行多个合约调用：

<<< @/../../docs-snippets/src/guide/contracts/multicalls.test.ts#multicall-2{ts:line-numbers}

您还可以为每个合约调用链接支持的合约调用方法，如 `callParams`：

<<< @/../../docs-snippets/src/guide/contracts/multicalls.test.ts#multicall-3{ts:line-numbers}

在 `multiCall` 中链接合约调用方法时，避免执行合约函数本身，例如 `.call`、`.get` 和 `.simulate`。

`multiCall` 方法为所有合约调用创建一个范围，只有在调用 `.call` 方法后才会执行。