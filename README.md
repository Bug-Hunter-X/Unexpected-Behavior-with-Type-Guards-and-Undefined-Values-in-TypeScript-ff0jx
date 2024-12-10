# Unexpected Behavior with Type Guards and Undefined Values in TypeScript

This repository demonstrates a common issue encountered in TypeScript when using type guards to handle null or undefined values.  The provided code snippet illustrates a situation where a function correctly handles null values but throws an error when an undefined value is passed.  The solution showcases how to explicitly handle undefined values to prevent this error.

## The Bug

The `greet` function attempts to gracefully handle null inputs by returning a default greeting. However, if an undefined value is passed, TypeScript's type system doesn't directly interpret this as fitting into the `string | null` type, resulting in a runtime error.  The provided `bug.ts` file shows this behavior.

## The Solution

The solution in `bugSolution.ts` addresses the issue by explicitly checking for both null and undefined values within the conditional statement. This ensures that the function handles all potential input scenarios correctly without throwing an error.