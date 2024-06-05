# 设置自定义链

`launchNodeAndGetWallets` 方法允许您使用各种自定义启动本地 Fuel 节点。

在下面的代码片段中，我们提供了一个包含几个文件的快照目录：

- `chainConfig.json`
- `stateCondig.json`
- `metadata.json`

您可以使用自定义快照来自定义诸如链的共识参数或为链指定一些初始状态等内容。

以下是一些示例：

- [`chainConfig.json`](https://github.com/FuelLabs/fuels-ts/blob/master/.fuel-core/configs/chainConfig.json)
<!-- - [`stateConfig.json`](https://github.com/FuelLabs/fuels-ts/blob/master/.fuel-core/configs/stateConfig.json)
- [`metadata.json`](https://github.com/FuelLabs/fuels-ts/blob/master/.fuel-core/configs/metadata.json) -->

<<< @/../../../packages/account/src/test-utils/launchNodeAndGetWallets.test.ts#launchNode-custom-config{ts:line-numbers}

## 自定义选项

正如您在上一个代码片段中看到的，您可以选择向 `launchNodeAndGetWallets` 方法传递 `walletCount` 和一些 `launchNodeOptions`。

`walletCount` 选项允许您指定要生成的钱包数量。默认值为 10。

`launchNodeOptions` 选项允许您为节点指定一些附加选项。可用的选项包括：

<<< @/../../../packages/account/src/test-utils/launchNode.ts#launchNode-launchNodeOptions{ts:line-numbers}

> 注意：您可以通过运行 `pnpm fuels core run -h` 查看所有可用的 fuel-core 参数。
