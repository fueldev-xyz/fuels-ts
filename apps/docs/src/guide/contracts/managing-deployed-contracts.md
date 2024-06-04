# 管理部署的合约

要使用 SDK 与已部署的合约进行交互，而不需要重新部署它，你只需要合约 ID 和它的 JSON ABI。这使你可以绕过部署设置。

## 合约 ID

[`Contract`](../../api/Program/Contract.md) 类的 `contractId` 属性是 [`AbstractAddress`](../../api/Interfaces/AbstractAddress.md) 类型，这是一个抽象类，专门由 [`Address`](../../api/Address/Address.md) 类扩展。

[`Address`](../../api/Address/Address.md) 类包装了 [`AbstractAddress`](../../api/Interfaces/AbstractAddress.md) 类的所有方法，并添加了一个属性：`bech32Address`。该属性是一个以 [`Bech32`](../types/bech32.md) 格式编码的字符串，可通过人类可读的前缀 `fuel`，后跟分隔符 `1` 进行识别。

当你使用 `console.log` 记录一个已实例化合约的 `contractId` 属性时，输出如下：

```console
  Address {
    bech32Address: 'fuel1e5tdjlzufcvwut5dvs5yglweepmrevpnvuvt2djj6pyl3mygkwaq8m7f20'
  }
```

---

如果你已经有了一个实例化和部署的合约，你可以简单地使用 `contractId` 属性和合约的 JSON ABI 来创建另一个合约实例：

<<< @/../../docs-snippets/src/guide/contracts/managing-deployed-contracts.test.ts#managing-deployed-contracts-1{ts:line-numbers}

前面的示例假设你手头有一个 [`Contract`](../../api/Program/Contract.md) 实例。然而，一些 Fuel 工具和 Sway 使用了 [`b256`](../types/bits256.md) 类型格式，即十六进制编码的类似字符串的类型，用于合约 ID。

例如，如果你使用 `forc deploy` 部署了你的合约，则可能会有这种格式。

当使用 `b256` 类型的合约 ID 时，实例化一个 [`Contract`](../../api/Program/Contract.md) 的过程保持不变：

<<< @/../../docs-snippets/src/guide/contracts/managing-deployed-contracts.test.ts#managing-deployed-contracts-2{ts:line-numbers}