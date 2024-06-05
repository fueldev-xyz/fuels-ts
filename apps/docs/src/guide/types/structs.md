# 结构体

在 Sway 中，`struct` 的作用类似于 TypeScript 中的 `Object`。它定义了一个自定义数据结构，具有指定的属性名称和类型。Sway 结构体中的属性名称和类型必须与相应的 TypeScript 定义相匹配。

## 示例

以下是 Sway 中 `struct` 的示例：

<<< @/../../docs-snippets/test/fixtures/forc-projects/employee-data/src/lib.sw#struct-1{rust:line-numbers}

这是 TypeScript 中表示的等效结构：

<<< @/../../docs-snippets/src/guide/types/struct.test.ts#struct-2{ts:line-numbers}

## 处理不同的数据类型

请注意，TypeScript 不支持 `u8` 和 `u64` 类型。相反，使用 `number` 类型来表示它们。

此外，TypeScript 不支持指定字符串长度，因此对于 `name`，只需使用 `string` 即可。

类似地，由于 SDK 上的类型 `b256` 只是一个十六进制字符串，因此我们也使用 `string`。
