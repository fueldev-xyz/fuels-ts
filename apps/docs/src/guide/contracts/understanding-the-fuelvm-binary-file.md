# 理解 FuelVM 二进制文件

当您使用 `forc build` 命令编译您的 Sway 代码时，它会生成一个字节码文件。这个二进制文件包含了 Fuel 虚拟机 (FuelVM) 将解释和执行的编译后的代码。

例如，考虑以下智能合约：

<<< @/../../docs-snippets/test/fixtures/forc-projects/echo-values/src/main.sw#understanding-fuel-binary-file{ts:line-numbers}

运行 `forc build` 后，将生成一个具有以下内容的二进制文件：

```sh
$ cat out/debug/echo-values.bin
�GT]����]@`I]G�I@sH]G�I@sHr�{6�]D`J]C�%E]@`J$@Ͼ{RD�^�%
```

乍一看，内容似乎难以理解。但是，`forc` 提供了一个有用的解释器来解析这个字节码：`forc parse-bytecode` 命令。该命令接受二进制数据，并输出等效的 FuelVM 汇编代码：

```sh
$ forc parse-bytecode out/debug/echo-values.bin
half-word   byte   op                raw           notes
        0   0      JI(4)             90 00 00 04   jump to byte 16
        1   4      NOOP              47 00 00 00
        2   8      Undefined         00 00 00 00   data section offset lo (0)
        3   12     Undefined         00 00 00 34   data section offset hi (52)
        4   16     LW(63, 12, 1)     5d fc c0 01
        5   20     ADD(63, 63, 12)   10 ff f3 00
        6   24     LW(17, 6, 73)     5d 44 60 49
        7   28     LW(16, 63, 1)     5d 43 f0 01
        8   32     EQ(16, 17, 16)    13 41 14 00
        9   36     JNZI(16, 11)      73 40 00 0b   conditionally jump to byte 44
       10   40     RVRT(0)           36 00 00 00
       11   44     LW(16, 63, 0)     5d 43 f0 00
       12   48     RET(16)           24 40 00 00
       13   52     Undefined         00 00 00 00
       14   56     Undefined         00 00 00 01
       15   60     Undefined         00 00 00 00
       16   64     XOR(20, 27, 53)   21 51 bd 4b
```

在使用 SDK 部署您的智能合约时，二进制文件发挥着至关重要的作用。它被发送到 FuelVM 中的一个交易中，使 FuelVM 能够解释和执行您的智能合约。