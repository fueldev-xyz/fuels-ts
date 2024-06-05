# `StdString`

可以使用 `StdString` 类型表示可变长度的动态字符串，也称为标准库字符串或 `std-lib-string`。它在大多数语言中的行为类似于动态字符串，实质上是一个字符数组。

<<< @/../../docs-snippets/src/guide/types/std-string.test.ts#std-string-1{ts:line-numbers}

## 使用 `StdString`

`StdString` 类型可以与您的合约调用集成。考虑以下可以比较并返回字符串的合约：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-std-string/src/main.sw#std-string-1{ts:line-numbers}

可以使用原生 JavaScript 字符串来创建字符串，并发送到 Sway 合约：

<<< @/../../docs-snippets/src/guide/types/std-string.test.ts#std-string-2{ts:line-numbers}
