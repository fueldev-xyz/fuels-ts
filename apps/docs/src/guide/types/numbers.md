# 数字

在 Sway 中，有多种原始数字类型：

1. `u8`（8位无符号整数）
1. `u16`（16位无符号整数）
1. `u32`（32位无符号整数）
1. `u64`（64位无符号整数）
1. `u256`（256位无符号整数）

本指南解释了如何在使用 SDK 时创建和操作 Sway 数字。

## 创建数字

### 对于 `u64` 和 `u256`

当您从 JavaScript 传递 `u64` 或 `u256` 到 Sway 程序时，必须首先将其转换为 `BigNum` 对象。这是因为这些类型的最大值可以非常大（分别为 `2^64` 和 `2^256`），而 JavaScript 的 `Number` 类型只能容纳高达 53 位的精度（`2^53`）。

<<< @/../../docs-snippets/src/guide/types/numbers.test.ts#numbers-docs-1{ts:line-numbers}

您还可以从字符串创建 `BigNum`。当您想要传递无法表示为 JavaScript 数字的大数字时，这很有用。以下是如何做到这一点的示例：

<<< @/../../docs-snippets/src/guide/types/numbers.test.ts#numbers-docs-2{ts:line-numbers}

### 对于 `u8`、`u16` 和 `u32`

您不需要做任何特殊操作来创建这些数字。您可以直接传递一个 JavaScript 数字。有关更多详细信息，请参见下面的示例。

## 示例：与合约方法交互中的数字

### 对于 `u64` 和 `u256`

<<< @/../../docs-snippets/src/guide/types/numbers.test.ts#numbers-docs-3{ts:line-numbers}

> 注意：如果合约调用返回的数字太大，无法表示为 JavaScript 数字，则可以使用 `.toString()` 方法将其转换为字符串，而不是 `.toNumber()`。

### 对于 `u8`、`u16` 和 `u32`

<<< @/../../docs-snippets/src/guide/types/numbers.test.ts#numbers-docs-4{ts:line-numbers}

### 使用 `ethers` 中的 `BigNum` 与 `fuels`

<<< @/../../docs-snippets/src/guide/types/numbers.test.ts#numbers-docs-5{ts:line-numbers}
