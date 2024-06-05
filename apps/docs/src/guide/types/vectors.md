# 向量

在 Sway 中，向量是具有相同类型的动态大小元素集合。向量可以持有任意类型，包括非原始类型。

## 在 SDK 中使用向量

在 Sway 中，基本的向量类似于 TypeScript 数组：

<<< @/../../docs-snippets/src/guide/types/vector.test.ts#vector-1{ts:line-numbers}

考虑下面的 Sway 中 `EmployeeData` 结构体的示例：

<<< @/../../docs-snippets/test/fixtures/forc-projects/employee-data/src/lib.sw#struct-1{rust:line-numbers}

现在，让我们看一下以下合约方法。它接收一个 `Transaction` 结构体类型的向量作为参数，并返回向量中的最后一个 `Transaction` 条目：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-employee-data-vector/src/main.sw#vector-3{ts:line-numbers}

下面的代码片段演示了如何调用这个接受 `Vec<Transaction>` 的 Sway 合约方法：

<<< @/../../docs-snippets/src/guide/types/vector.test.ts#vector-4{ts:line-numbers}

## 将字节码转换为向量

有些函数需要您将字节码传递给函数。字节码参数的类型通常是 `Vec<u8>`，以下是如何将字节码传递给函数的示例：

<<< @/../../docs-snippets/test/fixtures/forc-projects/bytecode-input/src/main.sw#vector-bytecode-input-sway{ts:line-numbers}

要将字节码传递给此函数，您可以使用 `arrayify` 函数将字节码文件内容转换为 `UInt8Array`，这是 Sway 的 `Vec<u8>` 类型的 TS 兼容类型，然后将其传递给函数：

<<< @/../../docs-snippets/src/guide/types/vector.test.ts#vector-bytecode-input-ts{ts:line-numbers}
