# 单位转换

在内部，我们使用[任意精度](https://mathworld.wolfram.com/ArbitraryPrecision.html)算术（也称为大数算术）来处理大数字和不同的资产。

在 Fuel 网络上，我们使用 9 位小数来表示单位下的金额。这取决于不同的链，所以了解您正在使用的链上使用的小数位数是很重要的。

> 注意：[`@fuels/assets`](https://www.npmjs.com/package/@fuels/assets)包提供了一组资产及其小数位数的列表。

以下我们将介绍单位转换的一些常见用例。

使用我们的 `BN` 类，我们可以实例化这些数字。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#instantiation-1{ts:line-numbers}

或者使用我们的 `bn` 实用函数。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#instantiation-2{ts:line-numbers}

## 合约调用

通常，当我们从 JavaScript 向 Sway 程序传递 `u64` 和 `u256` 数字时，我们需要将它们转换为 `BN` 对象。有关更多信息，请参阅[此处](../types/numbers.md)。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#contract-calls-1{ts:line-numbers}

> 注意：如果合约调用返回的数字太大，无法表示为 JavaScript 数字，您可以使用 `toString` 方法而不是 `toNumber` 将其转换为字符串。

## 解析

解析字符串表示的数字（来自用户输入）从未如此简单，使用 `parseUnits` 函数。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#parse-units-1{ts:line-numbers}

我们可以解析大数字。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#parse-units-2{ts:line-numbers}

或者格式化为人类可读的数字。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#parse-units-3{ts:line-numbers}

我们还可以解析其他计量单位的数字。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#parse-units-4{ts:line-numbers}

## 格式化

我们可以使用 `format` 函数格式化常见的计量单位。

在下面的示例中，我们将一个表示一个 Gwei 的 BigNumber 格式化为 Fuel 网络的单位（保留 3 位小数）。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#format-1{ts:line-numbers}

我们还可以通过指定 `units` 变量来格式化其他计量单位的数字。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#format-2{ts:line-numbers}

`precision` 变量将允许格式化具有特定小数位数的数字。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#format-3{ts:line-numbers}

### 格式化单位

`formatUnits` 函数是 `format` 函数的一个较小的替代方案，因为它将保持与输入值相同的精度。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#format-units-1{ts:line-numbers}

我们还可以通过指定 `units` 变量来格式化其他计量单位的数字。

<<< @/../../docs-snippets/src/guide/utilities/unit-conversion.test.ts#format-units-2{ts:line-numbers}

## 另请参阅

- [Sway 数字](../types/numbers.md)
