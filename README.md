# React setInterval Memory Leak

This repository demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook: forgetting to clear the interval when the component unmounts. This results in a memory leak and can lead to unexpected behavior.

The `bug.js` file shows the problematic code.  The `bugSolution.js` file provides a corrected version.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console (if you add a `console.log` in the component) to check for memory leaks and unexpected behavior.

## Solution

Always ensure that you clear any intervals, timeouts, or other resources within the cleanup function returned by `useEffect`. This function is called when the component is unmounted or when the dependencies change.