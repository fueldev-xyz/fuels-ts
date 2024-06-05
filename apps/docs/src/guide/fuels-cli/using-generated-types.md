<!-- TODO: Replace plan-text by code-snippets -->

# 使用生成的类型

通过以下方式生成类型：

```console
pnpm fuels typegen -i ./abis/*-abi.json -o ./types
```

我们可以像这样使用这些文件：

<<< @/../../demo-typegen/src/demo.test.ts#typegen-demo-contract-factory-connect{ts:line-numbers}

## 合约

让我们使用 Contract 类来部署一个合约：

<<< @/../../demo-typegen/src/demo.test.ts#typegen-demo-contract-factory-deploy{ts:line-numbers}

### 自动加载存储槽

Typegen 试图在 `MyContract__factory` 类中解析、自动加载并嵌入您的合约的[存储槽](../contracts/storage-slots.md)。但是，在调用 `deployContract` 方法时，您仍然可以覆盖它以及来自 [`DeployContractOptions`](https://github.com/FuelLabs/fuels-ts/blob/a64b67b9fb2d7f764ab9151a21d2266bf2df3643/packages/contract/src/contract-factory.ts#L19-L24) 的其他选项：

<<< @/../../demo-typegen/src/demo.test.ts#typegen-demo-contract-storage-slots{ts:line-numbers}

## 脚本

通过以下方式生成类型：

```console
pnpm fuels typegen -i ./abis/*-abi.json -o ./types --script
```

我们可以像这样使用这些文件：

<<< @/../../demo-typegen/src/demo.test.ts#typegen-demo-script{ts:line-numbers}

## 断言

通过以下方式生成类型：

```console
pnpm fuels typegen -i ./abis/*-abi.json -o ./types --predicate
```

我们可以像这样使用这些文件：

<<< @/../../demo-typegen/src/demo.test.ts#typegen-demo-predicate{ts:line-numbers}

另请参阅：

- [为合约生成类型](./generating-types.md#generating-types-for-contracts)
- [为脚本生成类型](./generating-types.md#generating-types-for-scripts)
- [为断言生成类型](./generating-types.md#generating-types-for-predicates)
