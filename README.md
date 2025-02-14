# React useEffect Hook Missing Dependency Array
This example demonstrates a common error in React's `useEffect` hook: forgetting to specify the dependencies array.  This can lead to unexpected re-renders and stale closures.

## The Bug
The `MyComponent` function uses `useEffect` to log the `count` to the console. However, the dependency array is missing.  This means the effect will run on every render, regardless of changes to `count`, leading to potentially unexpected behavior and possibly infinite loops if the effect modifies state.

## The Solution
The solution is to add `count` to the dependency array. This ensures the effect runs only when the `count` value changes.