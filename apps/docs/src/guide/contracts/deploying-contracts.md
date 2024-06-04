<script setup>
  import { data } from '../../versions.data'
  const { forc } = data
  const indexUrl = `https://docs.fueldev.xyz/docs/sway/introduction/`
  const jsonAbiUrl = `https://docs.fueldev.xyz/docs/sway/introduction/sway_quickstart/`
</script>
# 部署合约

本指南将带您通过使用 SDK 部署合约，涵盖加载合约工件、初始化合约工厂和部署合约的过程。

## 1. 获取合约工件

在 Sway 中编写合约并使用 `forc build` 进行编译后（<a :href="indexUrl" target="_blank" rel="noreferrer">了解更多</a>关于如何使用 Sway），您将获得两个重要的工件：编译后的二进制文件和 JSON ABI 文件。这些文件是使用 SDK 部署合约所必需的。

## 2. 设置 SDK 环境

在部署合约之前，通过导入所需的 SDK 组件并初始化钱包和提供程序来设置必要的环境。

<<< @/../../docs-snippets/src/guide/contracts/deploying-contracts.test.ts#contract-setup-1{ts:line-numbers}

## 3. 加载合约工件

将从 Sway 源生成的合约字节码和 JSON ABI 加载到 SDK 中。

<<< @/../../docs-snippets/src/guide/contracts/deploying-contracts.test.ts#contract-setup-2{ts:line-numbers}

## 4. 部署合约

使用合约字节码、ABI 和钱包初始化 [`ContractFactory`](../../api/Contract/ContractFactory.md)。部署合约并使用其方法。

<<< @/../../docs-snippets/src/guide/contracts/deploying-contracts.test.ts#contract-setup-3{ts:line-numbers}

## 5. 执行合约调用

现在合约已部署，您可以与其进行交互。在接下来的步骤中，您将学习如何执行合约调用。

<<< @/../../docs-snippets/src/guide/contracts/deploying-contracts.test.ts#contract-setup-4{ts:line-numbers}

要了解更全面的 TypeScript 支持的 Fuel 使用，请学习如何[从 ABI 生成类型](../fuels-cli/generating-types.md)。