# React useEffect Hook Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug is caused by omitting the dependency array in the `useEffect` hook, leading to an infinite rendering loop.

## Bug Description

The provided code contains a `useEffect` hook that is missing its dependency array. This hook logs the current value of `count` to the console after each render.  Because there's no dependency array, the effect runs after *every* render, causing `setCount` to be called repeatedly, which triggers another re-render, and so on. This creates an infinite loop, eventually causing the application to crash.

## Solution

The solution involves adding the `count` variable to the dependency array. This ensures that the effect function only runs when the value of `count` changes. This prevents the infinite loop and solves the bug.
