# 实例化断言

在 Sway 中，断言可以像下面这样简单：

<<< @/../../docs-snippets/test/fixtures/forc-projects/return-true-predicate/src/main.sw#predicate-index-1{rust:line-numbers}

在这个最简示例中，`main` 函数不接受任何参数，只是简单地返回 true。

就像 Sway 中的合约一样，一旦您创建了一个断言，您可以使用 `forc build` 编译它。有关使用 Sway 的更多信息，请参阅 <a :href="introUrl" target="_blank" rel="noreferrer">Sway 文档</a>。

编译后，您将获得断言的二进制文件和其 JSON ABI（应用程序二进制接口）。使用这些，您可以像下面的代码片段一样在 TypeScript 中实例化一个断言：

<<< @/../../docs-snippets/src/guide/predicates/index.test.ts#predicate-index-2{ts:line-numbers}

创建的 [`Predicate`](../../api/Account/Predicate.md) 实例，除其他外，有三个重要属性：断言 `bytes`（字节码）、`chainId` 和断言 `address`。

这个地址，由字节码生成，对应于比特币中使用的 Pay-to-Script-Hash（P2SH）地址。

## 带有多个参数的断言

您可以将多个参数传递给一个断言。例如，下面是一个断言，如果两个参数不相等，则评估为 `true`：

<<< @/../../../packages/fuel-gauge/test/fixtures/forc-projects/predicate-multi-args/src/main.sw#predicate-multi-args-sw{rust:line-numbers}

您可以像这样将两个参数传递给这个断言：

<<< @/../../../packages/fuel-gauge/src/predicate/predicate-arguments.test.ts#predicate-multi-args{ts:line-numbers}

## 带有结构参数的断言

您也可以将结构作为参数传递给断言。以下是一个期望结构作为参数的断言示例：

<<< @/../../../packages/fuel-gauge/test/fixtures/forc-projects/predicate-main-args-struct/src/main.sw#Predicate-main-args{rust:line-numbers}

您可以像这样将结构作为参数传递给这个断言：

<<< @/../../../packages/fuel-gauge/src/predicate/predicate-arguments.test.ts#predicate-struct-arg{ts:line-numbers}
