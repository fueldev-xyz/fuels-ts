# Bytes32

在 Sway 和 FuelVM 中，`bytes32` 用于表示哈希。它保存了一个 256 位（32 字节）的值。

## 生成随机 bytes32 值

要生成随机的 `bytes32` 值，可以使用 fuels 模块中的 `randomBytes` 函数：

<<< @/../../docs-snippets/src/guide/types/bytes32.test.ts#bytes32-1{ts:line-numbers}

## 字节数组和字符串之间的转换

您可以使用 `hexlify` 函数将字节数组转换为十六进制字符串，使用 `arrayify` 函数将十六进制字符串转换回字节数组：

<<< @/../../docs-snippets/src/guide/types/bytes32.test.ts#bytes32-2{ts:line-numbers}

## 在 Fuel 中使用 b256

在 Fuel 中，有一种特殊的类型称为 b256，它类似于 `bytes32`。与 `bytes32` 类似，`b256` 也用于表示哈希并保存 256 位值。您可以在 [Bits256 文档](./bits256.md)中了解有关使用 `b256` 值的更多信息。
