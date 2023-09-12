# ESLint and Prettier config example

## packages
- "@typescript-eslint/eslint-plugin"
- "@typescript-eslint/parser"
- "eslint-config-prettier"
- "eslint-plugin-prettier"
- "eslint"
- "prettier"

## config eslint
```bash
npm init @eslint/config
```

`.eslintrc.cjs`
```js
module.exports = {
  env: {
    browser: true,
    es2021: true,
  },
  extends: [
    "eslint:recommended",
    "plugin:@typescript-eslint/recommended",
    "plugin:prettier/recommended",
  ],
  overrides: [
    {
      env: {
        node: true,
      },
      files: [".eslintrc.{js,cjs}"],
      parserOptions: {
        sourceType: "script",
      },
    },
  ],
  parser: "@typescript-eslint/parser",
  parserOptions: {
    ecmaVersion: "latest",
    sourceType: "module",
  },
  plugins: ["@typescript-eslint"],
  rules: {},
};
```

## config prettier
```ts
bun add @typescript-eslint/eslint-plugin eslint-plugin-prettier prettier
```

`.prettierrc.json`
```json
{
  "trailingComma": "all",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": false
}
```
