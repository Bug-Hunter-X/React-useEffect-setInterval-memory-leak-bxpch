# React useEffect setInterval Memory Leak

This repository demonstrates a common mistake when using the `setInterval` function within a React `useEffect` hook, leading to a memory leak.  The provided code snippet showcases the incorrect implementation and a corrected version to prevent memory leaks. The issue arises from a missing cleanup function within the `useEffect` hook.  This prevents the interval from being cleared when the component unmounts, causing the `setInterval` function to continue executing, even after the component is no longer in the DOM. This results in a memory leak and can negatively impact performance, especially in components with long lifecycles.

## Solution
The solution involves returning a cleanup function from the `useEffect` hook. This function will clear the interval when the component unmounts, preventing the memory leak.
