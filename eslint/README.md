**Installation**

Install peer dependencies:

- eslint
- prettier
- @typescript-eslint/eslint-plugin
- @typescript-eslint/parser
- eslint-config-airbnb
- eslint-config-prettier
- eslint-plugin-import
- eslint-plugin-jsx-a11y
- eslint-plugin-prettier
- eslint-plugin-react
- eslint-plugin-react-hooks

Installation one-liner:

```
yarn add -D eslint prettier @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-config-airbnb eslint-config-prettier eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks
```

**Edit `package.json`**:

```jsonc
"eslintConfig": {
    // ...
    "extends": "./node_modules/@megafon/frontend-presets/eslint"
},
```

or

**Create `.eslintrc.js`** for override:

```js
module.exports = {
  ...require("@megafon/frontend-presets/eslint"),
};
```
