# 多签名者的交易

当一个交易包含一个可花费的输入（例如一个硬币）时，它必须包含该硬币所有者的签名才能被花费。如果硬币所有者也提交了交易，那么这是直截了当的。但是，如果需要外部地址对交易进行签名，则交易必须包含多个签名。在 SDK 中，可以通过在交易请求上调用 `addAccountWitnesses` 来添加帐户签名到交易中。

考虑一个需要两个签名才能花费的脚本：

<<< @/../../docs-snippets/test/fixtures/forc-projects/script-signing/src/main.sw#multiple-signers-1{rust:line-numbers}

在上面的代码片段中，我们使用内置的 Sway 函数 `tx_witness_data()` 来检索见证签名和 `tx_id()` 来获取交易哈希。然后，我们检索签名地址以验证脚本。

我们可以通过从调用范围创建一个交易请求来在 SDK 中与此脚本进行交互。对于合约也是一样。考虑以下脚本：

<<< @/../../docs-snippets/src/guide/cookbook/signing-transactions.test.ts#multiple-signers-2{ts:line-numbers}

同样的方法也可以用于断言，通过实例化并将其添加到交易请求中。考虑以下断言：

<<< @/../../docs-snippets/test/fixtures/forc-projects/predicate-signing/src/main.sw#multiple-signers-3{rust:line-numbers}

我们可以通过以下实现在 SDK 中与此断言进行交互：

<<< @/../../docs-snippets/src/guide/cookbook/signing-transactions.test.ts#multiple-signers-4{ts:line-numbers}
