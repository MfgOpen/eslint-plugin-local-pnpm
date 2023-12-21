# eslint-plugin-local-pnpm

**ESLint plugin for implementing a custom ESLint plugin (including custom rules) for a project locally.**

For more information, see [this issue](https://github.com/eslint/eslint/issues/8769).

Inspired by [taskworld/eslint-plugin-local](https://github.com/taskworld/eslint-plugin-local).

## Usage

To install the plugin:

```
npm install --dev eslint-plugin-local-pnpm
```

Create a custom plugin at `.eslintplugin.js` or `.eslintplugin/index.js` in the local project.

```js
exports.rules = {
  'enforce-only-string-literals-in-l10n-functions': {
    create: function (context) {
      return { ... }
    }
  }
}
```

Adding the plugin to the ESLint configuration file:

```json
{
    // ...
    "plugins": [
        "@mfgopen/local-pnpm"
    ],
    "rules": {
        "@mfgopen/local-pnpm/enforce-only-string-literals-in-l10n-functions": "error"
    },
    // ...
}
```