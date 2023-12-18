# @sunwise/eslint-config

ESLint config for JavaScript, TypeScript, Vue 2, Vue 3, Prettier.

Forked from [antfu/eslint-config](https://github.com/sxzz/eslint-config-legacy/tree/main)

## Usage

```bash
pnpm i -D @sunwise/eslint-config-basic # JavaScript only
# Or yarn add -D / npm install -D
pnpm i -D @sunwise/eslint-config-ts # JavaScript and TypeScript
pnpm i -D @sunwise/eslint-config-vue # JavaScript, TypeScript and Vue 2/3 (Auto detect)
pnpm i -D @sunwise/eslint-config-prettier # Prettier only
pnpm i -D @sunwise/eslint-config # JavaScript, TypeScript, Vue 2/3 and Prettier
```

## Quick start

### Vue 3

```bash
pnpm i -D @sunwise/eslint-config
```

```javascript
// .eslintrc.js
module.exports = {
  root: true,
  extends: ['@sunwise/eslint-config'],
  rules: {
    // Your custom rules
  }
}
```

```jsonc
// .prettierrc
{
  "semi": false,
  "singleQuote": true
}
```

### VSCode

```jsonc
// settings.json
{
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "html",
    "vue",
    "json",
    "json5",
    "jsonc",
    "yaml"
  ],
  "eslint.probe": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "html",
    "vue",
    "json",
    "json5",
    "jsonc",
    "yaml"
  ]
}
```

### 参考资料

[使用 pnpm 创建一个 monorepo](https://juejin.cn/post/7302249560032690216?searchId=20231218160039CADC0756C3AA466D67DA)
