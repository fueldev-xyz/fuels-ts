# `Bits256`

在 Fuel 中，类型 `b256` 代表哈希并保存一个 256 位（32 字节）的值。TypeScript SDK 将 `b256` 表示为十六进制字符串值以实现可移植性，并提供将 [原始字节](./bytes32.md) 转换为 `Uint8Array` 的实用工具。

## 生成随机的 `b256` 值

要生成随机的 `b256` 值，您可以使用 `getRandomB256()` 函数：

<<< @/../../docs-snippets/src/guide/types/bits256.test.ts#bits256-1{ts:line-numbers}

### 在 `b256` 和 `Uint8Array` 之间进行转换

要在 `b256` 十六进制字符串和 `Uint8Array` 之间进行转换，您可以使用 `arrayify` 和 `hexlify` 函数：

<<< @/../../docs-snippets/src/guide/types/bits256.test.ts#bits256-2{ts:line-numbers}

## `Address` 类的支持

作为 [`Address`](../../api/Address/Address.md) 类的一部分，`b256` 值也得到了支持，可与应用程序的其他组件无缝集成。要从 b256 值创建一个 [`Address`](../../api/Address/Address.md) 实例，请使用 `Address.fromB256()` 方法：

<<< @/../../docs-snippets/src/guide/types/bits256.test.ts#bits256-3{ts:line-numbers}
