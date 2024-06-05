# 实例化钱包

SDK中可以以多种方式实例化钱包。

## 生成新钱包

要生成一个新的、解锁的钱包，请使用[`generate`](../../api/Account/Wallet.md#generate)方法。此方法会创建一个新的[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)实例，该实例立即可用。

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-1{ts:line-numbers}

## 实例化解锁的钱包

创建您现有钱包的[`WalletUnlocked`](../../api/Account/WalletUnlocked.md)实例很容易，可以通过多种方式完成：

从私钥：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-2{ts:line-numbers}

从助记词短语：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-3{ts:line-numbers}

从种子：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-4{ts:line-numbers}

从分层确定性（HD）派生密钥：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-5{ts:line-numbers}

从JSON钱包：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-6{ts:line-numbers}

可以从`WalletLocked`实例化一个`WalletUnlocked`：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-7{ts:line-numbers}

## 实例化锁定的钱包

您还可以仅使用钱包地址实例化[`WalletLocked`](../../api/Account/WalletLocked.md)实例：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-8{ts:line-numbers}

## 连接到提供程序

虽然钱包可以独立于[`Provider`](../../api/Account/Provider.md)使用，但需要进行区块链交互的操作将需要提供程序。

将现有钱包连接到提供程序：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-9{ts:line-numbers}

使用提供程序实例化钱包：

<<< @/../../docs-snippets/src/guide/wallets/instantiating-wallets.test.ts#instantiating-wallets-10{ts:line-numbers}
