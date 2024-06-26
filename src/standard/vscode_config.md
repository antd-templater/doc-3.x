---
aside: false
---

# 项目开发配置

项目根目录下建立 .vscode/settings.json 文件，统一开发配置

```json
{
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[less]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[stylus]": {
    "editor.defaultFormatter": "thisismanta.stylus-supremacy"
  },
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint"
  },
  "[typescript]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint"
  },
  "[jsonc]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "[json]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "[vue]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint"
  },
  "editor.codeActionsOnSave": {
    "source.fixAll": "explicit"
  },
  "editor.tabSize": 2,
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.detectIndentation": false,
  "editor.renderControlCharacters": true,
  "eslint.useFlatConfig": true,
  "eslint.format.enable": true,
  "eslint.probe": [
    "javascript",
    "javascriptreact",
    "typescriptreact",
    "typescript",
    "html",
    "wxml",
    "vue"
  ],
  "prettier.semi": false,
  "prettier.useTabs": false,
  "prettier.tabWidth": 2,
  "prettier.printWidth": 200,
  "prettier.singleQuote": true,
  "prettier.bracketSpacing": true,
  "prettier.bracketSameLine": false,
  "prettier.jsxSingleQuote": false,
  "prettier.vueIndentScriptAndStyle": false,
  "prettier.htmlWhitespaceSensitivity": "ignore",
  "prettier.quoteProps": "consistent",
  "prettier.arrowParens": "avoid",
  "prettier.trailingComma": "es5"
}
```
