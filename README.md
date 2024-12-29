# F# Mutable Variable Bug

This repository demonstrates a subtle bug involving mutable variables in F#.  The `add` function unexpectedly modifies its input parameters, leading to different results than what might be initially expected.

## Bug Description

The `add` function uses mutable variables `x` and `y`.  Although it seems straightforward, the way mutable values are updated within the function leads to counter-intuitive results. The values are modified within the function in such a way that the final result is inconsistent with the original function design.

## How to Reproduce

1.  Clone this repository.
2.  Open the `bug.fs` file.
3.  Compile and run the code.
4. Observe the unexpected output values of x, y, and the result.

## Solution

The solution involves a change in how the function manipulates the variables.  Instead of modifying the inputs directly, the function now uses local variables to calculate the intermediate values and returns the desired final result without altering the initial values of x and y.

## Lessons Learned

This example highlights the importance of understanding how mutable variables behave in F# functions. Carefully consider the scope and impact of mutable variable assignments to avoid unexpected side effects.