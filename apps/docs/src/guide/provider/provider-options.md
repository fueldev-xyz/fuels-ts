# 提供者选项

您可以在 `Provider` 实例化时提供各种[选项](../../api/Account/index.md#provideroptions)来修改其行为。

### `retryOptions`

通过 `Provider` 对燃料节点的调用如果无法建立连接，则会失败。
指定重试选项允许您在最终抛出错误之前自定义处理该失败场景的方式。

_注意：仅在无法建立连接时才会重试。如果已建立连接并且节点抛出错误，则不会进行重试。_

您可以提供以下设置：

- `maxRetries` - 在初始尝试失败后重新尝试的次数。
- `backoff` - 用于定义尝试之间间隔的策略。
  - `exponential` （默认）：每次尝试时将延迟加倍。
  - `linear` - 每次尝试时以线性方式增加延迟。
  - `fixed`：使用恒定的延迟时间间隔。
- `baseDelay` （默认为 150ms） - 用于 backoff 策略的基本时间，单位为毫秒。

<<< @/../../docs-snippets/src/guide/provider/provider.test.ts#options-retryOptions{ts:line-numbers}

### `requestMiddleware`

允许您修改请求对象以添加额外的标头、修改请求体等。

<<< @/../../docs-snippets/src/guide/provider/provider.test.ts#options-requestMiddleware{ts:line-numbers}

### `timeout`

指定每个请求的超时时间（毫秒）。

<<< @/../../docs-snippets/src/guide/provider/provider.test.ts#options-timeout{ts:line-numbers}

### `fetch`

提供一个自定义的 `fetch` 函数，它将替换默认的 fetch 调用。

_注意：如果定义了 `fetch`，则 `requestMiddleware`、`timeout` 和 `retryOptions` 也会应用于此自定义的 `fetch` 函数。_

<<< @/../../docs-snippets/src/guide/provider/provider.test.ts#options-fetch{ts:line-numbers}
