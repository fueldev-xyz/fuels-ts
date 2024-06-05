# 从私钥创建钱包

可以通过提供 `Wallet.generate` 方法来创建具有随机生成私钥的新钱包。

<<< @/../../docs-snippets/src/guide/wallets/access.test.ts#wallets{ts:line-numbers}

或者，您也可以通过私钥创建钱包：

<<< @/../../docs-snippets/src/guide/wallets/private-keys.test.ts#wallet-from-private-key{ts:line-numbers}

您可以使用 `Signer` 包获取私钥的地址：

<<< @/../../docs-snippets/src/guide/wallets/private-keys.test.ts#signer-address{ts:line-numbers}
