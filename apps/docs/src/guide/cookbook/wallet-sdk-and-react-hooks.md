# 钱包 SDK 和 React Hooks

本指南将向您展示如何使用 [Fuel 钱包](https://wallet.fuel.network/) SDK 及其 [React Hooks](https://wallet.fuel.network/docs/dev/hooks-reference/) 构建一个简单的 React 应用程序，让用户将其钱包连接到您的应用程序并查看其余额。

## 设置

首先，我们将设置一个 Next.js 项目。

::: code-group

```sh [npm]
npm create next-app my-fuel-app
```

```sh [pnpm]
pnpm create next-app my-fuel-app
```

:::

接下来，我们将安装 Fuel Wallet React SDK 和 Fuel TypeScript SDK。

::: code-group

```sh [npm]
npm install fuels @fuels/connectors @fuels/react @tanstack/react-query
```

```sh [pnpm]
pnpm add fuels @fuels/connectors @fuels/react @tanstack/react-query
```

:::

## 提供者

为了使用 Fuel Wallet SDK 提供的 React hooks，我们需要将我们的应用程序包装在 `FuelProvider` 组件中。该组件将为 hooks 提供必要的上下文，以与 Fuel Wallet SDK 进行交互。将以下内容添加到您的 `pages/_app.tsx` 文件中：

<!-- prettier-ignore -->
<<< @/../../demo-wallet-sdk-react/pages/_app.tsx#wallet-sdk-react-provider{tsx:line-numbers}

## 构建 UI

转到您的 `pages/index.tsx` 文件，并将其内容替换为以下内容：

<<< @/../../demo-wallet-sdk-react/pages/index.tsx#wallet-sdk-react-ui{tsx:line-numbers}

让我们分解一下这里发生了什么。

`useConnectors` hook 返回一个可用钱包连接器的列表。

一旦用户选择了连接器，`useConnect` hook 将返回一个 `connect` 函数，该函数可用于将用户的钱包连接到您的应用程序。

`useAccount` hook 返回用户账户的信息（如果他们已连接）。

`useBalance` hook 返回用户的 ETH 余额（如果他们已连接）。

## 进一步阅读

- [钱包 SDK React Hooks 参考](https://wallet.fuel.network/docs/dev/hooks-reference/)
