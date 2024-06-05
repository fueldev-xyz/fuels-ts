# 地址

在 Sway 中，[`Address`](../../api/Address/Address.md) 类型作为对原始 `b256` 类型的类型安全包装器。SDK 采用了不同的方法，并为 [Address](../../api/Address/Address.md) 类型提供了自己的抽象。

## `AbstractAddress` 类

SDK 定义了 [AbstractAddress](../../api/Interfaces/AbstractAddress.md) 类，它提供了一组实用函数，用于轻松操作和在不同地址格式之间进行转换。

<<< @/../../../packages/interfaces/src/index.ts#address-1{ts:line-numbers}

## Address 类

除了符合 [`AbstractAddress`](../../api/Interfaces/AbstractAddress.md) 的接口之外，[`Address`](../../api/Address/Address.md) 类还定义了一个属性；`bech32Address`，它是 [`Bech32`](./bech32.md) 类型。

<<< @/../../../packages/address/src/address.ts#address-2{ts:line-numbers}

## 创建地址

由于 [`AbstractAddress`](../../api/Interfaces/AbstractAddress.md) 类提供的实用函数，有几种方法可以创建 [`Address`](../../api/Address/Address.md) 实例：

### 从 `Bech32` 地址创建

要从 `Bech32` 地址创建 [`Address`](../../api/Address/Address.md)，请使用以下代码片段：

<<< @/../../docs-snippets/src/guide/types/address.test.ts#address-2{ts:line-numbers}

### 从公钥创建

要从公钥创建 [`Address`](../../api/Address/Address.md)，请使用以下代码片段：

<<< @/../../docs-snippets/src/guide/types/address.test.ts#address-3{ts:line-numbers}

### 从 256 位地址创建

要从 256 位地址创建 [`Address`](../../api/Address/Address.md)，请使用以下代码片段：

<<< @/../../docs-snippets/src/guide/types/address.test.ts#address-4{ts:line-numbers}

## 实用函数

[`Address`](../../api/Address/Address.md) 类还提供了一些实用函数：

1. `fromString`: 从可能是 `Bech32` 或 `B256` 地址的模糊源创建一个新的 [`Address`](../../api/Address/Address.md)：

<<< @/../../docs-snippets/src/guide/types/address.test.ts#address-5{ts:line-numbers}

2. `fromDynamicInput`: 当地址源未知时创建一个新的 [`Address`](../../api/Address/Address.md)：

<<< @/../../docs-snippets/src/guide/types/address.test.ts#address-6{ts:line-numbers}

3. `equals:` 正如您可能已经注意到的，`equals` 函数可以比较地址实例：

<<< @/../../docs-snippets/src/guide/types/address.test.ts#address-7{ts:line-numbers}
