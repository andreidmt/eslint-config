<!-- markdownlint-disable no-duplicate-header line-length -->

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [4.0.2] - 28 December 2018

### Add

- `import/resolver` setting in [`node`](src/targets/node.js#L45) and [`react`](src/targets/react.js#L59) target files

## [4.0.1] - 8 December 2018

### Remove

- Disable [promise/always-return](rules/promise.js#L23)

## [4.0.0] - 8 December 2018

### Change

- Change [`flowtype/type-id-match`](rules/flow.js#L139) to allow multiple starting uppercase letters
- [`flowtype-errors/enforce-min-coverage`](rules/flow.js#L139) lowered to 60. Makes learning curve easier
- Remove `style` from [`react/forbid-dom-props`](rules/react.js#L50)

### Remove

- Remove `jsx-control-statements` plugin. Adds too much complexity when using with `flow`
- Disable [`react/no-unused-prop-types`](rules/flow.js#L31) rule when using `flow`
- Disable [`flowtype/require-exact-type`](rules/flow.js#L77) rule. Too strict and unrealistic
- Disable [`unicorn/filename-case`](rules/unicorn.js#57) and [`unicorn/no-fn-reference-in-iterator`](rules/unicorn.js#L21)
- Disable [`promise/prefer-await-to-then`](rules/promise.js#L58) and [`promise/prefer-await-to-callbacks`](rules/promise.js#L61)

## [3.0.2] - 25 November 2018

### Change

- Fix flow rules assing to `flowtype-errors` instead of `flowtype`

## [3.0.1] - 17 November 2018

Update packages and rename to @asd14

## [3.0.0] - 8 October 2018

Restructuring bundles as "target" files. Supporting React and Node.js, with optional Flow support.

Delegating all stylistic rules to [`prettier`](https://prettier.io) via [`eslint-config-prettier`](https://github.com/prettier/eslint-config-prettier) and [`eslint-plugin-prettier`](https://github.com/prettier/eslint-plugin-prettier).

### Added

- unicorn: [`unicorn/no-process-exit`](/rules/unicorn.js#L12), [`unicorn/number-literal-case`](/rules/unicorn.js#L20), [`unicorn/no-fn-reference-in-iterator`](/rules/unicorn.js#L23), [`unicorn/import-index`](/rules/unicorn.js#L29), [`unicorn/prefer-spread`](/rules/unicorn.js#L36), [`unicorn/prefer-add-event-listener`](/rules/unicorn.js#L45), [`unicorn/prefer-exponentiation-operator`](/rules/unicorn.js#L48)
- react: [`react/void-dom-elements-no-children`](/rules/react.js#L12), [`react/prefer-es6-class`](/rules/react.js#L15), [`react/no-unused-prop-types`](/rules/react.js#L18), [`react/no-unused-state`](/rules/react.js#L21), [`react/no-unsafe`](/rules/react.js#L24), [`react/no-will-update-set-state`](/rules/react.js#L27), [`react/forbid-dom-props`](/rules/react.js#L30), [`react/forbid-prop-types`](/rules/react.js#L32), [`react/jsx-filename-extension`](/rules/react.js#L40), [`react/jsx-max-depth`](/rules/react.js#L43)
- flowtype-errors: [`flowtype-errors/type-import-style`](/rules/flow.js#L34), [`flowtype-errors/require-types-at-top`](/rules/flow.js#L40), [`flowtype-errors/no-unused-expressions`](/rules/flow.js#L47), [`flowtype-errors/array-style-complex-type`](/rules/flow.js#L50), [`flowtype-errors/array-style-simple-type`](/rules/flow.js#L53)

### Changed

- [`jsx-control-statements/jsx-use-if-tag`](/rules/react.js#L339) from "error" -> "warn"
- [`react/sort-comp`](/rules/react.js#L247) added `getDerivedStateFromProps` and `componentDidCatch`
- [`flowtype/require-return-type`](/rules/flow.js#L) from "off" -> "error"

## [2.9.7] - 14 September 2018

Bumped versions

## [2.9.6] - 23 April 2018

Bumped versions

## [2.9.5] - 14 February 2018

### Added

- [`react/no-this-in-sfc`](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/no-this-in-sfc.md) - Prevent this from being used in stateless functional components
- [`unicorn/no-unsafe-regex`](https://github.com/sindresorhus/eslint-plugin-unicorn/blob/master/docs/rules/no-unsafe-regex.md) - Uses [safe-regex](https://github.com/substack/safe-regex) to disallow potentially catastrophic exponential-time regular expressions
- [`unicorn/error-message`](https://github.com/sindresorhus/eslint-plugin-unicorn/blob/master/docs/rules/error-message.md) - Enforce passing a message value when throwing a built-in error
- [`flowtype/newline-after-flow-annotation`](https://github.com/gajus/eslint-plugin-flowtype/blob/master/.README/rules/newline-after-flow-annotation.md) - Enforces that `@flow` annotations be followed by an empty line
- [`flowtype/require-exact-type`](https://github.com/gajus/eslint-plugin-flowtype/blob/master/.README/rules/require-exact-type.md) - Report all object type definitions that aren't exact
- [`flowtype/no-existential-type`](https://github.com/gajus/eslint-plugin-flowtype/blob/master/.README/rules/no-existential-type.md) - Disallows use of the existential type `*`

### Changed

- [`react/boolean-prop-naming`](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/boolean-prop-naming.md) - changed regexp `^(is|has)[A-Z]([A-Za-z0-9]?)+` from to `^(is|has|can|should).+` and added a custom message
- [`react/sort-comp`](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/sort-comp.md)
- [`unicorn/filename-case`](https://github.com/sindresorhus/eslint-plugin-unicorn/blob/master/docs/rules/filename-case.md) - from `camelCase` to `kebab-case`

## [2.9.4] - 14 January 2018

### Added

- [`camelcase`](/rules/style.js#L35)

## [2.9.3] - 2 December 2017

### Added

- [`react/jsx-one-expression-per-line`](/rules/react.js#L312)
- [`react/destructuring-assignment`](/rules/react.js#L318)
- [`react/no-access-state-in-setstate`](/rules/react.js#L323)
- [`react/button-has-type`](/rules/react.js#L328)
- [`react/jsx-wrap-multilines`](/rules/react.js#L333)

### Changed

- [`react/sort-comp`](/rules/rules.js#L252)
- [`react/require-default-props`](/rules/rules.js#L223)

## [2.9.2] - 12 November 2017

### Added

- configed all [`rules/unicorn`](/rules/unicorn.js), not just `fileCase`
- [`import/exports-last`](/rules/import.js#L86) - all exports are declared at the bottom of the file
- [`jest/prefer-to-have-length`](/rules/jest.js#L50) - use `toHaveLength`, not check `.length`

### Changed

- [`no-unused-expressions`](/rules/best-practices.js#L176)

## [2.9.1] - 17 October 2017

### Added

- [`import/ignore`](/rules/import.js#L11) to ignore css/scss/sass files
- [`import/extensions`](/rules/import.js#L77) `.js` and `['.js', '.jsx']` if [react](/rules/react.js#L361) is loaded.

### Changed

- [`react/jsx-no-comment-textnodes`](/rules/react.js#L30)
- [`object-property-newline`](/rules/style.js#L250)
- [`no-multi-spaces`](/rules/best.practices.js#L115)
- [`no-unused-vars`](/rules/variables.js#L42)
- [`space-before-function-paren`](/rules/style.js#L329)

## [2.9.0] - 16 October 2017

Update packages and new rules for react & promise

### Added

- [`react/jsx-curly-brace-presence`](/rules/react.js#L205)
- [`promise/no-return-in-finally`](/rules/promise.js#L65)

### Changed

- [`no-else-return`](/rules/best.practices.js#L55)
- [`array-bracket-newline`](/rules/style.js#L10)

## [2.8.3] - 24 September 2017

### Changed

- updated [`react`](/rules/react.js) rules with:
    - [`react/sort-comp`](/rules/react.js#L252) - predefined order of component methods (eslint-react [rule](https://github.com/yannickcr/eslint-plugin-react/blob/HEAD/docs/rules/sort-comp.md))
    - [`react/jsx-no-bind`](/rules/react.js#L306) - no longer bind function in render (eslint-react [rule](https://github.com/yannickcr/eslint-plugin-react/blob/HEAD/docs/rules/jsx-no-bind.md))

## [2.8.2] - 24 September 2017

### Changed

- updated [`react`](/rules/react.js#L125) with more jsx style rules

## [2.8.1] - 23 September 2017

Updated packages & added `eslint-plugin-jsx-control-statements`

### Added

- New [`jsx-control-statements`](https://github.com/asd14/eslint-config#jsx-control-statements) to the [react](/rules/react.js#L104) rules.

### Changed

- [`react/jsx-no-undef`](/rules/react.js#L36) - from v7, `eslint-plugin-react` does not check globals by default anymore and need to be set explicitly.

## [2.8.0] - 18 September 2017

Updated main packages (`eslint` & `flow-bin`) & others that kept up with eslint 4.7 update

## [2.7.2] - 18 August 2017

Removed Flow from both bundles, need to be loaded separately

### Added

- React [`boolean-prop-naming`](/rules/react.js#L85), [`no-typos`](/rules/react.js#L93) and [`jsx-boolean-value`](/rules/react.js#L40)

### Changed

- Removed [`flow`](/rules/flow.js) from both bundles. Need to include it [separately](https://github.com/asd14/eslint-config#flowtype--flowtype-errors)

## [2.7.1] - 4 August 2017

### Added

- New [`eslint-plugin-flowtype-errors`](https://github.com/asd14/eslint-config#eslint-plugin-flowtype-errors) to the [flow](/rules/flow.js#L4) config. It runs flow  and passes the errors as linting error.

### Changed

- [`prefer-destructuring`](/rules/backend.js#62) - set rule to warn and disabled for objects (was a nuisance)
- Removed [`jest`](/rules/jest.js) from frontend bundle. Need to include it [separately](https://github.com/asd14/eslint-config#eslint-plugin-jest)

## [2.6.0] - 23 July 2017

Updated to [ESLint 4.3](http://eslint.org/blog/2017/07/eslint-v4.3.0-released) and added support for [Jest](https://github.com/facebook/jest) testing framework.

### Added

- Plugin [`eslint-plugin-jest`](https://www.npmjs.org/package/eslint-plugin-jest) with rules in [`/rules/jest.js`](/rules/jest.js) and part of [`frontend`](/rules/frontend.js#L24)
- ESLint rule [`prefer-numeric-literals`](http://eslint.org/docs/rules/prefer-numeric-literals): Disllow parseInt() and Number.parseInt() in favor of binary, octal, and hexadecimal literals
    - Defined in [`errors.js`](/rules/errors.js#L115)
    - Current value: `"prefer-numeric-literals": "error"`
- ESLint rule [`prefer-destructuring`](http://eslint.org/docs/rules/prefer-destructuring): Prefer destructuring from arrays and objects.
    - Defined in [`variables.js`](/rules/variables.js#L63)
    - Current value:
        ```javascript
        "prefer-destructuring": [
            "error", {
                object: true,
                array : true,
            }, {
                enforceForRenamedProperties: true,
            },
        ],
        ```
    - Sample:
        ```javascript
        const array = [ 1,2,3,4,5 ]
        const lorem = {
            bar: "ipsum",
            foo: "dolor",
        }

        // const someIndex = 2
        // const foo = array[ someIndex ]
        const [ ,,foo ] = array

        // const bar = lorem.bar
        let { bar } = lorem;

        ( { bar } = {
            bar: 2,
            foo: 3,
        } );

        ( { foo: bar } = lorem )
        ```

## [2.5.1] - 21 July 2017

### Changed

Updated [`rules/style.js`](/rules/style.js#L263):

- changed [`object-curly-newline`](http://eslint.org/docs/rules/object-curly-newline)
- added [`object-property-newline`](http://eslint.org/docs/rules/object-property-newline)

Needed to satisfy:

```javascript
const a = { }
const obj = {
    foo: "foo",
    bar: "bar",
    baz: "baz",
}
let {} = obj
const obj2 = {
    foo: "foo",
    bar: "bar",
    baz: "baz",
}
const { f } = obj
const { g, h } = obj
const {
    i,
    j,
} = obj
const e = {
    foo( { x, y } ) {
        dosomething()
    },
}
const h = ( opt = {} ) => ( {
    x: 2,
    y: opt,
} )
```

## [2.5.0] - 16 July 2017

Added [`eslint-plugin-compat`](https://www.npmjs.com/package/eslint-plugin-compat) to show browser compatibility (using [caniuse](http://caniuse.com/)) of certain functionalities, ex. `fetch`.

### Added

- `eslint-plugin-compat` with rules in [`/rules/compat.js`](/rules/compat.js)

### Changed

- Turn off `react/require-optimization`. Better put these kind of rules in your project's `.eslintrc`

## [2.4.0] - 13 July 2017

React support

### Added

- `eslint-plugin-react` with recommended rules in [`/rules/react.js`](/rules/react.js)

## 2.3.2 - 11 July 2017

### Added

- ESLint 4.2: new rule [`getter-return`](http://eslint.org/docs/rules/getter-return) -  Enforces that a return statement is present in property getters.
    - Defined in [`error.js`](/rules/errors.js)
    - Current value: `"getter-return": "error"`

### Changed

- ESLint 4.2 allows [`no-sync`](http://eslint.org/docs/rules/no-sync) using sync methods on top level.
    - Defined in [`node.js`](/rules/node.js)
    - Current value:

    ```javascript
    "no-sync": [
        "error", {
            allowAtRootLevel: true,
        },
    ],
    ```
- [`no-unexpected-multiline`](http://eslint.org/docs/rules/no-unexpected-multiline) to protect against edge cases of not using semicolons
    - Defined in [`error.js`](/rules/errors.js):
    - Current value: `"no-unexpected-multiline": "error"`

[Unreleased]: https://github.com/asd14/eslint-config/compare/v4.0.2...HEAD

[4.0.2]: https://github.com/asd14/eslint-config/compare/v4.0.1...v4.0.2
[4.0.1]: https://github.com/asd14/eslint-config/compare/v4.0.0...v4.0.1
[4.0.0]: https://github.com/asd14/eslint-config/compare/v3.0.2...v4.0.0
[3.0.2]: https://github.com/asd14/eslint-config/compare/v3.0.1...v3.0.2
[3.0.1]: https://github.com/asd14/eslint-config/compare/v3.0.0...v3.0.1
[3.0.0]: https://github.com/asd14/eslint-config/compare/v2.9.7...v3.0.0
[2.9.7]: https://github.com/asd14/eslint-config/compare/v2.9.6...v2.9.7
[2.9.6]: https://github.com/asd14/eslint-config/compare/v2.9.5...v2.9.6
[2.9.5]: https://github.com/asd14/eslint-config/compare/v2.9.4...v2.9.5
[2.9.4]: https://github.com/asd14/eslint-config/compare/v2.9.3...v2.9.4
[2.9.3]: https://github.com/asd14/eslint-config/compare/v2.9.2...v2.9.3
[2.9.2]: https://github.com/asd14/eslint-config/compare/v2.9.0...v2.9.2
[2.9.1]: https://github.com/asd14/eslint-config/compare/v2.9.0...v2.9.1
[2.9.0]: https://github.com/asd14/eslint-config/compare/v2.8.3...v2.9.0
[2.8.3]: https://github.com/asd14/eslint-config/compare/v2.8.2...v2.8.3
[2.8.2]: https://github.com/asd14/eslint-config/compare/v2.8.1...v2.8.2
[2.8.1]: https://github.com/asd14/eslint-config/compare/v2.8.0...v2.8.1
[2.8.0]: https://github.com/asd14/eslint-config/compare/v2.7.2...v2.8.0
[2.7.2]: https://github.com/asd14/eslint-config/compare/v2.7.1...v2.7.2
[2.7.1]: https://github.com/asd14/eslint-config/compare/v2.6.0...v2.7.1
[2.6.0]: https://github.com/asd14/eslint-config/compare/v2.5.1...v2.6.0
[2.5.1]: https://github.com/asd14/eslint-config/compare/v2.5.0...v2.5.1
[2.5.0]: https://github.com/asd14/eslint-config/compare/v2.4.0...v2.5.0
[2.4.0]: https://github.com/asd14/eslint-config/compare/v2.3.2...v2.4.0
