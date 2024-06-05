# 选项

Sway 提供了 `Option`（可选）容器来处理可能具有值或标记为“无值”的变量。在处理变量可能有定义值或可能没有定义值的情况时，这个概念非常有用。

在本指南中，我们将解释如何在 Sway 中使用 Option 类型，并通过一个实际的例子来演示它们的用法。

## `Option` 类型概述

在 Sway 中，`Option` 类型是一种特殊的枚举类型的包装器。在 TypeScript 中，您可以使用 `undefined` 关键字表示 `Option` 类型，如下例所示：

<<< @/../../docs-snippets/src/guide/types/options.test.ts#options-1{ts:line-numbers}

在这个例子中，变量 `input1` 可以是一个 `number` 或 `undefined`。

## 示例：`Option<u8>` 参数

假设我们有一个合约函数接受两个 `Option<u8>` 参数。这两个参数都可以有值，也可以是未定义的。该函数检查每个输入是否有值；如果没有，它会将值设为 `0`。最后，函数返回两个输入的和。

下面是用 Sway 编写的合约函数：

<<< @/../../docs-snippets/test/fixtures/forc-projects/sum-option-u8/src/main.sw#options-2{rust:line-numbers}

您可以使用 SDK 与合约函数交互，如下所示：

<<< @/../../docs-snippets/src/guide/types/options.test.ts#options-3{ts:line-numbers}

在这种情况下，合约函数调用的结果是两个输入参数的总和。如果我们只传递一个参数，合约函数将默认另一个参数的值为 `0`。

<<< @/../../docs-snippets/src/guide/types/options.test.ts#options-4{ts:line-numbers}

在 Sway 中使用 `Option` 类型可以优雅地处理变量可能具有或可能没有定义值的情况。
