# 具有可配置项的脚本

与[合约](../contracts/configurable-constants.md)和[断言](../predicates/configurable-constants.md)一样，脚本也支持可配置的常量。此功能使您可以动态调整脚本中的某些值。

在脚本中添加和设置可配置的常量非常简单。

让我们考虑以下脚本：

<<< @/../../docs-snippets/test/fixtures/forc-projects/sum-script/src/main.sw#script-with-configurable-contants-1{rust:line-numbers}

在此脚本中，`AMOUNT` 是一个具有默认值 `10` 的可配置常量。主函数返回 `inputted_amount` 和可配置常量 `AMOUNT` 的总和。

要更改 `AMOUNT` 常量的值，我们可以使用 `setConfigurableConstants` 方法，如以下示例所示：

<<< @/../../docs-snippets/src/guide/scripts/script-with-configurable.test.ts#script-with-configurable-contants-2{ts:line-numbers}

在此示例中，我们为 `AMOUNT` 常量设置了一个新值 `81`。然后，我们调用主函数，输入值为 `10`。

期望的结果是脚本将返回输入值和 `AMOUNT` 新值的总和。

这样，脚本中的可配置常量允许在执行过程中实现更灵活和动态的行为。
