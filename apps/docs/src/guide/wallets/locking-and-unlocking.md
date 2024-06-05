# 锁定和解锁

我们可以对[`Wallet`](../../api/Account/Wallet.md)实例执行的操作取决于我们是否能够访问钱包的私钥。

为了区分是否知道其私钥的[`Wallet`](../../api/Account/Wallet.md)实例和不知道其私钥的实例，我们分别使用[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)和[`WalletLocked`](../../api/Account/WalletLocked.md)类型。

## 钱包状态

[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)类型表示已知私钥并存储在内存中的钱包。为了执行涉及[签署消息或交易](./signing.md)的操作，钱包必须是[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)类型。

[`WalletLocked`](../../api/Account/WalletLocked.md)类型表示私钥_不_已知或存储在内存中的钱包。相反，[`WalletLocked`](../../api/Account/WalletLocked.md)仅知道其公共地址。[`WalletLocked`](../../api/Account/WalletLocked.md)不能用于签署交易，但仍然可以执行一整套有用的操作，包括列出交易、资产查询余额等。

请注意，[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)类型实现了[`WalletLocked`](../../api/Account/WalletLocked.md)类型上可用的大多数方法。换句话说，[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)可以被认为是对[`WalletLocked`](../../api/Account/WalletLocked.md)的一个薄包装，通过私钥提供更大的访问权限。

## 基本示例

<<< @/../../docs-snippets/src/guide/wallets/access.test.ts#wallets{ts:line-numbers}

## 可选提供程序

您可以选择在`Wallet`构造函数上不传递提供程序参数：

<<< @/../../docs-snippets/src/guide/wallets/access.test.ts#wallet-optional-provider{ts:line-numbers}

## 状态转换

通过提供私钥，可以解锁[`WalletLocked`](../../api/Account/WalletLocked.md)实例：

<<< @/../../docs-snippets/src/guide/wallets/access.test.ts#wallet-locked-to-unlocked{ts:line-numbers}

可以使用`lock`方法将[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)实例锁定：

<<< @/../../docs-snippets/src/guide/wallets/access.test.ts#wallet-unlocked-to-locked{ts:line-numbers}

大多数创建或生成新钱包的钱包构造函数都在[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)类型上提供。考虑在处理新私钥后使用`lock`方法将钱包锁定，以减少钱包私钥存储在内存中的范围。

## 设计指南

在设计接受钱包作为输入的API时，我们应该仔细考虑所需的访问权限。API开发人员应尽量减少对[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)的使用，以确保私钥的存储时间不会超过必要的时间，从而减少下游库和应用程序中的攻击和漏洞的风险。
