# MegaFon Frontend Presets

## Установка

Установка зависимостей:

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

Установка одной строкой:

```
npm install eslint@^7.12.0 prettier@^2.1.2 @typescript-eslint/eslint-plugin@^4.6.0 @typescript-eslint/parser@^4.6.0 eslint-config-airbnb@^18.2.0 eslint-config-prettier@^6.14.0 eslint-plugin-import@^2.22.1 eslint-plugin-jsx-a11y@^6.4.1 eslint-plugin-prettier@^3.1.4 eslint-plugin-react@^7.21.5 eslint-plugin-react-hooks@^4.2.0 stylelint@^13.7.2 stylelint-order@^4.1.0 --save-dev
```

```
yarn add -D eslint@^7.12.0 prettier@^2.1.2 @typescript-eslint/eslint-plugin@^4.6.0 @typescript-eslint/parser@^4.6.0 eslint-config-airbnb@^18.2.0 eslint-config-prettier@^6.14.0 eslint-plugin-import@^2.22.1 eslint-plugin-jsx-a11y@^6.4.1 eslint-plugin-prettier@^3.1.4 eslint-plugin-react@^7.21.5 eslint-plugin-react-hooks@^4.2.0 stylelint@^13.7.2 stylelint-order@^4.1.0
```

## eslint

**Добавить в `package.json`**:

```jsonc
"eslintConfig": {
    // ...
    "extends": "./node_modules/@megafon/frontend-presets/eslint"
},
```

или

**Создать `.eslintrc.js`** и добавить:

```js
module.exports = {
  ...require("@megafon/frontend-presets/eslint"),
};
```

## stylelint

**Создать `.stylelintrc.json`** и добавить
```json
{
  "extends": "@megafon/frontend-presets/stylelint"
}
```

## prettier

**Изменить `package.json`**:

```jsonc
{
  // ...
  "prettier": "@megafon/frontend-presets/prettier"
}
```

или

**Создать `.prettierrc.js`** и записать:

```js
module.exports = {
  ...require("@megafon/frontend-presets/prettier"),
  semi: false,
};
```

## Релиз

Выполнить одну из следующих комманд:

```
yarn release --patch
yarn release --minor
yarn release --major
```

Затем пушните изменения с созданным тегом. Github Actions опубликует новый пакет в npm.
