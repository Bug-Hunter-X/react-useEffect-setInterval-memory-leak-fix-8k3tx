# React useEffect setInterval memory leak
This repository demonstrates a common error in React applications: memory leaks caused by improper usage of `setInterval` within the `useEffect` hook.  The bug.js file shows the faulty code, while bugSolution.js provides the corrected version.

## Bug Description
The original code uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, leading to a memory leak.  The interval continues to run even after the component is no longer needed, causing unnecessary resource consumption.

## Solution
The corrected version uses `clearInterval` within the cleanup function of `useEffect` to properly stop the interval when the component is unmounted. This prevents the memory leak and ensures the application runs efficiently.