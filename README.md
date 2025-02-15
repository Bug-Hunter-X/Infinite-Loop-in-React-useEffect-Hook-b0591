# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite rendering loop due to a missing dependency in the `useEffect` hook's dependency array.

## Bug Description

The `MyComponent` component uses `useState` to manage a count. The `useEffect` hook logs the count to the console. However, because `count` is not included in the dependency array, the `useEffect` hook runs on every render, causing the component to re-render infinitely, leading to a performance degradation and a potential crash.

## Solution

The solution involves adding `count` to the dependency array. This ensures that the `useEffect` hook only runs when the value of `count` changes.