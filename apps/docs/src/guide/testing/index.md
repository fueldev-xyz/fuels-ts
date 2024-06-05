<script setup>
  import { data } from '../../versions.data'
  const { forc } = data
  const url = `https://docs.fueldev.xyz/docs/forc/commands/forc_test/`
</script>

# 测试

为了测试您的 Sway 和 TS-SDK 应用程序，您可以通过多种方式测试您的代码：

1. 使用 TS-SDK 进行测试：编译您的 Sway 代码并使用 TS-SDK 和 JS 测试框架连接到方法
2. 使用 `forc test`，请参阅 <a :href="url" target="_blank" rel="noreferrer">Sway 文档</a> 了解更多信息
3. 使用 [Rust SDK](https://docs.fueldev.xyz/docs/fuels-rs/testing/)

### 使用 TS-SDK 进行测试

要使用 TS-SDK 测试您的 Sway 应用程序，您可以选择您感觉舒适的任何测试库或框架。没有特定的测试框架是必需的，完全取决于用户。尽管如此，TS-SDK 使用 [`Vitest`](https://vitest.dev/) 进行测试。

### 钱包测试实用工具

在测试合同时，您经常会想要创建一个或多个测试钱包。

为此，您可以在账户包中找到两个简单的实用程序：

- [`@fuel-ts/account`](https://github.com/FuelLabs/fuels-ts/tree/master/packages/account#test-utilities)

除了这两个实用程序之外，如果您想要快速启动并运行本地节点，您可以使用 `@fuel-ts/account/test-utils` 包中的 `launchNodeAndGetWallets`。

```ts
import { launchNodeAndGetWallets } from "@fuel-ts/account/test-utils";

const { stop, wallets, provider } = await launchNodeAndGetWallets();

// ... 进行您的测试 - 使用钱包部署合同，从提供程序获取信息，等等。

// 测试完成后停止节点
stop();
```

另请参阅：

1. [设置测试钱包](../wallets/test-wallets.md)
2. [在 TS 中进行测试](./testing-in-ts.md)
