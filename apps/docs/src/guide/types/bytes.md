# Bytes

可以使用 `Bytes` 类型表示字节值的动态数组，该类型表示原始字节。

<<< @/../../docs-snippets/src/guide/types/bytes.test.ts#bytes-1{ts:line-numbers}

## 使用 Bytes

`Bytes` 类型可以与您的合约调用集成。考虑以下合约，它可以比较并返回一个 `Bytes`：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-bytes/src/main.sw#bytes-1{ts:line-numbers}

可以使用 JavaScript 的本机数组或大数数组创建一个 `Bytes` 数组，并发送到 Sway 合约：

<<< @/../../docs-snippets/src/guide/types/bytes.test.ts#bytes-2{ts:line-numbers}
