# 连接到测试网

**测试网** 是一个公共网络，允许你与 Fuel 虚拟机进行交互，用于测试和开发目的。

> [!NOTE] 最新测试网
> 开发测试网
>
> `https://devnet.fuel.network/v1/graphql`

我们为测试网提供了一些有用的资源：

- [**水龙头**](https://faucet-devnet.fuel.network/) - 用于为已创建的钱包提供资金。
- [**区块浏览器**](https://app.fuel.network/) - 用于查看交易和区块。
- [**GraphQL Playground**](https://devnet.fuel.network/v1/playground) - 用于测试 GraphQL 查询和变更。

---

在下面的示例中，我们连接一个 [提供程序](../provider/index.md) 到最新的测试网，并使用私钥创建一个新钱包。

> **注意：** 测试网上的新钱包将没有任何资产！你可以使用 [水龙头](https://faucet-devnet.fuel.network/) 来为你的钱包提供资金。

<<< @/../../docs-snippets/src/guide/introduction/getting-started.test.ts#connecting-to-the-testnet{ts:line-numbers}