# 钱包

钱包可以用于许多重要的事情，例如：

1. 检查余额；
2. 将硬币转移到目标地址或合约；
3. 签署消息和交易；
4. 在发送交易或部署智能合约时支付网络费用。

## 钱包实例

SDK中有多个与钱包实例相关的类：

- [Wallet](../../api/Account/Wallet.md)：简单地像一个包装器，提供了创建和实例化`WalletUnlocked`和`WalletLocked`实例的方法。

- [WalletLocked](../../api/Account/WalletLocked.md)：为锁定的钱包提供功能。

- [WalletUnlocked](../../api/Account/WalletUnlocked.md)：为解锁的钱包提供功能。

- [Account](../../api/Account/Account.md)：为钱包或账户与网络交互提供了基本功能的抽象。需要注意的是，`WalletLocked`和`WalletUnlocked`都是从`Account`类继承的。

让我们在以下子章节中探讨这些不同的方法。

> **注意：** 请记住，您永远不应分享您的私钥/密钥。对于从助记词短语派生的钱包，永远不要分享您的助记词短语。如果您打算将钱包存储在磁盘上，请不要存储明文私钥/密钥，也不要存储明文助记词短语。相反，使用`WalletManager`先加密其内容，然后再保存到磁盘上。
