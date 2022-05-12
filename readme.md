[![Build Status](https://travis-ci.com/sasial-dev/eslint-config-vue-standard-typescript.svg?branch=master)](https://travis-ci.com/sasial-dev/eslint-config-vue-standard-typescript)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![Releases](https://coderelease.io/badge/sasial-dev/eslint-config-vue-standard-typescript)](https://coderelease.io/github/repository/sasial-dev/eslint-config-vue-standard-typescript)

# eslint-config-vue-standard-typescript

An [ESLint shareable config](https://eslint.org/docs/developer-guide/shareable-configs) for TypeScript that is based on [eslint-config-standard](https://github.com/standard/eslint-config-standard) and has TypeScript specific rules from [@typescript-eslint/eslint-plugin](https://www.npmjs.com/package/@typescript-eslint/eslint-plugin) along with Vue support.

## Usage

`npm@<7` does not automatically install `peerDependencies`,
so if that's what you're using, install them manually.
Here is an example, but use it only for reference,
because your decisions regarding version ranges and range specifiers may vary.

```
npm install --save-dev typescript@* eslint@^8.0.1 eslint-config-vue-standard-typescript@latest
```

To remove the need for a large number of packages, yet allowing us to give you control, we use the rushstack [eslint-patch](https://www.npmjs.com/package/@rushstack/eslint-patch).

Here is an example `.eslintrc.js` / `.eslintrc.cjs`:

```js
require('@rushstack/eslint-patch/modern-module-resolution')

module.exports = {
  extends: 'vue-standard-typescript',
  parserOptions: {
    project: './tsconfig.json'
  }
}
```

Note: Please read some important instructions regarding the `project` option [here](https://github.com/typescript-eslint/typescript-eslint/blob/main/packages/parser/README.md#parseroptionsproject).

There are [some more `parserOptions`](https://github.com/typescript-eslint/typescript-eslint/blob/master/packages/parser/README.md#configuration) you may care about.

Example command line usage:

```
$ npx eslint .
```
