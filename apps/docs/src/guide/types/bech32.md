# `Bech32`

SDK 使用 `Bech32` 类型作为 [`Address`](../../api/Address/Address.md) 类的核心属性，具体来说是通过 `bech32Address` 属性。

最初设计用于比特币，`Bech32` 格式提供了许多优势，如增强的错误检测、简化的集成以及与未来升级的兼容性提高。基于这些优点，[`Address`](../../api/Address/Address.md) 类是围绕 `Bech32` 类型构建的。

您可以在[这里](https://thebitcoinmanual.com/articles/btc-bech32-address/)阅读有关 `Bech32` 类型的更多信息。

## 默认的可读部分 (HRP)

`Bech32` 地址由人类可读部分 (HRP) 后跟数字 `1` 组成，后者充当分隔符：

<<< @/../../../packages/interfaces/src/index.ts#bech32-1{ts:line-numbers}

完整的 `Bech32` 地址将类似于以下内容：

<<< @/../../docs-snippets/src/guide/types/bech32.test.ts#bech32-2{5 ts:line-numbers}

上面示例中的 HRP 是 `fuel`。此人类可读前缀包含在内，以提供更好的可读性，并防止用户意外使用错误的网络地址。
