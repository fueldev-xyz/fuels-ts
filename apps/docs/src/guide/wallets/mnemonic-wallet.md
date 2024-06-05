# 从助记词短语创建钱包

助记词短语是一个经过加密生成的单词序列，用于派生私钥。例如："oblige salon price punch saddle immune slogan rare snap desert retire surprise"将生成地址"0xdf9d0e6c6c5f5da6e82e5e1a77974af6642bdb450a10c43f0c6910a212600185"。

除此之外，我们还支持[分层确定性钱包](https://www.ledger.com/academy/crypto/what-are-hierarchical-deterministic-hd-wallets)和[派生路径](https://learnmeabitcoin.com/technical/derivation-paths)。你可能从某个地方认出了字符串"m/44'/60'/0'/0/0"；那就是一个派生路径。简单来说，它是从单个根钱包派生出许多钱包的一种方式。

SDK为您提供了两种从助记词实例化钱包的方法：一种是采用派生路径，另一种是使用默认的派生路径，以防您不想或不需要配置。

以下是如何使用助记词和派生路径创建钱包的方法：

<<< @/../../../packages/account/src/wallet-manager/wallet-manager.test.ts#wallet-manager-mnemonic{ts:line-numbers}
