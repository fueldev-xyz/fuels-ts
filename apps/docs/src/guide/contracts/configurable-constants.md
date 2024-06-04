# 可配置常量

Sway 引入了一个强大的功能：可配置常量。在创建合约时，你可以定义常量，并为每个常量分配一个默认值。

在部署合约之前，你可以重新定义这些常量的值，可以是所有常量，也可以是你需要的尽可能多的常量。

这个功能为动态合约环境提供了灵活性。它允许高度定制，从而导致更高效和更适应智能合约。

## 定义可配置常量

以下是一个合约的示例，在该合约中，我们声明了四个可配置的常量：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-configurables/src/main.sw#configurable-constants-1{rust:line-numbers}

在这个合约中，我们有一个名为 `echo_configurables` 的函数，该函数返回可配置常量的值。

如果每个常量都有新值分配给它们，函数将返回更新后的值。否则，函数将返回默认值。

## 为可配置常量设置新值

在合约部署期间，你可以为可配置常量定义新值。具体操作如下：

<<< @/../../docs-snippets/src/guide/contracts/configurable-constants.test.ts#configurable-constants-2{ts:line-numbers}

你可以为任何这些可配置常量分配新值。

如果你希望为其中一个常量分配新值，可以这样做：

<<< @/../../docs-snippets/src/guide/contracts/configurable-constants.test.ts#configurable-constants-3{ts:line-numbers}

请注意，当为 `Struct` 分配新值时，必须定义 `Struct` 的所有属性。如果未这样做，将会导致错误：

<<< @/../../docs-snippets/src/guide/contracts/configurable-constants.test.ts#configurable-constants-4{ts:line-numbers}