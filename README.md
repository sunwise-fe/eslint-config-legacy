# @sunwise/eslint-config

ESLint config for JavaScript, TypeScript, Vue 2, Vue 3, Prettier.

Forked from [sxzz/eslint-config](https://github.com/sxzz/eslint-config-legacy/tree/main)

## Usage

```bash
pnpm i -D @sunwise/eslint-config-legacy-basic # JavaScript only
# Or yarn add -D / npm install -D
pnpm i -D @sunwise/eslint-config-legacy-ts # JavaScript and TypeScript
pnpm i -D @sunwise/eslint-config-legacy-vue # JavaScript, TypeScript and Vue 2/3 (Auto detect)
pnpm i -D @sunwise/eslint-config-legacy-prettier # Prettier only
pnpm i -D @sunwise/eslint-config-legacy # JavaScript, TypeScript, Vue 2/3 and Prettier
```

## Quick start

### Vue 3

```bash
pnpm i -D @sunwise/eslint-config-legacy
```

> 注意如果你的项目中type为moudle，请修改配置文件为json或者rc格式

```javascript
// .eslintrc.js
module.exports = {
  root: true,
  extends: ['@sunwise/eslint-config-legacy', './.eslintrc-auto-import.json'],
  rules: {
    // Your custom rules
  }
}
```

```js
// .prettierrc.js
module.exports = {
  // 一行最多多少个字符
  printWidth: 100,
  // 指定每个缩进级别的空格数
  tabWidth: 2,
  // 使用空格而不是制表符缩进
  useTabs: false,
  // 在语句末尾打印分号
  semi: false,
  vueIndentScriptAndStyle: true,
  // 使用单引号而不是双引号
  singleQuote: true,
  // 更改引用对象属性的时间 可选值"<as-needed|consistent|preserve>"
  quoteProps: 'as-needed',
  // 在对象文字中的括号之间打印空格
  bracketSpacing: true,
  // 多行时尽可能打印尾随逗号。（例如，单行数组永远不会出现逗号结尾。） 可选值"<none|es5|all>"，默认none
  trailingComma: 'none',
  // jsx 标签的反尖括号需要换行
  jsxBracketSameLine: false,
  jsxSingleQuote: false,
  arrowParens: 'always', // allow paren-less arrow functions 箭头函数的参数使用圆括号
  insertPragma: false,
  requirePragma: false,
  // 使用默认的折行标准 always\never\preserve
  proseWrap: 'never',
  // 指定HTML文件的全局空格敏感度 css\strict\ignore
  htmlWhitespaceSensitivity: 'strict',
  endOfLine: 'auto',
  plugins: [require('prettier-plugin-tailwindcss')],
  tailwindConfig: './tailwind.config.js'
}
```

// .prettierignore

```txt
*.cssr.js
*.cssr.ts


public
build/*.js
dist
node_modules/*


#docs


.vscode/settings.json
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
