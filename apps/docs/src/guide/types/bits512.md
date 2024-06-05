# Bits512

在 Sway 中，`b512` 类型通常用于处理公钥和签名。本指南将解释在 Sway 中如何定义 `b512` 类型，如何使用 SDK 可视化 `b512` 值，以及如何与接受 `b512` 参数的合约函数进行交互。

在 Sway 中，`b512` 类型是两个 `b256` 类型的包装器，允许表示 64 字节的值。它被定义为一个结构体：

<<< @/../../docs-snippets/src/guide/types/bits512.test.ts#bits512-1{rust:line-numbers}

## SDK 中的 `b512`

在 SDK 中，您可以通过查看钱包的公钥来可视化 `b512` 值：

<<< @/../../docs-snippets/src/guide/types/bits512.test.ts#bits512-2{ts:line-numbers}

## 示例：在合约函数中回显 `b512` 值

让我们考虑一个接受 `b512` 参数并返回相同值的合约函数：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-values/src/main.sw#bits512-3{rust:line-numbers}

要调用此函数并验证返回的值，请按照以下步骤进行：

<<< @/../../docs-snippets/src/guide/types/bits512.test.ts#bits512-4{ts:line-numbers}

在这个示例中，我们生成一个钱包，使用其公钥作为 `b512` 输入，调用 `echo_b512` 合约函数，并期望返回的值与原始输入匹配。
