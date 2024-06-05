# 钱包管理器

`WalletManager` 是一个强大的工具，用于管理钱包的保险库。它提供了对保险库的强大管理，包括支持自定义存储和所有持有的保险库的强大加密。

## 主要特性

### 使用 `WalletManager` 管理保险库

这包括向特定保险库添加新钱包、从保险库检索所有钱包、导出特定保险库和导出私钥。`WalletManager` 类目前支持两种类型的保险库：`PrivateKeyVault` 和 `MnemonicVault`。

### 自定义存储解决方案

`WalletManager` 支持定义自定义存储解决方案，允许您指定加密的保险库保存在何处以及如何保存。通过支持自定义存储，您可以使 `WalletManager` 适应您的特定需求和安全要求。

### 锁定和解锁 `WalletManager`

`WalletManager` 实现了自动加密机制，安全保存钱包持有的保险库。这不仅保留了您的保险库状态，还确保了存储信息的强大保护。在需要时，您可以通过之前定义的密码轻松解锁和解密保险库。

## 使用 `WalletManager` 入门

本指南提供了有关如何使用 `WalletManager` 的逐步说明。

### 实例化 `WalletManager`

`WalletManager` 构造函数接受一个可选对象来定义其存储。存储描述了 `WalletManager` 将存储其保险库的方式和位置。如果未提供存储，则 `WalletManager` 使用一个默认存储，不会持久化数据。

现在，让我们保持简单，不用担心存储。稍后我们将详细讨论它。

要实例化 `WalletManager`，只需：

<<< @/../../docs-snippets/src/guide/wallet-manager/getting-started-with-wallet-manager.test.ts#getting-started-with-wallet-manager-1{ts:line-numbers}

### 设置 `WalletManager` 密码

默认情况下，创建 `WalletManager` 实例时会处于锁定状态。在使用之前，您需要通过调用 `unlock` 方法来解锁它并设置密码。

<<< @/../../docs-snippets/src/guide/wallet-manager/getting-started-with-wallet-manager.test.ts#getting-started-with-wallet-manager-2{ts:line-numbers}

一旦您的 `WalletManager` 解锁，它就可以管理您的钱包。



### 使用 `WalletManager` 管理保险库

`WalletManager` 中的保险库作为钱包的安全容器。`WalletManager` 通过与这些保险库的交互来管理钱包，支持操作如 `getAccounts`，该操作返回存储在保险库中的所有钱包的公共信息，以及 `exportAccount`，该操作为给定钱包地址导出私钥。

要添加保险库，我们使用 `addVault` 方法。以下是我们如何创建一个私钥保险库并将我们拥有的钱包的私钥添加到其中的示例：

<<< @/../../docs-snippets/src/guide/wallet-manager/getting-started-with-wallet-manager.test.ts#getting-started-with-wallet-manager-3{ts:line-numbers}

`addVault` 方法需要一个具有三个属性的对象：`type`、`secret` 和 `title`。`WalletManager` 目前支持两种类型的保险库：`privateKeyVault` 和 `mnemonicVault`。对于 `secret`，我们使用我们钱包的私钥，对于 `title`，我们可以提供一个自定义名称。

通过运行此代码，`WalletManager` 将创建一个新的类型为 `privateKey` 的保险库实例，并将一个帐户（我们的钱包）添加到这个新创建的保险库中。

`WalletManager` 的一个关键特性是它能够管理多个保险库，即使是相同类型的保险库。这意味着，如果您再次运行 `addVault` 方法，使用相同的参数，`WalletManager` 将创建另一个类型为 `privateKey` 的保险库，其中包含相同的钱包。以下是一个示例：

<<< @/../../docs-snippets/src/guide/wallet-manager/getting-started-with-wallet-manager.test.ts#getting-started-with-wallet-manager-4{ts:line-numbers}

执行此操作后，您会发现您的 `WalletManager` 管理两个 `privateKey` 保险库，都存储着相同的钱包。

请记住，当添加保险库时，`title` 和 `secret` 都是可选的，但提供 `title` 可以更轻松地管理您的保险库和钱包。如果添加保险库时没有提供 `secret`，则结果将是保险库自身生成一个新帐户（钱包）。

### 使用 `WalletManager`

设置好您的 `WalletManager` 后，您现在可以访问您的保险库和钱包。以下是如何检索保险库详细信息的方法：

<<< @/../../docs-snippets/src/guide/wallet-manager/getting-started-with-wallet-manager.test.ts#getting-started-with-wallet-manager-5{ts:line-numbers}

这将输出类似于以下内容：

<<< @/../../docs-snippets/src/guide/wallet-manager/getting-started-with-wallet-manager.test.ts#getting-started-with-wallet-manager-6{bash:line-numbers}

正如您所见，`WalletManager` 为每个保险库分配了唯一的 `vaultIds`。您添加的第一个保险库的 `vaultId` 是 `0`，第二个保险库的 `vaultId` 是 `1`。

让我们使用 `getWallet` 方法检索您的钱包实例：

<<< @/../../docs-snippets/src/guide/wallet-manager/getting-started-with-wallet-manager.test.ts#getting-started-with-wallet-manager-7{ts:line-numbers}

本指南通过步骤指导了如何实例化 `WalletManager`，设置其第一个保险库，并检索保险库信息。接下来的章节将探讨 `WalletManager` 的更多功能，并深入介绍其保险库的使用和存储系统的详细信息。

## 锁定和解锁 `WalletManager`

本指南将指导您使用 `WalletManager` 管理钱包的锁定状态的过程。

### 初始化和解锁 `WalletManager`

如前所述，`WalletManager` 实例开始时处于锁定状态。在使用之前，您需要通过 unlock 方法提供密码来解锁它。

<<< @/../../docs-snippets/src/guide/wallet-manager/locking-and-unlocking-wallet-manager.test.ts#locking-and-unlocking-wallet-manager-1{ts:line-numbers}



### 锁定 `WalletManager`

使用 `lock` 方法锁定 `WalletManager` 时，其所有保险库和关联的帐户（钱包）都将被清除。这种清除是可能的，因为所有数据都经过了存储系统的加密和保存。`WalletManager` 经常使用存储系统来保持其状态。因此，当它被锁定时，诸如导出保险库、私钥、访问钱包以及保存/加载 `WalletManager` 状态等敏感操作是不可能的。

<<< @/../../docs-snippets/src/guide/wallet-manager/locking-and-unlocking-wallet-manager.test.ts#locking-and-unlocking-wallet-manager-2{ts:line-numbers}

请记住，在不使用 `WalletManager` 时将其锁定是至关重要的，以确保您资金的安全性。

### 通过解锁 `WalletManager` 重新访问您的钱包

`unlock` 方法需要先前设置的密码才能解锁 `WalletManager` 及其所有保险库。密码解密存储的保险库，使得 `WalletManager` 能够加载其保存的数据。

<<< @/../../docs-snippets/src/guide/wallet-manager/locking-and-unlocking-wallet-manager.test.ts#locking-and-unlocking-wallet-manager-3{ts:line-numbers}

提供错误的密码将导致错误。但是，成功解锁后，`WalletManager` 将准备好再次使用。

### 验证锁定状态

您可以使用 `isLocked` 方法确认 `WalletManager` 的当前锁定状态：

<<< @/../../docs-snippets/src/guide/wallet-manager/locking-and-unlocking-wallet-manager.test.ts#locking-and-unlocking-wallet-manager-4{ts:line-numbers}

### 更新密码

要更改当前密码，请调用 `updatePassphrase` 方法，并提供旧密码和新密码：

<<< @/../../docs-snippets/src/guide/wallet-manager/locking-and-unlocking-wallet-manager.test.ts#locking-and-unlocking-wallet-manager-5{ts:line-numbers}

### 提醒：始终锁定您的 `WalletManager`

确保在完成操作后始终锁定 `WalletManager`。这一步对于保护您的钱包至关重要。

<<< @/../../docs-snippets/src/guide/wallet-manager/locking-and-unlocking-wallet-manager.test.ts#locking-and-unlocking-wallet-manager-6{ts:line-numbers}

通过使用 `WalletManager` 管理锁定和解锁状态，您引入了额外的安全层。在不使用时，永远不要忘记锁定您的 `WalletManager`。
