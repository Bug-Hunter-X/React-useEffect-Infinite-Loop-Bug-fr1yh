# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React: creating an infinite loop within a `useEffect` hook by updating state based on the current state within the same effect's dependency array.  The solution shows how to correct the issue using functional updates or by adjusting the dependencies.

## Bug Description
The `useEffect` hook, when called with an empty dependency array `[]`, is designed to run only once after the initial render. However, in this case, the state update `setCount(count + 1)` creates a continuous update cycle, never allowing the component to settle.

## How to Reproduce
Clone the repository and run `npm start` to see the React application in action.  The counter will continuously increment, demonstrating the infinite loop.