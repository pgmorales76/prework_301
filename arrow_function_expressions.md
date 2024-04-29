# Arrow Function Expressions

An arrow function expression is a compact alternative to a traditional function expression

It has some semantic differences and deliberate limitations in usage:

- Arrow functions don't have their own bindings to `this`, `arguments`, or `super`, and should not be used as methods.
- Arrow functions cannot be used as constructors. Calling them with `new` throws a `TypeError`. They also don't have access to the `new.target` keyword.
- Arrow functions cannot use `yield` within their body and cannot be created as generator functions.

## Try It

## Syntax

## Description

## Examples

## Specifications

[Arrow Function Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)