# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can lead to infinite loops and unexpected behavior.

## The Bug

The `bug.js` file contains a component with a `useEffect` hook that doesn't properly list its dependencies.  This causes the effect to run on every render, creating an infinite loop due to the `setCount` call.

## The Solution

The `bugSolution.js` file shows the correct way to use `useEffect` in this scenario, by including `count` in the dependency array. This ensures that the effect only runs when `count` changes.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start` (assuming you have a development environment set up).
4. Observe the behavior of both components. You'll see that `bug.js` will have an error in console.