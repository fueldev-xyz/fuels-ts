<script setup>
  import { data } from './versions.data'
  const { forc, fuels, fuelCore } = data
  const url = `https://docs.fueldev.xyz/docs/forc/`
  const logoSrc = './fuel-logo.png'
</script>

# Fuel TypeScript SDK

Fuel TypeScript SDK 提供了 TypeScript 方法和工具，用于在 Fuel 网络及其[生态系统](https://docs.fueldev.xyz/docs/intro/what-is-fuel/)上进行开发或交互。

使用该 SDK 你可以：

- 部署、交互和测试 [Sway](https://docs.fueldev.xyz/docs/sway/) 合约。
- 使用 [create fuels CLI](https://docs.fueldev.xyz/docs/fuels-ts/creating-a-fuel-dapp/) 启动一个 dApp 和本地开发环境。
- 通过私钥、助记词或 JSON 生成和导入钱包，并在客户端上安全存储它们。
- 制作自定义交易，并通过添加资源、策略和签名者来修改它们并提交。
- 使用 [typegen](https://docs.fueldev.xyz/docs/fuels-ts/fuels-cli/abi-typegen/) 为 [Sway 程序](https://docs.fueldev.xyz/docs/sway/sway-program-types/) 生成类型，以实现端到端的类型安全。

## 版本

本文档使用 Fuels `v{{fuels}}`，Fuel Core `v{{fuelCore}}`，Sway `v{{forc}}` 和 Forc `v{{forc}}` 生成。