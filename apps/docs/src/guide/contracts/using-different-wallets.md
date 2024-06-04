# 使用不同的钱包或提供者进行调用

本指南演示了如何通过将 [`Account`](../../api/Account/Account.md) 或 [`Provider`](../../api/Account/Provider.md) 传递给合约实例来使用不同的钱包和提供者进行合约调用。

## 更改钱包

要更改与合约实例关联的钱包，请将新钱包分配给实例的 `account` 属性。这样可以以简洁的方式使用不同的钱包进行合约调用：

<<< @/../../docs-snippets/src/guide/contracts/calls-with-different-wallets.test.ts#calls-with-different-wallets-1{ts:line-numbers}

## 更改提供者

类似地，您可以通过修改其 `provider` 属性为合约实例分配自定义提供者。这样可以使用您选择的提供者包装器：

<!-- TODO: Replace with a proper snippet. We lost this snippet because this test had to be removed/changed -->

```ts
const newProvider = await Provider.create(NEW_URL);
deployedContract.provider = newProvider;
```

> **注意：** 当将不同的钱包连接到现有的合约实例时，用于部署合约的提供者优先于新设置的提供者。如果您有两个钱包连接到不同的提供者（每个与不同的 fuel-core 实例通信），则将使用分配给部署钱包的提供者进行合约调用。此行为仅在存在多个提供者（即 fuel-core 实例）时才相关，并且在其他情况下可以忽略。