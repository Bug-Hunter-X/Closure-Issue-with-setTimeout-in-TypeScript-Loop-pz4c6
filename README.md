# Closure Issue with setTimeout in TypeScript Loop

This repository demonstrates a common issue with closures in JavaScript and TypeScript when using `setTimeout` within a loop. The value of 'i' is not captured at the time of `setTimeout` invocation, leading to unexpected results.

## Bug

The `printNumbers2` function attempts to print numbers from 1 to n with a delay using `setTimeout`. However, due to the closure over `i`, it prints 6 five times instead of 1, 2, 3, 4, 5.

## Solution

The solution involves using an immediately invoked function expression (IIFE) or `let` to create a new scope for `i` within each iteration of the loop. This ensures that the correct value of `i` is captured by the `setTimeout` callback function.

## How to run

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `tsc bug.ts` and `tsc bugSolution.ts` to compile the TypeScript code.
4. Run `node bug.js` and `node bugSolution.js` to see the output.