# 存储槽位

在部署合约时，您可以指定要使用的自定义存储槽位。

<<< @/../../../packages/fuel-gauge/src/storage-test-contract.test.ts#contract-deployment-storage-slots{ts:line-numbers}

## 使用普通 JavaScript

在上面的示例中，我们直接从由 Sway 编译器生成的 JSON 文件中导入了存储槽位。

您也可以直接在代码中指定自定义的存储槽位，而不是从文件中导入：

<<< @/../../../packages/fuel-gauge/src/storage-test-contract.test.ts#contract-deployment-storage-slots-inline{ts:line-numbers}

## 自动加载存储槽位

使用 [Typegen](../fuels-cli/generating-types.md) 生成的代码会自动为您[加载](../fuels-cli/using-generated-types.md#autoloading-of-storage-slots)存储槽位。