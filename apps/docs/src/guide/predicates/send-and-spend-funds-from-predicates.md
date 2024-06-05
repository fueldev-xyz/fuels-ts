# 从断言发送和花费资金

断言可以用于验证交易。这意味着断言可以保护资产，仅当断言条件满足时才允许它们的转移。

本指南将演示如何使用断言发送和花费资金。

## 断言示例

考虑以下断言：

<<< @/../../docs-snippets/test/fixtures/forc-projects/simple-predicate/src/main.sw#send-and-spend-funds-from-predicates-1{rust:line-numbers}

这个断言接受一个类型为 `b256` 的地址，并将其与相同类型的硬编码地址进行比较。如果两个地址相等，断言返回 true，否则返回 false。

## 使用 SDK 与断言交互

让我们使用上面的断言来验证我们的交易。

一旦你编译了断言（`forc build`），你将获得两个重要的工件：JSON ABI 和断言的二进制代码。这些需要用来实例化一个新的断言。

在这里我们还要传入断言的数据。注意我们断言示例中的 `main` 函数需要一个名为 `input_address` 类型为 `b256` 的参数。我们将把这个参数传递给 `Predicate` 构造函数，同时传入字节码和 JSON ABI。

<<< @/../../docs-snippets/src/guide/predicates/send-and-spend-funds-from-predicates.test.ts#send-and-spend-funds-from-predicates-2{ts:line-numbers}

> 注意：如果你想在实例化 `Predicate` 后传入断言数据，或者想使用与构造函数中传入的不同的数据，你将不得不创建一个新的 `Predicate` 实例。

有了断言实例化后，我们可以将资金转移到它的地址。这要求我们有足够的资金的钱包。如果你对如何使用 SDK 中的钱包不确定，我们建议查阅我们的 [钱包](../wallets/) 指南。

<<< @/../../docs-snippets/src/guide/predicates/send-and-spend-funds-from-predicates.test.ts#send-and-spend-funds-from-predicates-3{ts:line-numbers}

现在我们的断言持有资金，我们可以使用它来验证交易，从而执行我们的转账。我们可以通过以下方式实现：

<<< @/../../docs-snippets/src/guide/predicates/send-and-spend-funds-from-predicates.test.ts#send-and-spend-funds-from-predicates-5{ts:line-numbers}

请注意，转移方法有两个参数：收件人的地址和拟转移的金额。

一旦断言基于其预定义条件解析出一个返回值 `true`，我们的断言成功地通过转账将资金转移到目标钱包。

---

在类似的方法中，你可以使用 `createTransfer` 方法，它返回一个 [`ScriptTransactionRequest`](../../api/Account/ScriptTransactionRequest.md)。然后，我们可以通过调用 `sendTransaction` 方法提交此交易请求。

如果你需要在实际提交到节点之前知道交易 ID，这可能会有用。

<<< @/../../docs-snippets/src/guide/predicates/send-and-spend-funds-from-predicates.test.ts#send-and-spend-funds-from-predicates-8{ts:line-numbers}

## 花费整个断言持有的金额

试图转发断言持有的全部金额会导致错误，因为没有剩余资金来支付交易费用。尝试这样做会导致错误消息，如：

<<< @/../../docs-snippets/src/guide/predicates/send-and-spend-funds-from-predicates.test.ts#send-and-spend-funds-from-predicates-6{ts:line-numbers}

## 断言验证失败

当断言无法验证时会发生什么？回想一下，我们的断言只有在 `input_address` 匹配硬编码的 `valid_address` 时才会验证。因此，如果我们设置与 `valid_address` 不同的数据，断言将无法验证。

当断言无法验证时，SDK 抛出的错误如下所示：

<<< @/../../docs-snippets/src/guide/predicates/send-and-spend-funds-from-predicates.test.ts#send-and-spend-funds-from-predicates-7{ts:line-numbers}

## 预分配交易

在某些情况下，您可能希望在提交执行之前预分配断言事务。为此，您可以在 `Predicate` 类上使用 `createTransfer` 方法。

在以下示例中，我们正在预先配置一个交易，以便在实际提交交易之前知道交易 ID。

<<< @/../../docs-snippets/src/guide/predicates/send-and-spend-funds-from-predicates.test.ts#predicates-prestage-transaction{ts:line-numbers}
