# 调用参数

<!-- 此部分应解释调用参数 -->
<!-- call_params:example:start -->

在与合约交互时，你可以使用 `callParams` 方法为合约调用配置特定的参数。可用的调用参数包括：

1. `forward`
2. `gasLimit`
<!-- call_params:example:end -->

> **注意**：在调用合约时，也可以设置交易参数。有关更多信息，请参阅[交易参数](../transactions/transaction-parameters.md)。

## 转发参数

<!-- 此部分应解释 `forward` 参数 -->
<!-- forward:example:start -->

`forward` 参数允许在调用函数时向合约发送特定数量的代币。当合约函数需要代币来执行时（例如支付费用或转移资金），转发参数有助于控制分配给合约调用的资源，并提供了对潜在成本高昂操作的保护。

<!-- forward:example:end -->

<<< @/../../docs-snippets/src/guide/contracts/call-parameters.test.ts#call-params-1{ts:line-numbers}

## Gas 限制参数

<!-- 此部分应解释 `gasLimit` 参数 -->
<!-- gas_limit:example:start -->

`gasLimit` 指的是仅由合约调用本身消耗的最大气体量，与交易的其余部分分开。

<!-- gas_limit:example:end -->

<<< @/../../docs-snippets/src/guide/contracts/call-parameters.test.ts#call-params-2{ts:line-numbers}

## 调用参数 `gasLimit` vs 交易参数 `gasLimit`

调用的 `gasLimit` 参数设置了实际合约调用的最大气体限制，而交易的 `gasLimit` （请参阅[交易参数](../transactions/transaction-parameters.md)）设置了整个交易的最大气体限制，并约束了调用的 `gasLimit`。如果调用的 `gasLimit` 设置为大于 _可用_ 交易气体的值，则整个可用的交易气体将用于合约调用执行。

如果不设置调用的 `gasLimit`，则将应用交易的 `gasLimit`。

## 设置两个参数

你可以在同一个合约函数调用中设置调用参数和交易参数。

<<< @/../../docs-snippets/src/guide/contracts/call-parameters.test.ts#call-params-3{ts:line-numbers}