# 加密和解密

JSON 钱包是一种存储钱包的标准化方式，可以安全地存储钱包。它们遵循特定的模式，并使用密码进行加密。这使得管理多个钱包并将它们安全地存储在磁盘上变得更加容易。本指南将带您了解使用 Typescript SDK 加密和解密 JSON 钱包的过程。

## 加密钱包

我们将从 [`WalletUnlocked`](../../api/Account/WalletUnlocked.md) 实例中调用 `encrypt` 方法，该方法将密码作为参数。它将使用密码对私钥进行加密，并返回 JSON Keystore 钱包。然后，您可以安全地存储此 JSON 钱包。

以下是如何完成此操作的示例：

<<< @/../../docs-snippets/src/guide/wallets/encrypting-and-decrypting-json-wallets.test.ts#encrypting-and-decrypting-json-wallets-1{ts:line-numbers}

请注意，`encrypt` 必须在 [`WalletUnlocked`](../../api/Account/WalletUnlocked.md) 的实例内调用。通过传递私钥或助记词短语到已锁定的钱包，才能获得此实例。

## 解密钱包

要解密 JSON 钱包并检索您的私钥，您可以在 [Wallet](../../api/Account/Wallet.md) 实例上调用 `fromEncryptedJson`。它将加密的 JSON 钱包和密码作为其参数，并返回解密的钱包。

以下是一个示例：

<<< @/../../docs-snippets/src/guide/wallets/encrypting-and-decrypting-json-wallets.test.ts#encrypting-and-decrypting-json-wallets-2{ts:line-numbers}

在此示例中，`decryptedWallet` 是 [`WalletUnlocked`](../../api/Account/WalletUnlocked.md) 类的实例，现在可以使用。

## 重要提示

记住要安全地存储您的加密的 JSON 钱包和密码。如果丢失它们，将无法恢复您的钱包。出于安全原因，请勿与任何人共享您的私钥、加密的 JSON 钱包或密码。
