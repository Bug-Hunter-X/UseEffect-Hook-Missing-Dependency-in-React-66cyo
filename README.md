# useEffect Hook Missing Dependency
This example demonstrates a common error in React's `useEffect` hook: forgetting to include dependencies in the dependency array.  This can lead to unexpected behavior, often an infinite render loop.

## The Problem
The original `MyComponent` has an `useEffect` that logs the count to the console. However, it doesn't list `count` in its dependency array. As a result, the effect runs after every render, causing an infinite loop because each log causes a re-render, leading to another log, and so on. 

## The Solution
The `bugSolution.js` file shows the corrected code.  By adding `count` to the dependency array, the effect only runs when the `count` value changes. This fixes the infinite loop.