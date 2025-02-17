# Uncontrolled setInterval in useEffect causing memory leak
This example demonstrates a common error in React components: using `setInterval` within the `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Bug
The `MyComponent` uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts or when the dependency array changes. This causes the interval to continue running even after the component is no longer needed, resulting in a memory leak.

## Solution
The corrected component uses the return value of `useEffect` to clear the interval when the component unmounts.  This ensures that the interval is properly stopped, preventing memory leaks and unexpected behavior.
