# 交易依赖估算

[之前](./variable-outputs.md)，我们提到合约调用可能需要您手动指定外部合约或变量输出。

然而，无论何时您调用合约函数或尝试发送交易，SDK 都会自动估算这些依赖关系，并在一切井然有序时进行双重检查。

SDK 使用 `estimateTxDependencies` 辅助函数来设置估算过程中发现的任何缺失的依赖项。这需要在后台模拟交易几次。

<<< @/../../../packages/account/src/providers/provider.ts#Provider-sendTransaction{ts:line-numbers}

虽然依赖于 SDK 的自动估算是一个不错的默认行为，但我们建议如果依赖项在预先知道的情况下，手动指定它们，以避免估算过程的性能影响。