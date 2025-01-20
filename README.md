# Unexpected behavior when passing undefined to function with optional parameter

This example demonstrates an unexpected behavior in TypeScript when passing `undefined` to a function with an optional or nullable parameter. The type system does not automatically consider `undefined` as a valid value when handling optional or nullable parameters.

The code demonstrates this using a `greet` function that takes a name parameter which can be a string or null.  It handles `null` but not `undefined`. Passing undefined results in a runtime error, or unexpected behavior depending on your handling of parameters.

## How to reproduce the bug

1. Run the `bug.ts` file in a TypeScript compiler.
2. Observe the error when calling `greet` with `undefined`. 

## Solution

The solution file `bugSolution.ts` demonstrates how to handle the case of `undefined` appropriately, either by adding it to the type union or explicitly handling it within the function.