# Arrow Function Expressions

An arrow function expression is a compact alternative to a traditional function expression

It has some semantic differences and deliberate limitations in usage:

- Arrow functions don't have their own bindings to `this`, `arguments`, or `super`, and should not be used as methods.
- Arrow functions cannot be used as constructors. Calling them with `new` throws a `TypeError`. They also don't have access to the `new.target` keyword.
- Arrow functions cannot use `yield` within their body and cannot be created as generator functions.

## Syntax

    () => expression

    param => expression

    (param) => expression

    (param1, paramN) => expression

    () => {
      statements
    }

    param => {
      statements
    }

    (param1, paramN) => {
      statements
    }

Rest parameters, default parameters, and destructuring within params are supported, and always require parentheses:
    (a, b, ...r) => expression
    (a = 400, b = 20, c) => expression
    ([a, b] = [10, 20]) => expression
    ({ a, b } = { a: 10, b: 20 }) => expression

Arrow functions can be `async` by prefixing the expression with the `async` keyword.
    async param => expression
    async (param1, param2, ...paramN) => {
      statements
    }

## Description

## Examples

## Specifications

[Arrow Function Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
