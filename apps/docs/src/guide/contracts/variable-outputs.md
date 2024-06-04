# 可变输出

Sway 包括用于将资产转移到钱包和合约的强大功能。

在您的 Sway 项目中使用这些转账功能时，重要的是要意识到每次调用都需要事务的 [Outputs](https://specs.fuel.network/master/tx-format/output.html) 中的一个 [Output Variable](https://specs.fuel.network/master/tx-format/output.html#outputvariable)。

例如，如果合约函数调用了 Sway 转账函数 3 次，则在事务的输出列表中需要存在 3 个输出变量。

## 示例：需要 `Output Variable` 的 Sway 函数

<<< @/../../docs-snippets/test/fixtures/forc-projects/token/src/main.sw#variable-outputs-1{ts:line-numbers}

## 向合约调用添加可变输出

当您的合约调用了其中任何一个函数，或者如果它调用了导致另一个合约调用这些函数的函数时，您需要添加相应数量的输出变量。

可以如下所示执行此操作：

<<< @/../../docs-snippets/src/guide/contracts/variable-outputs.test.ts#variable-outputs-2{ts:line-numbers}

在 TypeScript SDK 中，输出变量会自动添加到事务的输出列表中。

这个过程是通过一种蛮力策略来完成的，执行连续的干扰运行，直到不再返回错误为止。这种方法确定了处理事务所需的输出变量的数量。

然而，这可能会显著延迟事务处理。因此，**强烈建议**在提交事务之前手动添加正确数量的输出变量。