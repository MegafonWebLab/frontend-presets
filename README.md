# MegaFon Frontend Presets

## Installation

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

## eslint

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

## prettier

**Edit `package.json`**:

```jsonc
{
  // ...
  "prettier": "@megafon/frontend-presets/prettier"
}
```

or

**Create `.prettierrc.js`** for override:

```js
module.exports = {
  ...require("@megafon/frontend-presets/prettier"),
  semi: false,
};
```

## Release

Run one of the following commands:

```
yarn release --patch
yarn release --minor
yarn release --major
```

Then push changes with created tag. Github Actions will publish new package to npm.
