# 运行脚本

假设您的 Sway 脚本 `main` 函数是使用传递给 `main` 函数的参数编写的，如下所示：

<<< @/../../../packages/fuel-gauge/test/fixtures/forc-projects/script-main-args/src/main.sw#script-with-main-args{rust:line-numbers}

您仍然可以手动编写一个解决方案包装器，使用 `callScript` 实用程序调用您的带有数据的脚本。但是，如果您更喜欢使用从脚本生成的 ABI，您可以使用 `ScriptFactory` 辅助工具：

<<< @/../../../packages/fuel-gauge/src/script-main-args.test.ts#script-call-factory{ts:line-numbers}
