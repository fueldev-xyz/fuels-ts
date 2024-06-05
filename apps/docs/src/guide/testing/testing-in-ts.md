# 在 TS 中进行测试

正如在[测试介绍](./index.md)中所述，您可以自由地使用任何可用的 JS 框架来测试您的 Sway 和 TS-SDK 代码。下面是一个使用 `Vitest` 加载和测试合约的示例，但是任何测试工具的一般原理和步骤都是相同的。

这是一个简单的 Sway 程序，它接受一个输入然后返回它：

<<< @/../../demo-typegen/contract/src/main.sw#Testing-in-ts-rust{rust:line-numbers}

以下是使用传统的 `Vitest` 设置测试上述程序的 JavaScript 代码：

<<< @/../../demo-typegen/src/demo.test.ts#Testing-in-ts-ts{ts:line-numbers}

> **注意：** TS-SDK 最近迁移到了 `Vitest`，但它与 Jest 具有非常相似的 API，上面的示例同样适用于 Jest。
