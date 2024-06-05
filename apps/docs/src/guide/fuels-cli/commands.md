<script setup>
  import { data } from '../../versions.data'
  const { fuels, forc, fuelCore } = data
</script>

# 命令

`fuels` CLI 包含几个命令。

## `fuels init`

```console-vue
npx fuels@{{fuels}} help init
```

```console
Options:
  -w, --workspace <path>          Forc 工作区的相对目录路径
  -c, --contracts <path|global>   智能合约的相对路径/全局路径
  -s, --scripts <path|global>     脚本的相对路径/全局路径
  -p, --predicates <path|global>  断言的相对路径/全局路径
  -o, --output <path>             生成 TypeScript 的相对目录路径
```

创建一个示例 `fuel.config.ts` 文件：

```console-vue
npx fuels@{{fuels}} init --contracts ./my-contracts/* --output ./src/sway-contracts-api
```

使用 [Forc 工作区](https://docs.fueldev.xyz/docs/forc/workspaces/)？请尝试以下操作：

```console-vue
npx fuels@{{fuels}} init --workspace ./sway-programs --output ./src/sway-programs-api
```

这将为您提供一个最小的配置：

<<< @../../../demo-fuels/fuels.config.minimal.ts#config{ts:line-numbers}

简而言之：

```sh
.
├── sway-programs # <— forc 工作区
├── src
│   └── sway-programs-api # <— 输出
├── fuels.config.ts
└── package.json
```

### 查看更多

- [Forc 工作区](https://docs.fueldev.xyz/docs/forc/workspaces/)

## `fuels build`

```console-vue
npx fuels@{{fuels}} help build
```

```console
Options:
  -p, --path <path>  项目根目录路径 (默认值: "/Users/anderson/Code/fuel/fuels-ts/apps/docs")
  -d, --deploy       构建后部署合约（如果需要，会自动启动 `fuel-core` 节点）
  -h, --help         显示帮助信息
```

示例：

```console-vue
npx fuels@{{fuels}} build
```

1. 使用 `forc` 构建工作区下的所有 Sway 程序 <sup>[1](https://docs.fueldev.xyz/docs/forc/commands/forc_build/)</sup>
1. 为它们生成类型使用 `fuels-typegen` <sup>[2](#fuels-typegen)</sup>

```console-vue
npx fuels@{{fuels}} build --deploy
```

使用 `--deploy` 标志还会额外执行以下操作：

1. 如果 _需要_，自动启动短暂的 `fuel-core` 节点（[文档](./config-file.md#autostartfuelcore)）
1. 在该节点上运行 `deploy`

> _在与合约一起工作时，此选项非常有用，因为合约的 ID 仅在部署时生成。_

## `fuels deploy`

```console-vue
npx fuels@{{fuels}} deploy
```

> [!NOTE] 注意
> 我们建议仅在将合约部署到本地节点时使用 `fuels deploy` 命令。
> 如果要将合约部署到像测试网这样的真实网络，建议改用 [`forc deploy`](https://docs.fueldev.xyz/docs/intro/quickstart-contract/#deploy-to-testnet) 命令。

`fuels deploy` 命令执行两个操作：

1. 部署工作区下的所有 Sway 合约。
1. 将它们的部署 ID 保存到：
   - _`./src/sway-programs-api/contract-ids.json`_

```json
{
  "myContract1": "0x..",
  "myContract2": "0x.."
}
```

在实例化您的合约时使用它：

<<< @../../../demo-fuels/src/index.test.ts#using-generated-files{ts:line-numbers}

有关完整示例，请参见：

- [使用生成的类型](./using-generated-types.md)


## `fuels dev`

```console-vue
npx fuels@{{fuels}} dev
```

`fuels dev` 命令执行三个操作：

1. 自动启动一个短暂的 `fuel-core` 节点（[文档](./config-file.md#autostartfuelcore)）
1. 在启动时运行 `build` 和 `deploy` 一次
1. 监视您的 Forc 工作区，并在每次更改时重复上一步

> _在 `dev` 模式下，每次您更新 Forc `workspace` 上的合约时，我们会重新生成类型定义和工厂类，并将其保存到您预先配置的 [`output`](./config-file.md#output) 目录中。如果它是在另一个以开发模式运行的构建系统中（例如 `next dev`），您可以期望它重新构建 / 自动重新加载。_

## `fuels node`

```console-vue
npx fuels@{{fuels}} node
```

`fuels node` 命令启动一个短暂的 `fuel-core` 节点（[文档](./config-file.md#autostartfuelcore)）。

## `fuels typegen`

从 ABI JSON 文件手动生成类型定义和工厂类。

```console-vue
npx fuels@{{fuels}} help typegen
```

```console
Options:
  -i, --inputs <path|glob...>  Abi JSON 文件的输入路径/全局路径
  -o, --output <dir>           生成文件的目录路径
  -c, --contract               为合约生成类型 [默认]
  -s, --script                 为脚本生成类型
  -p, --predicate              为断言生成类型
  -S, --silent                 省略输出消息
```

了解更多信息，请查看：

- [从 ABI 生成类型](./generating-types.md)

## `fuels versions`

检查您的 [Fuel Toolchain](https://docs.fueldev.xyz/docs/sway/introduction/fuel_toolchain/#the-fuel-toolchain) 组件版本之间的版本不兼容性，将它们与您使用的 Typescript SDK 版本支持的版本进行匹配。


```console-vue
npx fuels@{{fuels}} versions
```

```console-vue
┌───────────┬───────────┬────────────────┬─────────────┐
│           │ Supported │ Yours / System │ System Path │
├───────────┼───────────┼────────────────┼─────────────┤
│ Forc      │ {{forc}}    │ {{forc}}         │ forc        │
├───────────┼───────────┼────────────────┼─────────────┤
│ Fuel-Core │ {{fuelCore}}    │ {{fuelCore}}         │ fuel-core   │
└───────────┴───────────┴────────────────┴─────────────┘

You have all the right versions! ⚡
```
