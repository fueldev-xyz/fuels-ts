# Class: TransactionResponse

[@fuel-ts/account](/api/Account/index.md).TransactionResponse

Represents a response for a transaction.

## Constructors

### constructor

• **new TransactionResponse**(`id`, `provider`, `abis?`): [`TransactionResponse`](/api/Account/TransactionResponse.md)

Constructor for `TransactionResponse`.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | The transaction ID. |
| `provider` | [`Provider`](/api/Account/Provider.md) | The provider. |
| `abis?` | [`JsonAbisFromAllCalls`](/api/Account/index.md#jsonabisfromallcalls) | - |

#### Returns

[`TransactionResponse`](/api/Account/TransactionResponse.md)

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:101](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L101)

## Properties

### abis

• `Optional` **abis**: [`JsonAbisFromAllCalls`](/api/Account/index.md#jsonabisfromallcalls)

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:93](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L93)

___

### gasUsed

• **gasUsed**: `BN`

Gas used on the transaction

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:89](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L89)

___

### gqlTransaction

• `Optional` **gqlTransaction**: `Object`

The graphql Transaction with receipts object.

#### Type declaration

| Name | Type |
| :------ | :------ |
| `id` | `string` |
| `rawPayload` | `string` |
| `status?` | ``null`` \| { `block`: { `id`: `string`  } ; `reason`: `string` ; `receipts`: { `amount?`: ``null`` \| `string` ; `assetId?`: ``null`` \| `string` ; `contractId?`: ``null`` \| `string` ; `data?`: ``null`` \| `string` ; `digest?`: ``null`` \| `string` ; `gas?`: ``null`` \| `string` ; `gasUsed?`: ``null`` \| `string` ; `id?`: ``null`` \| `string` ; `is?`: ``null`` \| `string` ; `len?`: ``null`` \| `string` ; `nonce?`: ``null`` \| `string` ; `param1?`: ``null`` \| `string` ; `param2?`: ``null`` \| `string` ; `pc?`: ``null`` \| `string` ; `ptr?`: ``null`` \| `string` ; `ra?`: ``null`` \| `string` ; `rb?`: ``null`` \| `string` ; `rc?`: ``null`` \| `string` ; `rd?`: ``null`` \| `string` ; `reason?`: ``null`` \| `string` ; `receiptType`: `GqlReceiptType` ; `recipient?`: ``null`` \| `string` ; `result?`: ``null`` \| `string` ; `sender?`: ``null`` \| `string` ; `subId?`: ``null`` \| `string` ; `to?`: ``null`` \| `string` ; `toAddress?`: ``null`` \| `string` ; `val?`: ``null`` \| `string`  }[] ; `time`: `string` ; `totalFee`: `string` ; `totalGas`: `string` ; `type`: ``"FailureStatus"``  } \| { `reason`: `string` ; `type`: ``"SqueezedOutStatus"``  } \| { `time`: `string` ; `type`: ``"SubmittedStatus"``  } \| { `block`: { `id`: `string`  } ; `programState?`: ``null`` \| { `data`: `string` ; `returnType`: `GqlReturnType`  } ; `receipts`: { `amount?`: ``null`` \| `string` ; `assetId?`: ``null`` \| `string` ; `contractId?`: ``null`` \| `string` ; `data?`: ``null`` \| `string` ; `digest?`: ``null`` \| `string` ; `gas?`: ``null`` \| `string` ; `gasUsed?`: ``null`` \| `string` ; `id?`: ``null`` \| `string` ; `is?`: ``null`` \| `string` ; `len?`: ``null`` \| `string` ; `nonce?`: ``null`` \| `string` ; `param1?`: ``null`` \| `string` ; `param2?`: ``null`` \| `string` ; `pc?`: ``null`` \| `string` ; `ptr?`: ``null`` \| `string` ; `ra?`: ``null`` \| `string` ; `rb?`: ``null`` \| `string` ; `rc?`: ``null`` \| `string` ; `rd?`: ``null`` \| `string` ; `reason?`: ``null`` \| `string` ; `receiptType`: `GqlReceiptType` ; `recipient?`: ``null`` \| `string` ; `result?`: ``null`` \| `string` ; `sender?`: ``null`` \| `string` ; `subId?`: ``null`` \| `string` ; `to?`: ``null`` \| `string` ; `toAddress?`: ``null`` \| `string` ; `val?`: ``null`` \| `string`  }[] ; `time`: `string` ; `totalFee`: `string` ; `totalGas`: `string` ; `type`: ``"SuccessStatus"``  } |

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:91](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L91)

___

### id

• **id**: `string`

Transaction ID

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:85](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L85)

___

### provider

• **provider**: [`Provider`](/api/Account/Provider.md)

Current provider

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:87](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L87)

## Methods

### decodeTransaction

▸ **decodeTransaction**&lt;`TTransactionType`\>(`transactionWithReceipts`): `Transaction`&lt;`TTransactionType`\>

Decode the raw payload of the transaction.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `TTransactionType` | `void` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `transactionWithReceipts` | `Object` | The transaction with receipts object. |
| `transactionWithReceipts.id` | `string` | - |
| `transactionWithReceipts.rawPayload` | `string` | - |
| `transactionWithReceipts.status?` | ``null`` \| { `block`: { `id`: `string`  } ; `reason`: `string` ; `receipts`: { `amount?`: ``null`` \| `string` ; `assetId?`: ``null`` \| `string` ; `contractId?`: ``null`` \| `string` ; `data?`: ``null`` \| `string` ; `digest?`: ``null`` \| `string` ; `gas?`: ``null`` \| `string` ; `gasUsed?`: ``null`` \| `string` ; `id?`: ``null`` \| `string` ; `is?`: ``null`` \| `string` ; `len?`: ``null`` \| `string` ; `nonce?`: ``null`` \| `string` ; `param1?`: ``null`` \| `string` ; `param2?`: ``null`` \| `string` ; `pc?`: ``null`` \| `string` ; `ptr?`: ``null`` \| `string` ; `ra?`: ``null`` \| `string` ; `rb?`: ``null`` \| `string` ; `rc?`: ``null`` \| `string` ; `rd?`: ``null`` \| `string` ; `reason?`: ``null`` \| `string` ; `receiptType`: `GqlReceiptType` ; `recipient?`: ``null`` \| `string` ; `result?`: ``null`` \| `string` ; `sender?`: ``null`` \| `string` ; `subId?`: ``null`` \| `string` ; `to?`: ``null`` \| `string` ; `toAddress?`: ``null`` \| `string` ; `val?`: ``null`` \| `string`  }[] ; `time`: `string` ; `totalFee`: `string` ; `totalGas`: `string` ; `type`: ``"FailureStatus"``  } \| { `reason`: `string` ; `type`: ``"SqueezedOutStatus"``  } \| { `time`: `string` ; `type`: ``"SubmittedStatus"``  } \| { `block`: { `id`: `string`  } ; `programState?`: ``null`` \| { `data`: `string` ; `returnType`: `GqlReturnType`  } ; `receipts`: { `amount?`: ``null`` \| `string` ; `assetId?`: ``null`` \| `string` ; `contractId?`: ``null`` \| `string` ; `data?`: ``null`` \| `string` ; `digest?`: ``null`` \| `string` ; `gas?`: ``null`` \| `string` ; `gasUsed?`: ``null`` \| `string` ; `id?`: ``null`` \| `string` ; `is?`: ``null`` \| `string` ; `len?`: ``null`` \| `string` ; `nonce?`: ``null`` \| `string` ; `param1?`: ``null`` \| `string` ; `param2?`: ``null`` \| `string` ; `pc?`: ``null`` \| `string` ; `ptr?`: ``null`` \| `string` ; `ra?`: ``null`` \| `string` ; `rb?`: ``null`` \| `string` ; `rc?`: ``null`` \| `string` ; `rd?`: ``null`` \| `string` ; `reason?`: ``null`` \| `string` ; `receiptType`: `GqlReceiptType` ; `recipient?`: ``null`` \| `string` ; `result?`: ``null`` \| `string` ; `sender?`: ``null`` \| `string` ; `subId?`: ``null`` \| `string` ; `to?`: ``null`` \| `string` ; `toAddress?`: ``null`` \| `string` ; `val?`: ``null`` \| `string`  }[] ; `time`: `string` ; `totalFee`: `string` ; `totalGas`: `string` ; `type`: ``"SuccessStatus"``  } | - |

#### Returns

`Transaction`&lt;`TTransactionType`\>

The decoded transaction.

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:160](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L160)

___

### fetch

▸ **fetch**(): `Promise`&lt;{ `id`: `string` ; `rawPayload`: `string` ; `status?`: ``null`` \| { `block`: { `id`: `string`  } ; `reason`: `string` ; `receipts`: { `amount?`: ``null`` \| `string` ; `assetId?`: ``null`` \| `string` ; `contractId?`: ``null`` \| `string` ; `data?`: ``null`` \| `string` ; `digest?`: ``null`` \| `string` ; `gas?`: ``null`` \| `string` ; `gasUsed?`: ``null`` \| `string` ; `id?`: ``null`` \| `string` ; `is?`: ``null`` \| `string` ; `len?`: ``null`` \| `string` ; `nonce?`: ``null`` \| `string` ; `param1?`: ``null`` \| `string` ; `param2?`: ``null`` \| `string` ; `pc?`: ``null`` \| `string` ; `ptr?`: ``null`` \| `string` ; `ra?`: ``null`` \| `string` ; `rb?`: ``null`` \| `string` ; `rc?`: ``null`` \| `string` ; `rd?`: ``null`` \| `string` ; `reason?`: ``null`` \| `string` ; `receiptType`: `GqlReceiptType` ; `recipient?`: ``null`` \| `string` ; `result?`: ``null`` \| `string` ; `sender?`: ``null`` \| `string` ; `subId?`: ``null`` \| `string` ; `to?`: ``null`` \| `string` ; `toAddress?`: ``null`` \| `string` ; `val?`: ``null`` \| `string`  }[] ; `time`: `string` ; `totalFee`: `string` ; `totalGas`: `string` ; `type`: ``"FailureStatus"``  } \| { `reason`: `string` ; `type`: ``"SqueezedOutStatus"``  } \| { `time`: `string` ; `type`: ``"SubmittedStatus"``  } \| { `block`: { `id`: `string`  } ; `programState?`: ``null`` \| { `data`: `string` ; `returnType`: `GqlReturnType`  } ; `receipts`: { `amount?`: ``null`` \| `string` ; `assetId?`: ``null`` \| `string` ; `contractId?`: ``null`` \| `string` ; `data?`: ``null`` \| `string` ; `digest?`: ``null`` \| `string` ; `gas?`: ``null`` \| `string` ; `gasUsed?`: ``null`` \| `string` ; `id?`: ``null`` \| `string` ; `is?`: ``null`` \| `string` ; `len?`: ``null`` \| `string` ; `nonce?`: ``null`` \| `string` ; `param1?`: ``null`` \| `string` ; `param2?`: ``null`` \| `string` ; `pc?`: ``null`` \| `string` ; `ptr?`: ``null`` \| `string` ; `ra?`: ``null`` \| `string` ; `rb?`: ``null`` \| `string` ; `rc?`: ``null`` \| `string` ; `rd?`: ``null`` \| `string` ; `reason?`: ``null`` \| `string` ; `receiptType`: `GqlReceiptType` ; `recipient?`: ``null`` \| `string` ; `result?`: ``null`` \| `string` ; `sender?`: ``null`` \| `string` ; `subId?`: ``null`` \| `string` ; `to?`: ``null`` \| `string` ; `toAddress?`: ``null`` \| `string` ; `val?`: ``null`` \| `string`  }[] ; `time`: `string` ; `totalFee`: `string` ; `totalGas`: `string` ; `type`: ``"SuccessStatus"``  }  }\>

Fetch the transaction with receipts from the provider.

#### Returns

`Promise`&lt;{ `id`: `string` ; `rawPayload`: `string` ; `status?`: ``null`` \| { `block`: { `id`: `string`  } ; `reason`: `string` ; `receipts`: { `amount?`: ``null`` \| `string` ; `assetId?`: ``null`` \| `string` ; `contractId?`: ``null`` \| `string` ; `data?`: ``null`` \| `string` ; `digest?`: ``null`` \| `string` ; `gas?`: ``null`` \| `string` ; `gasUsed?`: ``null`` \| `string` ; `id?`: ``null`` \| `string` ; `is?`: ``null`` \| `string` ; `len?`: ``null`` \| `string` ; `nonce?`: ``null`` \| `string` ; `param1?`: ``null`` \| `string` ; `param2?`: ``null`` \| `string` ; `pc?`: ``null`` \| `string` ; `ptr?`: ``null`` \| `string` ; `ra?`: ``null`` \| `string` ; `rb?`: ``null`` \| `string` ; `rc?`: ``null`` \| `string` ; `rd?`: ``null`` \| `string` ; `reason?`: ``null`` \| `string` ; `receiptType`: `GqlReceiptType` ; `recipient?`: ``null`` \| `string` ; `result?`: ``null`` \| `string` ; `sender?`: ``null`` \| `string` ; `subId?`: ``null`` \| `string` ; `to?`: ``null`` \| `string` ; `toAddress?`: ``null`` \| `string` ; `val?`: ``null`` \| `string`  }[] ; `time`: `string` ; `totalFee`: `string` ; `totalGas`: `string` ; `type`: ``"FailureStatus"``  } \| { `reason`: `string` ; `type`: ``"SqueezedOutStatus"``  } \| { `time`: `string` ; `type`: ``"SubmittedStatus"``  } \| { `block`: { `id`: `string`  } ; `programState?`: ``null`` \| { `data`: `string` ; `returnType`: `GqlReturnType`  } ; `receipts`: { `amount?`: ``null`` \| `string` ; `assetId?`: ``null`` \| `string` ; `contractId?`: ``null`` \| `string` ; `data?`: ``null`` \| `string` ; `digest?`: ``null`` \| `string` ; `gas?`: ``null`` \| `string` ; `gasUsed?`: ``null`` \| `string` ; `id?`: ``null`` \| `string` ; `is?`: ``null`` \| `string` ; `len?`: ``null`` \| `string` ; `nonce?`: ``null`` \| `string` ; `param1?`: ``null`` \| `string` ; `param2?`: ``null`` \| `string` ; `pc?`: ``null`` \| `string` ; `ptr?`: ``null`` \| `string` ; `ra?`: ``null`` \| `string` ; `rb?`: ``null`` \| `string` ; `rc?`: ``null`` \| `string` ; `rd?`: ``null`` \| `string` ; `reason?`: ``null`` \| `string` ; `receiptType`: `GqlReceiptType` ; `recipient?`: ``null`` \| `string` ; `result?`: ``null`` \| `string` ; `sender?`: ``null`` \| `string` ; `subId?`: ``null`` \| `string` ; `to?`: ``null`` \| `string` ; `toAddress?`: ``null`` \| `string` ; `val?`: ``null`` \| `string`  }[] ; `time`: `string` ; `totalFee`: `string` ; `totalGas`: `string` ; `type`: ``"SuccessStatus"``  }  }\>

Transaction with receipts query result.

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:130](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L130)

___

### getTransactionSummary

▸ **getTransactionSummary**&lt;`TTransactionType`\>(`contractsAbiMap?`): `Promise`&lt;[`TransactionSummary`](/api/Account/index.md#transactionsummary)&lt;`TTransactionType`\>\>

Retrieves the TransactionSummary. If the `gqlTransaction` is not set, it will
fetch it from the provider

#### Type parameters

| Name | Type |
| :------ | :------ |
| `TTransactionType` | `void` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `contractsAbiMap?` | [`AbiMap`](/api/Account/index.md#abimap) | The contracts ABI map. |

#### Returns

`Promise`&lt;[`TransactionSummary`](/api/Account/index.md#transactionsummary)&lt;`TTransactionType`\>\>

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:174](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L174)

___

### wait

▸ **wait**&lt;`TTransactionType`\>(`contractsAbiMap?`): `Promise`&lt;`TransactionResult`&lt;`TTransactionType`\>\>

Waits for transaction to complete and returns the result.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `TTransactionType` | `void` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `contractsAbiMap?` | [`AbiMap`](/api/Account/index.md#abimap) | The contracts ABI map. |

#### Returns

`Promise`&lt;`TransactionResult`&lt;`TTransactionType`\>\>

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:293](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L293)

___

### waitForResult

▸ **waitForResult**&lt;`TTransactionType`\>(`contractsAbiMap?`): `Promise`&lt;`TransactionResult`&lt;`TTransactionType`\>\>

Waits for transaction to complete and returns the result.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `TTransactionType` | `void` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `contractsAbiMap?` | [`AbiMap`](/api/Account/index.md#abimap) |

#### Returns

`Promise`&lt;`TransactionResult`&lt;`TTransactionType`\>\>

The completed transaction result

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:249](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L249)

___

### waitForStatusChange

▸ **waitForStatusChange**(): `Promise`&lt;`void`\>

#### Returns

`Promise`&lt;`void`\>

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:219](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L219)

___

### create

▸ **create**(`id`, `provider`, `abis?`): `Promise`&lt;[`TransactionResponse`](/api/Account/TransactionResponse.md)\>

Async constructor for `TransactionResponse`. This method can be used to create
an instance of `TransactionResponse` and wait for the transaction to be fetched
from the chain, ensuring that the `gqlTransaction` property is set.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `string` | The transaction ID. |
| `provider` | [`Provider`](/api/Account/Provider.md) | The provider. |
| `abis?` | [`JsonAbisFromAllCalls`](/api/Account/index.md#jsonabisfromallcalls) | - |

#### Returns

`Promise`&lt;[`TransactionResponse`](/api/Account/TransactionResponse.md)\>

#### Defined in

[packages/account/src/providers/transaction-response/transaction-response.ts:115](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/account/src/providers/transaction-response/transaction-response.ts#L115)
