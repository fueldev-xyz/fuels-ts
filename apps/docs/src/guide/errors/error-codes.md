# 错误代码

以下是 SDK 可能抛出的预期错误代码列表。这些错误代码用于帮助理解抛出的错误，并提供可能的解决方法。

## `ABI_MAIN_METHOD_MISSING`

当您的 ABI 没有主方法时。

这可以通过向 ABI 添加主方法来解决。

## `ABI_TYPES_AND_VALUES_MISMATCH`

当提供给函数的参数与所需的最小输入长度不匹配时。

检查提供给函数的参数是否与所需类型匹配。

## `ACCOUNT_REQUIRED`

在操作中需要 [`Account`](../../api/Account/Account.md)。通常会是一个 [`Wallet`](../wallets/index.md)。

这可能是在部署合约期间需要账户签名交易时引起的。可以通过按照[此处](../contracts/deploying-contracts.md)的部署指南解决。

## `CONVERTING_FAILED`

将大数转换为不兼容的格式时。

确保您提供给大数的值与要转换为的值兼容。

## `DUPLICATED_POLICY`

当交易中存在相同类型的策略时。

确保交易中没有重复（按类型）的策略。

## `ERROR_BUILDING_BLOCK_EXPLORER_URL`

当传递了多于以下选项之一时：`path`、`address`、`txId`、`blockNumber`。

检查只传递了以下选项之一：`path`、`address`、`txId`、`blockNumber`。

## `FUNCTION_NOT_FOUND`

在 ABI 中找不到具有给定名称、签名或选择器的函数时。

检查函数名称、签名或选择器是否在 ABI 中正确存在。

## `GAS_LIMIT_TOO_LOW`

当气体限制低于最小气体限制时。

将气体限制增加到大于最小气体限制。

## `GAS_PRICE_TOO_LOW`

当气体价格低于最低气体价格时。

将气体价格增加到大于最低气体价格。

## `HD_WALLET_ERROR`

硬件钱包将根据不受支持的配置引发错误。

错误消息将确定配置中的哪个元素是不正确的。可能是由于公钥或私钥不正确，或者在配置到/从扩展密钥时。

## `INVALID_CHECKSUM`

提供的助记词的校验和验证失败。

确保助记词正确。

## `INVALID_CONFIGURABLE_CONSTANTS`

当程序类型没有可配置的常量要设置时；或者所提供的可配置常量不属于程序类型，如其 ABI 所定义的那样。

确保所提供的可配置常量是正确的，并且在 ABI 中定义。

## `INVALID_COMPONENT`

在 ABI 中未找到或格式不正确的预期组件时。

确保您对 [数组](../types/arrays.md) 和 [向量](../types/vectors.md) 使用了正确形式的 Sway 类型。

## `INVALID_CREDENTIALS`

提供的密码不正确时。

确保密码是正确的。

## `INVALID_DATA`

当值超过最大值时。

确保值小于最大值。

## `INVALID_ENTROPY`

当熵不是介于 16 和 32 字节之间时；不是 4 的倍数时。

确保熵介于 16 和 32 字节之间，并且是 4 的倍数。

## `INVALID_EVM_ADDRESS`

提供的 EVM 地址无效时。

确保 [EVM 地址](../types/evm-address.md) 有效。

## `INVALID_INPUT_PARAMETERS`

提供的输入参数无效时。

错误消息将确定缺少哪个参数。可能是由于提供的程序类型不是以下之一 `contract`、`script` 或 `predicate`。

## `INVALID_MNEMONIC`

提供的助记词无效时。

检查消息以获取更多详细信息。可能是因为助记词短语的长度不是以下之一：12、15、18、21 或 24。

## `INVALID_MULTICALL`

当多次调用中有一个调用返回的堆类型不是最后一个调用，或者多次

# 错误代码

以下是 SDK 可能抛出的预期错误代码列表。这些错误代码用于帮助理解抛出的错误，并提供可能的解决方法。

## `INVALID_PASSWORD`

提供的密码不正确时。

确保密码是正确的。

## `INVALID_POLICY_TYPE`

当提供的策略类型对于给定的脚本无效时。

检查策略类型是否在 `PolicyType` 中定义。

## `INVALID_PUBLIC_KEY`

提供的公钥无效时。

确保公钥是有效的。

## `INVALID_RECEIPT_TYPE`

收据类型无效时。

检查类型是否在 `ReceiptType` 范围内。

## `INVALID_REQUEST`

当对 Fuel 节点的请求失败时，错误消息从 Fuel 节点传播。

检查来自 Fuel 节点的错误消息。

## `INVALID_SEED`

种子长度不在 16 到 64 字节之间时。

确保种子长度在 16 到 64 字节之间。

## `INVALID_TRANSACTION_INPUT`

输入类型无效时。

检查类型是否在 `InputType` 范围内。

## `INVALID_TRANSACTION_OUTPUT`

输出类型无效时。

检查类型是否在 `OutputType` 范围内。

## `INVALID_TRANSACTION_STATUS`

从节点接收到的交易状态不符时。

检查接收到的状态是否在 `TransactionStatus` 范围内。

## `INVALID_TRANSACTION_TYPE`

来自 Fuel 节点的交易类型 _不_ 有效时。

类型在 [`TransactionType`](../../api/Account/TransactionType.md) 范围内。

## `INVALID_TTL`

TTL 小于或等于零时。

确保 TTL 是一个数字，并且 TTL 大于零。

## `INVALID_WORD_LIST`

单词列表长度不等于 2048 时。

提供给助记词的单词列表长度应等于 2048。

## `JSON_ABI_ERROR`

当 ABI 类型不符合正确的格式时。

通常是由于程序中的类型/数不正确造成的，请查看此处我们支持的类型和其期望的格式的类型[文档](../types/index.md)。

## `LOG_TYPE_NOT_FOUND`

提供的日志类型 ID 无法在 ABI 中找到时。

检查日志类型 ID 是否正确并存在于 ABI 中。

## `MISSING_CONNECTOR`

在给定操作需要连接器时，连接器丢失。

确保已向 `Account` 或 `Wallet` 提供了连接器。

## `MISSING_PROVIDER`

在给定操作需要提供程序时，提供程序丢失。

这可能是由于未为 [`Account`](../../api/Account/index.md) 或 [`Wallet`](../wallets/index.md) 设置提供程序而导致的 - 使用 `connect` 方法附加提供程序。

## `MISSING_REQUIRED_PARAMETER`

当给定方法未提供所需参数时。

错误消息将确定缺少哪个参数。这可能是在类型生成期间引起的，当未提供 `inputs` 或 `filepaths` 时（至少需要一个）。

## `NODE_INFO_CACHE_EMPTY`

当 Fuel 节点信息缓存为空时；这通常是由于未连接到 Fuel 节点引起的。

确保提供程序已成功连接到 Fuel 节点。

## `TYPE_NOT_FOUND`

当给定类型 ID 的类型在 ABI 中未找到时。

检查类型 ID 是否正确并存在于 ABI 中。

## `TYPE_NOT_SUPPORTED`

检测到意外类型时 - 错误消息将确定哪个类型不正确。

检查类型与 ABI 是否匹配，并确保它是正确的。您可以在[此处](../types/index.md)找到我们所有类型的列表。

## `WALLET_MANAGER_ERROR`

钱包管理器将由于多种原因而抛出错误。错误消息将确定配置中的哪个元素是不正确的。

可能是由于密码错误和/或钱包不在管理器中。

## `HASHER_LOCKED`

哈希算法当前已锁定，任何后续尝试注册新实现都会抛出此错误。
锁定函数的目的是提供一种确保特定哈希算法的实现一旦被锁定就不能更改的方法。在您的应用程序中保证哈希函数的完整性和一致性时，这可能是有用的。