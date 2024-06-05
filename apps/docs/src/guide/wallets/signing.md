# 签名

## 签名消息

在区块链环境中，使用钱包对消息进行签名是一项基本的安全实践。它验证所有权并确保数据的完整性。以下是使用 `wallet.signMessage` 方法签名消息的方法：

<<< @/../../docs-snippets/src/guide/wallets/signing.test.ts#signing-1{ts:line-numbers}

`wallet.signMessage` 方法内部使用 SHA-256 算法对消息进行哈希处理，然后对哈希消息进行签名，并将签名作为十六进制字符串返回。

`hashMessage` 辅助函数给出了原始消息的哈希。这对于确保签名过程中使用的哈希与地址恢复过程中使用的哈希相匹配至关重要。

`Signer` 类的 `recoverAddress` 方法接受哈希消息和签名，以恢复签名者的地址。这确认了签名是由与该地址关联的私钥持有者创建的，从而确保了签名消息的真实性和完整性。

## 签名交易

签署交易涉及使用您的钱包对交易ID（也称为[交易哈希](https://specs.fuel.network/master/identifiers/transaction-id.html)）进行签名，以授权使用您的资源。操作步骤如下：

1. `生成签名`：使用钱包基于交易ID创建签名。

2. `在交易上使用签名`：将签名放置在交易的 `witnesses` 数组中。每个Coin / Message输入都应具有匹配的 `witnessIndex`。此索引指示签名在 `witnesses` 数组中的位置。

3. `安全机制`：交易ID源自交易字节（不包括 `witnesses`）。如果交易更改，则ID更改，从而使之前的签名无效。这确保在签名后不能进行未经授权的更改。

以下代码片段说明了如何签署交易：

<<< @/../../docs-snippets/src/guide/wallets/signing.test.ts#signing-2{ts:line-numbers}

与签署消息示例类似，上述代码使用了 `Signer.recoverAddress` 来从交易ID和已签名数据中获取钱包的地址。

当使用钱包通过 `wallet.sendTransaction()` 提交交易时，SDK 已经处理了与签署交易和将签名添加到 `witnesses` 数组相关的步骤。因此，在大多数情况下，您可以跳过这一步：

<<< @/../../docs-snippets/src/guide/wallets/signing.test.ts#signing-3{ts:line-numbers}
