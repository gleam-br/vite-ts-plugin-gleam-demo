# 🎓 Demo: Vite + TS plugin to gleam

Gleam build:

```sh
gleam clean
gleam build
```

Vite build:

```sh
npx vite build
```

## How this project was created

Vite create:

```sh
npm create vite
```

1. Project name -> `vite-ts-plugin-gleam-demo`
2. Select a framework -> `Vanilla`
3. Select a variant -> `TypeScript` *
4. Use rolldown-vite (Experimental) -> `No`
5. Install with npm and start now -> `No`

Add plugin:

```sh
cd vite-ts-plugin-gleam-demo
npm install --save-dev ts-plugin-gleam
npm install --save-dev vite-plugin-gleam
```

Vite config [vite.config.js](./vite.config.js):

```js
import { defineConfig } from "vite";
import vitePluginGleam from "vite-plugin-gleam";

export default defineConfig({
  plugins: [vitePluginGleam()]
})
```

TS config [tsconfig.json](./tsconfig.json):

```json
{
  "compilerOptions": {
    "plugins": [{"name": "ts-plugin-gleam"}]
  }
}
```

Gleam new:

```sh
cd vite-ts-plugin-gleam-demo
gleam new vite_plugin_gleam_demo --skip-git --skip-github --template javascript .
```

Install libs:

```sh
npm install
```

Vite dev:

```sh
npx vite dev
```

TS check:

🚧 **Work in progress** not production ready.

```sh
npx tsc
# error TS2307: Cannot find module './counter.gleam' or its corresponding type declarations.
# ts-plugin-gleam not resolve this error :(
```

## ✅ Plugins

- [ts-plugin-gleam](https://github.com/gleam-br/ts-plugin-gleam)
- [vite-plugin-gleam](https://github.com/gleam-br/vite-plugin-gleam)
- [bun-plugin-gleam](https://github.com/gleam-br/bun-plugin-gleam)

## 🧪 Demo

- [bun-plugin-gleam-demo](https://github.com/gleam-br/bun-plugin-gleam-demo)
- [bunup-plugin-gleam-demo](https://github.com/gleam-br/bunup-plugin-gleam-demo)
- [vite-plugin-gleam-demo](https://github.com/gleam-br/vite-plugin-gleam-demo)
