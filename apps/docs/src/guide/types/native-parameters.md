# 本地参数类型

下面是如何在常见的 Sway 程序输入和输出类型之间进行转换的示例:

- [`地址`](#地址)
- [`合约标识`](#合约标识)
- [`身份`](#身份)
- [`资产标识`](#资产标识)

## `地址`

### `地址输入`

要将 `地址` 作为 Sway 程序的输入参数传递，可以按以下方式定义输入:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#address-input

### `地址输出`

对于返回 `地址` 类型的 Sway 程序，您可以将返回值转换为 `fuels` 中的 `地址` 类型，如下所示:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#address-output

## `合约标识`

### `合约标识输入`

要将 `合约标识` 作为 Sway 程序的输入参数传递，可以按以下方式定义输入:


<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#contract-id-input


### `合约标识输出`

对于返回 `合约标识` 类型的 Sway 程序，您可以将返回值转换为 `字符串`，如下所示:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#contract-id-output

## `身份`

### `身份输入`

要将 `身份` 作为 Sway 程序的输入参数传递，可以按以下方式定义输入:

对于地址:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#identity-address-input

对于合约:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#identity-contract-input

### `身份输出`

对于返回 `身份` 类型的 Sway 程序，您可以将返回值转换为 `地址` 或 `字符串`，如下所示:

对于地址:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#identity-address-output

对于合约:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#identity-contract-output

## `资产标识`

### `资产标识输入`

要将 `资产标识` 作为 Sway 程序的输入参数传递，可以按以下方式定义输入:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#asset-id-input

### `资产标识输出`

对于返回 `资产标识` 类型的 Sway 程序，您可以将返回值转换为 `字符串`，如下所示:

<<< @/../../docs-snippets/src/guide/types/contract-types.test.ts#asset-id-output
