# Arrow Function Expressions

An arrow function expression is a compact alternative to a traditional function expression.

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

A **function expression** is a function, defined within an expression, that expression being, among other kinds, a value assigned to a variable.

Here are some syntax examples of function expressions:
function (param0) {
statements
}
function (param0, param1) {
statements
}
function (param0, param1, /_…,_/ paramN) {
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

An arrow function expression is the same as above, but in a compact (arrow) form.

A `function` expression is very similar to, and has almost the same syntax as, a `function` declaration. The main difference between a `function` expression and a `function` declaration is the `function` name, which can be omitted in `function` expressions to create anonymous functions. A `function` expression can be used as an IIFE (Immediately Invoked Function Expression) which runs as soon as it is defined.

The following codeblock will illustrate the decoposition of a traditional function expression down to the simplest arrow function, step-by-step

    // Traditional anonymous function
    (function (a) {
      return a + 100;
    });

    // 1. Remove the word "function" and place arrow between the argument and opening body brace
    (a) => {
      return a + 100;
    };

    // 2. Remove the body braces and word "return" — the return is implied.
    (a) => a + 100;

    // 3. Remove the parameter parentheses
    a => a + 100;

In the example above, both the parentheses around the parameter and the braces around the function body may be omitted. However, they can only be omitted in certain cases.

The parentheses can only be omitted if the function has a single simple parameter. If it has multiple parameters, no parameters, or default, destructured, or rest parameters, the parentheses around the parameter list are required.

    // Traditional anonymous function - notice the parentheses around the entire function declaration?
    (function (a, b) {
      return a + b + 100;
    });

    // Arrow function
    (a, b) => a + b + 100;

    const a = 4;
    const b = 2;

    // Traditional anonymous function (no parameters)
    (function () {
      return a + b + 100;
    });

    // Arrow function (no parameters)
    () => a + b + 100;

The braces can only be omitted if the function directly returns an expression. If the body has additional lines of processing, the braces are required — and so is the return keyword. Arrow functions cannot guess what or when you want to return.

    // Traditional anonymous function
    (function (a, b) {
      const chuck = 42;
      return a + b + chuck;
    });

    // Arrow function
    (a, b) => {
      const chuck = 42;
      return a + b + chuck;
    };

Arrow functions are always unnamed. If the arrow function needs to call itself, use a named function expression instead. You can also assign the arrow function to a variable so it has a name.

// Traditional Function
function bob(a) {
return a + 100;
}

// Arrow Function (similar to the one given at the top)
const bob2 = (a) => a + 100;

## Examples

## Specifications

[Arrow Function Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
