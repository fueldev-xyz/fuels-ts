# GraphQL 集成

Fuel 网络提供了 [GraphQL API](https://docs.fueldev.xyz/docs/graphql/overview/) 用于查询区块链。要更好地了解底层模式和其他操作，您可以访问 [playground](https://devnet.fuel.network/v1/playground) 进行交互式深入探讨。

## 操作

为了满足自身的需求，SDK 基于 API 的模式创建自定义操作，并通过代码生成工具自动生成 TypeScript 客户端代码。
该代码生成的最终结果是 [`Provider`](../provider/index.md) 上可用的操作，以下是其中的一些示例：

<<< @/../../docs-snippets/src/guide/provider/provider.test.ts#operations{ts:line-numbers}

请注意，这些操作主要用于满足 SDK 和 `Provider` 方法的需求，它们可以封装对多个操作的调用、解析响应等。

如果您的查询需求超出了 `Provider` 提供的范围，我们建议您按照同样的流程编写自己的自定义查询操作，例如：

```gql
query getChain {
  latestBlock {
    transactions {
      id
    }
  }
}
```

### 变更和订阅

对于变更和订阅，我们强烈建议您通过 `Provider` 与节点通信，而不是编写自己的自定义 GraphQL 操作，因为在其方法中，`Provider` 在将它们发送到节点之前和之后进行了额外的处理，这可能需要对各种 Fuel 领域特定主题有详细的了解。
