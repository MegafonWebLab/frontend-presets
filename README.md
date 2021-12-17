# MegaFon Frontend Presets

Collection of tools configuration.

[![npm (scoped with tag)](https://img.shields.io/npm/v/@megafon/frontend-presets/latest?label=%40megafon%2Ffrontend-presets)](https://www.npmjs.com/package/@megafon/frontend-presets)
[![Github Actions](https://github.com/MegafonWebLab/frontend-presets/workflows/auto%20publish%20ci/badge.svg)](https://github.com/MegafonWebLab/frontend-presets/actions)

## Installation

Dependencies:

- stylelint
- stylelint-order
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

```bash
npm install --save-dev @megafon/frontend-presets @typescript-eslint/eslint-plugin@^4.33.0 @typescript-eslint/parser@^4.33.0 eslint@^7.32.0 eslint-config-airbnb@^18.2.1 eslint-config-prettier@^8.3.0 eslint-plugin-import@^2.24.2 eslint-plugin-jsx-a11y@^6.4.1 eslint-plugin-prettier@^4.0.0 eslint-plugin-react@^7.26.1 eslint-plugin-react-hooks@^4.2.0 prettier@^2.4.1 stylelint@^13.13.1 stylelint-order@^4.1.0
```

```bash
yarn add -D @megafon/frontend-presets @typescript-eslint/eslint-plugin@^4.33.0 @typescript-eslint/parser@^4.33.0 eslint@^7.32.0 eslint-config-airbnb@^18.2.1 eslint-config-prettier@^8.3.0 eslint-plugin-import@^2.24.2 eslint-plugin-jsx-a11y@^6.4.1 eslint-plugin-prettier@^4.0.0 eslint-plugin-react@^7.26.1 eslint-plugin-react-hooks@^4.2.0 prettier@^2.4.1 stylelint@^13.13.1 stylelint-order@^4.1.0
```

## eslint

**Add to `package.json`**:

```jsonc
"eslintConfig": {
    // ...
    "extends": "./node_modules/@megafon/frontend-presets/eslint"
},
```

or

**Add to `.eslintrc.json`**:

```json
{
    // ...
    "extends": "./node_modules/@megafon/frontend-presets/eslint",
}
```

> NOTE: It's important to add this extend at the end of existing extends on your project in order to override previously extended rules

```json
"extends": [
  "foo",
  "plugin:bar/recommended",
  "./node_modules/@megafon/frontend-presets/eslint"
]
```

or

**Create `.eslintrc.js`**:

```js
module.exports = {
  ...require('@megafon/frontend-presets/eslint'),
};
```

## stylelint

**Create `.stylelintrc.json`**:

```json
{
  "extends": "@megafon/frontend-presets/stylelint"
}
```

## prettier

**Change `package.json`**:

```jsonc
{
  // ...
  "prettier": "@megafon/frontend-presets/prettier"
}
```

or

**Create `.prettierrc.js`**:

```js
module.exports = {
  ...require('@megafon/frontend-presets/prettier'),
  // overrides
  semi: false,
};
```

## Contributing

Follow [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
