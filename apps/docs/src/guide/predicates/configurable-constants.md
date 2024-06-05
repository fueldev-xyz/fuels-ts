# 具有可配置常量的断言

与[合约](../contracts/configurable-constants.md)和[脚本](../scripts/configurable-constants.md)类似，断言也支持可配置常量。这使得断言能够适应特定的用例并增强其功能性。

## 示例：资产转移验证

让我们考虑一个断言用于验证资产转移的示例。在这种情况下，转移只有在接收方地址位于预先批准的白名单上时才会执行。

以下代码片段演示了如何实现这一点：

<<< @/../../docs-snippets/test/fixtures/forc-projects/whitelisted-address-predicate/src/main.sw#predicate-with-configurable-constants-1{rust:line-numbers}

在这个示例中，您会注意到使用了一个名为 `WHITELISTED` 的可配置常量。该常量具有一个默认值，表示默认批准的地址。

## 修改白名单

如果需要将另一个地址加入白名单，可以轻松更新 `WHITELISTED` 常量。以下代码片段演示了如何为 `WHITELISTED` 常量设置一个新值，并使断言执行转移：

<<< @/../../docs-snippets/src/guide/predicates/predicate-with-configurable.test.ts#predicate-with-configurable-constants-2{ts:line-numbers}

通过确保更新后的 `WHITELISTED` 地址与预期的接收方地址匹配，断言将成功验证转移。

## 默认白名单地址

在默认白名单地址已经是预期的接收方的情况下，无需更新 `WHITELISTED` 常量。断言将基于默认值验证转移。以下是此场景的示例：

<<< @/../../docs-snippets/src/guide/predicates/predicate-with-configurable.test.ts#predicate-with-configurable-constants-3{ts:line-numbers}

在断言内部配置常量的能力提供了一种灵活的机制，用于定制其行为，从而增强了我们的资产转移流程的健壮性和多功能性。

需要注意的是，这些自定义不会直接修改原始断言。断言的地址是其字节码的哈希值。对字节码的任何更改，包括更改常量值，都会生成不同的字节码，从而生成不同的哈希值。这将导致创建一个具有新地址的新断言。

这并不意味着我们正在更改原始断言的行为。相反，我们正在创建一个具有不同配置的新断言。

因此，虽然可配置常量确实增强了断言的灵活性和健壮性，但是它是通过创建具有不同配置的新断言来实现的，而不是通过更改现有断言的行为。
