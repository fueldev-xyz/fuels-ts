<script setup>
  import { data } from '../../versions.data'
  const { fuels } = data
</script>

# 安装

在使用此库之前，我们建议你安装 [Fuel Toolchain](https://docs.fueldev.xyz/docs/sway/introduction/fuel_toolchain/#the-fuel-toolchain)。请按照[本指南](https://docs.fueldev.xyz/guides/installation/)进行安装。

下一步是将 `fuels` 依赖添加到你的项目中。你可以使用以下命令来完成：

::: code-group

```sh-vue [npm]
npm install fuels@{{fuels}} --save
```

```sh-vue [pnpm]
pnpm add fuels@{{fuels}}
```

:::

**注意**：请使用版本 `{{fuels}}` 以确保与 `testnet` 网络兼容——查看[文档](https://docs.fueldev.xyz/guides/installation/#using-the-latest-toolchain)。

---

如果你使用的是 bun，你需要在 `package.json` 中添加一个 `trustedDependencies` 字段：

```json
{
  // ...
  "trustedDependencies": ["@fuel-ts/fuel-core", "@fuel-ts/forc"]
}
```

这是为了确保 bun 在你的项目中包含 `fuel-core` 和 `forc` 二进制文件。

> 重要：我们尚未正式支持 `bun`；使用它需自行承担风险。