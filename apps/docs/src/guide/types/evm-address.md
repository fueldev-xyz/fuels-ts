# `EvmAddress`

以太坊虚拟机 (EVM) 地址可以使用 `EvmAddress` 类型表示。其定义与 Sway 标准库类型相匹配，是一个围绕内部 `Bits256` 值的 `Struct` 包装器。

<<< @/../../docs-snippets/src/guide/types/evm-address.test.ts#evm-address-1{ts:line-numbers}

## 创建 EVM 地址

EVM 地址仅有 20 字节，因此 `Bits256` 值的前 12 字节设置为 0。在 SDK 中，可以实例化一个 `Address`，并使用 `toEvmAddress()` 函数将其转换为一个包装的、与 Sway 兼容的 EVM 地址：

<<< @/../../docs-snippets/src/guide/types/evm-address.test.ts#evm-address-2{ts:line-numbers}

## 使用 EVM 地址

`EvmAddress` 类型可以与您的合约调用集成。考虑以下可以比较和返回 EVM 地址的合约：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-evm-address/src/main.sw#evm-address-1{ts:line-numbers}

可以使用 SDK 并将 `EvmAddress` 传递给合约函数，如下所示：

<<< @/../../docs-snippets/src/guide/types/evm-address.test.ts#evm-address-3{ts:line-numbers}

并验证返回的值：

<<< @/../../docs-snippets/src/guide/types/evm-address.test.ts#evm-address-4{ts:line-numbers}
