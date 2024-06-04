# 用法

有了 Fuels 依赖设置，现在你可以创建一个连接到 Fuel 提供程序并检索给定钱包地址的基本资产余额的 React 组件。以下是如何实现的示例：

<!-- TODO: Create properly code snippet on new package: `app/react-app` after https://github.com/FuelLabs/fuels-ts/pull/827 got merged -->

```tsx
import { BN, Provider, Wallet } from "fuels";
import { useEffect, useState } from "react";

function App() {
  const [balance, setBalance] = useState(0);

  useEffect(() => {
    async () => {
      const provider = await Provider.create("https://devnet.fuel.network/v1/graphql");
      const myWallet = Wallet.fromAddress("0x...", provider);
      myWallet.getBalances().then((data) => {
        setBalance(new BN(data[0].amount).toNumber());
      });
    }()
  }, []);

  return <div>My Balance: {balance}</div>;
}

export default App;
```

## CDN 用法（仅限浏览器）

为了快速测试或仅仅是玩玩，你可以直接从我们的 CDN 在你的 Web 应用程序中加载它。

```html
<script type="module">
  import {
    Wallet,
    Provider,
  } from "https://cdnjs.cloudflare.com/ajax/libs/fuels/{{fuels}}/browser.mjs";

  const exec = async () => {
    const provider = await Provider.create(
      "https://devnet.fuel.network/v1/graphql",
    );
    const { name } = provider.getChain();
    console.log(name);
  };
  exec();
</script>
```