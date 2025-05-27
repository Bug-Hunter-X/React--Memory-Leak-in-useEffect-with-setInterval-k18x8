# React Memory Leak Bug

This repository demonstrates a common React bug: a memory leak caused by the improper use of `setInterval` within the `useEffect` hook.  The bug is explained in detail, and a solution is provided.

## Bug Description
The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to include a cleanup function within the `useEffect` hook's return statement to clear the interval when the component unmounts. This leads to a memory leak because the interval continues to run even after the component is removed from the DOM.

## Solution
The solution involves adding a cleanup function that calls `clearInterval` to stop the interval when the component is unmounted.  This prevents the memory leak and ensures the component behaves as expected.

## How to Run
1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npm start`.

You can observe the memory leak by inspecting the browser's developer tools (memory tab).
