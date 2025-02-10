# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug involving the `useEffect` hook. The provided code causes unnecessary re-renders and potential performance issues due to an incorrectly specified dependency array.

## Bug Description

The `useEffect` hook is designed to perform side effects after a component renders.  However, if the dependency array is incorrect or missing, the effect may run more frequently than intended. In this example, the effect runs after every render, leading to an unnecessary log statement in each render cycle.

## Bug Solution

The solution involves correctly specifying the dependency array. By including `count` in the array, the effect only runs when the `count` value changes. This prevents unnecessary re-renders and improves performance. 

## How to reproduce the bug

1. Clone the repo
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs

## How to fix the bug

Examine the `bugSolution.js` file to see the corrected `useEffect` hook implementation.