<script setup>
  import { data } from '../../versions.data'
  const { forc } = data
  const url = `
    https://docs.fueldev.xyz/docs/sway/introduction/
  `
</script>

# 实例化脚本

与合约和断言类似，一旦您在 Sway 中编写了脚本并使用 `forc build` 编译它（了解有关如何使用 Sway 的更多信息，请阅读<a :href="url" target="_blank" rel="noreferrer">此处</a>），您将获得脚本二进制文件。使用二进制文件，您可以像下面的代码片段一样实例化一个 `script`：

<<< @/../../../packages/script/src/script.test.ts#script-init{ts:line-numbers}

在[下一节](./running-scripts.md)中，我们将展示如何运行一个脚本。

