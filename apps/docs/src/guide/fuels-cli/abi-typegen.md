<script setup>
  import { data } from '../../versions.data'
  const { forc } = data
  const abiUrl = `
    https://docs.fueldev.xyz/docs/sway/sway-program-types/smart_contracts/#the-abi-declaration
  `
  const contractsUrl = `
    https://docs.fueldev.xyz/docs/sway/sway-program-types/smart_contracts/
  `
  const scriptsUrl = `
    https://docs.fueldev.xyz/docs/sway/sway-program-types/scripts/
  `
</script>

# ABI 类型生成器

## JSON ABI 文件

无论您是要部署还是连接到预先存在的智能合约，<a :href="abiUrl" target="_blank" rel="noreferrer">JSON ABI</a> 文件都是实现这一目标的关键。

它向 SDK 提供有关您的 <a :href="contractsUrl" target="_blank" rel="noreferrer">智能合约</a> 和 <a :href="scriptsUrl" target="_blank" rel="noreferrer">脚本</a> 中的 <a :href="abiUrl" target="_blank" rel="noreferrer">ABI 方法</a> 的信息。

给定以下 Sway 智能合约：

```rust:line-numbers
contract;

abi MyContract {
    fn test_function() -> bool;
}

impl MyContract for Contract {
    fn test_function() -> bool {
        true
    }
}
```

JSON ABI 文件可能如下所示：

```json
$ cat out/debug/my-test-abi.json
[
  {
    "type": "function",
    "inputs": [],
    "name": "test_function",
    "outputs": [
      {
        "name": "",
        "type": "bool",
        "components": null
      }
    ]
  }
]
```

另请参阅：

- [生成类型](./generating-types.md)
- [使用生成的类型](./using-generated-types.md)

