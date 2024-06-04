# 连接到本地节点

首先，你需要在你的机器上运行一个本地节点。我们推荐以下方法之一：

- [测试工具](../testing/index.md#wallet-test-utilities) 可以帮助你以编程方式启动一个短暂的节点。
- 在本地运行 [fuel-core](https://docs.fueldev.xyz/guides/running-a-node/running-a-local-node/)。

在下面的示例中，我们创建了一个提供程序来连接到本地节点并签署消息。

<<< @/../../docs-snippets/src/guide/introduction/getting-started.test.ts#connecting-to-the-local-node{ts:line-numbers}