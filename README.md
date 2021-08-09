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
$ npm install --save-dev @megafon/frontend-presets eslint@^7.24.0 prettier@^2.2.1 @typescript-eslint/eslint-plugin@^4.22.0 @typescript-eslint/parser@^4.22.0 eslint-config-airbnb@^18.2.1 eslint-config-prettier@^8.2.0 eslint-plugin-import@^2.22.1 eslint-plugin-jsx-a11y@^6.4.1 eslint-plugin-prettier@^3.4.0 eslint-plugin-react@^7.23.2 eslint-plugin-react-hooks@^4.2.0 stylelint@^13.12.0 stylelint-order@^4.1.0
```

```bash
$ yarn add -D @megafon/frontend-presets eslint@^7.24.0 prettier@^2.2.1 @typescript-eslint/eslint-plugin@^4.21.0 @typescript-eslint/parser@^4.22.0 eslint-config-airbnb@^18.2.1 eslint-config-prettier@^8.2.0 eslint-plugin-import@^2.22.1 eslint-plugin-jsx-a11y@^6.4.1 eslint-plugin-prettier@^3.4.0 eslint-plugin-react@^7.23.2 eslint-plugin-react-hooks@^4.2.0 stylelint@^13.12.0 stylelint-order@^4.1.0
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

## Release

There are multiple commands to make a release:

```bash
$ yarn release --patch
$ yarn release --minor
$ yarn release --major
```

After executing it, a new tag is created. When it's pushed, `Github Actions` will publish a new package to npm automatically.

## Contributing

Follow [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
