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

A **function expression** is a function, defined within an expression, that expression being, among other kinds, a value assigned to a variable

Here are some syntax examples of function expressions:
    function (param0) {
      statements
    }
    function (param0, param1) {
      statements
    }
    function (param0, param1, /*…,*/ paramN) {
      statements
    }

    function name(param0) {
      statements
    }
    function name(param0, param1) {
      statements
    }
    function name(param0, param1, /* …, */ paramN) {
      statements
    }

An arrow function expression is the same as above, but in a compact (arrow) form

A `function` expression is very similar to, and has almost the same syntax as, a `function` declaration. The main difference between a `function` expression and a `function` declaration is the `function` name, which can be omitted in `function` expressions to create anonymous functions. A `function` expression can be used as an IIFE (Immediately Invoked Function Expression) which runs as soon as it is defined

## Examples

## Specifications

[Arrow Function Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
