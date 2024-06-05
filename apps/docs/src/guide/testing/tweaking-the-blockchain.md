# 生成区块

您可以使用 `produceBlocks` 辅助函数来强制生成区块，以达到任意的区块高度。当您想进行一些关于交易成熟度的测试时，这将非常有用。

<<< @/../../../packages/account/src/providers/provider.test.ts#Provider-produce-blocks{ts:line-numbers}

# 使用自定义时间戳生成区块

您还可以使用 `produceBlocks` 辅助函数通过指定第二个可选参数来生成具有自定义区块时间的区块。

<<< @/../../docs-snippets/src/guide/testing/tweaking-the-blockchain.test.ts#Provider-produceBlocks-custom-timestamp{ts:line-numbers}
