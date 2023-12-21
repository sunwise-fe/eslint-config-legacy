# @sunwise/eslint-config

ESLint config for JavaScript, TypeScript, Vue 2, Vue 3, Prettier.

Forked from [sxzz/eslint-config](https://github.com/sxzz/eslint-config-legacy/tree/main)

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

> 注意如果你的项目中type为moudle，请修改配置文件为json或者rc格式

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
{
  "recommendations": [
    "Vue.volar",
    "Vue.vscode-typescript-vue-plugin",
    "esbenp.prettier-vscode",
    "dbaeumer.vscode-eslint",
    "stylelint.vscode-stylelint",
    "wangzy.sneak-mark"
  ]
}
```

> 注意: 如果你的项目中还有style部分，需要追加进去相关的配置

```jsonc
// settings.json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.organizeImports": "never",
    "source.fixAll.eslint": "explicit",
    "source.fixAll.stylelint": "explicit"
  },
  // 关闭 vscode 默认的检查工具
  "css.validate": false,
  "less.validate": false,
  "scss.validate": false,
  "stylelint.validate": ["css", "less", "postcss", "scss", "vue", "sass"],
  "eslint.run": "onSave",
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "vue-html",
    "vue",
    "html",
    "vue",
    "json",
    "json5",
    "jsonc",
    "yaml"
  ],
  "eslint.options": {
    "extensions": [".ts", ".tsx", ".vue"]
  },
  "typescript.tsdk": "node_modules/typescript/lib",
  "svg.preview.background": "black"
}
```
