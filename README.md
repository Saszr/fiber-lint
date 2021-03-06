# fiber-lint

[![license](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

> fork from [umi-fabric](https://github.com/umijs/fabric)

- 一个包含 prettier，eslint，stylelint 的配置文件合集
- 对比 `umi-fabric` 更高的自定义，通过命令可以生成配置的原文件

## Instructions

```bash
npm i fiber-lint --save-dev
```

in `.eslintrc.js`

> [eslint 配置在 monorepo 仓库下的 fix](https://github.com/umijs/fabric/issues/108#issuecomment-1085071151)

```js
const fiberLint = require('fiber-lint');

module.exports = {
  ...fiberLint.eslintConfig(__dirname),
  rules: {
    // your rules
  },
};
```

in `.stylelintrc.js`

```js
const fiberLint = require('fiber-lint');

module.exports = {
  ...fiberLint.stylelint,
  rules: {
    // your rules
  },
};
```

or

```js
module.exports = {
  extends: [require.resolve('fiber-lint/dist/stylelintrc')],
  rules: {
    // your rules
  },
};
```

in `.prettierrc.js`

```js
const fiberLint = require('fiber-lint');

module.exports = {
  ...fiberLint.prettier,
};
```

## Co-construction

- 公告 / 讨论 / 建议 ==> [Discussions](https://github.com/Saszr/fiber-lint/discussions)
- Bug / 优化 / 实现 ==> [Issues](https://github.com/Saszr/fiber-lint/issues)
- Code Review / 参与 ==> [Pull requests](https://github.com/Saszr/fiber-lint/pulls)
