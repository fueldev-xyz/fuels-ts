# 将 dApp 部署到测试网络

在本指南中，我们将使用 `npm create fuels` 命令将一个全栈 dApp 部署到 Fuel 测试网络。

> 确保您已经使用 `npm create fuels` 创建了一个 dApp。如果没有，请参考[此指南](./index.md)。

将我们的 dApp 上线到测试网络主要有两个步骤：

1. 将合约部署到测试网络
2. 将前端部署到云端

## 部署合约

我们将使用 [`forc`](https://docs.fueldev.xyz/docs/forc/) 来将我们的合约部署到测试网络。`forc` 是 Fuel 工具链的一部分。

> 如果您尚未安装 Fuel 工具链，请按照[此指南](https://docs.fueldev.xyz/guides/installation/)进行安装。

第一步是进入包含您的合约的目录：

```sh
cd sway-programs/contract
```

然后，运行以下命令并按照提示将合约部署到测试网络：

```sh
forc deploy --testnet
```

> 您可以查看[此指南](https://docs.fueldev.xyz/docs/intro/quickstart-contract/#deploy-to-testnet)了解更多有关将合约部署到测试网络的信息。

您应该会看到类似以下的消息：

```md
Contract deploy-to-testnet Deployed!

Network: https://devnet.fuel.network
Contract ID: 0x8342d413de2a678245d9ee39f020795800c7e6a4ac5ff7daae275f533dc05e08
Deployed in block 0x4ea52b6652836c499e44b7e42f7c22d1ed1f03cf90a1d94cd0113b9023dfa636
```

复制合约 ID 并保存以备后用。

## 部署前端

现在让我们准备好前端，以便我们可以将其部署到云端。

进入您的 `.env.local` 文件并添加一个名为 `NEXT_PUBLIC_TESTNET_CONTRACT_ID` 的新变量。将其值设置为您之前在部署合约时复制的合约 ID。

```md
NEXT_PUBLIC_TESTNET_CONTRACT_ID=0x8342d413de2a678245d9ee39f020795800c7e6a4ac5ff7daae275f533dc05e08
```

如果您感兴趣，这个环境变量在 `src/pages/index.tsx` 文件中用于设置合约 ID：

<<< @/../../create-fuels-counter-guide/src/pages/index.tsx#deploying-dapp-to-testnet-frontend-contract-id{ts:line-numbers}

您会注意到这段代码根据当前环境获取合约 ID。如果环境是 `local`，它将使用自动生成的 `contract-ids.json` 文件中的合约 ID。否则，对于测试网络部署，它将使用您提供的合约 ID。

`CURRENT_ENVIRONMENT` 变量在 `lib.ts` 文件中定义：

<<< @/../../create-fuels-counter-guide/src/lib.ts#deploying-dapp-to-testnet-lib-current-environment{ts:line-numbers}

如您所见，它依赖于 `NEXT_PUBLIC_DAPP_ENVIRONMENT` 环境变量。如果您查看您的 `.env.local` 文件，您会看到它默认设置为 `local`。如果您将此值更改为 `testnet`，则前端现在将连接到测试网络，而不是您的本地节点。

现在，请在您的 `.env.local` 文件中将 `NEXT_PUBLIC_DAPP_ENVIRONMENT` 值更改为 `testnet`。
如果现在运行您的前端，您应该能够在测试网络上与您的合约交互。

要将您的前端部署到云端，您可以使用任何服务，比如 [Vercel](https://vercel.com/)。确保您正确设置了环境变量，并且您的合约 ID 正确。您的环境变量应该如下所示：

```md
NEXT_PUBLIC_HAS_CONTRACT=true
NEXT_PUBLIC_DAPP_ENVIRONMENT=testnet
NEXT_PUBLIC_TESTNET_CONTRACT_ID=0x8342d413de2a678245d9ee39f020795800c7e6a4ac5ff7daae275f533dc05e08

（其他环境变量是可选的）
```

## 结论

恭喜！您已成功将您的 Fuel dApp 部署到测试网络。

要简要总结，将您的 dApp 部署到测试网络，您需要执行以下步骤：

1. 使用 `forc deploy --testnet` 命令将您的合约部署到测试网络。
2. 在 `src/pages/index.tsx` 中的前端代码中指定此合约 ID。
3. 将 `NEXT_PUBLIC_DAPP_ENVIRONMENT` 环境变量设置为 `testnet`。
