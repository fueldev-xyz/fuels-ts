# 存款和取款

考虑以下合约：

<<< @/../../docs-snippets/test/fixtures/forc-projects/liquidity-pool/src/main.sw#deposit-and-withdraw-cookbook-1{rust:line-numbers}

顾名思义，这个合约代表了一个简化版本的流动性池。`deposit()` 方法允许您提供任意数量的 `BASE_TOKEN`。作为回应，它会将流动性资产的两倍数量铸造到调用者的地址。同样，`withdraw()` 方法将 `BASE_TOKEN` 的一半数量转移回调用者的地址。

现在，让我们将一些代币存入流动性池合约中。由于这需要将资产转发到合约，我们需要在创建合约调用时将适当的值传递给 `callParams`。

<<< @/../../docs-snippets/src/guide/cookbook/deposit-and-withdraw.test.ts#deposit-and-withdraw-cookbook-2{ts:line-numbers}

作为最后的演示，让我们使用所有的流动性资产余额从池中取款，并确认我们收回了初始数量。为此，我们获取流动性资产的余额，并通过 `callParams` 将其提供给 `withdraw()` 函数。

<<< @/../../docs-snippets/src/guide/cookbook/deposit-and-withdraw.test.ts#deposit-and-withdraw-cookbook-3{ts:line-numbers}
