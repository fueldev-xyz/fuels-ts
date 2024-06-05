# String

在 Sway 中，字符串是静态大小的，这意味着您必须预先定义字符串的大小。静态大小的字符串使用 `str[x]` 语法表示，其中 `x` 表示字符串的大小。
本指南将解释如何在使用 SDK 时创建和与静态大小的字符串进行交互。

## 创建静态大小的字符串

<<< @/../../docs-snippets/src/guide/types/string.test.ts#string-1{ts:line-numbers}

## 在合约方法中与静态大小的字符串进行交互

当合约方法接受并返回 `str[8]` 时，相应的 SDK 包装方法也将接受并返回相同长度的字符串。您可以像这样将字符串传递给合约方法：

<<< @/../../docs-snippets/src/guide/types/string.test.ts#string-2{ts:line-numbers}

在使用静态大小的字符串时，请确保输入和输出字符串具有正确的长度，以避免错误行为。

如果您传递的字符串对于合约方法来说太长或太短，调用将失败，如下所示：

<<< @/../../docs-snippets/src/guide/types/string.test.ts#string-3{ts:line-numbers}
