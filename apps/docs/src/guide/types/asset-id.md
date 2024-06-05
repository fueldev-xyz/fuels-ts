# 资产 ID

资产 ID 可以使用 `AssetId` 类型表示。它的定义与 Sway 标准库类型相匹配，是围绕内部 `Bits256` 值的 `Struct` 包装器。

<<< @/../../docs-snippets/src/guide/types/asset-id.test.ts#asset-id-1{ts:line-numbers}

## 使用资产 ID

`AssetId` 类型可以与您的合约调用集成。考虑以下可以比较并返回资产 ID 的合约：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-asset-id/src/main.sw#asset-id-1{ts:line-numbers}

`AssetId` 类型可以与 SDK 集成，并传递给合约函数，如下所示：

<<< @/../../docs-snippets/src/guide/types/asset-id.test.ts#asset-id-3{ts:line-numbers}

并验证返回值：

<<< @/../../docs-snippets/src/guide/types/asset-id.test.ts#asset-id-4{ts:line-numbers}
