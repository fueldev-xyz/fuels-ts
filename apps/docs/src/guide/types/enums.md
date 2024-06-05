# Enums

Sway Enums 与 TypeScript Enums 有一些不同之处。在本文档中，我们将探讨如何在 SDK 中表示 Sway Enums，以及如何在 Sway 合约函数中使用它们。

## 基本的 Sway Enum 示例

考虑下面的基本 Sway Enum，名为 `StateError`：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-enum/src/main.sw#enum-1{rust:line-numbers}

类型 `()` 表示每个 Enum 变体都没有关联的额外数据。Sway 允许您创建 Enums of Enums 或将类型与 Enum 变体关联起来。

## 将 Sway Enums 用作函数参数

让我们定义一个 Sway 合约函数，它以 `StateError` Enum 变体作为参数，并返回它：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-enum/src/main.sw#enum-2{rust:line-numbers}

要执行合约函数并验证响应，我们可以使用以下代码：

<<< @/../../docs-snippets/src/guide/types/enums.test.ts#enum-3{ts:line-numbers}

在此示例中，我们只需将 Enum 变体作为值传递以执行合约函数调用。

## Enum of Enums 示例

在此示例中，`Error` Enum 是其他两个 Enums：`StateError` 和 `UserError` 的 Enum。

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-enum/src/main.sw#enum-4{rust:line-numbers}

## 使用 Enums of Enums 与合约函数

现在，让我们创建一个 Sway 合约函数，它接受 `Error` Enum 的任何变体作为参数，并立即将其返回。这个变体可以来自 `StateError` 或 `UserError` Enums。

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-enum/src/main.sw#enum-5{rust:line-numbers}

由于 `Error` Enum 是 Enums 的 Enums，我们需要以不同的方式传递函数参数。参数将是一个 TypeScript 对象：

<<< @/../../docs-snippets/src/guide/types/enums.test.ts#enum-6{ts:line-numbers}

在这种情况下，由于变体 `InsufficientPermissions` 属于 `UserError` Enum，我们使用 Enum 名称作为对象键，将变体作为对象值创建一个 TypeScript 对象。

如果我们打算使用 `StateError` Enum 中的变体，我们将采用相同的方法：

<<< @/../../docs-snippets/src/guide/types/enums.test.ts#enum-7{ts:line-numbers}
