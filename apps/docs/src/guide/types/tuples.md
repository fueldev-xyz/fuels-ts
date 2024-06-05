# 元组

在 Sway 中，元组是固定长度的异构元素集合。元组可以存储多种数据类型，包括基本类型、结构体和枚举。本指南将演示如何在 TypeScript 中表示和处理元组，并与接受元组作为参数的合约函数进行交互。

在 TypeScript 中，您可以使用指定类型的数组来表示 Sway 元组，每个元素的类型都不同：

<<< @/../../docs-snippets/src/guide/types/tuples.test.ts#tuples-1{ts:line-numbers}

在这个示例中，Typescript 的 `tuple` 变量包含三个不同类型的元素：一个数字、一个布尔值和另一个数字。

## 示例：将元组作为参数传递

让我们考虑一个接受元组作为参数并返回相同元组的合约函数：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-values/src/main.sw#tuples-2{rust:line-numbers}

要使用 SDK 执行和验证合约函数，请按照以下步骤进行：

<<< @/../../docs-snippets/src/guide/types/tuples.test.ts#tuples-3{ts:line-numbers}

在这个示例中，我们创建了一个包含三个元素的元组，调用了 `echo_tuple` 合约函数，并期望返回的元组与原始元组相匹配。请注意，我们使用 `new BN(value[2]).toNumber()` 将返回的元组的第三个元素转换为数字。

Sway 中的元组提供了一种方便的方式来存储和操作异构元素的集合。了解如何在 TypeScript 和 Sway 合约中表示和处理元组将使您能够创建更多样化和表达力强的代码。
