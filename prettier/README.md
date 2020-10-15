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