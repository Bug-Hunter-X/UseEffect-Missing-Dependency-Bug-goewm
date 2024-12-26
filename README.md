# React useEffect Missing Dependency Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook and missing dependencies.  The example shows a component that re-renders unexpectedly due to a missing dependency in the `useEffect` hook's dependency array.

## Bug Description
The `useEffect` hook is used to perform side effects after every render.  If the dependency array is missing a variable that changes within the effect, the effect will run more frequently than intended.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output and the behavior of the component.

## Solution
The solution involves correctly specifying all dependencies used within the `useEffect` function in the dependency array.  Failing to include a state variable that changes within the effect in this array will lead to unexpected re-renders.
