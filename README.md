# JavaScript setTimeout Closure Issue

This example demonstrates a common closure-related issue when using `setTimeout` within a loop in JavaScript.  The expected behavior is to print numbers from 0 to 9 with a one-second delay between each. However, due to the way closures work, all the `setTimeout` functions end up referencing the final value of `i` (which is 10). 

The `bug.js` file contains the code exhibiting this issue. The `bugSolution.js` provides a corrected version using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, preserving the correct value of `i` for each `setTimeout` call.