<script setup>
  import { data } from '../../versions.data'
  const { fuels } = data
</script>

# 从 ABI 生成类型

## 安装

首先，我们将 `fuels` 安装到我们的项目中：

```console-vue
pnpm add fuels@{{fuels}}
```

## 帮助

首先浏览文档：

```console
$ pnpm fuels typegen -h

Usage: fuels typegen [options]

Generate Typescript from Sway ABI JSON files

Options:
  -i, --inputs <path|glob...>  Input paths/globals to your ABI JSON files
  -o, --output <dir>           Directory path for generated files
  -c, --contract               Generate types for Contracts [default]
  -s, --script                 Generate types for Scripts
  -p, --predicate              Generate types for Predicates
  -S, --silent                 Omit output messages
  -h, --help                   Display help
```

## 生成合约类型

您可以使用以下命令为 Sway 合约生成类型：

<!-- This section should have the command to generate types for a Sway contract -->
<!-- gen_types:example:start -->

```console
pnpm fuels typegen -i ./abis/*-abi.json -o ./types
```

<!-- gen_types:example:end -->

<!-- This section should explain the flags used in the typegen command -->
<!-- flags:example:start -->

输入标志 `-i` 后面的路径应指向在构建合约时生成的以 `-abi.json` 结尾的文件。

输出标志 `-o` 后面的路径将是生成类型的输出目录。

您可以在此处省略 `--contract` 选项，因为它是默认值。

<!-- flags:example:end -->

## 生成脚本类型

要为 Sway 脚本生成类型，请使用 `--script` 标志：

```console
pnpm fuels typegen -i ./abis/*-abi.json -o ./types --script
```

## 生成断言类型

要为 Sway 断言生成类型，请使用 `--predicate` 标志：

```console
pnpm fuels typegen -i ./abis/*-abi.json -o ./types --predicate
```

---

另请参阅：

- [使用生成的合约类型](./using-generated-types.md#contract)
- [使用生成的脚本类型](./using-generated-types.md#script)
- [使用生成的断言类型](./using-generated-types.md#predicate)
