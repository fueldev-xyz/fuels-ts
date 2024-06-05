# 配置文件

在这里，您可以了解有关所有配置选项的更多信息。

## `workspace`

到 Forc 工作空间的相对目录路径。

<<< @../../../demo-fuels/fuels.config.full.ts#workspace{ts:line-numbers}

> _属性 `workspace` 与 [`contracts`](#contracts)、[`predicates`](#predicates) 和 [`scripts`](#scripts) 不兼容。_

## `contracts`

到 Sway 合约的相对目录路径列表。

<<< @../../../demo-fuels/fuels.config.full.ts#contracts{ts:line-numbers}

> _属性 `contracts` 与 [`workspace`](#workspace) 不兼容。_

## `predicates`

到 Sway 断言的相对目录路径列表。

<<< @../../../demo-fuels/fuels.config.full.ts#predicates{ts:line-numbers}

> _属性 `predicates` 与 [`workspace`](#workspace) 不兼容。_

## `scripts`

到 Sway 脚本的相对目录路径列表。

<<< @../../../demo-fuels/fuels.config.full.ts#scripts{ts:line-numbers}

> _属性 `scripts` 与 [`workspace`](#workspace) 不兼容。_

## `output`

生成 TypeScript 定义时要使用的相对目录路径。

<<< @../../../demo-fuels/fuels.config.full.ts#output{ts:line-numbers}

## `providerUrl`

部署合约时要使用的 URL。

<<< @../../../demo-fuels/fuels.config.full.ts#providerUrl{ts:line-numbers}

> _当 [`autostartFuelCore`](#autostartfuelcore) 属性设置为 `true` 时，`providerUrl` 会被最近由 [`fuels dev`](./commands.md#fuels-dev) 命令启动的本地短暂 `fuel-core` 节点的 URL 覆盖。_

## `privateKey`

部署合约时使用的钱包私钥。

此属性应该理想地来自环境变量 — `process.env.MY_PRIVATE_KEY`。

<<< @../../../demo-fuels/fuels.config.full.ts#privateKey{ts:line-numbers}

> _当 [`autostartFuelCore`](#autostartfuelcore) 属性设置为 `true` 时，`privateKey` 会被最近由 [`fuels dev`](./commands.md#fuels-dev) 命令启动的本地短暂 `fuel-core` 节点的 `consensusKey` 覆盖。_

## `snapshotDir`

> - _仅由 [`fuels dev`](./commands.md#fuels-dev) 使用_。

包含自定义配置（例如 `chainConfig.json`、`metadata.json`、`stateConfig.json`）的目录的相对路径。

仅当 [`autoStartFuelCore`](#autostartfuelcore) 为 `true` 时才会生效。

<<< @../../../demo-fuels/fuels.config.full.ts#snapshotDir{ts:line-numbers}

## `autoStartFuelCore`

> - _仅由 [`fuels dev`](./commands.md#fuels-dev) 使用_。

当设置为 `true` 时，它将自动执行以下操作：

1. 作为 [`fuels dev`](./commands.md#fuels-dev) 命令的一部分启动一个短暂的 `fuel-core` 节点
1. 使用最近启动的 `fuel-core` 节点的 URL 覆盖属性 [`providerUrl`](#providerurl)

<<< @../../../demo-fuels/fuels.config.full.ts#autoStartFuelCore{ts:line-numbers}

如果设置为 `false`，您必须自己启动一个 `fuel-core` 节点，并通过 [`providerUrl`](#providerurl) 设置其 URL。

## `fuelCorePort`

> - _仅由 [`fuels dev`](./commands.md#fuels-dev) 使用_。
> - _当 [`autoStartFuelCore`](#autostartfuelcore) 设置为 `false` 时忽略_。

启动本地 `fuel-core` 节点时要使用的端口。

<<< @../../../demo-fuels/fuels.config.full.ts#fuelCorePort{ts:line-numbers}

## `forcBuildFlags`

> - _由 [`fuels build`](./commands.md#fuels-build) 和 [`fuels deploy`](./commands.md#fuels-deploy) 使用_。

Sway 程序默认以 `debug` 模式编译。

在此处，您可以自定义所有构建标志，例如以 `release` 模式构建程序。

<<< @../../../demo-fuels/fuels.config.full.ts#forcBuildFlags{ts:line-numbers}

还请查看：

- [Forc 文档](https://docs.fueldev.xyz/docs/forc/commands/forc_build/#forc-build)

## `deployConfig`

您可以提供一个就绪的部署配置对象：

<<< @../../../demo-fuels/fuels.config.full.ts#deployConfig-obj{ts:line-numbers}

或使用一个函数来构建动态部署流程：

- 如果您需要从远程数据源获取并使用配置或数据
- 如果您需要使用已部署合约的 ID — 在这种情况下，我们可以使用 `options.contracts` 属性获取所需的合约 ID。例如：

<<< @../../../demo-fuels/fuels.config.full.ts#deployConfig-fn{ts:line-numbers}

## `onSuccess`

传递一个回调函数，在成功运行后调用。

参数：

- `event` — 触发此执行的事件
- `config` — 加载的配置（`fuels.config.ts`）

<<< @../../../demo-fuels/fuels.config.full.ts#onSuccess{ts:line-numbers}

## `onFailure`

传递一个回调函数，以处理错误情况。

参数：

- `error` — 原始错误对象
- `config` — 加载的配置（`fuels.config.ts`）

<<< @../../../demo-fuels/fuels.config.full.ts#onFailure{ts:line-numbers}

## `forcPath`

`forc` 二进制文件的路径。

当未提供时，默认使用 `system` 二进制文件（`forc`）。

<<< @../../../demo-fuels/fuels.config.full.ts#forcPath{ts:line-numbers}

## `fuelCorePath`

`fuel-core` 二进制文件的路径。

当未提供时，默认使用 `system` 二进制文件（`fuel-core`）。

<<< @../../../demo-fuels/fuels.config.full.ts#fuelCorePath{ts:line-numbers}

## 加载环境变量

如果您想要从 `.env` 文件中加载环境变量，您可以使用 `dotenv` 包。

首先，安装它：

::: code-group

```sh [pnpm]
pnpm install dotenv
```

```sh [npm]
npm install dotenv
```

:::

然后，您可以在您的 `fuels.config.ts` 文件中使用它：

<<< @../../../create-fuels-counter-guide/fuels.config.ts#fuels-config-file-env{ts:line-numbers}
