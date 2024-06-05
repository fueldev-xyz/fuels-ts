<script setup>
  import { data } from '../../versions.data'
  const { fuels } = data
</script>

# 创建 Fuel dApp

`npm create fuels` 是一个命令行工具，可帮助您搭建新的全栈 Fuel dApp。在本指南中，我们将使用 `npm create fuels` 创建一个新的计数器 dApp，并为其添加递减功能。最终结果将如下所示：

![此指南的最终结果](../../public/creating-a-fuel-dapp-create-fuels-end-result.png)

## 初始化项目

首先要做的是运行以下命令：

::: code-group

```sh-vue [npm]
npm create fuels@{{fuels}}
```

```sh-vue [pnpm]
pnpm create fuels@{{fuels}}
```

:::

一旦运行命令，您将会看到一些简单的问题。我们将按以下方式回答：

```md
◇ 您的项目名称是什么？
│ my-fuel-project
│
◇ 选择一个包管理器：
│ pnpm
│
◆ 您想要哪些 Sway 程序？（切换空格）
│ ● 合约
│ ○ 断言
│ ○ 脚本
└
```

该工具将为您搭建项目并安装必要的依赖项。然后，您将看到以下消息：

```md
⚡️ 成功！已在 my-fuel-project 中创建了一个全栈 Fuel dapp

要开始使用：

- 进入项目目录：cd my-fuel-project
- 启动本地 Fuel 开发服务器：pnpm fuels:dev
- 运行前端：pnpm dev

-> TS SDK 文档：https://docs.fueldev.xyz/docs/fuels-ts/
-> Sway 文档：https://docs.fueldev.xyz/docs/sway/
-> 如果您有任何问题，请查看 Fuel 论坛：https://forum.fuel.network/
```

## 目录结构

由 `npm create fuels` 搭建的项目大致具有以下目录结构：

```md
my-fuel-project
├── src
│ ├── pages
│ │ ├── index.tsx
│ │ └── ...
│ ├── components
│ │ └── ...
│ ├── styles
│ │ └── ...
│ └── lib.ts
├── public
│ └── ...
├── sway-programs
│ ├── contract
│ │ └── src
│ │ └── main.sw
│ ├── Forc.lock
│ └── Forc.toml
├── fuels.config.ts
├── package.json
└── ...
```

这是一个 Next.js 项目，带有一些额外的文件和文件夹。让我们更详细地查看一些重要的文件：

### `./fuels.config.ts`

这是 [`fuels` CLI](../fuels-cli/index.md) 的配置文件，该 CLI 和工具为项目提供支持。它确保所有的 Sway 程序都持续编译并部署到您的本地 Fuel 节点。您可以在 [Fuels CLI 文档](../fuels-cli/config-file.md) 中了解有关 `fuels.config.ts` 文件的更多信息。

### `./sway-programs/contract/src/main.sw`

这是我们的 Sway 合约所在的位置。默认情况下，它是一个简单的计数器合约，只能递增。我们将在下一步中为其添加递减功能。

### `./src/pages/index.tsx`

该文件包含我们的 dApp 前端的源代码。它是一个 Next.js 页面，用于呈现计数器值，并允许用户递增计数器。

### 开发环境设置

现在我们已经搭建了项目，让我们设置开发环境。

首先启动我们的 Fuel Dev 服务器。这将启动一个本地 Fuel 节点，并持续编译和部署我们的 Sway 程序。

::: code-group

```sh [npm]
pnpm fuels:dev
```

```sh [pnpm]
pnpm fuels:dev
```

:::

一旦服务器启动，我们可以在另一个终端中启动我们的 Next.js 开发服务器。

::: code-group

```sh [npm]
pnpm dev
```

```sh [pnpm]
pnpm dev
```

:::

现在，您应该能够在 `http://localhost:3000` 看到计数器 dApp 正在运行。您可以尝试更改 `./sway-programs/contract/src/main.sw` 文件的内容，并在不重新启动服务器的情况下看到 UI 中的更改。

![全栈 Fuel Dev 工作流程](../../public/creating-a-fuel-dapp-create-fuels-split-view.png)

## 添加递减功能

为了向我们的计数器添加递减功能，我们需要做两件事：1. 在我们的 Sway 合约中添加一个 `decrement_counter` 函数，2. 修改 `./src/pages/index.tsx` 文件以添加一个调用此函数的按钮。

### 1. 修改 Sway 合约

要向我们的 Sway 合约添加一个 `decrement_counter` 函数，我们将修改 `./sway-programs/contract/src/main.sw` 文件。

添加新函数到 Sway 程序时有两个步骤。第一步是指定函数的 ABI。

在文件顶部，您将找到合约的 ABI 部分。让我们向其中添加一个新函数：

<<< @/../../create-fuels-counter-guide/sway-programs/contract/src/main.sw#create-fuels-counter-guide-abi{rust:line-numbers}

第二步是实现函数。

我们将在 `increment_counter` 函数的下方添加 `decrement_counter` 函数的实现。

<<< @/../../create-fuels-counter-guide/sway-programs/contract/src/main.sw#create-fuels-counter-guide-impl{rust:line-numbers}


### 2. 修改前端

我们现在将在前端添加一个新按钮，当点击时将调用 `decrement_counter` 函数。为此，我们将修改 `./src/pages/index.tsx` 文件。

首先，我们将添加一个名为 `onDecrementPressed` 的函数，类似于 `onIncrementPressed` 函数：

<<< @/../../create-fuels-counter-guide/src/pages/index.tsx#create-fuels-counter-guide-on-decrement-react-function{ts:line-numbers}

其次，我们将在界面上添加一个新的按钮，当点击时将调用 `onDecrementPressed` 函数：

<!-- TODO：我们的文档引擎当前无法检测 JSX 中的注释 -->

```tsx
<Button onClick={onDecrementPressed} className="mt-6">
  减少计数器
</Button>
```

恭喜！这就是全部。您现在应该能够在 `http://localhost:3000` 上看到计数器 dApp 运行，并且具有我们新添加的减少功能。

您可以在[这里](https://github.com/FuelLabs/fuels-ts/tree/master/apps/create-fuels-counter-guide)找到我们构建的完整 dApp 的源代码。

![此指南的最终结果](../../public/creating-a-fuel-dapp-create-fuels-end-result.png)

每当您想要为您的 dApp 添加新功能并快速原型设计时，您可以按照本指南中的相同步骤操作。

## 下一步

- 现在您已经有了一个基本的计数器 dApp，并且拥有 `npm create fuels` 工作流支持，您可以开始使用 Fuel Stack 构建更复杂的 dApps。一个好的起点是 [Sway Applications Repo](https://github.com/FuelLabs/sway-applications)，那里有关于想法和参考代码的好地方。

- 如果您想要将您的 dApp 部署到测试网，请查看我们的[将 dApp 部署到测试网](./deploying-a-dapp-to-testnet.md)指南。

- 如果您有任何问题或需要帮助，请随时在[官方 Fuel 论坛](https://forum.fuel.network/)上联系我们。

- 如果您想了解更多关于 Fuel Stack 的信息，请查阅 [Fuel 文档](https://docs.fueldev.xyz/)。
