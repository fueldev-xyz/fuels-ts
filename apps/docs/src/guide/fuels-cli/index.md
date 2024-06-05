<script setup>
  import { data } from '../../versions.data'
  const { fuels } = data
</script>

# Fuels CLI

构建全栈 Fuel dApps 的最快方式。

- [`fuels init`](./commands.md#fuels-init) — 创建新的 `fuels.config.ts` 文件
- [`fuels build`](./commands.md#fuels-build) — 构建 `forc` workspace 并为所有内容生成 Typescript 类型
- [`fuels deploy`](./commands.md#fuels-deploy) — 部署 workspace 合约并将它们的 ID 保存到 JSON 文件中
- [`fuels dev`](./commands.md#fuels-dev) — 在每次文件更改时启动本地 Fuel Core _节点_ 并执行 `build` + `deploy`

## 入门指南

假设您有以下文件结构：

```sh
my-fuel-dapp # NextJS app or similar
├── sway-programs # Forc's workspace
│   ├── src
│   ├── ...
│   └── Forc.toml
├── public
│   └── ...
├── src
│   ├── app
│   ├── ...
├   └── sway-programs-api # Type-safe generated API
└── package.json
```

## 先决条件

[Fuel 工具链](https://docs.fueldev.xyz/docs/sway/introduction/fuel_toolchain/#the-fuel-toolchain) 及其组件（主要是 `forc` 和 `fuel-core`）是使用 Fuels CLI 进行几个操作的先决条件。例如：

- 使用 [`fuels build`](./commands.md#fuels-build) 构建合约需要 `forc`。
- 使用 [`fuels deploy`](./commands.md#fuels-deploy) 在本地部署合约需要 `fuel-core`。

如果您尚未安装它们，请按照 [安装指南](https://docs.fueldev.xyz/guides/installation/) 进行操作。

## 安装

将其添加到您的 `my-fuel-dapp` 项目中：

::: code-group

```console-vue [npm]
npm install fuels@{{fuels}} --save
```

```console-vue [pnpm]
pnpm add fuels@{{fuels}}
```

:::

## 再次检查

```console-vue
npx fuels@{{fuels}} -v
```

## 下一步

使用 [`pnpm fuels init`](./commands.md#fuels-init) 创建 [`fuel.config.ts`](./config-file.md) 文件。
