# 地址

在与去中心化应用程序交互时，地址和不同的地址格式是常见的。此外，不同的网络可能会强制使用不同的地址格式。

Fuel 网络使用 [`Bech32`](../types/bech32.md) 地址格式进行交互，下面是一个示例：

<<< @/../../docs-snippets/src/guide/types/bech32.test.ts#addresses-1{ts:line-numbers}

然而，一个十六进制的 [Bits256](../types/bits256.md)（hex）是另一种常见的地址格式；下面是一个示例：

<<< @/../../docs-snippets/src/guide/types/bits256.test.ts#addresses-2{ts:line-numbers}

有时，这些甚至可以包装在一个 [Struct](../types/structs.md) 中。比如 [Asset ID](../types/asset-id.md) 或 [EVM Address](../types/evm-address.md)：

<<< @/../../docs-snippets/src/guide/types/evm-address.test.ts#addresses-3{ts:line-numbers}

TS-SDK 通过 [Address](../types/address.md) 辅助类使得在这些地址之间进行转换变得简单，该类提供了各种转换的工具函数。

下面的 [转换指南](./address-conversion.md#address-conversion) 将展示如何利用这个类来在不同的地址格式和 Sway 标准类型之间进行转换。

## 地址转换

本指南演示了如何使用辅助函数来在地址格式和 Sway 标准类型之间进行转换。原生类型是字节的封装，您可以通过利用这些函数和类来在它们之间执行转换。

## 从 `Bech32` 到 `b256`

通过实例化一个 [`Address`](../../api/Address/Address.md)，我们可以验证一个 `Bech32` 地址并将其轻松转换为 `b256`：

<<< @/../../docs-snippets/src/guide/types/conversion.test.ts#conversion-5{ts:line-numbers}

或者，如果您更喜欢直接使用工具函数进行验证和转换，您可以使用 `isBech32` 和 `toB256`：

<<< @/../../docs-snippets/src/guide/types/conversion.test.ts#conversion-6{ts:line-numbers}

## 从 `b256` 到 `Bech32`

类似地，我们有 [`Address`](../../api/Address/Address.md) 上的类函数和可用于 `b256` 验证和转换的工具：

<<< @/../../docs-snippets/src/guide/types/conversion.test.ts#conversion-7{ts:line-numbers}

并通过使用 `isB256` 和 `toBech32` 工具：

<<< @/../../docs-snippets/src/guide/types/conversion.test.ts#conversion-8{ts:line-numbers}

## 转换合约 ID

合约 `id` 属性具有 [`AbstractAddress`](../types/address.md#abstractaddress-class) 类型。因此，可以使用 [`Address`](../../api/Address/Address.md) 类函数（如 `toAddress` 和 `toB256`）进行转换：

<<< @/../../docs-snippets/src/guide/types/conversion.test.ts#conversion-2{ts:line-numbers}

## 转换钱包地址

同样，钱包 `address` 属性也是 [`AbstractAddress`](../types/address.md#abstractaddress-class) 类型，因此可以使用相同的 [`Address`](../../api/Address/Address.md) 类函数进行转换：

<<< @/../../docs-snippets/src/guide/types/conversion.test.ts#conversion-3{ts:line-numbers}

## 转换资产 ID

[Asset IDs](../types/asset-id.md) 是一个包装的 [b256](../types/bits256.md) 值。下面的示例演示了如何从 `b256` 类型创建一个 [`Address`](../../api/Address/Address.md)：

<<< @/../../docs-snippets/src/guide/types/conversion.test.ts#conversion-4{ts:line-numbers}
