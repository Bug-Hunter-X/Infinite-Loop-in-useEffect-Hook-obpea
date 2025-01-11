# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug occurs when the `useEffect` hook is used without a dependency array, leading to an infinite loop.

## Bug Description

The provided code snippet shows a simple counter component. The `useEffect` hook logs the current count to the console after every render.  Because `count` changes on every click, the effect runs repeatedly, creating an infinite render loop.  The browser's console will show the log message rapidly, and the application might become unresponsive.

## Solution

A dependency array is added to the `useEffect` hook to fix this issue. The dependency array specifies that the effect should only re-run when the `count` variable changes. The array specifies the values that the effect depends upon.  If any value in the array changes, the effect is re-run. This prevents the infinite loop by only triggering the effect when the count is updated.