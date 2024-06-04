# 使用 SDK 进行合约间调用

本指南介绍如何使用 SDK 执行合约调用，其中一个合约与另一个合约进行交互。我们将使用一个简单的场景，涉及到一个 `SimpleToken` 合约和一个 `TokenDepositor` 合约。

## `SimpleToken` 和 `TokenDepositor` 合约

在这个例子中，我们有一个 `SimpleToken` 合约，代表一个基本的代币合约，能够为不同地址保存余额。我们还有一个 `TokenDepositor` 合约，它将代币存入 `SimpleToken` 合约。

### 合约：`SimpleToken`

这是一个简单的代币合约，允许保存余额：

<<< @/../../docs-snippets/test/fixtures/forc-projects/simple-token/src/main.sw#inter-contract-calls-1{ts:line-numbers}

### 合约：`TokenDepositor`

`TokenDepositor` 合约导入 `SimpleToken` 合约并调用其 `deposit` 函数存入代币：

<<< @/../../docs-snippets/test/fixtures/forc-projects/token-depositor/src/main.sw#inter-contract-calls-2{ts:line-numbers}

## 使用 SDK 进行合约间调用

一旦两个合约都部署了，我们就可以使用 SDK 使 `TokenDepositor` 合约调用 `SimpleToken` 合约。

<<< @/../../docs-snippets/src/guide/contracts/inter-contract-calls.test.ts#inter-contract-calls-3{ts:line-numbers}

请注意 `TokenDepositor` 合约调用的 `addContracts` 方法。该方法接受一个已部署合约实例的数组。如果不调用此方法，合约间调用将不起作用。