# 数组

在 Sway 中，`Array` 是一个固定大小的相同类型元素的集合，类似于 `Tuple`。`Arrays` 可以容纳任意类型，包括非原始类型，在编译时确定其大小。

## 在 SDK 中使用数组

您可以像将数组传递给 TypeScript 函数一样轻松地将 TypeScript `Array` 传递给您的合约方法。

SDK 在后台处理从 TypeScript 到 Sway 的转换，允许通过类型传递预期的数据，而不管数组类型如何。

在以下示例中演示了 Sway 中的数组就是一个有类型的数组：

<<< @/../../docs-snippets/src/guide/types/arrays.test.ts#arrays-1{ts:line-numbers}

在 Sway 中，`Arrays` 的大小是固定的，因此存储大小是在程序编译时确定的，而不是在运行时确定的。

假设您有一个合约，它以长度为 2 的 `u64` 类型的数组作为参数，并返回它：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-u64-array/src/main.sw#arrays-2{rust:line-numbers}

要使用 SDK 执行合约调用，您可以这样做：

<<< @/../../docs-snippets/src/guide/types/arrays.test.ts#arrays-2{ts:line-numbers}

您可以像前面的示例中演示的那样轻松访问和验证合约方法返回的数组。

如前所述，Sway `Arrays` 具有预定义的类型和大小，因此在将数组作为参数传递给合约调用时需要小心。

传递大小不正确的数组，无论它的元素数量多还是少于指定的长度，都会导致错误：

<<< @/../../docs-snippets/src/guide/types/arrays.test.ts#arrays-3{ts:line-numbers}

类似地，传递类型不正确的数组也会导致错误：

<<< @/../../docs-snippets/src/guide/types/arrays.test.ts#arrays-4{ts:line-numbers}

## 向量

如果您的数组大小在运行时未知，请考虑使用 [Vectors](./vectors.md) 类型，这更适合于动态大小的集合。
