# 处理合约日志

当你在合约方法中记录一个值时，它会生成一个日志条目，添加到日志收据中，并且变量类型会记录在合约的 ABI 中。SDK 可以让你将这些值解析为 TypeScript 类型。

考虑下面的示例合约：

<<< @/../../docs-snippets/test/fixtures/forc-projects/log-values/src/main.sw#log-1{rust:line-numbers}

要在 TypeScript 中访问记录的值，可以使用合约调用结果的 `FunctionInvocationResult` 中的 `logs` 属性。日志数据将存储在一个 `Array<any>` 中：

<<< @/../../docs-snippets/src/guide/contracts/logs.test.ts#log-2{ts:line-numbers}

这种方法让你可以无缝地处理合约中记录的值，使得更容易理解和调试合约的行为。