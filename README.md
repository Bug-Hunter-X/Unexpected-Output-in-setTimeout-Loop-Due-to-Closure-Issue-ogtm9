# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that arises when using `setTimeout` within a loop. The problem lies in how variables are captured within the callback function of `setTimeout`.

## Bug Description

The `bug.js` file contains a function `myFunction` that uses a `for` loop and `setTimeout` to log the value of `i` after a 1-second delay.  Due to the closure issue, the expected output (0 through 9) is not produced.  Instead, all callbacks will log the final value of `i` (which is 10). 

## Bug Solution

The `bugSolution.js` file provides a corrected version that uses an immediately-invoked function expression (IIFE) to create a new scope for each iteration of the loop, correctly capturing the value of `i` for each callback.