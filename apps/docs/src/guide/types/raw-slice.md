# `RawSlice`

可以使用 `RawSlice` 类型表示值的动态数组。原始切片可以是值引用或原始指针。

<<< @/../../docs-snippets/src/guide/types/raw-slice.test.ts#raw-slice-1{ts:line-numbers}

## 使用 `RawSlice`

`RawSlice` 类型可以与您的合约调用集成。考虑以下可以比较并返回 `RawSlice` 的合约：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-raw-slice/src/main.sw#raw-slice-1{ts:line-numbers}

可以使用原生 JavaScript 数组或大数数组来创建 `RawSlice`，并发送到 Sway 合约：

<<< @/../../docs-snippets/src/guide/types/raw-slice.test.ts#raw-slice-2{ts:line-numbers}
