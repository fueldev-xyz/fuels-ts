# 日期转换

为了更容易地处理日期和时间，SDK 导出了 `DateTime` 类，它是 [内置](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) `Date` 类的包装器。下面我们将介绍实例化、实用函数和时间格式的方法。

在内部，交易和其他时间/日期资产使用 [`TAI64`](#tai-format) 格式进行编码。我们返回一个 `DateTime` 类，以便更容易地在这两种格式之间进行转换和格式化。

## 实例化 `DateTime`

我们有一系列静态方法用于 **实例化** 我们的 `DateTime` 类。

<<< @/../../docs-snippets/src/guide/types/date-time.test.ts#create-from-multiple-sources{ts:line-numbers}

### TAI64

`fromTai64` 是一个 _静态_ 方法，允许从 `TAI64` 字符串创建 `DateTime` 类。

`toTai64` 是一个 _实例_ 方法，允许将 `DateTime` 类转换为 `TAI64` 字符串。

<<< @/../../docs-snippets/src/guide/types/date-time.test.ts#from-tai-64-and-to-tai-64{ts:line-numbers}

### UNIX

`fromUnixMilliseconds` 是一个 _静态_ 方法，允许从 UNIX 毫秒数创建 `DateTime` 类。

`toUnixMilliseconds` 是一个 _实例_ 方法，允许将 `DateTime` 类转换为以毫秒为单位的 `UNIX` 数字。

<<< @/../../docs-snippets/src/guide/types/date-time.test.ts#from-unix-milliseconds-and-to-unix-milliseconds{ts:line-numbers}

`fromUnixSeconds` 是一个 _静态_ 方法，允许从 UNIX 秒数创建 `DateTime` 类。

`toUnixSeconds` 是一个 _实例_ 方法，允许将 `DateTime` 类转换为以秒为单位的 `UNIX` 数字。

<<< @/../../docs-snippets/src/guide/types/date-time.test.ts#from-unix-seconds-and-to-unix-seconds{ts:line-numbers}

### 日期

`DateTime` 类扩展了 `Date` 对象的功能，因此所有方法都可供您使用。

<<< @/../../docs-snippets/src/guide/types/date-time.test.ts#date-object-methods{ts:line-numbers}

## 格式

这里我们将介绍 SDK 中使用的不同日期/时间格式。在区块链内部，我们使用 `TAI64` 格式，但为了方便使用，我们也支持 `UNIX` 格式。

### UNIX 格式

UNIX 时间是自 **协调世界时 (UTC) 1970 年 1 月 1 日星期四 00:00:00** 以来经过的秒数，减去闰秒。每天被视为包含确切的 86400 秒，因此忽略了闰秒。

### TAI 格式

TAI 代表 _国际原子时间_，是当前国际实时标准 [来源](https://cr.yp.to/libtai/tai64.html)。

我们使用 `TAI64`，它是一个表示自纪元以来的纳秒数的 64 位整数。

- TAI 秒开始于 1970 年 TAI 开始之前的 _(2^62 - s) 秒_，如果 s 在 0（包含）和 2^62（不包含）之间；或

- TAI 秒开始于 1970 年 TAI 开始之后的 _(2^62 + s) 秒_，如果 s 在 -2^62（包含）和 0（不包含）之间。

[来源](https://cr.yp.to/libtai/tai64.html)
