# JavaScript Loose Comparison Bug

This repository demonstrates a common error in JavaScript caused by loose comparison (==) when handling null and undefined values.

## The Problem

JavaScript's loose equality (==) operator does not always behave as expected, particularly when dealing with null and undefined. In the provided `bug.js` file, the function `foo` intends to return 0 if the input `x` is null, -1 if `x` is negative, and 1 otherwise. However, due to loose comparison, `undefined` is incorrectly evaluated as not being less than 0, leading to an unexpected output of 1 instead of -1.

## The Solution

The `bugSolution.js` file corrects this issue by using strict equality (===) to ensure that the comparison is precise and consistent.  Strict equality explicitly checks for both the value and the type, resolving the ambiguity.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js` to see the incorrect behavior.
4. Run `node bugSolution.js` to see the correct behavior using strict equality.

## Conclusion

This example highlights the importance of using strict equality (===) in JavaScript when comparing values, especially when dealing with null and undefined, to avoid unexpected and potentially harmful errors.